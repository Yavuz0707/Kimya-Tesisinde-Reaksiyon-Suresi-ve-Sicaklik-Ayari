Kimya Tesisinde Reaksiyon Süresi ve Sıcaklık Ayarı Optimizasyonu
Proje Özeti

Bu proje, kimyasal üretim süreçlerinde reaksiyon verimini artırmaya yönelik olarak tasarlanmış bir optimizasyon çalışmasıdır. Reaksiyon süresi ve sıcaklık gibi temel proses parametrelerinin uygun şekilde belirlenmesi, üretim kalitesi, enerji tüketimi ve güvenlik açısından kritik öneme sahiptir. Çalışmada, bu parametrelerin en uygun değerleri matematiksel optimizasyon yöntemleri kullanılarak analiz edilmiştir.

Problem Bağlamı

Kimya endüstrisinde reaksiyon koşullarının doğru belirlenmesi, üretim verimliliğini doğrudan etkiler. Özellikle reaksiyon süresi ve sıcaklık, kimyasal dönüşüm oranlarını belirleyen temel faktörlerdir. Bu parametrelerin hatalı seçilmesi aşağıdaki sorunlara yol açabilir:

Ürün veriminde düşüş

Gereksiz enerji tüketimi

Üretim süresinin uzaması

Proses güvenliğinin azalması

Bu nedenle, söz konusu parametrelerin sistematik bir şekilde optimize edilmesi gerekmektedir.

Çalışmanın Kapsamı

Bu çalışmada, kısıtlı bir optimizasyon problemi ele alınmış ve iki farklı optimizasyon yaklaşımı kullanılarak çözüm aranmıştır. Hem gradyan tabanlı hem de evrimsel optimizasyon yöntemleri uygulanarak elde edilen sonuçlar karşılaştırılmış ve en uygun çalışma koşulları belirlenmiştir.

Çalışmanın Amacı

Belirlenen operasyonel ve güvenlik kısıtları altında, reaksiyon verimini maksimize eden reaksiyon süresi ve sıcaklık değerlerini tespit etmek ve kullanılan optimizasyon yöntemlerinin performanslarını analiz etmektir.

Matematiksel Modelleme
Amaç Fonksiyonu

Problem, aşağıdaki reaksiyon verimi fonksiyonunun maksimize edilmesi şeklinde modellenmiştir:

maximize y = 8x1 + 3x2 − x1·x2 + x1²


Fonksiyonda yer alan terimlerin anlamı:

8x1: Reaksiyon süresinin verime doğrusal katkısı

3x2: Sıcaklığın verime olan pozitif etkisi

−x1·x2: Süre ve sıcaklığın birlikte aşırı artmasının olumsuz etkisi

x1²: Uzun reaksiyon süresinin dönüşüm oranını artırıcı etkisi

Karar Değişkenleri
Reaksiyon Süresi (x1)

Birim: Dakika

Değer Aralığı: 10 ≤ x1 ≤ 60

Açıklama: Kimyasal reaksiyonun reaktör içerisinde devam ettiği süre

Sıcaklık (x2)

Birim: °C

Değer Aralığı: 40 ≤ x2 ≤ 120

Açıklama: Reaksiyon ortamının sıcaklık seviyesi

Kısıtlar
Toplam Yük Kısıtı
x1 + x2 ≤ 140


Bu kısıt, yüksek sıcaklık ve uzun reaksiyon süresinin birlikte oluşturabileceği güvenlik risklerini sınırlamak amacıyla tanımlanmıştır.

Minimum Sıcaklık Kısıtı
x2 ≥ 60


Reaksiyonun gerçekleşebilmesi için gerekli minimum aktivasyon enerjisini temsil eder.

Sınır Kısıtları
10 ≤ x1 ≤ 60
40 ≤ x2 ≤ 120


Bu sınırlar, ekipman kapasitesi ve operasyonel güvenlik gerekleri doğrultusunda belirlenmiştir.

Problem Özellikleri

Problem tipi: Kısıtlı, doğrusal olmayan optimizasyon

Değişken sayısı: 2

Kısıt sayısı: 2 eşitsizlik + sınır kısıtları

Çözüm uzayı: İki boyutlu sürekli alan

Fonksiyon yapısı: Kuadratik ve konveks olmayan

Notebook İçeriği

Notebook dosyasında aşağıdaki adımlar yer almaktadır:

Gerekli kütüphanelerin içe aktarılması ve grafik ayarları

Amaç fonksiyonunun ve kısıtların tanımlanması

Optimizasyon algoritmalarının uygulanması

Sonuçların tablo ve grafiklerle karşılaştırılması

Duyarlılık analizi ve yorumlama

Çözüm doğrulaması ve istatistiksel değerlendirme

Optimizasyon Yöntemleri
SLSQP (Sequential Least Squares Programming)

Kısıtlı problemlerde etkili bir gradyan tabanlı yöntem

Hızlı yakınsama sağlar

Başlangıç noktasına duyarlıdır

Differential Evolution

Evrimsel ve küresel arama yeteneğine sahiptir

Başlangıç noktasına duyarsızdır

Daha fazla hesaplama süresi gerektirir

Her iki yöntemden elde edilen sonuçlar karşılaştırılarak en uygun çözüm seçilmiştir.

Görselleştirme ve Analiz

Amaç fonksiyonunun 3B yüzey grafiği

Kısıt bölgeleri ile birlikte kontur grafikleri

Optimal nokta işaretlemeleri

Parametrelerin tek tek etkisini gösteren kesit grafikleri

Duyarlılık Analizi

Optimal çözüm etrafında küçük parametre değişikliklerinin verim üzerindeki etkisi incelenmiştir. Bu analiz, sistemin hangi parametreye daha hassas olduğunu ortaya koymakta ve operasyonel kararlar için yol gösterici olmaktadır.

Çözümün Doğrulanması

Çözümün güvenilirliğini test etmek amacıyla farklı başlangıç noktalarından çoklu optimizasyon çalışmaları gerçekleştirilmiş ve elde edilen sonuçların tutarlılığı analiz edilmiştir.

Sonuç ve Öneriler

Elde edilen sonuçlar, reaksiyon süresi ve sıcaklık parametrelerinin doğru şekilde optimize edilmesinin verimlilik üzerinde önemli bir etkisi olduğunu göstermektedir. Özellikle reaksiyon süresi değişkeninin sistem üzerinde daha baskın bir rol oynadığı gözlemlenmiştir.

Bu çalışma, kısıtlı ve doğrusal olmayan optimizasyon problemlerinde matematiksel ve evrimsel yöntemlerin etkinliğini ortaya koymaktadır.
