# Tubi Portfolyo Sitesi — Tasarım Brief'i (Son Sürüm)

> Bu dosya Claude Code'a verilmek üzere hazırlanmıştır. Tasarım dili (neobrutalism),
> sayfa yapısı ve içerik burada tanımlı. İçerik metinleri taslaktır — Tubi di’lediği
> gibi düzenleyebilir. Bu, yaygın bir tasarım trendinin (neobrutalism) kendi
> içeriğimizle uygulanmasıdır; kimsenin metni/logosu/fotoğrafı kopyalanmaz.

---

## 1. Tasarım Dili: Neobrutalism

- **Kalın siyah çizgiler:** Kart, buton, ikon, etiket etrafında ~3px koyu (#1A1A1A) kontur.
- **Sert gölgeler:** Blur YOK. Düz, kaydırılmış siyah blok. Örn: `box-shadow: 6px 6px 0 #1A1A1A;`
- **Gradient YOK** (temel UI'da düz renk).
- **Yuvarlatılmış köşeler:** Kartlarda 14–18px, butonlarda pill (tam yuvarlak).
- **Bol boşluk + büyük, kalın tipografi** (800–900 weight, genelde uppercase başlık).
- **Krem zemin** (#F7F0E4) üstünde canlı renk blokları.
- **Dekoratif "sticker" şekiller:** Kenarlarda soyut yarım daireler, üçgenler, oklar
  (siyah konturlu, canlı renkli) — ferahlığı bozmadan, abartısız.

---

## 2. Renk Paleti

| Rol | Hex | Kullanım |
|-----|-----|----------|
| Krem (zemin) | `#F7F0E4` | Ana arka plan |
| Kart beyazı | `#FFFDF8` | Kart iç zemini |
| Siyah (kontur/metin) | `#1A1A1A` | Kenarlık, gölge, ana metin |
| Pembe | `#EC5A9E` | Aksan, etiket, dekoratif |
| Sarı | `#F5C842` | Birincil buton (CTA), vurgu |
| Teal | `#2BA88E` | İkon/etiket, ikincil vurgu |
| Periwinkle (mavi-mor) | `#6E7BE8` | İkon/etiket, logo rengi |
| Mor | `#9D5CE0` | İkon/etiket, dekoratif |
| Mercan/kırmızı | `#E84C3D` | Seyrek vurgu |

> Renkli zemin üstüne metin: aynı ailenin koyu tonu (saf siyah değil).
> Pembe üstünde `#4B1528`, mavi üstünde `#042C53`, teal üstünde `#04342C`.

---

## 3. Tipografi

- **Font:** `Work Sans` (Google Fonts, ücretsiz, **Türkçe karakter desteği tam**: ç ş ğ ı İ ö ü).
  - Alternatif başlık fontu (daha retro/bold): `Bricolage Grotesque`, `Space Grotesk`, `Archivo Black` — hepsi Türkçe destekli.
- **Ağırlık:** Başlık 800–900, gövde 400–500.
- **Başlık:** UPPERCASE, sıkı line-height (~0.95), hafif negatif letter-spacing.
- **Ölçek:** H1 48–72px · H2 36–48px · H3 18–22px · Gövde 16–18px (line-height 1.5–1.7).
- `<html lang="tr">` ve tüm fontlarda Türkçe karakter kontrolü şart.

---

## 4. Bileşen Stilleri

- **Buton (CTA):** Sarı zemin, 3px kontur, pill, `3px 3px 0 #1A1A1A` gölge, 800 weight. Hover'da yukarı-sola kayma + gölge büyür.
- **Buton (ikincil):** Krem/beyaz zemin, aynı kontur+gölge.
- **Kart:** Beyaz zemin, 3px kontur, 14px köşe, `5px 5px 0 #1A1A1A`. İçeride: renkli ikon kutusu → başlık → açıklama → "→" link.
- **Etiket/pill:** Küçük, canlı, 2.5px kontur, pill, kalın metin (kategori etiketleri).
- **Form input:** Beyaz zemin, 3px kontur, sade; odakta kontur kalınlaşır.
- **Navbar:** Krem zemin, solda logo (pill içinde), sağda menü; mobilde hamburger.
- **İkonlar:** Çizgisel, siyah konturlu, renkli dolgulu sticker tarzı (Tabler/Phosphor outline + renk).
- **Dekoratif şekiller:** Kenarlara `position:absolute`; mobilde sayısı azaltılır.

---

## 5. Animasyon

- Kart/buton hover'da "kaldırma" (translate -2px,-2px + gölge büyür), ~150ms.
- Scroll'da sade fade-in / yukarı kayma (opsiyonel, abartısız).
- Ağır parallax yok.

---

## 6. Teknik Notlar (Claude Code için)

- **Stack:** Basitlik için **tek sayfa scroll + HTML/CSS (+minik JS)** önerilir; portfolyo büyürse React + Tailwind.
- **Responsive:** Mobile-first. Kart gridleri mobilde tek sütun, masaüstünde 2–3 sütun.
- **Erişilebilirlik:** Alt metinler, kontrast, klavyeyle gezilebilir nav.
- **Performans:** Görseller webp, font `display: swap`.
- **SEO:** Anlamlı title, meta description, Open Graph.

---

## 7. Sayfalar ve İçerik

### 7.1 Hero
- Üst satır: **Merhaba, ben Tuba.**
- Başlık (birini seç): **TÜRKÇE YAPAY ZEKA İNŞA EDİYORUM.** / VERİYİ MODELE DÖNÜŞTÜRÜYORUM. / VERİ & YAPAY ZEKA ÜRETİYORUM.
- Açıklama: *"Mad Cat Labs'ta Data & AI Associate'im. Türkçe dil modelleri eğitiyor, veri pipeline'ları kuruyor ve öğrendiklerimi @tubac3l1k'te paylaşıyorum."*
- Buton: **Projelerime bak →**
- Görsel: [Tubi'nin fotoğrafı veya avatar — sticker çerçeve içinde]

### 7.2 Ne Yapıyorum — Üç Sütun (3 kart)
Başlık: **NE YAPIYORUM**

1. **Web Tasarım & Geliştirme** (ikon: periwinkle ekran)
   *"Modern, kişiselleştirilmiş web siteleri tasarlıyor ve hayata geçiriyorum. Temiz tasarım dili, responsive yapı ve markaya özgü bir his — fikirden canlı siteye kadar."*
   Link: **Projelerime bak →**

2. **Veri** (ikon: teal grafik)
   *"Karmaşık veriyi anlaşılır içgörüye dönüştürüyorum. Python ve Pandas ile veri temizleme, kalite kontrolleri ve keşifsel analiz; Looker Studio, Power BI ve GA4 ile karar verdiren dashboard'lar."*
   Link: **Detaylar →**

3. **Yapay Zeka** (ikon: pembe/mor AI)
   *"Türkçe dil modelleri eğitiyorum. 60.000+ satırlık eğitim setleri, Qwen & Gemma fine-tuning (LoRA/DPO), değerlendirme pipeline'ları ve on-prem dağıtım — uçtan uca LLM geliştirme."*
   Link: **Yazılarımı oku →**

> Not: Web tasarım vitrini = bu sitenin kendisi. İstenirse kartın linki "bu siteyi ben tasarladım" anlatısına bağlanır.

### 7.3 Öne Çıkan Projeler
Başlık: **SEÇİLMİŞ ÇALIŞMALAR** (alternatifli satır düzeni: sol görsel/sağ metin, sonra ters)

1. **MMX — Türkçe Pazarlama LLM'i** · `LLM` `Fine-tuning` `Veri Mühendisliği`
   *"Türkçe dijital pazarlama için uçtan uca dil modeli geliştirme. 12 alanı kapsayan 60.000+ satırlık sentetik eğitim seti kurdum, JSONL pipeline'ı tasarladım ve %94 format uyumu sağlayan otomatik kalite doğrulaması ekledim."* → Medium / GitHub

2. **Qwen3.5 Çok-Model Fine-tuning Deneyi** · `LoRA` `DPO` `Benchmark`
   *"2B'den 27B'ye dört Qwen3.5 varyantını LoRA ve DPO ile karşılaştırdım. 27B'deki token açığını teşhis ederek üretim katmanı kararını şekillendirdim. Bulguları yazıya döktüm (2.000+ görüntülenme)."* → Medium

3. **LLM Değerlendirme Pipeline'ı Yeniden Tasarımı** · `LLMOps` `Evaluation`
   *"Skorlama pipeline'ını denetleyip ölçülen performansı ~15 puan baskılayan 12+ metrik tutarsızlığını tespit ettim ve 200+ soruda standart metriklerle yeniden tasarladım."*

4. **Kredi Kartı Geç Ödeme Risk Analizi** · `Python` `Pandas` `Veri Analizi`
   *"Müşteri düzeyinde finansal veriyle uçtan uca risk analizi: veri temizleme, eksik değer kontrolleri, keşifsel analiz ve kural tabanlı risk skorlama. Kaggle/GitHub'da paylaşıldı."* → GitHub / Kaggle

5. (Opsiyonel) **On-prem LLM Platformu** · `Gemma` `Qwen` `Ollama` `Open WebUI` `DGX Spark`
   *"Açık kaynak modellerle güvenli, on-prem bir LLM platformu kurulumuna katıldım; Ollama ve Open WebUI ile model serving deneyimi."*

### 7.4 Hakkımda
Başlık: **HAKKIMDA**
*"Veriyle düşünmeyi analitik tarafında öğrendim, sonra tüm odağımı yapay zekaya verdim. Bugün Türkçe dil modelleri eğitiyorum — veri mühendisliğinden değerlendirme pipeline'larına, fine-tuning'den on-prem dağıtıma kadar. İçerik üretmeyi de seviyorum; öğrendiklerimi @tubac3l1k'te ve Medium'da paylaşıyorum."*
- Görsel: [fotoğraf + dekoratif sticker'lar]

### 7.5 İçerik Üreticiliği (@tubac3l1k)
Başlık: **İÇERİK ÜRETİYORUM**
*"Türkçe yapay zeka ve teknoloji içerikleri üretiyorum — karmaşık konuları sade, erişilebilir bir dile çeviriyorum."*
- Linkler: Instagram, Medium (aşağıdaki listeden)

### 7.6 Yetenekler (pill listesi)
Başlık: **YETENEKLER**
Python · Pandas · Hugging Face · Unsloth · LoRA · QLoRA · DPO · PEFT · JSONL · Sentetik Veri · n8n · Docker · Linux · Ollama · Open WebUI · F1/BLEU/Perplexity · GA4 · Looker Studio · SQL · Claude Code · Cursor

### 7.7 Deneyim (iki kademeli)
**Öne çıkan:**
- **Mad Cat Labs — Data & AI Associate** (Şub 2026 – günümüz)
  *Türkçe LLM (MMX) geliştirme: sentetik veri mühendisliği, fine-tuning deneyleri (LoRA/DPO), değerlendirme pipeline tasarımı, on-prem dağıtım, n8n otomasyonları.*

**Daha önce (tek satır, dipnot):**
- 4+ yıl dijital analitik ve performans pazarlaması — Link Dijital (2022–2026)

### 7.8 Eğitim
- **İşletme** — Beykoz Üniversitesi (2017–2022)

### 7.9 Sertifikalar
- edX — Advanced Fine-Tuning for LLMs
- Google Analytics 360
- Google Ads Display Network
- IBM Enterprise Design Thinking

### 7.10 İletişim
Başlık: **BİRLİKTE ÇALIŞALIM** (veya: İLETİŞİME GEÇ)
- Kısa davet: *"Bir projen mi var, ya da sadece merhaba mı demek istiyorsun? Yazmaktan çekinme."*
- E-posta: **tubacelikk11@gmail.com**
- (Opsiyonel) İletişim formu: Ad · E-posta · Mesaj
  > Form gerçekten çalışacaksa Formspree / Netlify Forms gibi bir servis gerekir.

### 7.11 Footer
- Logo + isim: **Tuba Çelik** · *Data & AI Associate*
- Sosyal ikonlar (aşağıdaki liste)
- Telif: © 2026 Tuba Çelik

---

## 8. Sosyal Linkler (footer + iletişim)

- GitHub: https://github.com/tubaacelik
- Kaggle: https://www.kaggle.com/tubacelikk1
- LinkedIn: https://www.linkedin.com/in/tuba-çelik/
- Medium: https://medium.com/@tubaacelikk11
- X (Twitter): https://x.com/ttubacelk
- Instagram: https://www.instagram.com/tubac3l1k
- E-posta: tubacelikk11@gmail.com

---

## 9. Claude Code'a Örnek İlk Komut

> "Ekteki tasarım brief'ine göre Türkçe bir kişisel portfolyo sitesi kur. Neobrutalism
> tasarım dili: krem zemin (#F7F0E4), 3px siyah konturlar, sert (blursuz) gölgeler,
> Work Sans fontu, canlı renk paleti (pembe/sarı/teal/periwinkle/mor), pill butonlar ve
> kartlar. Tek sayfa scroll, mobile-first, responsive, `<html lang='tr'>`. Brief'teki
> bölümleri ve içeriği birebir kullan. Önce iskeleti kur, sonra detayları birlikte
> rötuşlayalım."

---

### Karar verilenler
- Üç sütun: Web Tasarım · Veri · Yapay Zeka
- Hero: AI/veri odaklı
- Pazarlama geçmişi: tek satır, görünmez plan
- Boston University: SİTEDE YOK
- Sosyal linkler: yukarıdaki 6 platform + e-posta
