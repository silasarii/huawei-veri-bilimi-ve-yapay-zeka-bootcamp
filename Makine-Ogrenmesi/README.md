# 🤖 Makine Öğrenmesi Uygulamaları ve Projeleri

Bu klasör, **Huawei Student Developers** ve **Türkiye Yapay Zeka Akademisi** iş birliğiyle düzenlenen Veri Bilimi ve Makine Öğrenmesi Bootcamp'inin 3. haftası kapsamında tamamlanan temel ve uçtan uca makine öğrenmesi ödevlerini içermektedir.

---

## 📂 İçerik ve Dosya Yapısı

| Dosya Adı | Konu / Açıklama |
| :--- | :--- |
| `ara_odev.ipynb` | Müşteri Ayrılma (Customer Churn) tahmini odaklı temel makine öğrenmesi akışı |
| `final_odevi.ipynb` | Bank Marketing veri seti üzerinde geliştirilen uçtan uca makine öğrenmesi ve hiperparametre optimizasyonu projesi |

---

## 📊 Kullanılan Veri Setleri

| Ödev Türü | Veri Seti | Gözlem Sayısı | Değişken Sayısı | Hedef Değişken (`Target`) | Problem Türü |
| :--- | :--- | :---: | :---: | :--- | :--- |
| **Ara Ödev** | Müşteri Ayrılma (*Customer Churn*) | 120 | 8 | `churn` (0: Kalır, 1: Ayrılır) | Sınıflandırma (*Classification*) |
| **Final Ödevi** | Bank Marketing Veri Seti | 45.211 | 17 | `y` (Term Deposit: yes/no) | Sınıflandırma (*Classification*) |

---

## 📌 Ödev Detayları ve Uygulama Akışları

### 📄 1. Ara Ödev (`ara_odev.ipynb`)
**Müşteri Ayrılma Tahmini ile Temel Makine Öğrenmesi Akışı**
1. **Veri Hazırlama & İnceleme:** Veri setinin yapısal özellikleri, ilk satırları ve hedef değişken (`churn`) sınıf dağılımı analizi.
2. **Ön İşleme & Öznitelik Mühendisliği:**
   - Eksik değer kontrolleri ve temizleme.
   - Kategorik değişkenler için **One-Hot Encoding**.
   - Sayısal değişkenler üzerinde ölçekleme (*Feature Scaling*).
   - Yeni öznitelik türetimi (Örn: `gelir_grubu`, `destek_talebi_var_mi`).
3. **Veri Bölme:** Sınıf oranlarını korumak adına `stratify` parametresi kullanılarak **Train - Validation - Test** ayrımı.
4. **Model Eğitimi & Karşılaştırma:**
   - **Logistic Regression** ve **KNN (K-Nearest Neighbors)** modellerinin eğitimi.
   - Validation performansı kıyaslaması.
5. **Model Değerlendirme:** Test verisi üzerinde *Confusion Matrix*, *Accuracy*, *Precision*, *Recall* ve *F1-Score* metrikleri ile model başarısının yorumlanması.

---

### 📄 2. Final Ödevi (`final_odevi.ipynb`)
**Uçtan Uca Makine Öğrenmesi Projesi (Bank Marketing)**
1. **Problem Tanımı & EDA:** 45.211 gözlemli Bank Marketing veri seti üzerinde müşteri vadeli mevduat katılım tahmini.
2. **Gelişmiş Ön İşleme:**
   - Detaylı eksik/aykırı değer analizi ve tespiti.
   - Categorical Encoding & Feature Scaling işlemleri.
3. **Öznitelik Mühendisliği & Seçimi:**
   - Etkileşimli yeni özniteliklerin üretilmesi (En az 2 adet).
   - Korelasyon ve Feature Importance yöntemleri ile değişken seçimi (*Feature Selection*).
4. **Modelleme & Cross-Validation:**
   - En az 3 farklı modelin (**Logistic Regression, Decision Tree, Random Forest / SVM**) eğitimi.
   - Stratified Train-Validation-Test ayrımı ve modellerin metrik bazlı kıyaslanması.
5. **Hiperparametre Optimizasyonu:** Seçilen en başarılı model üzerinde **Grid Search / Random Search** ile parametre ince ayarı (*Tuning*).
6. **Model Açıklanabilirliği & Değerlendirme:**
   - Test seti üzerinde detaylı performans metrikleri (Confusion Matrix, Precision-Recall Curve, F1-Score).
   - Modelin Feature Importance veya katsayı yorumları üzerinden iş odaklı açıklaması.

---

## 🛠️ Kullanılan Kütüphaneler ve Ortam

- **Python**
- **Pandas & NumPy:** Veri manipülasyonu ve matris operasyonları.
- **Scikit-Learn:** Veri ön işleme, ölçekleme, model eğitimi, hiperparametre optimizasyonu ve değerlendirme metrikleri.
- **Matplotlib & Seaborn:** Confusion matrix ve model metrik görselleştirmeleri.
