# Byelmas — Yayına Alma Notları

Bu klasördeki her şey **statik** — sunucu tarafı kod, veritabanı veya build adımı gerekmiyor.
Aşağıdaki 3 dosyayı sunucunuzun/hosting'inizin **kök dizinine** (root) aynen kopyalayın:

- `index.html` — tek parça site (logo dahil, harici görsel dosyası yok)
- `robots.txt` — arama motorlarına izin veren dosya
- `sitemap.xml` — arama motorları için site haritası

## Yayına alma seçenekleri

**En basit — statik hosting (önerilen):**
Netlify, Vercel, Cloudflare Pages veya GitHub Pages'e bu 3 dosyayı sürükleyip bırakmanız yeterli.
Hepsi otomatik ve ücretsiz HTTPS sağlar.

**Kendi sunucunuz / cPanel varsa:**
Dosyaları `public_html/` (veya sunucunuzun web kök dizini neyse) içine yükleyin.
Sunucunuzda **Let's Encrypt** ile ücretsiz SSL sertifikası kurup HTTPS'i zorunlu kılın
(çoğu hosting panelinde "Force HTTPS" / "Always use HTTPS" seçeneği tek tıkla açılır).

## Alan adı (byelmas.com)

1. Domaini aldığınız yerden (Namecheap, GoDaddy vb.) DNS ayarlarına girin.
2. Hosting sağlayıcınızın verdiği DNS kayıtlarını (A kaydı veya CNAME) ekleyin.
3. DNS yayılması genelde birkaç dakika ile birkaç saat sürer.

## Yayına almadan önce son kontrol listesi

- [ ] `https://byelmas.com` açıldığında kilit simgesi (HTTPS) görünüyor mu?
- [ ] `https://byelmas.com/robots.txt` ve `/sitemap.xml` erişilebiliyor mu?
- [ ] Google Search Console'a siteyi ekleyip `sitemap.xml`'i gönderin (arama sonuçlarında görünmesi için).
- [ ] Ürünlerin App Store / Google Play linkleri yayına girdiğinde `index.html` içindeki
      `apps.apple.com/search?term=...` ve `play.google.com/store/search?...` linklerini
      gerçek uygulama sayfası linkleriyle değiştirin.
- [ ] `hello@byelmas.com` e-posta adresinin gerçekten aktif olduğundan emin olun (İletişim bölümünde kullanılıyor).

## Güncelleme yapmak isterseniz

Tüm site tek bir `index.html` dosyası — metin, renk veya bölüm değiştirmek için
bu dosyayı bir metin editörüyle açıp ilgili kısmı düzenleyip tekrar yüklemeniz yeterli.
