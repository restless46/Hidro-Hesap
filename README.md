
# iOS için PWA (Sıfırdan Başlangıç)

Bu klasör, iPhone'da **Ana Ekrana Ekle** ile uygulama gibi çalışan basit bir PWA örneği içerir.

## 1) Dosya yapısı
- `index.html`: Uygulama ana sayfası
- `manifest.webmanifest`: PWA manifesti (isim, ikonlar, başlangıç URL)
- `sw.js`: Service Worker (offline önbellek)
- `icons/*.png`: Uygulama ikonları

## 2) Yerelde deneme (opsiyonel)
Bir HTTP sunucu ile aç:
```bash
python -m http.server 8080
# sonra: http://localhost:8080
```

> Not: PWA özellikleri **HTTPS** üzerinde tam çalışır. (localhost istisna)

## 3) Yayınlama
- Netlify, Vercel ya da GitHub Pages'e yükle (HTTPS otomatik).
- Telefonunda Safari ile URL’i aç.
- Paylaş ► **Ana Ekrana Ekle** ► İsim ver ► Ekle.

## 4) Güncelleme
- `sw.js` içindeki CACHE_NAME’i artır (örn. v2).
- Yayınla; iOS’ta kullanıcı uygulamayı yeniden açtığında yeni içerik gelir.

## 5) İpuçları
- iOS tam ekran için index.html'de `apple-mobile-web-app-capable=yes` meta'sı var.
- Icon’ları kendi logonla değiştir.
- Offline kapsamını arttırmak için `ASSETS` listesine sayfalarını ekle.
