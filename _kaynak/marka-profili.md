# İdalina Beceren — Marka Profili ve Şablon Uyarlamaları

Bu dosya `blog-sablonu-v3.md` Bölüm 1'in doldurulmuş halidir ve şablonun bu siteye uyarlanmış kurallarını içerir. **Çakışma olursa bu dosya önceliklidir.**
Son güncelleme: 19 Kasım 2026 (değerler canlı siteden ve sitemap'ten alınmıştır).

## 1. Marka profili

| Alan | Değer | Kaynak |
| :-- | :-- | :-- |
| Marka adı | **İdalina Beceren** | Kullanıcı |
| İyelik/ek biçimi | İdalina Beceren'in, İdalina Beceren'e, İdalina Beceren'den | "Beceren" okunuşuna göre |
| Firma unvanı (yalnızca şema/yasal bağlam) | İda Beceren Zeytincilik | Sitenin `siteSettings.firmaAdi` ve BlogPosting şeması |
| Alan adı | https://idalinabeceren.com | Kullanıcı |
| Site altyapısı | Ticimax (blog gövdesi CKEditor'e satır içi stilli HTML olarak girilir) | Canlı sayfa kaynağı |
| Blog dizini | `/blog/icerik/<slug>` | Sitemap |
| Blog kategorileri | Zeytinyağı Rehberi (`/blog/kategori/zeytinyagi-rehberi`), Zeytinyağlı Tarifler (`/blog/kategori/zeytinyagli-tarifler`) | Canlı sayfa (sitemap'te yok, **bağlantı verilmez**, yalnızca CMS'te kategori seçimi için) |
| Ürün sayfaları | Kök dizinde, ör. `/5l-erken-hasat-zeytinyagi` | Sitemap |
| Kategori sayfaları | Kök dizinde, ör. `/erken-hasat-zeytinyagi` | Sitemap |
| Yayın dili / hedef ülke | Türkçe / Türkiye | Kullanıcı |
| Veri koruma mevzuatı | KVKK / Kişisel Verileri Koruma Kurumu (yalnızca konu gerektirirse) | — |
| Gıda mevzuatı (konu gerektirirse) | Türk Gıda Kodeksi (Zeytinyağı ve Prina Yağı Tebliği; Beslenme ve Sağlık Beyanları Yönetmeliği), Tarım ve Orman Bakanlığı, TÜRKPATENT coğrafi işaret kayıtları, Uluslararası Zeytin Konseyi (IOC) | Kullanılmadan önce resmi kaynaktan açılarak doğrulanır |
| Otomatik şema | Ticimax her yazıya **BlogPosting** ve **BreadcrumbList** şemasını kendisi ekliyor. Ayrıca Article şeması **eklenmez**. Sitede FAQPage şeması **yok**, yazı ile birlikte verilir. | Canlı sayfa kaynağı |

## 2. Şablonun e-ticarete uyarlanması (kullanıcı onaylı)

| Şablondaki kavram | Bu sitede karşılığı |
| :-- | :-- |
| Hizmet sayfası / ana hizmet sayfası | Konuyla eşleşen **kategori sayfası** (ör. `/erken-hasat-zeytinyagi`, `/soguk-sikim-zeytinyagi`, `/zeytin`) |
| Proje / referans sayfaları | **Ürün sayfaları** (yalnızca Bölüm 5'teki "bağlanabilir" listeden) |
| Teklif / iletişim sayfası | Yok. CTA = kategori sayfası + ilgili ürün sayfası. Kurumsal/hediye konularında `/kurumsal-hediye` |
| Marka geçiş kalıbı | "İdalina Beceren'in [kategori adı] seçkisi incelenebilir." / "… için İdalina Beceren'in [ürün adı] ürün sayfası incelenebilir." |
| Hizmet yazı türleri (tanım/fiyat/etki) | Rehber yazıları için geçerli. **Tarif yazıları** için Bölüm 4'teki iskelet kullanılır |

## 3. Dil ve içerik kuralları (şablona ek)

- Şablondaki varsayılan ton geçerlidir: üçüncü şahıs, **"biz" kullanılmaz**. (Not: eski yazılarda "kendi hasadımızdan… anlatıyoruz" gibi "biz" dili var. Yeni yazılar şablona uyar. Kullanıcı aksini söylerse bu madde güncellenir.)
- **Sağlık beyanı:** Hastalık önleme, tedavi ya da iyileştirme iddiası yazılmaz. Besin/sağlık bilgisi gerekiyorsa yalnızca resmi veya bilimsel birincil kaynağa dayanarak, temkinli dille yazılır ve Editör Notları'nda "sağlık beyanı – kontrol edilmeli" diye işaretlenir.
- Fiyat, indirim, kampanya kodu (ör. WELCOME10), stok ya da "son ürünler" ifadesi yazılmaz.
- Rakip marka adı yazılmaz.
- Hasat yılı ifadesi ürün adında nasıl geçiyorsa öyle yazılır (ör. "2026-2027 Hasadı", "Yeni Hasat 2026").
- Etiketler sitedeki biçimle yazılır: **virgülle, boşluksuz**, ör. `Fava tarifi,Kuru bakla,Ege mezeleri,Zeytinyağlı tarifler`. İlk harf büyük, gerisi cümle düzeninde. (Şablondaki " · " biçimi bu site için geçersizdir.)

## 4. Tarif yazısı iskeleti

Tahmini uzunluk: **1.200–1.600 kelime** (tablolar ve malzeme listesi hariç).

| # | Bölüm | Not |
| :-: | :-- | :-- |
| 1 | H1 | "[Yemek] Tarifi: [ayırt edici özellik]" (ör. sitedeki fava/humus başlıkları) |
| 2 | Giriş P1: tanım | "[Yemek], … -dır/-dir." |
| 3 | Giriş P2: yol haritası | "Bu yazıda … ele alınmıştır." (N püf noktası sayısı geçer) |
| 4 | H2: Malzemeler | Porsiyon bilgisi + madde listesi. Ölçüler tarifin kendi değeridir; sağlık/kalori iddiası yok |
| 5 | H2: Yapılışı | Numaralı adım listesi (`<ol>`) |
| 6 | H2: N püf noktası (özet liste) + H2 × N | Şablonun numaralı çerçevesi; madde başı 80–120 kelime |
| 7 | H2: Tablo | ör. "Hangi aşamada hangi zeytinyağı?" (Aşama / Önerilen yağ türü / Neden) |
| 8 | H2: Kontrol listesi | "… Yaparken Nelere Dikkat Edilmeli?" 6–8 madde |
| 9 | H2: Ürün kutuları | "[Yemek] tabağınız için" + 2–3 ürün kutusu (Bölüm 6.6) |
| 10 | H2: S.S.S. | 3–5 soru |
| 11 | H2: Sonuç | Özet + CTA |
| 12 | H2: Kaynaklar | 1–3 resmi kaynak (tarifte zorunlu değil, gıda güvenliği/mevzuat varsa zorunlu) |
| 13 | Etiketler | Virgüllü tek satır |

Rehber yazılarında şablonun Bölüm 3 iskeleti aynen kullanılır, sonuçtan önce Bölüm 9'daki ürün kutusu bölümü eklenir.

## 5. Bağlantı kuralları ve ürün listesi

**Ürün durumu 19.11.2026'da canlı siteden kontrol edildi** (stok > 0 = satışta). Aynı ürünün eski ve yeni hasat sürümleri varsa **yalnızca yeni hasat** sürümüne bağlantı verilir.

### Bağlanabilir ürünler

| Adres | Ürün adı |
| :-- | :-- |
| /idalina-ilk-gun-hasat-soguk-sikim-zeytinyagi-5-l | İlk Gün Hasat Soğuk Sıkım Natürel Sızma Zeytinyağı 5 L · 2026-2027 Hasadı |
| /2li-5l-ilk-gun-hasat-soguk-sikim-zeytinyagi-2026-2027 | İlk Gün Hasat Soğuk Sıkım Zeytinyağı 5 L 2'li Paket · 2026-2027 Hasadı |
| /5l-premium-ilk-gun-hasadi-zeytinyagi-yeni-hasat-2026 | Premium İlk Gün Hasat Zeytinyağı 5 L · Yeni Hasat 2026 |
| /750ml-premium-ilk-gun-hasadi-zeytinyagi-yeni-hasat-2026 | Premium İlk Gün Hasat Zeytinyağı 750 ml · Yeni Hasat 2026 |
| /2li-5l-premium-ilk-gun-hasadi-zeytinyagi-2026-2027 | Premium İlk Gün Hasat Zeytinyağı 5 L 2'li Paket · 2026-2027 Hasadı |
| /5l-erken-hasat-zeytinyagi | Erken Hasat Soğuk Sıkım Zeytinyağı 5 L · 2026-2027 Hasadı |
| /erken-hasat-soguk-sikim-zeytinyagi-5-l-2li-paket-2026-2027-hasadi | Erken Hasat Soğuk Sıkım Zeytinyağı 5 L 2'li Paket · 2026-2027 Hasadı |
| /1l-natural-sizma-zeytinyagi | Natürel Sızma Zeytinyağı 1 L · 2026-2027 Hasadı |
| /2l-soguk-sikim-naturel-sizma-zeytinyagi | Soğuk Sıkım Natürel Sızma Zeytinyağı 2 L · 2026-2027 Hasadı |
| /5l-organik-zeytinyagi | Organik Natürel Sızma Zeytinyağı 5 L · 2026-2027 Hasadı |
| /750ml-domat-soguk-sikim-natural-sizma-zeytinyagi | Domat Zeytini Soğuk Sıkım Natürel Sızma Zeytinyağı 750 ml · 2026-2027 Hasadı |
| /250ml-delice-zeytinyagi | Delice Zeytinyağı 250 ml (Yabani Zeytin) · 2026-2027 Hasadı |
| /250ml-zerdecalli-zeytinyagi | Zerdeçallı Çeşnili Zeytinyağı 250 ml |
| /750ml-aci-biber-cesnili-soguk-sikim-zeytinyagi | Acı Biber Çeşnili Soğuk Sıkım Zeytinyağı 750 ml |
| /250ml-zeytin-sutu | Zeytin Sütü 250 ml |
| /bebek-sutu-natural-sizma-zeytinyagi | Bebek Zeytinyağı – Natürel Sızma Bebek Bakım Yağı |
| /5li-saf-zeytinyagi-sabunu | Saf Zeytinyağı Sabunu 5'li Paket |
| /siyah-zeytin | Kazdağları Siyah Salamura Zeytin |
| /yesil-zeytin | Kazdağları Yeşil Çizik Zeytin |
| /kazdaglari-duble-iri-zeytin | Kazdağları Duble İri Boy Zeytin |
| /kahvaltilik-kazdaglari-baharati | Kazdağları Kahvaltılık Baharatı |
| /idalina-lezzet-sofrasi-seti | İdalina Lezzet Sofrası Hediye Seti |
| /idalina-dogal-yasam-seti | İdalina Doğal Yaşam Hediye Seti |

### Bağlantı verilmeyecek ürünler

| Adres | Neden |
| :-- | :-- |
| /5l-olgun-hasat-soguk-sikim-zeytinyagi, /2li-5l-olgun-hasat-soguk-sikim-zeytinyagi, /15l-olgun-hasat-soguk-sikim-zeytinyagi-2l-hediye, /olgun-hasat-sicak-sikim-zeytinyagi | Stok 0 (olgun hasat ürünlerinin tamamı tükenmiş). Olgun hasat konularında ürün yerine `/olgun-hasat-zeytinyagi` kategorisine bağlanır ve Editör Notları'nda belirtilir |
| /750ml-filtresiz-soguk-sikim-zeytinyagi | Stok 0. Filtresiz konularında `/filtresiz-zeytinyagi` kategorisi kullanılır |
| /5l-premium-ilk-gun-hasadi-zeytinyagi, /750ml-premium-ilk-gun-hasadi-zeytinyagi, /2li-5l-premium-ilk-gun-hasadi-zeytinyagi, /2li-5l-ilk-gun-hasat-soguk-sikim-zeytinyagi, /2li-5l-erken-hasat-zeytinyagi | 2025-2026 hasadı. Yeni hasat sürümü var |
| /naturel-sizma-zeytinyagi, /naturel-sizma-soguk-sikim-zeytinyagi, /natural-sizma-zeytinyagi-500ml-6li-paket, /natural-sizma-zeytinyagi-250ml-6li-paket | 2025-2026 hasadı. Yalnızca konuyla birebir eşleşen başka satışta ürün yoksa kullanılır ve Editör Notları'nda belirtilir |

### Diğer bağlantı kuralları
- `/kasima-ozel`, `/kampanyalar` ve hukuki sayfalar (`/mesafeli-satis-sozlesmesi`, `/iade-kosullari`, `/kisisel-verilerin-korunmasi`, `/uyelik-sozlesmesi`) bağlanmaz.
- `/blog/icerik/1-litre-zeytinyagi-kac-kilo` ve `/blog/icerik/1-litre-zeytinyagi-kac-kilo-zeytinden-cikar-randiman` aynı aramayı hedefliyor. Randıman konusu için ikincisi kullanılır, ikisi aynı yazıda bağlanmaz.
- İç bağlantılar göreli yazılır (`/erken-hasat-zeytinyagi`); sitedeki mevcut kullanım böyle.
- Yazı, sitemap'teki bir blog yazısıyla aynı aramayı hedefliyorsa yazıma başlanmadan önce Editör Notları'nda "çakışma riski" olarak belirtilir.

## 6. Tasarım bileşenleri (canlı siteden birebir)

Tüm gövde CKEditor'e yapıştırılacak **satır içi stilli HTML**'dir. `<style>` bloğu, sınıf adı, `<details>/<summary>` kullanılmaz (sitedeki tasarım açılır-kapanır değil, şablon kuralı gereği akordeona çevrilmez). Renk ve ölçüler aşağıdakilerden başka değer almaz. Referans: `_kaynak/ornekler/*.html`.

### 6.1 Paragraf
```html
<p style="color:#333;font-size:16px;line-height:1.75;margin:0 0 16px;">…</p>
```

### 6.2 H2
```html
<h2 style="border-left:4px solid #3F6B3A;color:#2E4A2B;font-size:24px;line-height:1.3;margin:36px 0 14px;padding-left:12px;">…</h2>
```
H1'i Ticimax yazı başlığı alanından kendisi basar; gövdeye H1 yazılmaz. Sitede H3 stili tanımlı değil. Rehberde H3 gerekirse S.S.S.'deki H3 stili (6.7) kullanılır.

### 6.3 Liste
```html
<ul style="color:#333;font-size:16px;margin:0 0 20px;padding-left:22px;">
  <li style="color:#333;font-size:16px;line-height:1.7;margin:0 0 8px;"><strong>Etiket:</strong> …</li>
</ul>
<ol style="color:#333;font-size:16px;margin:0 0 20px;padding-left:22px;"> … aynı li stili … </ol>
```

### 6.4 Bağlantı (metin içi)
```html
<a href="/erken-hasat-zeytinyagi" style="color:#3F6B3A;font-weight:600;">…</a>
```
Dış kaynak: aynı stil + `target="_blank" rel="noopener"`.

### 6.5 Bilgi kutusu (not, uyarı)
```html
<div style="background-color:#F3F7F0;border-left:5px solid #3F6B3A;border-radius:8px;margin:24px 0;padding:18px 20px;">
  <p style="color:#2E4A2B;font-size:16px;margin:0 0 6px;"><strong>Başlık</strong></p>
  <p style="color:#333;font-size:15px;line-height:1.7;margin:0;">…</p>
</div>
```
Sarı kampanya kutusu (`#FBF7EA` / `#C9A227`) kullanılmaz.

### 6.6 Ürün kutusu ("Ürünü İncele")
```html
<div style="background-color:#fff;border-radius:12px;border:1px solid #DDE5D8;margin:14px 0;padding:18px 20px;">
  <p style="color:#2E4A2B;font-size:17px;margin:0 0 4px;"><strong>[Ürün adı, Bölüm 5'teki gibi]</strong></p>
  <p style="color:#555;font-size:15px;line-height:1.6;margin:0 0 12px;">[Tek cümle, tarafsız kullanım önerisi; fiyat/indirim yok]</p>
  <p><a href="/[ürün-adresi]" style="background-color:#3F6B3A;border-radius:6px;color:#fff;display:inline-block;font-size:14px;padding:10px 20px;text-decoration:none;"><strong>Ürünü İncele →</strong></a></p>
</div>
```
Bir yazıda 2–3 kutu, "[Konu] için" başlıklı tek H2 altında. Ürün kutusu bağlantıları iç bağlantı sayısına (6–9) dahil edilmez, Editör Notları'nda ayrıca listelenir.

### 6.7 Tablo
```html
<div style="margin:20px 0;overflow-x:auto;"><figure class="table" style="width:100%;"><table style="border-collapse:collapse;border-color:#E5E9E1;border-radius:10px;border-style:solid;overflow:hidden;width:100%;">
<thead><tr>
  <th style="background-color:#3F6B3A;color:#fff;font-size:14px;font-weight:600;padding:12px 14px;text-align:left;">…</th>
</tr></thead>
<tbody>
  <tr style="background-color:#fff;">
    <td style="border-bottom:1px solid #E5E9E1;color:#2E4A2B;font-size:14px;padding:11px 14px;"><strong>[satır başlığı]</strong></td>
    <td style="border-bottom:1px solid #E5E9E1;color:#333;font-size:14px;padding:11px 14px;">…</td>
  </tr>
  <tr style="background-color:#F8FAF6;"> … (satırlar #fff / #F8FAF6 dönüşümlü) … </tr>
</tbody></table></figure></div>
```

### 6.8 S.S.S.
Başlık kalıbı sitede: **"Sıkça sorulan sorular"** (H2, 6.2 stili). Soru metni şablonun sabit kuralı gereği `<h3>`'tür; görünümü sitedeki soru satırıyla aynıdır.
```html
<h2 style="border-left:4px solid #3F6B3A;color:#2E4A2B;font-size:24px;line-height:1.3;margin:36px 0 14px;padding-left:12px;">Sıkça sorulan sorular</h2>
<div style="margin:0 0 24px;">
  <div style="border-bottom:1px solid #E5E9E1;padding:16px 0;">
    <h3 style="color:#2E4A2B;font-size:16px;font-weight:700;line-height:1.4;margin:0 0 6px;">[Soru]</h3>
    <p style="color:#333;font-size:15px;line-height:1.7;margin:0;">[Cevap]</p>
  </div>
</div>
```
(`font-weight:700` ve `line-height:1.4`, sitedeki `<strong>` görünümünü H3'te korumak için eklendi; Editör Notları'nda belirtilir.)

FAQPage JSON-LD ayrı bir `<script type="application/ld+json">` bloğu olarak `sss.html` sonunda verilir. **Doğrulanmalı:** Ticimax blog editörü `<script>` etiketini koruyor mu? Korumuyorsa şema, Ticimax'in sayfa/SEO ek kod alanına girilir.
