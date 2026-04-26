# 🌐 Gün 07: Şəbəkənin onurğası
AzFreeCode-un 7-ci gününə xoş gəlmisiniz! Bu dərsdə internetin "görünməz magistral yollarını" və o yollarda hərəkəti idarə edən əsas cihazları öyrənəcəyik.
# 🚀 Şəbəkənin Onurğa Sütunu: Router, Switch və Firewall

### Giriş: İnternet necə işləyir?

Çoxumuz elə bilirik ki, internet birbaşa göydən gəlir və ya bir kabel taxmaqla hər şey bitir. Əslində isə, sən bu mətni oxuyarkən məlumat paketləri minlərlə kilometr yolu yüzlərlə cihazın içindən keçərək qət edir. Bu kursda biz həmin "görünməz qəhrəmanları" söküb yığacağıq.



## 🏗️ Switch (Daxili Şəbəkənin Ürəyi)

Təsəvvür et ki, bir otaqda 10 nəfər var və hamı eyni vaxtda bir-birinə nəsə qışqırır. Bu, **Hub**-dır (köhnə və axmaq sistem). Amma hər kəsin qulağında xüsusi qulaqlıq olsa və məlumat yalnız lazım olan şəxsə çatdırılsa? Bu, **Switch**-dir.

-   **MAC Cədvəli:** Switch-in beynidir. O, hansı cihazın hansı portda olduğunu "öyrənir".
    
-   **Collision (Toqquşma):** Switch olan şəbəkədə məlumatlar bir-birinə dəymir, çünki hər yol özəldir.
    "Full-Duplex" və "Half-Duplex" anlayışı
Bunu mütləq qeyd etməliyik.

Half-Duplex (Köhnə Hub-lar): Eyni vaxtda ya məlumat göndərilir, ya da qəbul edilir. (Sanki dar bir körpü kimidir, bir maşın keçməlidir ki, o biri keçsin).

Full-Duplex (Müasir Switch-lər): Cihaz eyni saniyədə həm məlumat göndərir, həm də qəbul edir. Bu, sürəti ikiqat artırır.

> **Mühəndis qeydi:** Əgər eyni otaqdakı printerə fayl göndərə bilmirsənsə, birinci Switch-i və kabelləri yoxla.

----------

## 🌍 Router (Dünyaya Açılan Qapı)

Router sənin daxili şəbəkənlə (LAN) xarici dünya (WAN) arasındakı **tərcüməçidir**.

-   **NAT (Görünməzlik Pərdəsi):** Evdəki hər kəsin fərqli daxili IP-si var (`192.168.1.x`), amma dünyaya çıxanda Router hamını tək bir IP ilə təqdim edir. Bu, həm təhlükəsizlikdir, həm də IP ünvanlarına qənaətdir.
    
-   **Routing (Yönləndirmə):** Router ən qısa yolu deyil, ən **sağlam** yolu seçir.
    "Routing Protocols" (Yol Seçmə Qaydaları)
Router yolu necə tapır? O, "ağıllı" olduğu üçün xüsusi dillərdə (protokollarda) danışır:

RIP: Yolu sadəcə "neçə dənə routerdən keçəcəm" deyə hesablayır.

OSPF: Yolu "hansı xətt daha sürətlidir" deyə hesablayır. (Sanki Google Maps kimi, tıxac olmayan yolu seçir).

----------

## 🛡️  Firewall (Sərhəd Mühafizəçisi)

Şəbəkədə hər kəs dost deyil. Firewall sənin icazə vermədiyin hər şeyi qapıda saxlayır.

-   **Portların İdarəsi:** İnternetdə 65,535 qapı (port) var. Firewall işləməyən bütün qapıları kilidləyir.
    
-   **Stateful Inspection:** Firewall sadəcə kimin gəldiyinə baxmır, o, "söhbətin tarixçəsini" bilir. Sən bir saytı çağırmamısansa, o saytdan gələn heç nəyi içəri buraxmır.
    
Böyük şirkətlərdə firewall-un arxasında "neytral zona" yaradılır.

Nədir? Məsələn, bir şirkətin veb saytı hər kəsə açıq olmalıdır, amma şirkətin daxili sənədləri gizli qalmalıdır. Firewall elə tənzimlənir ki, sayt "orta zonada" (DMZ) qalır, daxili şəbəkə isə "ən arxa zonada". Beləcə, haker saytı sındırsa belə, şirkətin içinə girə bilmir.
----------

## 🛠️ Praktiki Tapşırıq (Lab)

İndi öyrəndiklərimizi canlı görək. Kompüterində Terminalı (CMD) aç və bunu yaz:

`tracert google.com` (və ya hər hansı bir sayt)

**Nəticəni belə oxu:**

1.  **1-ci sətir:** Sənin daxili Routerindir (Switch vasitəsilə ora çatdın).
    
2.  **2-5-ci sətirlər:** Provayderinin (ISP) routerləri.
    
3.  **Sonuncu sətir:** Hədəf server.
    

----------

### 📝 Bilik Yoxlaması (Quiz)

**Sual:** Sən ofisdəsən. İnternet yoxdur, amma yanındakı həmkarının kompüterindəki ortaq qovluğa daxil ola bilirsən. Problem hansı cihazdadır?

-   A) Switch xarabdır.
    
-   B) Firewall səni bloklayıb.
    
-   C) Router və ya internet xəttində problem var.
    

_(Düzgün cavab: **C**. Çünki Switch işləyir ki, sən lokalda (otaq daxilində) həmkarına bağlana bilirsən. Amma "çölə" çıxa bilmirsən, deməli qapı (Router) bağlıdır.)_

----------

## 
#Azfreecode #Azfreecode

Təbriklər! Şəbəkənin təməlini öyrəndin. 

**AzFreeCode – Öyrən, Kodla, Paylaş**
