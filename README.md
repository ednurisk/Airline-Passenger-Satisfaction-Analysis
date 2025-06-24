✈️ Airline Passenger Satisfaction – Veri Analizi Raporu

📌 1. Veri Seti Genel Bilgisi
Veri seti Kaggle üzerinden yüklenmiştir: /kaggle/input/airline-passenger-satisfaction/train.csv

Unnamed: 0 sütunu gereksiz olduğu için analizden çıkarılmıştır.

Toplam gözlem sayısı: 103,904

Toplam değişken sayısı: 25 (1 tanesi çıkarıldıktan sonra)



Sayısal sütunlar: int64, float64 tipindeki sütunlar seçildi.
Kategorik sütunlar: object tipindeki sütunlar.

📊 2. Sayısal Değişkenlerin Özeti

Sayısal sütunlara ilişkin temel istatistikler (ortalama, min, max, std) incelenmiştir. Bu veriler:
Genel dağılımı,
Standart sapma ile yayılımı,
Aykırı değerlere dair ilk fikirleri vermektedir.


📈 3. Sayısal Değişkenlerin Dağılımı
Her sayısal sütun için histogram (dağılım grafiği) çizildi. Bu grafikler:
Verinin simetrik mi sağa/sola çarpık mı olduğunu,
Dağılımda yoğunluk noktalarını,
Normal dağılıma yakın olup olmadığını gösterir.

🔍 Gözlemler:

Bazı değişkenlerde tek tepe noktası (unimodal) gözlenmiştir.
Aykırı değerler bazı grafiklerde dikkat çekmiştir (örneğin Flight Distance).


🧩 4. Kategorik Değişkenlerin Özeti
Kategorik sütunların mod (en sık değer), benzersiz değer sayısı ve en sık tekrar eden değerin frekansı gösterildi.
Her kategorik değişken için ayrıca bar grafikleri çizildi. Bu sayede:
Sınıf dengesizlikleri (örneğin satisfaction, Gender) kolayca gözlemlendi.
Bazı sınıflar baskın olabilir; bu da modelleme aşamasında dikkate alınmalıdır.


❗ 5. Eksik Değer Analizi
Eksik değer sayısı ve oranı hesaplandı:
Eksik veri içeren sütunlar sadece gösterildi.
Eksik veri oranı görsel olarak barplot ile gösterildi.

🔍 Gözlemler:

Arrival Delay in Minutes gibi bazı sütunlarda düşük oranda eksik veri bulundu.
Eksik veri oranı genellikle %5’in altında. Bu oran, basit işlemlerle (median doldurma gibi) tolere edilebilir.

🚨 6. Aykırı Değer Analizi (Outliers)
Her sayısal sütun için IQR yöntemiyle (Q1 - 1.5IQR, Q3 + 1.5IQR) aykırı değerler bulundu.
Her sütun için aykırı değer sayısı ve oranı hesaplandı.
Aykırı oranı %10’dan fazla olan değişkenler dikkatle ele alınmalıdır.

📦 Boxplot Görselleştirmeleri:
Boxplot’lar ile her sütundaki uç değerler görselleştirildi.
Özellikle Flight Distance, Departure Delay, Arrival Delay gibi değişkenlerde ciddi aykırılıklar bulunmakta.

🔚 Genel Değerlendirme
Kategori	Gözlem
Veri Kalitesi	Yüksek (çok az eksik veri)
Aykırı Değerler	Bazı değişkenlerde yüksek
Sütunlar	Çoğu anlamlı ve modellemeye uygun
Görselleştirme	Dağılımlar, kategorik yapı net bir şekilde gösterilmiş

✅ Öneriler – Bir Sonraki Adım İçin:
Eksik veriler:
Ortalama/medyan ile doldurulabilir.
Alternatif olarak KNN Imputer gibi daha sofistike yöntemler uygulanabilir.

Aykırı değerler:
Aykırı değerler modelleri bozabilir. Bu yüzden:
Winsorization,
Log-transform,
Outlier removal gibi yöntemler uygulanabilir.

Veri Normalizasyonu:
Özellikle Flight Distance, Delay gibi değişkenlerde büyük aralıklar var. StandardScaler veya MinMaxScaler kullanılabilir.

Korelasyon ve Feature Engineering:
Sayısal değişkenler arası korelasyon analizi yapılmalı.
Gerekirse yeni değişkenler türetilebilir.

Modelleme için uygunluk:
Veriler sınıflandırma modelleri için oldukça uygun gözüküyor (satisfaction hedef değişken olarak kullanılabilir).

