🧬 Genetik Algoritma ile Optimizasyon
Kimya Tesisinde Reaksiyon Süresi ve Sıcaklık Ayarı

Bu projede, bir kimya tesisinde reaksiyon süresi (x1) ve sıcaklık (x2) parametrelerinin reaksiyon verimi üzerindeki etkisi Genetik Algoritma (GA) kullanılarak optimize edilmiştir.
Çalışma, genetik algoritmanın temel bileşenleri manuel olarak uygulanarak gerçekleştirilmiştir.

👤 Öğrenci Bilgileri

Ad Soyad: Şükrü YAVUZ

Öğrenci No: 2312729015

Ders: Genetik Algoritmalar

🎯 Problem Tanımı

Amaç, aşağıdaki matematiksel ifadeyle tanımlanan reaksiyon verimini maksimum yapan parametreleri bulmaktır:

𝑦
=
8
𝑥
1
+
3
𝑥
2
−
𝑥
1
𝑥
2
+
𝑥
1
2
y=8x
1
	​

+3x
2
	​

−x
1
	​

x
2
	​

+x
1
2
	​

🔧 Değişkenler

x1: Reaksiyon süresi (dk) → [10, 60]

x2: Sıcaklık (°C) → [40, 120]

⚠️ Kısıtlar

𝑥
1
+
𝑥
2
≤
140
x
1
	​

+x
2
	​

≤140

𝑥
2
≥
60
x
2
	​

≥60

🧠 Genetik Algoritma Yaklaşımı

Bu çalışmada genetik algoritma hazır GA kütüphaneleri kullanılmadan, adım adım manuel olarak uygulanmıştır.

Kullanılan GA Bileşenleri

Kromozom Yapısı: [x1, x2]

Başlangıç Popülasyonu: Rastgele oluşturma

Uygunluk (Fitness) Fonksiyonu: Amaç fonksiyonu

Kısıt Yönetimi: Ceza (Penalty) yöntemi

Seçilim: Turnuva seçimi (Tournament Selection)

Çaprazlama: Aritmetik çaprazlama

Mutasyon: Rastgele gen mutasyonu

Elitizm: En iyi bireylerin korunması

Jenerasyon Sayısı: 100

Bu yapı sayesinde algoritma, geçerli çözüm uzayına yönlendirilmiş ve optimum sonuca ulaşmıştır.

📊 Elde Edilen Sonuçlar

Genetik algoritma çalıştırıldığında aşağıdaki sonuçlar elde edilmiştir:

Optimal Reaksiyon Süresi (x1): ≈ 60 dk

Optimal Sıcaklık (x2): ≈ 60 °C

Maksimum Reaksiyon Verimi: ≈ 660

📈 Üretilen Grafikler

Genetik algoritma yakınsama grafiği (fitness – jenerasyon)

Amaç fonksiyonunun kontur grafiği

Kısıt bölgelerinin görsel gösterimi

Bulunan optimal çözümün çözüm uzayı üzerinde işaretlenmesi

🔍 Duyarlılık Analizi ve Yorum

Elde edilen sonuçlar, optimum noktanın kısıtların izin verdiği sınır bölgede oluştuğunu göstermektedir.

x1 (reaksiyon süresi) değişkeni, fonksiyonda karesel terim (
𝑥
1
2
x
1
2
	​

) içermesi nedeniyle verim üzerinde daha baskın etkiye sahiptir.

Reaksiyon süresinde yapılan küçük azalışlar, verimde belirgin düşüşlere yol açmaktadır.

Bu durum, sistemin reaksiyon süresine karşı daha hassas olduğunu göstermektedir.

▶️ Çalıştırma Talimatları
Gerekli Kütüphaneler
pip install numpy matplotlib

Çalıştırma

Kod Jupyter Notebook veya VS Code (Python) ortamında çalıştırılabilir.

Hücreler sırasıyla çalıştırıldığında tüm sonuçlar ve grafikler otomatik olarak üretilecektir.

✅ Sonuç

Bu çalışma kapsamında:

Genetik algoritma mantığı eksiksiz şekilde uygulanmış,

Problem kısıtları dikkate alınmış,

Sonuçlar grafiklerle desteklenerek analiz edilmiştir.

Elde edilen bulgular, genetik algoritmanın kısıtlı ve çok değişkenli optimizasyon problemlerinde etkili bir yöntem olduğunu göstermektedir.
