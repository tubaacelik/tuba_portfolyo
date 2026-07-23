# CONTENT-TODO: Yanıt Bekleyen İçerik Soruları

Bu dosya, portföy içeriğinde gerçek verisi olmadığı için boş bırakılan ya da
eksik doldurulan noktaları listeler. Her bölümdeki soruları yanıtladıktan
sonra ilgili HTML dosyasındaki TODO yorumlarını temizle.

---

## MMX: Türkçe Pazarlama LLM'i
**Dosya:** `projeler/mmx-turkce-pazarlama-llm.html`, `index.html`, `projeler.html`

- [ ] Fine-tuning öncesinde hangi alternatifler değerlendirildi? (örn: prompt engineering, RAG, genel amaçlı LLM)
- [ ] Baseline format uyum oranı neydi? (%94'e kıyasla başlangıç değeri)
- [ ] İnsan değerlendirme skoru: başlangıç vs. son (1-5 skalası veya karşılaştırmalı tercih testi)
- [ ] Model üretimde aktif mi? Kaç kullanıcı/istek?
- [ ] Hangi model ailesi seçildi? (MMX için nihai model: Qwen mi, Gemma mi?)

---

## Qwen Fine-tuning Deneyi
**Dosya:** `projeler/qwen-fine-tuning-deneyi.html`, `index.html`, `projeler.html`

- [ ] Üretim için hangi model seçildi? (2B mi, 7B mi?)
- [ ] Her modelin benchmark skoru neydi? (mutlak sayılar, sadece "27B geri kaldı" değil)
- [ ] 27B ile 7B arasındaki skor farkı tam olarak ne kadar?
- [ ] Sonuçlar hangi kararı değiştirdi? (model boyutu seçimi mi, eğitim verisi yaklaşımı mı?)

---

## LLM Değerlendirme Pipeline Yeniden Tasarımı
**Dosya:** `projeler/llm-degerlendirme-pipeline.html`, `index.html`, `projeler.html`

- [ ] Yeni sistemle hangi modeller yeniden değerlendirildi?
- [ ] Yeniden değerlendirme sonrası model sıralaması değişti mi?
- [ ] %85 insan uyum oranı nasıl ölçüldü? (metodoloji: annotator sayısı, sorgu seti, ölçek)
- [ ] "~15 puan bastırma" iddiası: hangi metrikte, hangi model için?

---

## Kredi Kartı Risk Analizi
**Dosya:** `projeler/kredi-karti-risk-analizi.html`, `projeler.html`

- Bilgi tamamlanmış görünüyor. Kaggle not defteri bağlantısı aktif mi? Kontrol et.
- [ ] Model üretimde kullanıldı mı? Yoksa akademik/Kaggle projesi mi olarak kaldı?

---

## On-Prem LLM Platformu
**Dosya:** `projeler/on-prem-llm-platformu.html`, `projeler.html`

- [ ] Platform kaç aktif kullanıcı veya departmanla kullanılıyor?
- [ ] AWQ vs GPTQ kalite delta benchmarkı: sayısal fark var mı?
- [ ] Eş zamanlı istek kapasitesi testi sonucu (örn: max X istek/dakika)
- [ ] DGX Spark'tan önce hangi altyapı kurgulanmıştı?

---

## Risk Skorlama Aracı
**Dosya:** `projeler/risk-skorlama-araci.html`, `projeler.html`

- [ ] %91 precision rakamı hangi test setinde, hangi eşik değeriyle ölçüldü?
- [ ] Recall oranı neydi? (Precision yüksek ama recall çok düşükse anlamı değişir)
- [ ] %60 manuel iş yükü azalması nasıl ölçüldü? (süre, işlem sayısı, ekip geri bildirimi?)
- [ ] Dashboard kaç kişi tarafından aktif kullanılıyor?
- [ ] LLM katmanının eğitim kalitesine etkisi ölçüldü mü?

---

## Genel Eksikler

- [ ] **CV dosyası:** `TODO_CV_FILE` placeholder'ı hâlâ aktif. CV hazır olduğunda `index.html:112` satırını aç.
- [ ] **Formspree ID:** `TODO_FORMSPREE_FORM_ID` placeholder'ı hâlâ aktif. `index.html:513` ve `iletisim.html`'de güncelle.
- [ ] **Instagram:** @tubac3l1k aktif hale geldiğinde `index.html` ve `hakkimda.html`'deki span'ı `<a>` etiketine çevir.
- [ ] **English pages:** `/en/` dizinindeki sayfalar Türkçe içerikle senkron değil. Stratejik yeniden yazım bekliyor.
- [ ] **bm-cenevre-yapay-zeka-yonetisimi.html:** meta/main/skip link yapısı güncellenmedi.
