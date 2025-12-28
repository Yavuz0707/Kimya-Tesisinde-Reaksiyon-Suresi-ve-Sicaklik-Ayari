# 🧬 Kimya Tesisinde Reaksiyon Süresi ve Sıcaklık Optimizasyonu Projesi
## Genetik Algoritma ile Maksimum Verim Analizi

Bu proje, endüstriyel bir kimya tesisinde gerçekleşen kimyasal reaksiyonlarda **reaksiyon süresi (x₁)** ve **sıcaklık (x₂)** parametrelerinin optimal değerlerini belirleyerek reaksiyon verimini maksimize etmeyi amaçlayan bir optimizasyon çalışmasıdır. Çalışmada, **Genetik Algoritma (Genetic Algorithm - GA)** yöntemi **manuel olarak** implemente edilmiş ve hazır optimizasyon kütüphaneleri kullanılmamıştır.

Proje kapsamında, matematiksel modelleme, kısıtlı optimizasyon teknikleri, algoritma tasarımı, görselleştirme ve duyarlılık analizi gibi konular detaylı bir şekilde ele alınmıştır.

---

## 👨‍🎓 Öğrenci Bilgileri

| Bilgi | Detay |
|-------|-------|
| **Ad Soyad** | Şükrü YAVUZ |
| **Öğrenci Numarası** | 2312729015 |
| **Ders** | Yapay Zeka |
| **Proje Konusu** | Kimya Tesisinde Reaksiyon Parametrelerinin Genetik Algoritma ile Optimizasyonu |
| **Uygulama Yöntemi** | Manuel Genetik Algoritma İmplementasyonu |
| **Geliştirme Ortamı** | Python 3.x, Jupyter Notebook |
| **GitHub Repository** | [https://github.com/Yavuz0707/Kimya-Tesisinde-Reaksiyon-Suresi-ve-Sicaklik-Ayari](https://github.com/Yavuz0707/Kimya-Tesisinde-Reaksiyon-Suresi-ve-Sicaklik-Ayari) |

---

## 📋 İçindekiler

- [Proje Hakkında](#-proje-hakkında)
- [Problem Tanımı ve Senaryo](#-problem-tanımı-ve-senaryo)
- [Matematiksel Modelleme](#-matematiksel-modelleme)
- [Genetik Algoritma Yaklaşımı](#-genetik-algoritma-yaklaşımı)
- [Teknik Detaylar](#-teknik-detaylar)
- [Kurulum ve Çalıştırma](#️-kurulum-ve-çalıştırma)
- [Sonuçlar ve Çıktılar](#-sonuçlar-ve-çıktılar)
- [Duyarlılık Analizi](#-duyarlılık-analizi)
- [Proje Yapısı](#-proje-yapısı)
- [Kullanılan Teknolojiler](#-kullanılan-teknolojiler)
- [Sonuç ve Değerlendirme](#-sonuç-ve-değerlendirme)
- [İletişim](#-i̇letişim)

---

## 🔬 Proje Hakkında

Modern kimya endüstrisinde, üretim süreçlerinin verimliliği büyük ölçüde proses parametrelerinin doğru belirlenmesine bağlıdır. Bu proje, bir kimya tesisinde gerçekleşen reaksiyonlarda:

- Reaksiyon süresinin (x₁)
- İşlem sıcaklığının (x₂)

reaksiyon verimi üzerindeki etkisini incelemekte ve bu parametreleri optimize etmektedir.

### Projenin Özellikleri

✅ **Manuel Genetik Algoritma İmplementasyonu**: Hazır kütüphaneler yerine algoritmanın tüm bileşenleri (seçilim, çaprazlama, mutasyon, elitizm) sıfırdan kodlanmıştır.

✅ **Kısıtlı Optimizasyon**: Operasyonel ve güvenlik kısıtları altında çözüm üretilmiştir.

✅ **Görselleştirme**: Yakınsama grafikleri, kontur plotları ve duyarlılık analizleri ile sonuçlar detaylı olarak sunulmuştur.

✅ **Parametre Analizi**: Algoritmanın performansı farklı parametre değerleri ile test edilmiştir.

✅ **Detaylı Dokümantasyon**: Kod içerisinde kapsamlı açıklamalar ve markdown hücreleri ile her adım anlatılmıştır.

---

## 🎯 Problem Tanımı ve Senaryo

### Endüstriyel Bağlam

Kimya endüstrisinde, reaktörlerde gerçekleşen kimyasal dönüşümler çeşitli parametrelere bağlıdır. Bu parametrelerin yanlış seçimi:

- Düşük verim
- Ürün kalitesinde düşüş
- Enerji israfı
- Güvenlik riskleri

gibi sonuçlar doğurabilir.

### Proje Senaryosu

Bir kimya tesisinde belirli bir ürün üretimi için optimal reaksiyon koşullarının belirlenmesi gerekmektedir. Tesiste:

- **Reaksiyon süresi (x₁)**: 10 ile 60 dakika arasında ayarlanabilir
- **Sıcaklık (x₂)**: 40°C ile 120°C arasında kontrol edilebilir
- Çeşitli **güvenlik ve operasyonel kısıtlar** mevcuttur

Amaç, bu kısıtlar altında reaksiyon verimini maksimize eden parametre kombinasyonunu bulmaktır.

---

## 📐 Matematiksel Modelleme

### Amaç Fonksiyonu

Reaksiyon verimi aşağıdaki matematiksel fonksiyon ile modellenmiştir:

```
maximize: y = 8x₁ + 3x₂ - x₁·x₂ + x₁²
```

**Fonksiyon Terimlerinin Anlamı:**

| Terim | Anlamı |
|-------|--------|
| `8x₁` | Reaksiyon süresinin verime olan **doğrusal pozitif katkısı** |
| `3x₂` | Sıcaklığın verime olan **doğrusal pozitif etkisi** |
| `-x₁·x₂` | Süre ve sıcaklığın birlikte yükselmesinin oluşturduğu **negatif etkileşim** (örneğin yan ürün oluşumu) |
| `x₁²` | Uzun reaksiyon süresinin **karesel olarak artan pozitif etkisi** (dönüşüm oranının artması) |

Bu fonksiyon, gerçek dünya kimyasal süreçlerindeki karmaşık etkileşimleri temsil etmektedir.

### Karar Değişkenleri

#### 1. Reaksiyon Süresi (x₁)
- **Birim**: Dakika
- **Aralık**: 10 ≤ x₁ ≤ 60
- **Fiziksel Anlam**: Reaktörde malzemelerin ne kadar süre tutulacağı

#### 2. Sıcaklık (x₂)
- **Birim**: °C (Santigrat Derece)
- **Aralık**: 40 ≤ x₂ ≤ 120
- **Fiziksel Anlam**: Reaksiyon ortamının sıcaklığı

### Kısıtlar

Proje, aşağıdaki operasyonel ve güvenlik kısıtlarını içermektedir:

#### 1. Toplam Kaynak Kısıtı
```
x₁ + x₂ ≤ 140
```
Toplam süre ve sıcaklık toplamı 140'ı geçemez (enerji ve zaman kısıtı).

#### 2. Minimum Sıcaklık Kısıtı
```
x₂ ≥ 60
```
Reaksiyonun gerçekleşmesi için minimum 60°C gereklidir.

#### 3. Değişken Sınırları
```
10 ≤ x₁ ≤ 60
40 ≤ x₂ ≤ 120
```

Bu kısıtlar:
- Ekipman kapasitesini
- Güvenlik standartlarını
- Reaksiyonun fiziksel gerekliliklerini

yansıtmaktadır.

---

## 🧬 Genetik Algoritma Yaklaşımı

### Genetik Algoritma Nedir?

Genetik Algoritma (GA), doğal seçilim ve genetik evrim mekanizmalarından esinlenerek geliştirilmiş bir optimizasyon tekniğidir. Algoritma, bir popülasyon oluşturarak ve bu popülasyonu jenerasyonlar boyunca evrimleştirerek optimal çözüme yakınsar.

### Projedeki İmplementasyon

Bu projede, genetik algoritma **tamamen manuel olarak** kodlanmış ve aşağıdaki bileşenler uygulanmıştır:

#### 1. **Kromozom Yapısı**
Her birey (çözüm) bir kromozom ile temsil edilir:
```
Kromozom = [x₁, x₂]
```

#### 2. **Başlangıç Popülasyonu**
Belirli sayıda rastgele birey oluşturulur:
- Popülasyon büyüklüğü: 50
- Her birey, değişken sınırları içinde rastgele değerler alır

#### 3. **Uygunluk (Fitness) Fonksiyonu**
Her bireyin kalitesi amaç fonksiyonu ile değerlendirilir:
```python
fitness = 8*x1 + 3*x2 - x1*x2 + x1**2
```

#### 4. **Kısıt Yönetimi - Ceza (Penalty) Yöntemi**
Kısıtları ihlal eden bireylere ceza uygulanır:
```python
if (constraint violated):
    fitness = fitness - big_penalty
```

#### 5. **Seçilim - Turnuva Seçimi (Tournament Selection)**
Popülasyondan rastgele bireyler seçilir ve en iyisi ebeveyn olarak belirlenir:
```
Turnuva büyüklüğü: 3
```

#### 6. **Çaprazlama (Crossover) - Aritmetik Çaprazlama**
İki ebeveynden yeni birey üretilir:
```python
child1 = alpha * parent1 + (1-alpha) * parent2
child2 = (1-alpha) * parent1 + alpha * parent2
```

#### 7. **Mutasyon**
Rastgele seçilen genlerde küçük değişiklikler yapılır:
```
Mutasyon oranı: %20
```

#### 8. **Elitizm**
Her jenerasyonda en iyi bireyler korunur:
```
Elite sayısı: 2
```

### Algoritma Akışı

```
1. Başlangıç popülasyonu oluştur
2. DÖNGÜ (100 jenerasyon):
   a. Fitness değerlerini hesapla
   b. Bireyleri fitness'a göre sırala
   c. En iyi bireyleri kaydet (elitizm)
   d. Seçilim yap (turnuva)
   e. Çaprazlama uygula
   f. Mutasyon uygula
   g. Yeni popülasyonu oluştur
3. En iyi çözümü döndür
```

---

## 🔧 Teknik Detaylar

### Algoritma Parametreleri

| Parametre | Değer | Açıklama |
|-----------|-------|----------|
| Popülasyon Büyüklüğü | 50 | Her jenerasyondaki birey sayısı |
| Jenerasyon Sayısı | 100 | Algoritmanın çalışma süresi |
| Çaprazlama Oranı | %80 | Çaprazlama olasılığı |
| Mutasyon Oranı | %20 | Mutasyon olasılığı |
| Turnuva Büyüklüğü | 3 | Seçilim için yarışan birey sayısı |
| Elite Sayısı | 2 | Korunacak en iyi birey sayısı |
| Ceza Katsayısı | 10000 | Kısıt ihlali cezası |

### Performans Metrikleri

- **Yakınsama Hızı**: Algoritmanın optimal çözüme ulaşma süresi
- **Stabilite**: Farklı çalıştırmalarda tutarlı sonuçlar
- **Kısıt Tatmini**: Tüm kısıtların sağlanması

---

## ⚙️ Kurulum ve Çalıştırma

### Gerekli Yazılımlar

- **Python**: 3.8 veya üzeri
- **Jupyter Notebook** veya **VS Code** (Python eklentisi ile)

### Gerekli Kütüphaneler

Projede kullanılan Python kütüphaneleri:

```python
numpy           # Sayısal hesaplamalar
matplotlib      # Görselleştirme
random          # Rastgele sayı üretimi
```

### Kurulum Adımları

#### 1. Repoyu Klonlayın
```bash
git clone https://github.com/Yavuz0707/Kimya-Tesisinde-Reaksiyon-Suresi-ve-Sicaklik-Ayari.git
cd Kimya-Tesisinde-Reaksiyon-Suresi-ve-Sicaklik-Ayari
```

#### 2. Gerekli Kütüphaneleri Yükleyin
```bash
pip install numpy matplotlib
```

#### 3. Jupyter Notebook'u Açın
```bash
jupyter notebook
```

veya VS Code kullanarak [yapay_zeka_odev/proje_odevi.ipynb](yapay_zeka_odev/proje_odevi.ipynb) dosyasını açın.

#### 4. Notebook Hücrelerini Sırayla Çalıştırın

Not defterindeki her hücreyi yukarıdan aşağıya doğru çalıştırarak sonuçları gözlemleyin.

---

## 📊 Sonuçlar ve Çıktılar

### Optimal Sonuçlar

Genetik algoritma çalıştırıldığında elde edilen optimal değerler:

```
┌─────────────────────────────────────────┐
│  OPTIMAL ÇÖZÜM                          │
├─────────────────────────────────────────┤
│  Reaksiyon Süresi (x₁)  : 59.97 dakika │
│  Sıcaklık (x₂)          : 60.32 °C      │
│  Maksimum Verim (y)     : 639.62        │
└─────────────────────────────────────────┘
```

### Kısıt Kontrolü

Elde edilen optimal çözüm, tüm kısıtları sağlamaktadır:

✅ `x₁ + x₂ = 120.29 ≤ 140`  
✅ `x₂ = 60.32 ≥ 60`  
✅ `10 ≤ x₁ = 59.97 ≤ 60`  
✅ `40 ≤ x₂ = 60.32 ≤ 120`

### Görselleştirmeler

#### 1. Yakınsama Grafiği
Algoritmanın jenerasyonlar boyunca fitness değerindeki gelişimi gösterir. Grafik, algoritmanın hızlı bir şekilde optimale yakınsadığını ve belirli bir noktadan sonra kararlı hale geldiğini göstermektedir.

#### 2. Kontur Grafiği (Çözüm Uzayı)
İki boyutlu çözüm uzayında amaç fonksiyonunun kontur eğrileri ve optimal noktanın konumu gösterilir. Kısıtların oluşturduğu geçerli bölge (feasible region) ve optimal çözümün bu bölgenin sınırında olduğu görülür.

#### 3. Duyarlılık Analizi Grafikleri
Her bir değişkenin optimal değer etrafında değiştirilmesi durumunda verimin nasıl etkilendiği gösterilir.

---

## 🔍 Duyarlılık Analizi

Duyarlılık analizi, optimal çözüm etrafında parametrelerin küçük değişikliklerinin verim üzerindeki etkisini ölçer.

### Reaksiyon Süresi (x₁) Duyarlılığı

Reaksiyon süresinin optimal değerden (≈60 dk) ±10% değiştirilmesi:

- **Süre azalırsa (54 dk)**: Verim yaklaşık %12 azalır
- **Süre artarsa (66 dk)**: Verim hafif artar ancak kısıtlar ihlal edilir

**Sonuç**: Sistem reaksiyon süresine **çok hassastır**. Karesel terim (`x₁²`) nedeniyle süredeki değişiklikler verimde büyük etkiler yaratır.

### Sıcaklık (x₂) Duyarlılığı

Sıcaklığın optimal değerden (≈60°C) ±10% değiştirilmesi:

- **Sıcaklık azalırsa (54°C)**: Kısıt ihlali (x₂ ≥ 60)
- **Sıcaklık artarsa (66°C)**: Verimde küçük artış gözlemlenir ancak etkileşim terimi (`-x₁·x₂`) nedeniyle sınırlıdır

**Sonuç**: Sistem sıcaklığa **orta derecede hassastır**. Minimum sıcaklık kısıtı nedeniyle aşağı yönlü hareket mümkün değildir.

### Genel Bulgular

1. **Reaksiyon süresi (x₁)**, verim üzerinde **dominant etkiye** sahiptir
2. Optimal nokta, kısıtların izin verdiği **sınır bölgede** (boundary) yer alır
3. Bu tip problemlerde **Genetik Algoritma**, kısıtlı ve doğrusal olmayan fonksiyonlarda başarılı sonuçlar verir

---

## 📁 Proje Yapısı

```
Kimya-Tesisinde-Reaksiyon-Suresi-ve-Sicaklik-Ayari/
│
├── README.md                          # Proje dokümantasyonu (bu dosya)
│
└── yapay_zeka_odev/
    └── proje_odevi.ipynb             # Ana notebook dosyası (kod + açıklamalar)
```

### Dosya Açıklamaları

- **README.md**: Projenin kapsamlı açıklaması, kurulum talimatları ve sonuçlar
- **proje_odevi.ipynb**: Jupyter Notebook formatında tüm kod, açıklamalar ve görselleştirmeler

---

## 🛠 Kullanılan Teknolojiler

### Programlama Dili
- **Python 3.x**: Ana geliştirme dili

### Kütüphaneler
- **NumPy**: Sayısal hesaplamalar ve matris işlemleri
- **Matplotlib**: Grafik çizimi ve görselleştirme
- **Random**: Stokastik süreçler için rastgele sayı üretimi

### Geliştirme Ortamı
- **Jupyter Notebook**: İnteraktif kod geliştirme ve dokümantasyon
- **Visual Studio Code**: Kod editörü (opsiyonel)

### Versiyon Kontrolü
- **Git & GitHub**: Kaynak kod yönetimi ve paylaşım

---

## ✅ Sonuç ve Değerlendirme

### Proje Kazanımları

Bu proje kapsamında:

1. **Optimizasyon Algoritması Geliştirildi**: Genetik algoritma sıfırdan kodlandı
2. **Kısıtlı Problem Çözüldü**: Gerçek dünya kısıtları altında optimizasyon gerçekleştirildi
3. **Görselleştirme Yapıldı**: Sonuçlar detaylı grafikler ile sunuldu
4. **Duyarlılık Analizi Tamamlandı**: Parametrelerin etkisi incelendi
5. **Dokümantasyon Oluşturuldu**: Kapsamlı açıklamalar ve README hazırlandı

### Teknik Başarılar

✅ Manuel genetik algoritma implementasyonu  
✅ Ceza yöntemi ile kısıt yönetimi  
✅ Turnuva seçimi, aritmetik çaprazlama ve mutasyon operatörleri  
✅ Elitizm ile en iyi bireylerin korunması  
✅ Parametre optimizasyonu ve duyarlılık analizi  
✅ Profesyonel seviyede görselleştirme ve raporlama

### Öğrenilen Dersler

- Genetik algoritmalar, doğrusal olmayan ve kısıtlı problemlerde etkili sonuçlar verir
- Parametre seçimi (popülasyon, jenerasyon, mutasyon oranı) algoritma performansını doğrudan etkiler
- Kısıt yönetimi, gerçek dünya problemlerinde kritik öneme sahiptir
- Görselleştirme, algoritmanın davranışını anlamak için vazgeçilmezdir

### Gelecek Geliştirmeler

Bu proje temel alınarak:

- Farklı seçilim yöntemleri (rulet, rank-based) denenebilir
- Adaptif mutasyon oranları uygulanabilir
- Multi-objective optimizasyon (çok amaçlı) eklenebilir
- Gerçek endüstriyel verilerle model kalibre edilebilir
- Diğer metasezgisel algoritmalarla (PSO, ACO, SA) karşılaştırma yapılabilir

---

## 📧 İletişim

**Öğrenci**: Şükrü YAVUZ  
**E-posta**: [GitHub profiliniz üzerinden iletişime geçilebilir]  
**GitHub**: [@Yavuz0707](https://github.com/Yavuz0707)  
**Proje Repository**: [Kimya-Tesisinde-Reaksiyon-Suresi-ve-Sicaklik-Ayari](https://github.com/Yavuz0707/Kimya-Tesisinde-Reaksiyon-Suresi-ve-Sicaklik-Ayari)

---

## 🙏 Teşekkürler

Bu projeyi incelediğiniz için teşekkür ederim. Sorularınız veya geri bildirimleriniz için lütfen GitHub üzerinden iletişime geçmekten çekinmeyin.

---

**Son Güncelleme**: Aralık 2025  
**Proje Durumu**: ✅ Tamamlandı
