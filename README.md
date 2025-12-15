# 🧬 Kimya Tesisinde Reaksiyon Süresi ve Sıcaklık Ayarı  
## Genetik Algoritma ile Optimizasyon

Bu proje, bir kimya tesisinde reaksiyon süresi (**x1**) ve sıcaklık (**x2**) parametrelerinin,
reaksiyon verimi üzerindeki etkisini inceleyen ve bu parametreleri **genetik algoritma**
kullanarak optimize eden bir çalışmadır.

Çalışma kapsamında genetik algoritma **manuel olarak** uygulanmış,
optimum çalışma koşulları kısıtlar altında belirlenmiştir.

---

## 👤 Öğrenci Bilgileri

- **Ad Soyad:** Şükrü YAVUZ  
- **Öğrenci No:** 2312729015  
- **Yöntem:** Genetik Algoritma (Manuel İmplementasyon)

---

## 🎯 Problem Tanımı

Kimyasal üretim süreçlerinde reaksiyon verimi, proses parametrelerinin doğru seçimine
doğrudan bağlıdır. Reaksiyon süresi ve sıcaklık, bu süreçte en kritik iki değişkendir.

Bu çalışmanın amacı, verilen güvenlik ve operasyonel kısıtlar altında
reaksiyon verimini maksimize eden parametre değerlerini bulmaktır.

---

## 📐 Matematiksel Modelleme

### Amaç Fonksiyonu

Problem aşağıdaki reaksiyon verimi fonksiyonunun **maksimize edilmesi**
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
Bu projede genetik algoritma hazır kütüphaneler kullanılmadan
manuel olarak uygulanmıştır.

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
Popülasyon, her jenerasyonda fitness değerine göre sıralanmıştır

En iyi bireyler elitizm yöntemiyle korunmuştur

Seçilim, çaprazlama ve mutasyon adımlarıyla yeni bireyler üretilmiştir

Algoritma 100 jenerasyon boyunca çalıştırılmıştır

📊 Sonuçlar ve Görselleştirme
Algoritma çalıştırıldığında aşağıdaki optimum değerlere ulaşılmıştır:

Optimal Reaksiyon Süresi (x1): ≈ 60 dk

Optimal Sıcaklık (x2): ≈ 60 °C

Maksimum Reaksiyon Verimi: ≈ 640

Üretilen Grafikler
Genetik algoritma yakınsama grafiği (fitness – jenerasyon)

Amaç fonksiyonunun kontur grafiği

Kısıt bölgeleri ve optimal çözümün görsel gösterimi

🔍 Duyarlılık Analizi
Optimum çözüm etrafında yapılan analizler göstermektedir ki:

Reaksiyon süresi (x1) değişkeni, karesel terim içermesi nedeniyle
verim üzerinde daha baskın bir etkiye sahiptir

Reaksiyon süresinde yapılan küçük azalışlar,
verimde önemli düşüşlere yol açmaktadır

Bu durum, sistemin reaksiyon süresine karşı daha hassas olduğunu göstermektedir.

✅ Sonuç
Bu çalışma, genetik algoritmanın kısıtlı ve doğrusal olmayan optimizasyon
problemlerinde etkili bir yöntem olduğunu göstermektedir.

Elde edilen sonuçlar, kimyasal proseslerde
reaksiyon süresi ve sıcaklık ayarının dikkatli bir şekilde optimize edilmesinin
verimlilik açısından kritik öneme sahip olduğunu ortaya koymaktadır.
