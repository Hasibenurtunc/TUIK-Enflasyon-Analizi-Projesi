# TÜİK Enflasyon Analizi Projesi

##  Proje Amacı

TÜİK (Türkiye İstatistik Kurumu) verileri kullanılarak son yıllardaki enflasyon eğilimleri, harcama kalemleri ve bölgesel farklılıkların incelenmesi. Temel istatistiksel analizler, grafikler ve basit zaman serisi uygulamaları ile Python'da veri analizi pratiği kazanmak.

##  Proje Hedefleri

- TÜFE (Tüketici Fiyat Endeksi) trend analizi
- Harcama grupları bazında enflasyon analizi
- Mevsimsel etkilerin belirlenmesi
- Kategoriler arası korelasyon analizi
- Hareketli ortalama ile trend tespiti
- Basit tahmin modeli geliştirme

##  Proje Yapısı

```
proje/
├── data/
│   ├── tuik_dataset.csv          # Orijinal TÜİK verileri
│   ├── tuik_dataset.xls          # Excel formatında veriler
│   └── tuik_tufe_long.csv        # Long format'a çevrilmiş veriler
├── notebooks/
│   ├── 1_veri_kesfetme.ipynb     # Veri temizleme ve hazırlama
│   ├── 2_analiz_ve_görsellestirme.ipynb  # Kapsamlı analizler
│   └── 3_tahmin_modeli.ipynb     # Makine öğrenmesi modeli
└── README.md                     # Proje dokümantasyonu
```

##  Veri Seti Bilgileri

### Veri Toplama
- **Kaynak:** TÜİK web sitesi
- **Veri Türü:** Tüketici Fiyat Endeksi (TÜFE)
- **Dönem:** 2005-2025
- **Kategoriler:** 12 ana harcama grubu
- **Frekans:** Aylık

### Veri Hazırlama Süreci
1. **Veri Toplama:** TÜİK'ten TÜFE verileri indirildi
2. **Veri Temizleme:** Eksik değerler kontrol edildi ve temizlendi
3. **Format Dönüşümü:** Wide format'tan long format'a çevrildi
4. **Tarih Sütunu:** Kronolojik sıralama için tarih sütunu oluşturuldu

### Veri Seti Özellikleri
- **Toplam kayıt:** 14,246
- **Kategori sayısı:** 12
- **Zaman aralığı:** 20 yıl (2005-2025)
- **Format:** CSV (UTF-8 encoding)

##  Yapılan Analizler

### 1. Temel İstatistiksel Analizler
- **Yıllık TÜFE trend analizi**
- **Yıllık artış oranları hesaplama**
- **En yüksek/düşük artış oranları tespiti**
- **Standart sapma analizi**

### 2. Harcama Kategorileri Analizi
- **En çok artan 10 kategori tespiti**
- **Kategori bazında trend analizi**
- **Harcama grupları karşılaştırması**

### 3. Zaman Serisi Analizleri
- **Mevsimsel etkiler analizi**
- **Aylık patterns tespiti**
- **Hareketli ortalama analizi (Sigorta kategorisi)**

### 4. Korelasyon Analizi
- **Gıda-Sağlık kategorileri arası korelasyon**
- **Korelasyon katsayısı: 0.997 (Güçlü pozitif korelasyon)**

### 5. Makine Öğrenmesi
- **Lineer regresyon modeli**
- **Gelecek 6 ay TÜFE tahmini**
- **Model performans değerlendirmesi (R² = 0.26)**

##  Önemli Bulgular

### Enflasyon Trendi
- 2005-2020: Görece istikrarlı artış
- 2020-2022: Dramatik artış dönemi
- 2022: En yüksek artış oranı (%66.31)
- 2023-2025: Yavaşlama trendi

### En Çok Artan Kategoriler
1. Sigorta
2. Gerçek Kira
3. Sosyal Hizmetler
4. Lokanta & Oteller
5. Posta Hizmetleri

### Korelasyon Analizi
- Gıda ve Sağlık kategorileri arasında güçlü pozitif korelasyon (0.997)
- Enflasyonun farklı harcama kalemlerini benzer şekilde etkilediği tespit edildi

## 🛠 Kullanılan Teknolojiler

### Python Kütüphaneleri
- **pandas** - Veri manipülasyonu ve analizi
- **numpy** - Sayısal hesaplamalar
- **matplotlib** - Temel görselleştirme
- **seaborn** - Gelişmiş görselleştirme
- **scikit-learn** - Makine öğrenmesi modelleri

### Veri İşleme
- **Veri temizleme:** NaN değer tespiti ve temizleme
- **Veri dönüşümü:** Wide to long format
- **Zaman serisi:** Hareketli ortalama hesaplama

##  Görselleştirmeler

### Üretilen Grafikler
1. **Yıllık TÜFE trend grafiği**
2. **Yıllık artış oranları bar grafiği**
3. **En çok artan 10 kategori line plot**
4. **Mevsimsel analiz grafiği**
5. **Korelasyon scatter plot**
6. **Hareketli ortalama analizi**
7. **Tahmin modeli performans grafiği**

##  Sonuçlar ve Öneriler

### Ana Bulgular
- Türkiye'de enflasyon 2021-2022 döneminde zirve yapmıştır
- Hizmet sektörü kategorileri en çok etkilenen gruplardır
- Gıda ve sağlık harcamaları arasında güçlü korelasyon vardır
- Mevsimsel etkiler TÜFE'de belirgin rol oynamaktadır

### Pratik Uygulamalar
- **Risk yönetimi:** Gelecek planlaması için trend analizi
- **Bütçe planlaması:** Harcama tahminleri
- **Politika kararları:** Ekonomik önlemler için veri desteği

##  Geliştirici

Bu proje, TÜİK verileri kullanılarak Python ile veri analizi pratiği kazanmak amacıyla geliştirilmiştir.

##  Lisans

Bu proje eğitim amaçlı geliştirilmiştir.


**Not:** Bu analiz sonuçları sadece eğitim amaçlıdır ve resmi ekonomik kararlar için kullanılmamalıdır.
