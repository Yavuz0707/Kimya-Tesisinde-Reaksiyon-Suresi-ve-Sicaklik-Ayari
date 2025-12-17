# 🧬 Kimya Tesisinde Reaksiyon Süresi ve Sıcaklık Ayarı  
## Genetik Algoritma ile Optimizasyon

Bu proje, bir kimya tesisinde reaksiyon süresi (**x1**) ve sıcaklık (**x2**) parametrelerinin
reaksiyon verimi üzerindeki etkisini inceleyen ve bu parametreleri **genetik algoritma**
kullanarak optimize eden bir çalışmadır.

Çalışmada genetik algoritma **manuel olarak** uygulanmış, elde edilen sonuçlar
grafikler ve duyarlılık analizi ile değerlendirilmiştir.

---

## 👤 Öğrenci Bilgileri:

- **Ad Soyad:** Şükrü YAVUZ  
- **Öğrenci No:** 2312729015  
- **Yöntem:** Genetik Algoritma (Manuel İmplementasyon)

---

## 🎯 Problem Tanımı

Kimyasal üretim süreçlerinde reaksiyon verimi, proses parametrelerinin doğru seçimine
doğrudan bağlıdır. Reaksiyon süresi ve sıcaklık, bu süreçte en kritik iki değişkendir.

Bu çalışmanın amacı, verilen operasyonel ve güvenlik kısıtları altında
reaksiyon verimini **maksimize eden** reaksiyon süresi ve sıcaklık değerlerini bulmaktır.

---

## 📐 Matematiksel Modelleme

### Amaç Fonksiyonu

Problem, aşağıdaki reaksiyon verimi fonksiyonunun **maksimize edilmesi**
şeklinde modellenmiştir:

```text
maximize y = 8x1 + 3x2 - x1·x2 + x1²
Fonksiyonda yer alan terimlerin anlamı:

8x1: Reaksiyon süresinin verime olan doğrusal katkısı

3x2: Sıcaklığın verime olan pozitif etkisi

−x1·x2: Süre ve sıcaklığın birlikte aşırı artmasının olumsuz etkisi

x1²: Uzun reaksiyon süresinin dönüşüm oranını artırıcı etkisi

🔧 Karar Değişkenleri
Reaksiyon Süresi (x1)
Birim: Dakika

Aralık: 10 ≤ x1 ≤ 60

Sıcaklık (x2)
Birim: °C

Aralık: 40 ≤ x2 ≤ 120

⚠️ Kısıtlar
x1 + x2 ≤ 140

x2 ≥ 60

10 ≤ x1 ≤ 60

40 ≤ x2 ≤ 120

Bu kısıtlar, güvenlik, ekipman kapasitesi ve reaksiyonun gerçekleşebilirliği
dikkate alınarak belirlenmiştir.

🧠 Genetik Algoritma Yapısı
Bu projede genetik algoritma hazır kütüphaneler kullanılmadan,
tamamen manuel olarak uygulanmıştır.

Kullanılan Bileşenler
Kromozom Yapısı: [x1, x2]

Popülasyon Oluşturma: Rastgele

Uygunluk (Fitness) Fonksiyonu: Amaç fonksiyonu

Kısıt Yönetimi: Ceza (Penalty) yöntemi

Seçilim: Turnuva seçimi (Tournament Selection)

Çaprazlama: Aritmetik çaprazlama

Mutasyon: Rastgele gen mutasyonu

Elitizm: En iyi bireylerin korunması

🔄 Optimizasyon Süreci
Popülasyon her jenerasyonda fitness değerine göre sıralanmıştır

En iyi bireyler elitizm yöntemiyle korunmuştur

Seçilim, çaprazlama ve mutasyon adımları ile yeni bireyler üretilmiştir

Algoritma 100 jenerasyon boyunca çalıştırılmıştır

📊 Örnek Çalışma Çıktıları
Algoritma çalıştırıldığında elde edilen sonuçlar:

text
Kodu kopyala
Optimal x1 (Süre)    : 59.9682 dk
Optimal x2 (Sıcaklık): 60.3198 °C
Maksimum Verim (y)   : 639.6160
Yakınsama Analizi
Yakınsama grafiği, genetik algoritmanın jenerasyonlar boyunca
fitness değerini artırdığını ve belirli bir noktadan sonra
kararlı hale geldiğini göstermektedir.

Çözüm Uzayı ve Kısıtlar
Kontur grafiğinde, çözümün kısıtların izin verdiği sınır bölgede
oluştuğu açıkça görülmektedir. Optimal nokta,
tüm kısıtları sağlamaktadır.

🔍 Duyarlılık Analizi
Yapılan analizler göstermektedir ki:

Reaksiyon süresi (x1) değişkeni, karesel terim içermesi nedeniyle
verim üzerinde daha baskın bir etkiye sahiptir

Reaksiyon süresinde yapılan küçük azalışlar,
verimde ciddi düşüşlere yol açmaktadır

Bu durum, sistemin reaksiyon süresine karşı daha hassas olduğunu göstermektedir.

⚙️ Kurulum ve Çalıştırma Yönergeleri
Gerekli Yazılımlar

Python 3.8 veya üzeri

Jupyter Notebook veya VS Code (Python eklentisi yüklü)

Gerekli Kütüphaneler

Projede aşağıdaki Python kütüphaneleri kullanılmaktadır:

numpy

matplotlib

Kurulum:

pip install numpy matplotlib

Projenin Çalıştırılması

Proje dosyaları GitHub üzerinden indirilir veya klonlanır

Proje klasörüne girilir

Jupyter Notebook kullanımı:

jupyter notebook

Notebook dosyası açılarak hücreler sırasıyla çalıştırılır.

VS Code kullanımı:

Proje klasörü VS Code ile açılır

Python dosyası veya notebook dosyası çalıştırılır

✅ Sonuç
Bu çalışma, genetik algoritmanın kısıtlı ve doğrusal olmayan
optimizasyon problemlerinde etkili bir yöntem olduğunu göstermektedir.

Elde edilen sonuçlar, kimyasal proseslerde
reaksiyon süresi ve sıcaklık ayarının dikkatli bir şekilde
optimize edilmesinin verimlilik açısından kritik öneme sahip olduğunu ortaya koymaktadır.
