
DONATE
 Giriş Yap

Coin Hunters
ANA SAYFA
ÖN SATIŞYENİ
STAKE
TESTNET
BLOG
HABER
HIZLI KEŞFET
CONTACT
Rivalz Ödüllü Testnet Rehberi

0xmtnslk tarafından
Mayıs 26, 2024
Okuma süresi: 6dk, 22sn

+
-
 0
Rivalz DePIN (Merkezi Olmayan Fiziksel Altyapı Ağları) aşağıdakileri sunmak üzere özel olarak tasarlanmıştır:

DePIN çözümü aracılığıyla değerli yapay zeka verilerinin merkezi olmayan bir şekilde güvenli bir şekilde depolanması.
FHE (Tam Homomorfik Şifreleme) aracılığıyla AI şirketleri ve aracıları için Güvenli Veri erişimi ve kullanımı.
Verileri işlemek ve depolamak için veri işleme modülü.
Şirketler ve üçüncü taraflarca paylaşılan özel veriler için uyumluluk ve doğrulama ile herhangi bir PII (Kişisel Tanımlayıcı Bilgi) verisi için ek izin doğrulama.
Geliştiriciler için kişiselleştirilmiş yapay zeka uygulamalarının geliştirilmesine olanak tanıyan daha fazla veri güvenliği
Yapay zeka aracılarının Web2 ve Web3 uygulamalarında kullanımı ve güçlendirilmesi.
Son dönemde hem web2 tarafında hem de web3 tarafında yapay zeka oldukça büyük yer kaplıyor. Merkezi yapılar olan Chatgpt ve Gemini yerine merkeziyetsiz olan web3 yapay zeka çalışmalarının temeli olan DePIN projeleri oldukça yüksek değerlere de ulaşabilir. Rivalz de bu projelerin başında geliyor.

Şimdi ödüllü testneti başladı. Burada testnetine katılarak RIVALZ token ve mainnet için Node kurma hakkı olan NFT’den kazanma şansımız var. Sizlere adım adım ne yapmanız gerektiğini içeren rehberi hazırladım. Aşağıdaki adımları takip ederek sizde bu testnete rahatlıkla katılabilirsiniz.

İlk olarak BURADAN testnet sitesine gidiyoruz. Buraya metamask cüzdanımızı bağlıyoruz. ilk olara RIVALZ test ağını cüzdanımıza ekleyecek sonrasında test ağında onaylama yapıp cüzdanla girişimizi tamamlıyoruz.


Buradan Sosyal Point Alanına gidiyoruz. Bu bölümde twitter, Discord adreslerimizi bağlayarak gerekli görevleri yerine getiriyoruz ve sosyal puanımızı arttırıyoruz.


Rivalz ile ilgili twitler atarak ve bu bölümden göndererek daha fazla puan alabilirsiniz.

rCLIENT Kurulumu ve Node Çalıştırma

rClient katılmak için üç farklı işletim sistemi kullanabilirsiniz. Windows, MacOS ve Linux. Biz bu rehberde, Windows için olanı anlatacağız. (Linux henüz çalışmıyor. Takım üzerinde çalıştıklarını belirtti. Düzelirse onu da rehberimize eklerim.)

Rivalz Windows Server Kurulumu
Node testnetine katılmak için bir tane VPS sunucu kiralıyoruz. Bu tarz testnetler için kendi bilgisayarlarınızı kullanmayın! Çünkü node testinde bilgisayarın iyi bir internete ve 24 saat açık kalmaya ihtiyacı var. O nedenle VPS sunucular tercih ediyoruz.

Bu rehberde Contabo için windows sunucu temini nasıl yapacağınızı anlatacağım. İlk olarak BURADAN contabo sitesine ulaşıyoruz. Ben bu işlemler için 9,5€ olan VPS sunucu tercih ettim. Siz istediğinizi alabilirsiniz. İlk alım yaparken Ubuntu 22.04 almanız yeterli olacaktır. Hiç bilmeyenler için nasıl alınacağını da aşağıya ekledim.


Sunucumuzu aldıktan sonra kendi panelinizde şu şekilde göreceksiniz.


Şuan sunucumuz Ubuntu 22.04 yani Linux yüklü. Biz onu windows server haline çevireceğiz. Bunun içinde yaklaşık olarak aylık 1,5$ civarında bir maliyeti olacak. Bu nedenle başladığımızda size gelen fiyat bildirimini kabul etmeli ve contaboya verdiğiniz kartta en az onun iki katı kadar bakiye bulundurulmalısınız.


Image URL: 	https://archive.org/download/newIsoForContabo/newIsoForContabo.iso
Image Name: 	Windows Contabo
Os Type: 	Windows
Version:	2019
Description:	İstediğiniz bir açıklama ekleyeblirsiniz.
Bu adımı yaptıktan sonra Next diyoruz sizden onaylar isteyecek onları da onayladıktan sonra;


Bu şekilde bir sayfaya yönlendirecek, yaklaşık yarım saat ile bir saat arasında sürüyor. Bu işlem bittikten sonra devam ediyoruz.

İso dosyasını sunucuya Yükleme

İlk önce Cloud-init kırmızı olarak gelecektir. Onu aktif ediyoruz. Radyo butona basmanız yeterli. İkinci olarak Re Install butonuna basıyoruz.


Gelen sayfada, görseldeki adımları tamamlıyoruz. Bu adımlardan sonra yaklaşık 5dk kadar bekleyin ve SSH terminaline geçiyoruz. Bu rehberde mobaxterm terminali kullanacağım. Eğer sizde yoksa BURADAN indirebilirsiniz.

Sunucuya Uzak Bağlantı ile Ulaşma

VNC bağlantı için görseldeki adımları takip edip, gerekli IP ve port numarasını bir yere not edelim ve şifremizi değiştirelim. Sonrasında Mobax terminali açıyoruz.


Session bölümüne basıyoruz ve oradan VNC terminali seçiyoruz.


VNC IP ve port numarasını girdikten sonra, belirlediğimiz şifreyi girip OK tuşuna basıyoruz.


Artık sunucumuza ulaştık. Burada Windows server için kurulum adımlarına geçiyoruz.

Windows Server Kurulumu

Görseldeki kurulumu seçiyoruz ve Next diyoruz. Sonraki gelen ekranda Custom Install olan seçeneğe basıyoruz ve devam ediyoruz.


Karşınıza görseldeki gibi ekranlar gelecek. Burada Load driver diyoruz. Sonrasında görsellerdeki adımları uygulayıp OK butonuna basıyoruz.


New butonuna basıyoruz ve hiçbir değişiklik yapmadan Apply butonuna basıyoruz. Sonrasında gelen uyarıya OK diyoruz. Kurulum bitene kadar bekliyoruz. Bittiğinde Administrator için şifre belirlemenizi isteyecek. Bu şifre önemli daha sonra bu sunucuya bağlanmak için o şifreye ihtiyacınız olacağı için, unutmayacağınız bir şifre girin.


İşlem tamamdır. Artık sunucumuza windows server ekledik. Açmak için VNC terminalde Ctrl +Alt+Del tuşu var ona basıyoruz ve biraz önce administrator için belirlediğimiz şifreyi giriyoruz.


Server manager bölümünde Manager özelliklerini görseldeki gibi yapıyoruz. İlk açtığınızda tick işaretiyle gelen alanı kaldırıyoruz ve görseldeki hale getirip OK tuşuna basıyoruz. Sonrasında;


Arama kutusuna Device Manager yazıp açıyoruz.


Gördüğünüz gibi ünlem işareti olan donanımlarımızın sürücülerini yükleyeceğiz. Update device diyoruz.


Browser my computer seçeneği işaretliyoruz. Sonrasında D:\ yazdıktan sonra Browser basıyoruz. Şimdi update için gerekli olan paketlerin yerini bulacağız. Diğer ünlem işaretli olanlarda bu adımı yapmanıza gerek yok. Bir kere yapmanız yeterli olacaktır.


Sizde de buna benzer bir dosya olacak seçip OK diyoruz sonrasında NEXT diyerek diğer eksik sürücüleri de yüklemiş oluyoruz.


VNC terminalde son işimiz ise uzak bağlantıyı aktif etmek. Yukarıdaki görsellere göre uzak bağlantıyı aktıf ediyoruz. Artık VNC terminalimizi kapatabiliriz.


Kendi PC’nizde Uzak Masaüstü Bağlantı programını arayın ve çalıştırın. Sonrasında, görseldeki adımları takip ederek windows servere ulaşabilirsiniz. Artık bildiğiniz windows kullanımının aynısı.

rCLIENT Çalıştırma

Yapacağınız işlemleri sırayla anlatayım. İlk olarak Windows server Edge veya Chrome tarayıcı indiriyoruz. Sonrasında rivalz sitesini server içinde tekrar açıyoruz. Bu nedenle rivalz katıldığınız metamask’ı server içinde tekrar açmanız gerekiyor. Bu adımları yaptıktan sonra Windows için Download rClient diyoruz ve exe dosyasını indiriyoruz. Karşınıza görseldeki gibi bir sayfa açılacak. Burada cüzdan adresimizi SAVE ediyoruz. Storage için Sunucunuza göre bir miktar veriyoruz. Sonrasında Run yani Play tuşuna basıyoruz. Normal ekranda client yansımaz ise; Üst menü de View bölümünden reload yada force reload yaparak kendi dashboardunuzda görünmesini sağlıyoruz.

En son göründüğünde Validated yapıyoruz ve aktif konuma geçiyor.

Bu Yazıya Tepkiniz Ne Oldu?
2
alk_l_yorum
Alkışlıyorum
0
be_endim
Beğendim
0
d_nceliyim
Düşünceliyim
0
be_enmedim
Beğenmedim
YORUM YAP
E-posta adresiniz yayınlanmayacak. Gerekli alanlar * ile işaretlenmişlerdir

Yorumunuz
Yorumunuz *
Adınız
Adınız *
E-Posta Adresiniz
E-Posta *
Değerlendirmeniz5 4 3 2 1 0
Daha sonraki yorumlarımda kullanılması için adım, e-posta adresim ve site adresim bu tarayıcıya kaydedilsin.


Yorum Gönder
Giriş Yap
BENZER YAZILAR
zksync era mainnet rehberi
zkSync Era Airdrop Rehberi
 Mart 25, 2023
scoll-alpha-testnet
Scroll Alpha Testnet Rehberi
 Şubat 28, 2023
GD5GK3DbMAEYKbo
Taiko Testnet Rehberi | Alpha 6
 Ocak 17, 2024
sui-testnet-v2
Sui Testnet Rehberi
 Ocak 26, 2023
Bültenimize Katılın
Hemen ücretsiz üye olun ve yeni güncellemelerden haberdar olan ilk kişi olun.


GİRİŞ YAP
 ANA SAYFA
 ÖN SATIŞYENİ
 STAKE
 TESTNET
 BLOG
 HABER
 HIZLI KEŞFET
 CONTACT
Ara …
Coin Hunters
Hakkımızda

İletişim

Borsa İndirimleri

Donate Us

Gizlilik Kuralları

Önemli Linkler
Metamask Kullanımı

Coinmarketcap Kullanımı

Hızlı Keşfet

Kategoriler

Kategori seçin
Bizi Takip Edin
Takip
Abone
Takip
© Copyright 2023, Coin Hunters. Tüm Hakları Saklıdır

Destek için# rivalz.ai
