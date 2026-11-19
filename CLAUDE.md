# İdalina Beceren Blog — Yazar Talimatı

Bu depo https://idalinabeceren.com blogu için yazı üretim alanıdır. Her yazı ayrı bir oturumda, blog yönetmeninden (ana oturum) gelen brief ile yazılır.

## Önce oku (sırayla)
1. `_kaynak/marka-profili.md`: Marka profili, e-ticaret uyarlamaları, bağlanabilir ürün listesi, tasarım bileşenleri. **Şablonla çakışırsa bu dosya geçerlidir.**
2. `_kaynak/blog-sablonu-v3.md`: Yazım şablonu (iskelet, dil, SEO, bağlantı, S.S.S., kontrol listesi).
3. `_kaynak/sitemap.xml`: İç bağlantıların **tek** kaynağı.
4. `_kaynak/ornekler/`: Yayındaki iki yazının gövde HTML'i (biçim referansı; dilini değil yapısını örnek alın, eski yazılarda "biz" dili var, yeni yazılarda yok).

## Teslim
Klasör: `yazilar/<slug>/`

| Dosya | İçerik |
| :-- | :-- |
| `yazi.md` | H1'den Etiketler'e kadar yayın metni (Markdown) + yatay çizgiden sonra **Editör Notları (yayınlanmayacak)**, şablon Bölüm 9 tablosu eksiksiz |
| `yazi.html` | CKEditor'e yapıştırılacak gövde. H1 hariç, giriş paragrafından Etiketler öncesine kadar; yalnızca marka-profili Bölüm 6'daki satır içi stiller. S.S.S. görsel bloğu dahil, `<script>` hariç |
| `sss.html` | S.S.S. bloğu (6.8) + FAQPage JSON-LD. Soru/cevaplar `yazi.md` ve `yazi.html` ile birebir aynı |

## Kurallar
- Tahmin yok. Bilgi eksikse yazma, Editör Notları'nda "Eksik / doğrulanmalı" altına yaz.
- İç bağlantı: yalnızca sitemap'te birebir bulunan adres ve marka-profili Bölüm 5'teki kısıtlar. Bağlantıları sitemap'e karşı bir betikle kontrol et ve sonucu Editör Notları'na yaz.
- Dış kaynak: yalnızca resmi/birincil kaynak; her adresi WebFetch (veya web-fetch alt ajanı) ile açarak doğrula. Açılamayanı kullanma ya da "doğrulanamadı" diye işaretle. Hafızadan adres yazma.
- Title/meta karakter sayılarını betikle say (Python `len`), tahmin yazma.
- Kelime sayısını betikle say ve Editör Notları'na yaz (tablolar hariç).
- Bitirmeden önce şablon Bölüm 10 kontrol listesini tek tek uygula ve sonucu Editör Notları'nın sonuna "Kontrol listesi" olarak ekle (her madde ✓ / ✗ + açıklama).
- `_kaynak/` klasörünü değiştirme.
- Commit mesajı: `yazi: <slug>` (revizyonlarda `revize: <slug> – <kısa not>`). Brief'te verilen dala push et.
