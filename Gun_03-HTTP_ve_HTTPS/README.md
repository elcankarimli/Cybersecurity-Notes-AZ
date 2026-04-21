# 🌐 3-cü Gün: HTTP və HTTPS Protokolları

HTTP (HyperText Transfer Protocol) və HTTPS (HyperText Transfer Protocol Secure) internet üzərindən məlumatların ötürülməsi üçün istifadə olunan əsas protokollardır.

## 📄 HTTP (HyperText Transfer Protocol)

* **Tərif:** HTTP internet üzərindən məlumatların ötürülməsi üçün istifadə olunan bir protokoldur. Mesajların necə formatlandığını və ötürüldüyünü, veb serverlərin və brauzerlərin müxtəlif əmrlərə necə cavab verməli olduğunu müəyyən edir.
* **Təhlükəsizlik:** HTTP təhlükəsiz deyil. Məlumatlar şifrələnmir, yəni hücum edənlər tərəfindən "man-in-the-middle" hücumları ilə asanlıqla ələ keçirilə bilər.
* **Port:** Standart olaraq **80** portundan istifadə edir.

> **Nümunə:** `http://example.com` ziyarət etdiyiniz zaman mübadilə edilən hər hansı bir məlumatı rabitəni ələ keçirən hər kəs görə bilər.

### 🛡️ Firewall-lardan Keçid və HTTP Tunneling
Bir çox şirkətlərdə Firewall-lar təhlükəsizlik üçün bəzi portları bağlasa da, **80** və **443** portlarını adətən açıq qoyur. Çünki bu portlar bağlansa, internetə çıxış dayanar.
* **Hakerlərin Taktikası:** Hakerlər öz zərərli proqramlarını (backdoor) elə tənzimləyirlər ki, onlar məhz 80-ci port üzərindən hakerin serverinə məlumat göndərsin. Buna şəbəkə dilində **HTTP Tunneling** deyilir.

---

## 🔒 HTTPS (HyperText Transfer Protocol Secure)



* **Tərif:** HTTP-nin təhlükəsiz versiyasıdır. Ötürülən məlumatları şifrələmək üçün **SSL/TLS** (Secure Sockets Layer / Transport Layer Security) istifadə edir.
* **Təhlükəsizlik:** HTTPS məlumatların şifrələnməsini, bütövlüyünü və autentifikasiyasını təmin edir.
* **Port:** Standart olaraq **443** portundan istifadə edir.

> **Nümunə:** `https://example.com` ziyarət edildikdə brauzer və server arasında bütün trafik şifrələnir.

### 🏛️ HTTPS-in Üç Sütunu

1.  **Şifrələmə (Encryption):** Məlumatlar koda çevrilir; haker trafiki tutsa belə, heç bir şey başa düşmür.
2.  **Məlumat Bütövlüyü (Data Integrity):** Məlumatın yolda dəyişdirilməsinin qarşısını alır (məsələn, bank köçürməsi zamanı məbləğin dəyişdirilməsi).
3.  **Autentifikasiya (Authentication):** Saytın həqiqətən kim olduğunu sübut edir (məsələn, həqiqi Google-da olduğunuzu təsdiqləyir).

---

## 📊 Əsas Fərqlər - Xülasə

| Xüsusiyyət | HTTP | HTTPS |
| :--- | :--- | :--- |
| **Şifrələmə** | Yoxdur (Açıq mətn) | Var (SSL/TLS) |
| **Port** | 80 | 443 |
| **Təhlükəsizlik** | Zəif / Riskli | Yüksək / Təhlükəsiz |
| **URL Prefiksi** | `http://` | `https://` |
| **İstifadə Sahəsi** | Həssas olmayan məlumatlar | Bankçılıq, E-ticarət, Giriş səhifələri |

