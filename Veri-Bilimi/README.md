# 📊 Veri Bilimi

Bu klasör, **Huawei Student Developers** ve **Türkiye Yapay Zeka Akademisi** iş birliğiyle düzenlenen Veri Bilimi ve Makine Öğrenmesi Bootcamp'inin 2. haftası kapsamında e-ticaret veri seti üzerinde gerçekleştirilen Veri Temizleme, Keşifçi Veri Analizi (EDA) ve Veri Hikayeleştirme çalışmalarını içermektedir.

---

## 📂 İçerik ve Dosya Yapısı

| Dosya / Klasör Adı | Tür | Açıklama |
| :--- | :---: | :--- |
| `e_ticaret_veri_seti.csv` | Veri Seti | Analizlerde kullanılan ham e-ticaret veri seti. |
| `temizlenmis_veri.csv` | Veri Seti | Ara ödev aşamasında temizlenmiş, dönüştürülmüş ve analize hazır hale getirilmiş veri seti. |
| `ara_odev.ipynb` | Notebook | Veri seti tanıma, eksik/aykırı değer temizleme, metin standartlaştırma, tip dönüşümleri ve temel EDA adımları. |
| `final_odevi.ipynb` | Notebook | **2. Hafta Bitirme Projesi:** Temizlenmiş veri seti üzerinden kategori, şehir, ödeme türü, zaman serisi ve çapraz kırılımlarla (şehir-kategori) iş odaklı analizler ve görselleştirmeler. |

---

## 📌 Ödev Detayları ve Kapsamı

### 📄 1. Ara Ödev (`ara_odev.ipynb`)
E-ticaret veri setinin temizlenmesi ve analize hazır hale getirilmesi adımlarını kapsar:
1. **Veri Setini Tanıma:** İlk/son 10 satır incelemesi, satır/sütun sayıları, `info()` ve `describe()` özetleri ile sayısal ve kategorik sütun ayrımı.
2. **Eksik Veri (Missing Data) Analizi:** Eksik veri oranlarının tespiti ve en yüksek 5 sütunun belirlenmesi.
   - `indirim_orani` & `musteri_puani` $\rightarrow$ Medyan (Median) ile doldurma.
   - `odeme_turu` & `musteri_tipi` $\rightarrow$ Mod (Mode) ile doldurma.
3. **Veri Tipleri & Sütun Türetimi:** `siparis_tarihi` sütununun `datetime` tipine çevrilerek `siparis_yili`, `siparis_ayi`, `siparis_gunu` ve `haftanin_gunu` sütunlarının üretilmesi.
4. **Tekrarlayan Kayıtlar (Duplicates):** Duplicate verilerin tespiti ve temizlenmesi.
5. **Metin & Kategori Standartlaştırma:** `sehir` (`İstanbul`, `istanbul` vb.) ve `kategori` (`Ev Yaşam`, `ev&yaşam` vb.) sütunlarındaki yazım tutarsızlıklarının tek biçime dönüştürülmesi.
6. **Mantıksal Hata & Aykırı Değer Analizi:**
   - Mantıksal hatalı kayıtların (`birim_fiyat <= 0`, `toplam_tutar <= 0`, `teslimat_gunu < 0`, `musteri_puani > 5`) çıkarılması.
   - `birim_fiyat` sütununda **IQR (Interquartile Range)** yöntemi ile aykırı değer tespiti.
7. **Keşifçi Veri Analizi (EDA):** Histogram, Box plot ve Count plot görselleştirmeleri ile iş sorularına yanıt aranması.

---

### 📄 2. Final Ödevi (`final_odevi.ipynb`)
Temizlenmiş e-ticaret veri seti üzerinden iş stratejileri ve karar destek analizleri çıkarma süreci:
1. **Kategori Bazlı Performans & Memnuniyet:** Sipariş sayısı, toplam gelir, ortalama sipariş tutarı, müşteri puanı ve teslimat sürelerinin analizi. Bar plot ile ticari performans ve memnuniyet kıyaslaması.
2. **Şehir Bazlı Potansiyel Analizi:** Şehirlerin gelir sıralaması, ilk 5 şehir görselleştirmesi ve *"Müşteri puanı yüksek ancak geliri geride kalmış"* büyüme adayı şehirlerin tespiti.
3. **Ödeme Türü & Müşteri Davranışı:** En yüksek gelir üreten ödeme yöntemi ile en yüksek memnuniyet sağlayan ödeme yönteminin karşılaştırması ve iş diliyle yorumlanması.
4. **Zaman Serisi & Satış Eğilimi:** Ay bazında sipariş sayısı ve gelir değişimi (Line Plot). Sipariş artışı ile gelir artışının paralelliğinin incelenmesi.
5. **Şehir - Kategori Çapraz Analizi:** En güçlü 10 şehir-kategori kombinasyonunun tespiti ve pazarlama/kampanya stratejilerine dönüştürülmesi.

---

## 🛠️ Kullanılan Teknolojiler ve Kütüphaneler

- **Python**
- **Pandas & NumPy:** Veri manipülasyonu, veri temizleme, gruplama (`groupby`) ve özet tablo oluşturma.
- **Matplotlib & Seaborn:** Veri görselleştirme (Bar plot, Line plot, Box plot, Count plot, Histogram).
