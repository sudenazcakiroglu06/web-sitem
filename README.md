# Sude Naz Çakıroğlu — Kişisel Portfoly

Gotik temalı (mor + kan kırmızısı + altın, leopard ve yıldız desenleriyle)
tek sayfalık kişisel portfoly sitesi. Harici kütüphane yok, sadece
HTML + CSS + JavaScript. Kurulum gerekmez.

## Dosyalar

```
index.html      Sayfanın tüm içeriği
css/style.css   Tüm tasarım, renk paleti, desenler
js/script.js    Menü, filtre, sayaçlar, yazı efekti, form doğrulama
```

## Çalıştırma

`index.html` dosyasına çift tıklayınca doğrudan açılır. Yerel sunucuyla
(önerilir) açmak için:

```bash
python -m http.server 8765
```

Ardından tarayıcıda `http://127.0.0.1:8765` adresini açın.

## Sık değiştirilen yerler

| Ne | Nerede |
|---|---|
| Ad, unvan, şehir, diller | `index.html` → "Hakkımda" bölümü, `fact-list` |
| E-posta / telefon | `index.html` → "İletişim" bölümü, `info-card` |
| Projeler | `index.html` → `project-grid` içindeki `project-card` |
| Eğitim geçmişi | `index.html` → `timeline` içindeki `tl-item` |
| Yetenekler & yüzdeler | `index.html` → `chip-list` ve `bar-row` |
| Hero'daki sayaçlar | `index.html` → `data-count` ve `data-suffix` |
| Yazı yazma animasyonundaki unvanlar | `js/script.js` → `roles` dizisi |
| Proje kategorileri | `index.html` → `data-filter` ve `data-category` |

## Fotoğraf ekleme

İki yerde monogram yerine fotoğrafınızı koyabilirsiniz:

```html
<!-- Hero bölümü -->
<div class="portrait-inner">
  <img src="profil.jpg" alt="Sude Naz Çakıroğlu">
</div>
```

`profil.jpg` dosyasını `index.html` ile aynı klasöre koymanız yeterli.

## Renk paleti

`css/style.css` en üstündeki `:root` bloğunda tanımlıdır. Koyu/açık tema
değerleri `[data-theme="light"]` bloğunda. Tema düğmesi seçimi `localStorage`
üzerinde saklar.

Temel renkler:

| Değişken | Renk | Kullanım |
|---|---|---|
| `--bg` | `#080410` | Sayfa arka planı (koyu tema) |
| `--purple-700` | `#2c1945` | Mor vurgular |
| `--wine` | `#6d1030` | Kan kırmızısı, butonlar |
| `--gold` | `#c9a227` | Altın çerçeveler, başlıklar |
| `--leopard-base` | `#33184a` | Leopard desen zemini |
| `--font-display` | Cinzel | Başlıklar, isim (okunaklı gotik) |
| `--font-gothic` | UnifrakturMaguntia | Siyah harf süslemeleri |
| `--font-body` | EB Garamond | Gövde metni |

## Yayına alma

Netlify, Vercel, GitHub Pages gibi statik barındırma servislerine klasörü
olduğu gibi yüklemeniz yeterlidir.
