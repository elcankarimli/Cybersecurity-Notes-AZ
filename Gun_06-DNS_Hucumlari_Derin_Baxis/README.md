 🌐 6-ci Gün (Part 2): DNS Təhlükəsizliyi və Qabaqcıl Hücum Metodları

DNS sistemi internetin ilk dövrlərində təhlükəsizlik prioritet sayılmadan yaradıldığı üçün bir çox struktur boşluqlarına malikdir. Bu boşluqlar hakerlərə istifadəçiləri saxta saytlara yönləndirmək və ya xidmətləri tamamilə dayandırmaq imkanı verir.

 🚩 1. DNS Hijacking (DNS-in Ələ Keçirilməsi)
DNS Hijacking zamanı haker sizin sorğularınızın gedəcəyi ünvanı dəyişərək sizi saxta (phishing) saytlara yönləndirir. Bu, 3 yolla baş verə bilər:

* **Router (Modem) Hijacking:** Evdəki modeminizin şifrəsi qırılır və DNS ayarları hakerin serveri ilə əvəzlənir.
* **Domain Registrar Hijacking:** Saytın qeydiyyatdan keçdiyi platformaya (məs: GoDaddy) sızılaraq "Nameserver" (NS) rekordları dəyişdirilir.
* **Local Hijacking:** Kompüterə düşən bir Trojan (virus) `hosts` faylını dəyişərək spesifik saytlar üçün saxta IP-lər təyin edir.



---

 🌊 2. DNS Flood (NXDOMAIN Hücumu)
NXDOMAIN cavabı - "Belə bir domen mövcud deyil" deməkdir. Hakerlər bu cavabı serveri çökdürmək üçün silah kimi istifadə edirlər.

 Hücumun Mexanizmi:
Hücumçu botnetlər vasitəsilə hədəf serverə milyonlarla mövcud olmayan alt-domen sorğusu göndərir:
- `abc123.google.com`
- `xyz789.google.com`
- `test999.google.com`

 Nəticə:
1.  **Resurs Tükənməsi:** Server hər uydurma ad üçün bazasını yoxlayır, tapa bilməyəndə digər serverlərdən soruşur.
2.  **Önbəlləyin (Cache) Zəhərlənməsi:** Serverin yaddaşı mənasız "yoxdur" cavabları ilə dolur, real istifadəçilərə cavab verə bilmir.

---

 👻 3.Phantom Domain Attack
Bu hücum DNS serverini "psixoloji" olaraq yoran və onu çıxılmaz vəziyyətə salan bir strategiyadır. Məqsəd serveri cavab verməyə deyil, **gözləməyə** məcbur etməkdir.



 Ofisiant Ssenarisi (Analogiya):
Təsəvvür edin ki, siz restoranda ofisiantsınız (DNS Server). Müştəri bir yemək sifariş verir, siz resepti öyrənmək üçün aşpaza (Hayalet Server) zəng edirsiniz. Aşpaz telefonu açır, amma "bir dəqiqə gözlə" deyib sizi 10 dəqiqə telefonda saxlayır. Siz telefonu qulağınızdan ayıra bilmirsiniz və digər müştərilərə xidmət edə bilmirsiniz.

 Hücumun Addımları:
1.  **Hayalet Serverlər:** Haker sorğulara qəsdən çox gec cavab verən serverlər qurur.
2.  **Sorğu Yağışı:** Botnetlər bu serverlərə minlərlə sorğu göndərir.
3.  **Kilitlənmə:** Qurban DNS serveri "Timeout" (vaxt bitimi) müddətinə qədər bağlantıları açıq saxlayır. Minlərlə bağlantı açıq qalanda serverin RAM və CPU resursları tükənir.

---

 🛠️ İstifadə Olunan Alətlər
Hakerlər bu hücumlar üçün adətən aşağıdakı vasitələrdən istifadə edirlər:
* **Python (Scapy/Twisted):** Sorğuları qəbul edib cavabı qəsdən gecikdirən skriptlər yazmaq üçün.
* **DDoS Alətləri:** Sorğuları kütləvi şəkildə göndərmək üçün.
* **VPS (Virtual Private Servers):** Kimliyi gizlətmək üçün dünyanın fərqli nöqtələrində yerləşən serverlər.

