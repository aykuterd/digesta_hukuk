# digesta_hukuk

Digesta'nın tanıtım sitesi ve yasal metinleri. GitHub Pages ile yayınlanır.

    /                      tanıtım sayfası
    /yasal/gizlilik/       Gizlilik Politikası
    /yasal/kullanim-sartlari/
    /yasal/mesafeli-satis/
    /yasal/iade/
    /yasal/kvkk/

## Yasal metinler elle düzenlenmez

`yasal/` altındaki sayfalar **üretilmiş dosyalardır**. Kaynak metin ana depoda
(`hukuk-rag`) `yasal.py` içinde durur; uygulama da aynı metni oradan servis
eder. İki kopya tutulmaz — biri güncellenip diğeri unutulmasın.

Firma künyesi girildikten sonra sayfaları yenilemek için, ana depoda:

    python site.py /yol/digesta_hukuk

Künye `.env` dosyasındaki `FIRMA_*` değişkenlerinden okunur. Künye eksik
olduğu sürece her sayfanın tepesinde TASLAK uyarısı çıkar ve sayfa
`noindex` ile işaretlenir; künye tamamlanınca ikisi de kendiliğinden kalkar.

## Yayına alma

Depo ayarlarında **Settings → Pages → Source: Deploy from a branch → main /(root)**.
Adres: `https://aykuterd.github.io/digesta_hukuk/`

Özel alan adı bağlanırsa yollar değişmez; bağlantılar görelidir.
