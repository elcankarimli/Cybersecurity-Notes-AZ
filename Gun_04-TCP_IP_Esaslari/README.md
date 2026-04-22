# 🌐 4-cü Gün: TCP/IP Modeli və Şəbəkə Protokolları

TCP/IP (Transmission Control Protocol / Internet Protocol) internetin və müasir şəbəkələrin təməl dilidir. Bu protokol dəsti məlumatların necə paketlənməli, ünvanlanmalı və hədəfə çatdırılmalı olduğunu müəyyən edir.

## 🧱 1. TCP/IP-nin 4 Təbəqəsi
OSI modelində 7 təbəqə olsa da, TCP/IP bunu daha sadə və funksional 4 təbəqəyə endirir:



1.  **Tətbiq Təbəqəsi (Application):** İstifadəçinin qarşılıqlı əlaqədə olduğu yer. (Məsələn: HTTP, SMTP, FTP).
2.  **Nəqliyyat Təbəqəsi (Transport):** Məlumatın hansı qayda ilə gedəcəyinə cavabdehdir. (TCP və ya UDP).
3.  **İnternet Təbəqəsi (Internet):** Paketlərin IP ünvanları vasitəsilə düzgün hədəfə yönləndirilməsi. (IP, ICMP).
4.  **Şəbəkə Girişi (Network Access):** Məlumatın fiziki ötürülməsi (Kabellər, Wi-Fi, MAC ünvanları).

---

## 🤝 2. İki Əsas Qəhrəman: TCP və IP
Bu sistemi bir kuryer xidməti kimi təsəvvür edək:

### 📍 IP (Internet Protocol) — "Ünvanlayıcı"
IP-nin tək işi paketi düzgün ünvana çatdırmaqdır. O, məktubun üzərindəki ünvan kimidir.
* Paketin haradan gəldiyini və hara getdiyini müəyyən edir.
* Lakin paketin yolda itib-itməməsinə və ya sırasının qarışmasına cavabdeh deyil.

### 👮 TCP (Transmission Control Protocol) — "Nəzarətçi"
TCP işin keyfiyyətinə və etibarlılığına baxır:
* **Parçalama:** Böyük məlumatı kiçik paketlərə bölür.
* **Nömrələmə:** Hər paketə sıra nömrəsi verir (1, 2, 3...).
* **Yoxlama:** Əgər 2 nömrəli paket yolda itsə, serverdən onu yenidən göndərməsini tələb edir.
* **Birləşdirmə:** Bütün paketlər çatanda onları düzgün sıra ilə birləşdirib əsl faylı bərpa edir.

---

## 🏎️ 3. TCP vs. UDP
Hər iki protokol nəqliyyat təbəqəsində çalışır, lakin fərqli məqsədlərə xidmət edir:

| Xüsusiyyət | TCP | UDP |
| :--- | :--- | :--- |
| **Etibarlılıq** | Çox etibarlıdır | Etibarsızdır (itki ola bilər) |
| **Sürət** | Daha yavaş (yoxlamalara görə) | Çox sürətlidir |
| **İstifadə sahəsi** | Fayl yükləmə, Veb-saytlar | Canlı yayım, Onlayn oyunlar |

> **Misal:** Onlayn oyunlarda (məsələn, FIFA) yaranan "lag" problemi çox vaxt UDP paketlərinin itməsi nəticəsində baş verir.

---

## 🔢 4. IPv4 və IPv6
İnternetdə hər cihazın bir ünvanı olmalıdır:

* **IPv4:** 32 bitlik ünvan sxemidir (təxminən 4.3 milyard ünvan). Nümunə: `192.168.0.1`
* **IPv6:** IPv4-ün yer çatışmazlığını həll etmək üçün yaradılmış 128 bitlik sistemdir. Nümunə: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`

---



