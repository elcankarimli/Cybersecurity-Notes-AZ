# 🐧 Linux Əsasları: Hissə 1
Bu repozitoriya Linux dünyasına yeni addım atanlar üçün fundamental terminal bacarıqlarını və sistem idarəetmə əsaslarını ehtiva edən bir bələdçidir.

## 🎯 Linux Nədir? (Nəzəriyyə)
Təsəvvür et ki, bir bina tikirsən. Windows və macOS sənə hər şeyi hazır, rənglənmiş və qapıları kilidli bir mənzil verir; içəridə nəyi isə dəyişmək çox çətindir. Linux isə sənə binanın kərpiclərini, sementini və planını verir. Sən istəsən divarı söküb pəncərə edə bilərsən.

Açıq Mənbə (Open Source): Linux-un kodu hər kəsə açıqdır. Bu, həm şəffaflıq (təhlükəsizlik üçün vacibdir), həm də azadlıq deməkdir.

Kernel (Nüvə): Linux əslində sistemin "beyni" olan nüvədir. O, proqram təminatı ilə kompüterin hissələri (RAM, Prosessor) arasında əlaqə yaradır.
## 🛠️ Fundamental Terminal Qısayolları
Terminalda effektivliyi artırmaq üçün ən çox istifadə olunan qısayollar:
*   **Açmaq:** `Ctrl + Alt + T` — Terminal pəncərəsini dərhal işə salır.
*   **Kursor İdarəetməsi:** `Ctrl + A` (sətrin əvvəli) və `Ctrl + E` (sətrin sonu).
*   **Təmizləmək:** `Ctrl + L` — Ekrandakı qarışıqlığı təmizləyir.
*   **Dayandırmaq:** `Ctrl + C` — İcra olunan hər hansı bir prosesi məcburi dayandırır.

## 📂 Fayl və Qovluq Əmrləri
Linux-da naviqasiya və fayl idarəetməsi üçün əsas "sağ qalma" əmrləri:
*   `pwd` — Hazırda olduğunuz qovluğun tam ünvanını göstərir.
*   `ls -la` — Gizli fayllar daxil olmaqla bütün faylları geniş siyahı şəklində göstərir.
*   `cd ~` — İstifadəçinin "home" (ev) qovluğuna sürətli keçid edir.
*   `mkdir [ad]` — Yeni qovluq yaradır.
*   `touch [fayl_adı].txt` — Boş bir mətn faylı yaradır.

## 🔍 Sistem Analizi
Sistemin vəziyyətini yoxlamaq üçün istifadə olunan əmrlər:
*   `uname -a` — Kernel versiyası və sistem arxitekturası haqqında tam məlumat.
*   `df -h` — Disk sahəsinin doluluğunu insan tərəfindən oxuna bilən (GB/MB) formatda göstərir.
*   `cat /etc/*release` — İstifadə olunan Linux distributivinin detallarını çap edir.


Möhtəşəm bir davamdır! Bu hissəni repozitoriyanın "Sistem Seçimi" və ya "Ekosistem" bölməsi kimi düşünə bilərik. "Digital Lawyer" vizyonuna uyğun olaraq, distributivlərin fərqini hüquqi bir dəqiqliklə izah edən `README.md` formatı aşağıdadır:

---

## 🐧 Linux Distributivləri (Distros)

Linux əslində bir əməliyyat sistemi deyil, o, sistemin ürəyi sayılan bir **Nüvədir (Kernel)**. Bu nüvə müxtəlif proqram təminatı, masaüstü mühitləri və paket idarəediciləri ilə birləşdirildikdə ortaya çıxan hazır sistemlərə **Distributiv** deyilir.



Hər bir distributiv fərqli bir məqsədə xidmət edir:

### 🌟 Populyar Distributivlərin Müqayisəsi

| Distributiv | Xüsusiyyəti | Kimlər Üçündür? |
| :--- | :--- | :--- |
| **Ubuntu** | "Yeni başlayanlar üçün qızıl standart". Quraşdırılması asandır və vizual interfeysi çox rahatdır. | Linux-a yeni keçid edən tələbələr və gündəlik istifadəçilər. |
| **Debian** | Stabilliyin simvoludur. İllərlə çökmədən və xəta vermədən işləmək üçün dizayn edilib. | Server idarəçiləri və stabil iş mühiti axtaran mütəxəssislər. |
| **Arch Linux** | Minimalist yanaşma. Hər bir detalı istifadəçi özü yığır. | Sistemi dərindən öyrənmək istəyən "Power User"lar. |
| **Kali Linux** | **Kibertəhlükəsizlik sahəsi üçün xüsusi seçilmişdir.** Debian əsaslıdır. | Penetrasiya testləri və etik hakerliklə məşğul olan mütəxəssislər. |

### 🛡️ Niyə Kali Linux?
Mənim kibertəhlükəsizlik və rəqəmsal hüquq (Cyber-law) sahəsindəki araşdırmalarım üçün Kali Linux əvəzedilməzdir. Çünki:
*   Daxilində yüzlərlə hazır kiber-təhlükəsizlik aləti (Nmap, Metasploit, Wireshark və s.) ilə gəlir.
*   Debian-ın möhkəm bazası üzərində qurulub, bu da onu həm güclü, həm də çevik edir.

> **Qeyd:** Bir rəqəmsal hüquqşünas üçün Linux sistemlərinin işləmə prinsipini bilmək, rəqəmsal sübutların toplanması və kiber-cinayətlərin analizi zamanı texniki üstünlük təmin edir.

---
## 🚀 İlk Tapşırıq (Hello Linux)
Yeni öyrənənlər üçün kiçik bir sınaq:
1. Terminalı açın.
2. `mkdir MyLinuxJourney` qovluğunu yaradın.
3. `cd MyLinuxJourney` ilə qovluğa daxil olun.
4. `echo "Linux is powerful!" > note.txt` əmri ilə qeyd yaradın.
5. `cat note.txt` ilə yazdığınız mətni oxuyun.

---

