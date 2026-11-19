\# \*\*Blog Yazısı Brief'i: Marka Bağımsız Analiz ve Yazım Şablonu (v3)\*\*

\*\*Sürüm notu (v3):\*\* Bu sürüm, Wucize için hazırlanan v2 şablonunun her marka için kullanılabilen halidir. Markaya özgü tüm bilgiler (marka adı, alan adı, URL yapısı, renkler, S.S.S. tasarımı, proje sayfaları, teklif formu) şablondan çıkarılmış ve \*\*ilk mesajda iletilecek girdilere\*\* bağlanmıştır.

\*\*Temel ilke: Tahmin yapılmaz.\*\* Şablondaki her `[köşeli parantez]` alanı yalnızca kullanıcının ilettiği bilgiyle doldurulur. Bir bilgi iletilmemişse yazar (Claude dahil) onu tahmin etmez, benzer sitelerden çıkarmaz, ekran görüntüsünden ölçmez; önce sorar. Sorulamıyorsa alan boş bırakılır ve Editör Notları'nda \*\*"Eksik: kullanıcıdan istenmeli"\*\* olarak işaretlenir.

\-----

\## \*\*0. İlk Mesajda İletilecekler\*\*

Yazıma başlamadan önce aşağıdakiler ilk mesajda iletilir.

| Gereken | Zorunlu mu | Eksikse ne yapılır |

\| :-- | :-- | :-- |

| Yazı başlığı (H1) | Evet | Yazıma başlanmaz, istenir. |

| Bu şablon dosyası | Evet | İstenir. |

| Marka adı (yazıldığı biçimiyle) ve alan adı | Evet | İstenir. Alan adı URL'lerden çıkarılmaz. |

| \*\*Sitemap\*\* (sitemap.xml, sitemap index + alt sitemap'ler veya düz URL listesi) | Evet | İç bağlantı verilmez. Sitemap index iletildiyse ve alt sitemap'ler eksikse, eksik olanlar istenir. |

| \*\*Mevcut S.S.S. tasarımı\*\* (HTML/CSS kodu tercih edilir) | Evet | S.S.S. kodu hazırlanmaz. Yalnızca ekran görüntüsü geldiyse renk kodu, yazı tipi, ölçü ve köşe değerleri istenir; görüntüden okunmaz. |

| Hedef hizmet sayfası | Hayır | Sitemap'te konuyla açıkça eşleşen sayfa varsa o kullanılır; birden fazla aday varsa sorulur. |

| Teklif / iletişim sayfası adresi | Hayır | Sitemap'te açıkça teklif veya iletişim sayfası varsa kullanılır; yoksa sorulur. |

| Yayın dili ve hedef ülke | Hayır | Belirtilmezse Türkçe ve Türkiye varsayılmaz, sorulur (mevzuat kaynağı buna bağlıdır). |

| Marka profili istisnaları (ton, "biz" dili, yasaklı ifadeler, rakip adları) | Hayır | Bölüm 1'deki varsayılan kurallar uygulanır. |

| Kümedeki mevcut blog yazıları | Hayır | Sitemap'teki `/blog/` (veya eşdeğer) adreslerinden seçilir; yazının içeriği bilinmiyorsa yalnızca başlık/slug açıkça konuyla eşleşiyorsa bağlanır. |

\### \*\*Kopyalanabilir başlangıç mesajı\*\*

\```

Şablon: ekte (blog-sablonu-v3)

Marka adı: [Marka]

Alan adı: https://[alan-adi]

H1: [Yazı başlığı]

Hedef hizmet sayfası: [URL veya "sitemap'ten seç"]

Teklif/iletişim sayfası: [URL]

Yayın dili / hedef ülke: [Türkçe / Türkiye]

Sitemap: ekte ([dosya adı])

Mevcut S.S.S. tasarımı: ekte ([kod dosyası / sayfa URL'si + kod])

Marka profili istisnaları: [varsa]

Rakip / yasaklı ifadeler: [varsa]

\```

\-----

\## \*\*1. Marka Profili\*\*

İlk mesajdaki bilgilerle doldurulur. Doldurulmayan alan yazıda kullanılmaz.

| Alan | Değer | Kaynak |

\| :-- | :-- | :-- |

| Marka adı | [Marka] | İlk mesaj |

| İyelik/ek biçimi | [Marka]'nın / 'nin / 'in … | Marka adının okunuşuna göre; okunuş belirsizse (yabancı ad, kısaltma) sorulur |

| Alan adı | https://[alan-adi] | İlk mesaj |

| Ana hizmet sayfası | [URL] | İlk mesaj veya sitemap |

| Teklif / iletişim sayfası | [URL] | İlk mesaj veya sitemap |

| Proje / referans sayfaları | [URL listesi] | Yalnızca sitemap |

| URL yapısı | [ör. /hizmetler/…, /blog/…] | Yalnızca sitemap'te gözlenen yapı |

| S.S.S. tasarım değerleri | renk, yazı tipi, ölçü, köşe | Yalnızca iletilen kod |

| Yayın dili / hedef ülke | [ ] | İlk mesaj |

| Veri koruma mevzuatı ve kurumu | [ör. Türkiye: KVKK / Kişisel Verileri Koruma Kurumu] | Hedef ülkeye göre; resmi kaynaktan doğrulanır |

| Ton istisnaları | [ ] | İlk mesaj |

\-----

\## \*\*2. Genel Yaklaşım\*\*

Yazılar bir içerik sisteminin parçasıdır. Ortak amaç: bir hizmet kategorisinde karar aşamasındaki okura tarafsız, ansiklopedik bir rehber sunmak ve okuru doğal biçimde markanın ilgili hizmet sayfasına yönlendirmek.

\- \*\*Cevap önce gelir.\*\* İlk cümle, başlıktaki soruyu tanım cümlesiyle yanıtlar. Öne çıkan snippet ve yapay zekâ arama motorlarında (AI Overviews, ChatGPT, Perplexity) alıntılanmaya uygundur.

\- \*\*Numaralı çerçeve.\*\* Konu sayılabilir parçalara bölünür (N çalışma, N kalem, N alan). Sayı başlığa veya girişe yazılır, önce özet liste, sonra her madde ayrı başlıkta açılır.

\- \*\*Satış dili yok.\*\* Fiyat, süre, sonuç vaadi yapılmaz; "garanti veren teklife dikkat" yaklaşımıyla güven inşa edilir. Marka adı yalnızca 2–3 yerde ve standart kalıpla geçer.

\- \*\*Karar destek araçları.\*\* Her yazıda en az bir tablo ve bir kontrol listesi bulunur.

\- \*\*Konu kümesi.\*\* Yazılar birbirine ve hizmet sayfalarına bağlanır; bağlantılar yalnızca sitemap'ten seçilir.

Tahmini uzunluk: \*\*1.800–2.200 kelime\*\* (tablolar hariç).

\### \*\*Yazı türleri\*\*

| Tür | H1 kalıbı | Numaralı çerçeve | Tablo |

\| :-- | :-- | :-- | :-- |

| Tanım yazısı | [Hizmet] Nedir? [Sağlayıcı] Ne İş Yapar? | N temel çalışma | Dönem / Yapılan iş / Çıktı |

| Fiyat yazısı | [Hizmet] Fiyatları Neye Göre Değişir? N Belirleyici Kalem | N kalem | Kalem / Ödeme biçimi / Fiyatı ne değiştirir? |

| Etki yazısı | [Hizmet]: [Çıktı] Markayı Nasıl Güçlendirir? | N alan | Aşama / Yapılan iş / Çıktı |

\-----

\## \*\*3. Ortak İskelet\*\*

| # | Bölüm | İçerik | Hedef uzunluk |

\| :-: | :-- | :-- | :-: |

| 1 | \*\*H1\*\* | Soru + gerekirse ikinci soru veya sayı | — |

| 2 | \*\*Giriş P1: tanım cümlesi\*\* | "[Konu], … -dır/-dir." | 60–90 kelime |

| 3 | \*\*Giriş P2: yol haritası\*\* | "Bu yazıda … ele alınmıştır." (N sayısı geçer) | 30–45 kelime |

| 4 | \*\*H2: soruyu yeniden soran başlık + kısa cevap\*\* | "[Konu] Ne Demek?" / "… Neye Göre Belirlenir?" | 60–100 kelime |

| 5 | \*\*H2: numaralı özet liste\*\* | \*\*Kalın etiket:\*\* tek cümle | liste + 1 geçiş cümlesi |

| 6 | \*\*H2 × N: her madde ayrı başlık\*\* | "1. Başlık" | madde başı 110–160 kelime |

| 7 | \*\*H2: süreç veya hesaplama tablosu\*\* | Yazı türüne göre (Bölüm 2) | 80–150 kelime + tablo |

| 8 | \*\*H2: zaman / ek bilgi\*\* (isteğe bağlı) | "Ne Kadar Sürede Sonuç Verir?", "Ne Sıklıkla Yenilenmelidir?" | 80–120 kelime |

| 9 | \*\*H2: kontrol listesi\*\* | "… Nelere Dikkat Edilmeli?" | 1–2 cümle + 7–8 madde |

| 10 | \*\*H2: karşılaştırma\*\* (isteğe bağlı) | ör. Ajans / Serbest çalışan / Şirket içi | 80–120 kelime + tablo |

| 11 | \*\*H2: "[Konu] Hakkında S.S.S."\*\* | H3 sorular, 3–5 soru, yayın biçimi Bölüm 7 | soru başı 50–90 kelime |

| 12 | \*\*H2: Sonuç\*\* | N maddenin tek cümlede özeti + CTA | 70–110 kelime |

| 13 | \*\*H2: Kaynaklar\*\* | Resmi, birincil kaynaklar | 2–4 kaynak |

| 14 | \*\*H2: Etiketler\*\* | Bölüm 8 | 8–10 etiket, tek satır |

Karşılaştırma tablosunun ardından tek cümlelik bir hüküm gelir ("İki yöntem birbirinin alternatifi değil tamamlayıcısıdır." gibi).

\### \*\*Madde bölümlerinin iç yapısı\*\*

1\. \*\*Paragraf 1: Tanım + kapsam.\*\* İlk cümle "X, … -dır/-dir." kalıbında tanımdır; ardından kapsama giren unsurlar sayılır.

2\. \*\*Paragraf 2: Pratik ayrıntı / dikkat noktası.\*\* Okurun karar verirken bilmesi gereken nüans. Uygunsa iç bağlantı burada verilir.

3\. \*\*Son cümle: Köprü cümlesi.\*\* Sonraki maddeye geçişi hazırlar. Kalıp korunur, fiil ve yapı her maddede değişir. Kaçınılacak: her maddenin "… ele alınır." ile bitmesi.

\### \*\*S.S.S. içeriği\*\*

\- Sorular kullanıcıların gerçekten arattığı biçimdedir (süre, yasal durum, garanti, fiyat, fark, dahil mi, bırakınca ne olur).

\- Cevap \*\*tek kelimelik hükümle\*\* başlar ("Evet.", "Hayır.", "Kısmen.", "Değişir.", "Genellikle hayır."), ardından 2–3 cümle gerekçe.

\- Konu uygunsa bir soru \*\*garanti\*\* konusuna ayrılır ve resmi bir kaynakla (platformun kendi dokümantasyonu) desteklenir.

\- İnsan, çalışan veya müşteri verisi içeren konularda bir soru, hedef ülkenin \*\*veri koruma mevzuatına\*\* ayrılır ve ilgili resmi kurum kaynağıyla desteklenir.

\- Bir soru komşu hizmete köprü kurar ("[Hizmet A] fiyatına [Hizmet B] dahil mi?"); komşu hizmet yalnızca sitemap'te varsa bağlanır.

\-----

\## \*\*4. Dil, Üslup ve Cümle Kuralları\*\*

Aşağıdakiler varsayılandır; marka profilindeki istisnalar önceliklidir.

\*\*Ton:\*\* Tarafsız, bilgilendirici, danışman gibi. Ansiklopedi maddesi ile uzman rehberi arası.

\*\*Yapılan:\*\*

\- Edilgen ve genel çatı ağırlıklı: "ele alınmıştır", "belirtilmelidir", "incelenebilir".

\- Üçüncü şahıs anlatım; "biz" kullanılmaz, "siz" çok nadir.

\- Tanım cümleleri "X, … -dır/-dir." kalıbında.

\- Karşıtlıkla netleştirme ve somut örnekle kıyas.

\- Yabancı terimler Türkçesiyle, parantez içinde: kaydırmalı gönderi (carousel), işveren markası (employer branding).

\- Paragraflar 2–4 cümle; cümleler ortalama 15–25 kelime.

\*\*Yapılmayan:\*\*

\- Ünlem, emoji, "harika", "mükemmel", "en iyi" gibi abartı sıfatları (kaynak başlıkları hariç).

\- Kesin rakam, fiyat aralığı, süre, sıralama veya sonuç vaadi. Süre sorularında "Değişir." + belirleyen etkenler verilir.

\- Okura doğrudan satış çağrısı (CTA yalnızca sonuçta).

\- Rakip marka adı.

\- Kaynakta dayanağı olmayan istatistik, oran veya mevzuat hükmü.

\*\*Marka geçiş kalıbı\*\* (yazı başına en fazla 3 kez; ek, marka profilindeki biçime göre):

\- "[Marka]'nın [hizmet adı] hizmeti incelenebilir."

\- "… için [Marka]'nın [hizmet] hizmeti incelenebilir veya teklif formu doldurulabilir." (sonuç CTA'sı)

\- "Bu yaklaşımın uygulamadaki örnekleri için [Marka]'nın [Proje A] ve [Proje B] proje sayfaları incelenebilir." (yalnızca sitemap'te proje sayfası varsa)

\-----

\## \*\*5. SEO ve Yapay Zekâ Arama Kurgusu\*\*

\*\*Anahtar kelime yerleşimi\*\*

\- Birincil anahtar kelime: H1 başı, slug, ilk cümle, meta açıklama, en az bir görsel alt metni.

\- Uzun kuyruk varyasyonlar H2 ve S.S.S. başlıklarına dağıtılır; her biri doğal akışta bir kez geçer. Yoğunluk hedeflenmez.

\*\*Alıntılanabilirlik (GEO)\*\*

\- Her H2'nin altındaki ilk cümle, bağlamdan koparıldığında da tek başına anlamlı bir cevaptır.

\- Numaralı liste + tablo + S.S.S. üçlüsü yapılandırılmış veri sağlar.

\- Article/BlogPosting şeması önerilir. FAQPage şeması S.S.S. kodunun içinde gelir; sitede bir eklenti zaten FAQ şeması üretiyorsa bu durum Editör Notları'nda belirtilir ve iki kez eklenmez.

\*\*Meta kuralları\*\*

\- Title: 50–60 karakter, anahtar kelime başta, sonda "| [Marka]".

\- Meta açıklama: 130–150 karakter, etken çatı, tırnak işareti yok, sonda eylem çağrısı.

\- Slug: kısa, Türkçe karaktersiz, soru eki olmadan; blog dizini sitemap'teki yapıya göre (ör. /blog/…). Dizin yapısı sitemap'te görülmüyorsa sorulur.

\- Karakter sayıları yazar tarafından sayılarak verilir, tahmini yazılmaz.

\-----

\## \*\*6. Bağlantı, Kaynak ve CTA Kuralları\*\*

\*\*İç bağlantılar (yazı başına 6–9; teklif/iletişim sayfası bu sayıya dahil değildir)\*\*

\- \*\*Tek kaynak: iletilen sitemap.\*\* Sitemap'te birebir bulunmayan adres yazılmaz; adres benzetme, slug türetme veya "muhtemelen vardır" çıkarımı yapılmaz.

\- URL yapısı (hizmet, blog, proje, teklif dizinleri) sitemap'te gözlendiği haliyle kullanılır ve marka profiline yazılır.

\- Bağlantı verilmeyecek adresler: demo/test kalıntıları, sayfalama (`/page/2`), etiket, kategori ve yazar arşivleri, ek/medya sayfaları, `noindex` olduğu bilinen sayfalar, parametreli adresler. Belirsiz bir adres varsa kullanılmaz ve Editör Notları'nda sorulur.

\- Hizmet sayfası bağlantıları ilgili maddenin 2. paragrafına cümle içinde yerleştirilir.

\- En az 1–2 bağlantı kümedeki başka blog yazılarına verilir.

\- Proje / referans sayfalarına 1–2 bağlantı, marka geçiş kalıbıyla; sitemap'te proje sayfası yoksa bu kural atlanır ve not düşülür.

\- Ana hizmet sayfası 2 kez bağlanır: gövdede bir kez ("Ne Demek?" bölümünde), sonuçta bir kez.

\- Sitemap'te 6 uygun adres yoksa sayı zorlanmaz; eksik sayı Editör Notları'na yazılır.

\*\*Dış kaynaklar (2–4)\*\*

\- Yalnızca resmi ve birincil kaynaklar: platform dokümantasyonları (Google Arama Merkezi, Meta, LinkedIn, TikTok yardım sayfaları), ilgili mevzuat ve resmi kurum sayfaları.

\- Her dış bağlantı yayından önce açılarak doğrulanır; hafızadan adres yazılmaz.

\- Gövdede bağlam içinde bağlanır, sonda "Kaynaklar" başlığıyla listelenir.

\*\*CTA\*\*

\- Yalnızca sonuç paragrafının son cümlesinde: hizmet sayfası + teklif/iletişim sayfası.

\-----

\## \*\*7. S.S.S. Yayın Biçimi\*\*

S.S.S. bölümü, \*\*ilk mesajda iletilen mevcut tasarıma\*\* göre kodlanır. Belgede normal H3 soru + paragraf olarak yazılır; yayın için ayrıca hazır HTML kodu teslim edilir (`sss.html`).

\*\*Başlık:\*\* Sitedeki mevcut S.S.S. başlık kalıbı iletilen tasarımdan alınır. Kalıp görünmüyorsa varsayılan: "[Konu] Hakkında S.S.S."

\*\*Tasarım kuralları\*\*

\- Renk kodları, yazı tipi, yazı boyutları, boşluklar, köşe yuvarlaklığı, kenar çizgileri, simgeler ve geçiş efektleri \*\*yalnızca iletilen koddan\*\* alınır.

\- Ekran görüntüsü yalnızca yapıyı (açılır-kapanır mı, simge konumu, ilk soru açık mı) anlamak için kullanılır; değer okunmaz. Değerler eksikse istenir.

\- İletilen tasarım açılır-kapanır değilse yapı korunur; akordeona çevrilmez.

\- İletilen kodda tanımlı olmayan bir durum (ör. bağlantı rengi, üzerine gelme rengi, mobil kırılım) uydurulmaz; sayfanın mevcut stilinin devralınması (`inherit`) tercih edilir ve Editör Notları'nda belirtilir.

\- Renkler kodun başındaki değişkenlerden yönetilir; değişkenlerin her biri iletilen koddaki karşılığıyla yorumlanır.

\*\*Sabit teknik kurallar\*\* (tasarımdan bağımsız)

\- Sorular `<h3>` olarak kalır; başlık `<h2>`.

\- Açılır-kapanır yapı, iletilen tasarım aksini gerektirmedikçe JavaScript'siz `<details>` / `<summary>` ile kurulur.

\- Klavye odağı görünür (`:focus-visible`).

\- FAQPage şeması (JSON-LD) kodun içinde gelir; cevap metinleri sayfadaki metinle birebir aynıdır, şemada bağlantı kullanılmaz.

\- HTML'deki soru ve cevaplar belgedeki metinle birebir aynıdır.

\*\*Kod iskeleti\*\* (`{{…}}` alanları yalnızca iletilen tasarımdan doldurulur; doldurulamayan alan silinir ve not düşülür):

\```html

<!-- [Marka] | [Yazı başlığı] | S.S.S. -->

<section class="brand-faq" aria-labelledby="brand-faq-title">

`  `<h2 id="brand-faq-title">[Konu] Hakkında S.S.S.</h2>

`  `<details class="brand-faq-item" open>

`    `<summary><h3>[Soru 1]</h3></summary>

`    `<div class="brand-faq-answer">

`      `<p>[Cevap 1, gerekirse <a href="https://[alan-adi]/[sitemap'teki adres]">iç bağlantı</a> veya <a href="https://..." target="\_blank" rel="noopener">dış kaynak</a>]</p>

`    `</div>

`  `</details>

`  `<details class="brand-faq-item">

`    `<summary><h3>[Soru 2]</h3></summary>

`    `<div class="brand-faq-answer">

`      `<p>[Cevap 2]</p>

`    `</div>

`  `</details>

`  `<!-- soru sayısı kadar tekrarlanır -->

</section>

<style>

`  `/\* [Marka] S.S.S. | Değerler iletilen tasarım kodundan alınmıştır: [kaynak dosya/sayfa] \*/

.brand-faq {

`    `--faq-accent: {{vurgu rengi}};

`    `--faq-link-underline: {{bağlantı alt çizgi rengi}};

`    `--faq-link-hover: {{bağlantı üzerine gelme rengi}};

`    `--faq-bg: {{bölüm zemini}};

`    `--faq-card: {{kart zemini}};

`    `--faq-border: {{kart kenar rengi}};

`    `--faq-text: {{metin rengi}};

`    `--faq-text-soft: {{cevap metni rengi}};

`    `--faq-radius: {{köşe yuvarlaklığı}};

`    `background: var(--faq-bg);

`    `font-family: inherit;

`  `}

.brand-faq > h2 { color: var(--faq-text); }  /\* boyut ve yazı tipi sitenin H2 stilinden gelir \*/

.brand-faq .brand-faq-item {

`    `background: var(--faq-card);

`    `border: 1px solid var(--faq-border);

`    `border-radius: var(--faq-radius);

`    `overflow: hidden;

`  `}

.brand-faq .brand-faq-item[open] { border-color: var(--faq-accent); }

.brand-faq .brand-faq-item > summary {

`    `list-style: none;

`    `cursor: pointer;

`    `display: flex;

`    `align-items: center;

`    `justify-content: space-between;

`    `gap: {{boşluk}};

`    `padding: {{iç boşluk}};

`  `}

.brand-faq .brand-faq-item > summary::-webkit-details-marker { display: none; }

.brand-faq .brand-faq-item > summary > h3 {

`    `margin: 0;

`    `font-family: inherit;

`    `font-size: {{soru yazı boyutu}};

`    `font-weight: {{soru yazı kalınlığı}};

`    `color: var(--faq-text);

`  `}

.brand-faq .brand-faq-item > summary::after {

`    `content: "{{kapalı simge}}";

`    `flex-shrink: 0;

`    `/\* simge ölçüleri ve biçimi iletilen tasarımdan \*/

`  `}

.brand-faq .brand-faq-item[open] > summary::after {

`    `/\* açık simge durumu iletilen tasarımdan \*/

`  `}

.brand-faq .brand-faq-answer { padding: {{cevap iç boşluğu}}; }

.brand-faq .brand-faq-answer p {

`    `margin: 0;

`    `font-size: {{cevap yazı boyutu}};

`    `color: var(--faq-text-soft);

`  `}

.brand-faq .brand-faq-answer a {

`    `color: var(--faq-text);

`    `text-decoration-color: var(--faq-link-underline);

`  `}

.brand-faq .brand-faq-answer a:hover { color: var(--faq-link-hover); }

.brand-faq .brand-faq-item > summary:focus-visible { outline: 2px solid var(--faq-accent); }

`  `@media (max-width: {{mobil kırılım}}) {

`    `/\* mobil değerler iletilen tasarımdan \*/

`  `}

</style>

<script type="application/ld+json">

{

`  `"@context": "https://schema.org",

`  `"@type": "FAQPage",

`  `"mainEntity": [

`    `{

`      `"@type": "Question",

`      `"name": "[Soru 1]",

`      `"acceptedAnswer": { "@type": "Answer", "text": "[Cevap 1, bağlantısız düz metin]" }

`    `}

`  `]

}

</script>

\```

\-----

\## \*\*8. Etiketler\*\*

\- Yazının en sonunda, "Kaynaklar" bölümünden sonra "Etiketler" başlığıyla yer alır.

\- 8–10 etiket, tek satırda, " · " ile ayrılır; her etiket büyük harfle başlar.

\- İçerik: birincil anahtar kelime + 3–4 uzun kuyruk/alt konu + ilgili hizmet ve disiplin adları + varsa mevzuat konusu.

\- Sitede mevcut bir etiket listesi iletildiyse önce oradaki etiketler kullanılır; yeni etiket gerekiyorsa Editör Notları'nda belirtilir.

\- Etiketler CMS'teki etiket alanına aynı biçimde girilir.

\-----

\## \*\*9. Teslim Formatı ve Editör Notları\*\*

Her yazı iki parça halinde teslim edilir:

1\. \*\*Yazı belgesi:\*\* H1'den Etiketler'e kadar yayınlanacak metin; altında yatay çizgiyle ayrılmış \*\*"Editör Notları (yayınlanmayacak)"\*\* bölümü.

2\. \*\*`sss.html`:\*\* S.S.S. kodu ve FAQPage şeması (Bölüm 7).

\*\*Editör Notları içeriği\*\*

| Alan | İçerik |

\| :-- | :-- |

| Title | Metin + karakter sayısı |

| Meta açıklama | Metin + karakter sayısı |

| Slug | Sitemap'teki blog dizinine göre |

| Birincil anahtar kelime | |

| Uzun kuyruk varyasyonlar | |

| Kapak görseli alt metni | |

| Şema | Article/BlogPosting + FAQPage (HTML kodunun içinde) |

| İç bağlantılar | Her adres + sitemap'te bulunduğunun teyidi |

| Dış kaynaklar | Her adres + açılarak doğrulandığının teyidi |

| S.S.S. tasarım kaynağı | Değerlerin alındığı dosya/sayfa |

| Etiketler | CMS etiket alanına girilecek liste |

| \*\*Eksik / doğrulanmalı\*\* | Tahmin edilmeyip boş bırakılan her alan ve kullanıcıya sorulacak her nokta |

\-----

\## \*\*10. Yayın Öncesi Kontrol Listesi\*\*

\*\*Girdiler\*\*

\- [ ] Marka adı, alan adı, sitemap ve S.S.S. tasarımı ilk mesajda iletildi.

\- [ ] Marka profili (Bölüm 1) yalnızca iletilen bilgilerle dolduruldu.

\- [ ] Tahmin edilen hiçbir değer yok; eksikler Editör Notları'nda listelendi.

\*\*Yapı\*\*

\- [ ] İlk cümle başlıktaki soruyu doğrudan tanımla yanıtlıyor.

\- [ ] Girişte "Bu yazıda … ele alınmıştır." yol haritası ve N sayısı var.

\- [ ] Numaralı özet liste, gövdedeki başlıklarla aynı sırada ve aynı adlarla.

\- [ ] Her madde tanım cümlesiyle açılıyor, çeşitlendirilmiş köprü cümlesiyle kapanıyor.

\- [ ] En az bir tablo ve bir kontrol listesi var.

\- [ ] Sonuç N maddenin tamamını tek cümlede sayıyor ve CTA ile bitiyor.

\- [ ] Kaynaklar'dan sonra 8–10 etiketlik Etiketler bölümü var.

\*\*S.S.S.\*\*

\- [ ] Cevaplar tek kelimelik hükümle başlıyor.

\- [ ] Gerekiyorsa garanti sorusu resmi kaynakla, kişisel veri sorusu hedef ülkenin resmi kurum kaynağıyla destekleniyor.

\- [ ] `sss.html`'deki tüm tasarım değerleri iletilen koddan alındı; uydurulmuş değer yok.

\- [ ] HTML'deki sorular ve cevaplar belgedeki metinle birebir aynı; FAQPage şeması bir kez ekli.

\*\*Dil\*\*

\- [ ] Ünlem, emoji, abartı sıfatı, fiyat, süre veya sonuç vaadi yok.

\- [ ] Marka adı en fazla 3 kez, standart kalıpla ve doğru ekle geçiyor.

\- [ ] Yabancı terimler Türkçe karşılığıyla verildi.

\- [ ] Paragraflar 4 cümleyi aşmıyor.

\- [ ] Yazım ve ligatür kontrolü yapıldı (fi/fl içeren kelimeler).

\*\*SEO ve bağlantılar\*\*

\- [ ] Birincil kelime H1, slug, ilk cümle, meta açıklama ve bir alt metinde geçiyor.

\- [ ] Title 50–60, meta açıklama 130–150 karakter (sayılarak).

\- [ ] 6–9 iç bağlantı (teklif/iletişim hariç), hepsi sitemap'te birebir mevcut; arşiv, demo ve parametreli adres yok.

\- [ ] En az 1 bağlantı kümedeki başka bir blog yazısına; proje sayfası varsa 1–2 bağlantı proje sayfalarına.

\- [ ] Ana hizmet sayfası 2 kez (gövde + sonuç) bağlandı.

\- [ ] Tüm dış kaynaklar açılarak doğrulandı.

\- [ ] Article şeması eklendi.
