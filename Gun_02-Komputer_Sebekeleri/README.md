# 🌐 2-ci Gün: Kompüter Şəbəkələri (Ümumi)


## 🏗️ Kompüter Şəbəkələrinin Əsasları

### 1. Şəbəkə Əsasları
* **Konsepsiyalar:** Şəbəkənin əsas komponentlərini (qovşaqlar, bağlantılar, protokollar) və onların ünsiyyətdəki rollarını anlayın.
* **Şəbəkələrin Növləri:** LAN (Yerli Sahə Şəbəkələri), WAN (Geniş Sahə Şəbəkələri) və MAN (Metropolitan Sahə Şəbəkələri) və PAN (Şəxsi Sahə Şəbəkələri) kimi digər növləri haqqında məlumat əldə edin.

### 2. Şəbəkə Arxitekturası

#### 📐 OSI Modeli
OSI (Açıq Sistemlər Qarşılıqlı Əlaqəsi) modeli və onun yeddi təbəqəsi ilə tanış olun:



1.  **Fiziki Təbəqə (Physical Layer):** Məlumatın kabellər, fiber-optik və ya simsiz dalğalar vasitəsilə bitlər (0 və 1) şəklində ötürüldüyü səviyyədir. Bura kabellər, hublar və konnektorlar daxildir.
2.  **Məlumat Bağlantısı Təbəqəsi (Data Link Layer):** Bu təbəqə fiziki ünvanları (MAC ünvanları) idarə edir. Məlumatlar burada "frame" (kadr) adlanır. Səhvlərin aşkarlanması və cihazlar arası birbaşa əlaqə burada baş verir (məsələn, Switch-lər).
3.  **Şəbəkə Təbəqəsi (Network Layer):** Məlumatın bir şəbəkədən digərinə necə yönləndiriləcəyinə qərar verir. Burada IP ünvanları işə düşür və ən qısa yolun seçilməsi (routing) həyata keçirilir. Məlumat vahidi "paket"dir.
4.  **Nəqliyyat Təbəqəsi (Transport Layer):** Məlumatın tam və doğru şəkildə qarşı tərəfə çatmasına cavabdehdir. TCP (etibarlı) və UDP (sürətli) protokolları burada çalışır. Məlumat burada "seqmentlərə" bölünür.
5.  **Sessiya Təbəqəsi (Session Layer):** İki kompüter arasındakı əlaqənin (sessiyanın) açılması, idarə olunması və bağlanmasını təmin edir. Məsələn, bir veb-sayta daxil olduğunuzda sessiyanın nə qədər aktiv qalacağını bu təbəqə tənzimləyir.
6.  **Təqdimat Təbəqəsi (Presentation Layer):** Məlumatın formatını müəyyən edir (məsələn, JPEG, MP4, GIF). Həmçinin məlumatların şifrələnməsi (encryption) və sıxılması da bu mərhələdə baş verir ki, proqram təbəqəsi onu oxuya bilsin.
7.  **Tətbiq Təbəqəsi (Application Layer):** İstifadəçinin birbaşa qarşılıqlı əlaqədə olduğu təbəqədir. Brauzerlər (Chrome), e-poçt proqramları bu təbəqədəki protokollardan (HTTP, FTP, SMTP) istifadə edir.

#### 🌍 TCP/IP Modeli
İnternet və əksər müasir şəbəkələr üçün əsas olan TCP/IP (Ötürmə Nəzarət Protokolu/İnternet Protokolu) modelini anlayın.

---

## 🛠️ Şəbəkə Protokolları və Texnologiyaları

### 3. Protokollar
* **TCP/IP Dəsti:** IP (İnternet Protokolu), TCP (Ötürmə Nəzarət Protokolu), UDP (İstifadəçi Dataqram Protokolu), ICMP (İnternet Nəzarət Mesaj Protokolu) və ARP (Ünvan Həll Protokolu) kimi əsas protokolları öyrənin.
* **DNS (Domen Adı Sistemi):** DNS-in domen adlarını IP ünvanlarına necə çevirdiyini və İnternet rabitəsindəki rolunu öyrənin.

### 4. Şəbəkə Cihazları
* **Routerlər və Kommutatorlar:** Şəbəkələr daxilində (routerlər) və məlumat bağlantısı qatında (kommutatorlar) trafikin yönləndirilməsindəki funksiyalarını başa düşün.
* **Firewall:** Firewall-ların əvvəlcədən müəyyən edilmiş təhlükəsizlik qaydalarına əsasən daxil olan və çıxan şəbəkə trafikini necə idarə etdiyini və izlədiyini öyrənin.

---

## 🔐 Şəbəkə Təhlükəsizliyi Mülahizələri

### 5. Şəbəkə Təhlükəsizliyi Prinsipləri
* **Təhlükəsizlik Protokolları:** HTTPS (HTTP Təhlükəsiz) və SSH (Təhlükəsiz Qabıq) kimi təhlükəsiz rabitə protokollarını araşdırın.
* **Şifrələmə:** Məlumat ötürülməsi və saxlanmasının təhlükəsizliyində şifrələmə alqoritmlərinin (AES, RSA və s.) rolunu başa düşün.

### 6. Şəbəkə Hücumları və Müdafiəsi
* **Ümumi Hücumlar:** DoS (Xidmətdən İmtina), DDoS (Paylanmış Xidmətdən İmtina), ortada olan hücumlar və paket iyləmə kimi şəbəkə hücumlarının növləri ilə tanış olun.
* **Müdafiə Mexanizmləri:** Təhlükəsizliyi artırmaq üçün müdaxilə aşkarlama və qarşısının alınması sistemləri (IDS/IPS), VPN-lər (Virtual Şəxsi Şəbəkələr) 
