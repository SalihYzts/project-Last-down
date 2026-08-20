# First Down — Tanıtım Sitesi

*First Down*; kıyamet sonrası bir dünyada tek bir hayatta kalanı yönettiğin,
hayatta kalma ile üs kurmayı birleştiren PC oyununun tanıtım sayfası.

## Yapı

```
index.html                    Tüm site (tek dosya: HTML + CSS + JS, bağımlılık yok)
assets/first-dawn-720p.mp4    Tanıtım videosu · 720p · 3:53 · 42 MB
assets/trailer-poster.jpg     Video poster karesi
```

Tek harici bağımlılık Google Fonts (Big Shoulders Display, Chivo, IBM Plex Mono).

## Çalıştırma

Statik site — kurulum gerekmez. Yerelde açmak için:

```bash
python3 -m http.server 8000
```

Sonra `http://localhost:8000` adresine git. (Video `file://` üzerinden de çalışır,
ama yerel sunucu daha sağlıklı.)

## Notlar

- Gündüz/gece düğmesi tüm sayfanın renk paletini değiştirir (`data-phase` özniteliği).
- Galeriye görsel eklemek için `.gal` içine bir `.gal-item` kopyalayıp
  `data-t` değerini `video`, `shot` veya `art` yap.
- Steam, Discord ve sosyal medya bağlantıları henüz bağlanmadı;
  `soonLink()` ve `wishlist()` fonksiyonlarındaki yer tutucuları güncelle.
- Video kaynağı 665 MB / 1080p idi; web için 720p / ~1.5 Mbps'e indirildi ve
  `faststart` ile yeniden paketlendi.
