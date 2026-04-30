
---

# 🐧 Linux Kursu: Hissə 2 - Sistem Analizi və Disk İdarəetməsi

Bu bölmədə Linux sisteminin daxili strukturunu anlamaq, işlədiyimiz mühiti müəyyən etmək və disk resurslarını effektiv idarə etmək üçün lazım olan fundamental əmrləri öyrənəcəyik

## 📋 Mövzular
*   Sistem və Distro məlumatlarının alınması
*   Nüvə (Kernel) versiyasının yoxlanılması
*   Disk sahəsinin analizi (`df` və `du`)
*   Fayl manipulyasiyası üçün qabaqcıl qısayollar

---

## 🔍 1. Sistem Məlumatlarının Müəyyən Edilməsi

Hər hansı bir proqram quraşdırmazdan əvvəl sistemin hansı "ailəyə" (Debian, RHEL və s.) aid olduğunu bilmək vacibdir[cite: 2].

| Əmr | Təsviri |
| :--- | :--- |
| `lsb_release -a` | Distro ID, versiya və kod adını göstərir |
| `cat /etc/os-release` | Müasir sistemlərdə paylanma haqqında geniş məlumat verir |
| `uname -r` | İstifadə olunan Linux Nüvəsinin (Kernel) versiyasını göstərir |
| `uname -m` | Sistemin arxitekturasını (məs: x86_64) göstərir |



---

## 💾 2. Disk və Yaddaş İdarəetməsi

Sistemin performansını qorumaq üçün disk doluluğunu mütəmadi yoxlamaq lazımdır.

### `df` (Disk Free)
Bölmələrin (partitions) ümumi vəziyyətini görmək üçün:
```bash
df -h
```
*   `-h` bayrağı məlumatları "human-readable" (insan tərəfindən oxunaqlı - GB, MB) formatına salır

### `du` (Disk Usage)
Hansı qovluğun daha çox yer tutduğunu tapmaq üçün:
```bash
du -sh *
```
*   `-s` (summary): Alt qovluqları tək-tək göstərmədən cəmi hesablayır[cite: 2].
*   `--threshold=1G`: Müəyyən ölçüdən (məsələn, 1GB) böyük faylları tapmaq üçün istifadə olunur[cite: 2].

---

## 📂 3. Fayl və Qovluq Əməliyyatları (Sürətli Baxış)

Terminalda işinizi sürətləndirəcək əsas əmrlər:

*   **Yaratma:** `touch fayl.txt` (yeni boş fayl)
*   **Ad dəyişmə/Köçürmə:** `mv kohne_ad yeni_ad`
*   **Oxuma:** `less boyuk_fayl.log` (faylı səhifələyərək oxumaq üçün)
*   **Silmə:** `rm -rf qovluq_adi` (qovluğu rekursiv və məcburi silir).

> [!CAUTION]
> `rm -rf` əmrini istifadə edərkən çox diqqətli olun; bu əməliyyatın geri dönüşü yoxdur.

---

## 🛠 Praktiki Tapşırıq
1. Sistemin `os-release` faylına baxaraq hansı distro işlətdiyinizi dəqiqləşdirin
2. Bütün sistemdə 500MB-dan çox yer tutan qovluqları tapmağa çalışın
3. `uname -a` çıxışını oxuyaraq prosessor arxitekturanızı müəyyən edin

