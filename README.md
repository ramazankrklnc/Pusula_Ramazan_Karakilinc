# 🏥 Physical Medicine & Rehabilitation Dataset Analysis

## Geliştirici: **Ramazan Karakılınç**
- 📧 Email: ramazankarakilinc06@gmail.com
- 💼 LinkedIn: [Ramazan Karakılınç](https://www.linkedin.com/in/ramazankarakilinc/)
- 🐙 GitHub: [@ramazankrklnc](https://github.com/ramazankrklnc)

---
## 📋 Proje Hakkında
Bu proje, **Pusula Talent Data Science** staj programı kapsamında gerçekleştirilen fizik tedavi ve rehabilitasyon veri seti analizi çalışmasıdır. 2235 hasta kaydı üzerinde kapsamlı bir keşifsel veri analizi (EDA) ve veri ön işleme süreci gerçekleştirilmiştir.

### 🎯 Proje Amacı
- **Hedef Değişken:** TedaviSuresi (Seans cinsinden)
- **Ana Görev:** Kapsamlı EDA, Pre-processing ve model-ready veri hazırlama
- **Sonuç:** 52 feature ile makine öğrenmesi için hazır veri seti
---
## 📊 Veri Seti Özeti

| Özellik | Değer |
|---------|-------|
| **Toplam Gözlem** | 2,235 |
| **Toplam Özellik** | 13 |
| **Sayısal Özellikler** | 2 |
| **Kategorik Özellikler** | 11 |
| **Hedef Değişken** | TedaviSuresi |

### 🔍 Veri Seti Özellikleri
- **HastaNo:** Anonim hasta kimliği
- **Yas:** Yaş bilgisi
- **Cinsiyet:** Cinsiyet bilgisi
- **KanGrubu:** Kan grubu
- **Uyruk:** Uyruk bilgisi
- **KronikHastalik:** Kronik hastalıklar
- **Bolum:** Bölüm/Klinik
- **Alerji:** Alerji bilgileri
- **Tanilar:** Tanılar
- **TedaviAdi:** Tedavi adı
- **TedaviSuresi:** Tedavi süresi (seans) - **HEDEF**
- **UygulamaYerleri:** Uygulama yerleri
- **UygulamaSuresi:** Uygulama süresi
---
## 🚀 Kurulum ve Kullanım
### Gereksinimler
```bash
Python 3.8+
pandas >= 1.3.0
numpy >= 1.21.0
matplotlib >= 3.3.0
seaborn >= 0.11.0
scikit-learn >= 1.0.0
missingno >= 0.5.0
```
### Kurulum
```bash
# Repository'yi klonlayın
git clone https://github.com/ramazankrklnc/Pusula_Ramazan_Karakilinc.git

# Proje dizinine gidin
cd Pusula_Ramazan_Karakilinc
```
### Kullanım
```bash
# Jupyter Notebook'u başlatın
jupyter notebook

# Ana analiz dosyasını açın
Last.ipynb
```
---
## 📈 Analiz Süreci

### 1. 🔍 Exploratory Data Analysis (EDA)
- **Veri Kalitesi Analizi:** Eksik değer tespiti ve analizi
- **Tekrarlanan Kayıt Analizi:** 392 hasta birden fazla kayda sahip
- **Hedef Değişken Analizi:** TedaviSuresi dağılımı ve kategorilere ayırma
- **Kategorik Değişken Analizi:** Tüm kategorik değişkenlerin detaylı analizi
- **Aykırı Değer Analizi:** IQR yöntemi ile outlier tespiti

### 2. 🛠️ Veri Ön İşleme
- **Eksik Değer Doldurma:** 3 farklı strateji ile 2,706 eksik değer dolduruldu
- **Veri Temizleme:** Tutarsızlıklar giderildi
- **Encoding:** OneHotEncoder ve LabelEncoder kullanımı
- **Normalizasyon:** StandardScaler ile sayısal değişkenler normalize edildi

### 3. 📊 Görselleştirme
- Eksik değer haritası
- Dağılım grafikleri
- Box plot'lar
- Korelasyon analizi
- Aykırı değer görselleştirmesi
---
## 🎯 Ana Bulgular

### 📊 Veri Kalitesi
- **2,706 eksik değer** başarıyla dolduruldu
- **392 hasta** birden fazla kayda sahip
- **0 eksik değer** kaldı

### 📈 Hedef Değişken Analizi
| Kategori | Hasta Sayısı | Oran |
|----------|--------------|------|
| Kısa (≤10 seans) | 296 | 13.2% |
| Orta (11-20 seans) | 1,887 | 84.4% |
| Uzun (>20 seans) | 52 | 2.3% |

### 👥 Hasta Profili
- **Yaş Dağılımı:** 2-92 yaş arası, ortalama 47.3
- **Cinsiyet:** Kadın hastalar daha fazla (%58.1)
- **Uyruk:** Çoğunluk Türkiye (%97.2)
---
## 🔧 Teknik Detaylar

### Kullanılan Kütüphaneler
```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
import missingno as msno
from sklearn.preprocessing import OneHotEncoder, LabelEncoder, StandardScaler
import re
import unicodedata
import warnings
```

### Ana Fonksiyonlar
1. **`extract_first_int()`** - Sayısal değer çıkarma
2. **`fill_from_same_patient()`** - Aynı hasta kayıtlarından doldurma
3. **`fill_by_tedavi()`** - Tedavi bazlı doldurma
4. **`categorize_tedavi_suresi()`** - Tedavi süresi kategorilere ayırma
---
## 📁 Proje Yapısı
```
physical-medicine-rehabilitation-analysis/
│
├── 📊 data.xlsx                            # Orijinal veri seti
├── 📓 Pusula_Ramazan_Karakilinc.ipynb      # Analiz notebook'u
├── 📄 Pusula_Intern_Data_Science_2025.pdf  # Proje gereksinimleri
├── 📄 Dokümantasyon.pdf                    # Detaylı rapor
├── 📄 README.md                            # Bu dosya
```
---
## 🎯 Sonuçlar

### ✅ Başarılı Tamamlanan Görevler
- **EDA:** Kapsamlı keşifsel veri analizi
- **Eksik Değer Doldurma:** 2,706 eksik değer dolduruldu
- **Veri Temizleme:** Tutarsızlıklar giderildi
- **Encoding:** Kategorik değişkenler encode edildi
- **Normalizasyon:** Sayısal değişkenler normalize edildi
- **Model-Ready Veri:** 52 feature ile hazır veri seti

### 🚀 Gelecek Adımlar
1. **Model Geliştirme:** Regression modelleri test edilebilir
2. **Feature Selection:** Önemli feature'lar seçilebilir
3. **Cross-Validation:** Model performansı değerlendirilebilir
4. **Hyperparameter Tuning:** Model parametreleri optimize edilebilir

### 🤖 Önerilen Modeller
- **Linear Regression:** Baseline model
- **Random Forest:** Feature importance analizi
- **XGBoost:** Yüksek performans
- **Neural Networks:** Karmaşık ilişkiler
---
## 👥 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some AmazingFeature'`)
4. Branch'inizi push edin (`git push origin feature/AmazingFeature`)
5. Pull Request oluşturun
---