############################

############################
# NETWORK DNS
############################

############################


# DNS (or Domain Name System)
internet adres resolving sistemini temsil eden genel bir terimdir. 

__DNS Server (or Name Server)__ ise IP'leri resolving yapmakla yükümlü yazılımdır. Bazen __Domain Name Server__ denir fakat yanlış bir kullanımdır.

# International Corporation for Assigned Names and Numbers (or ICANN)
2019 yılı itibariyle hala en yetkili kuruluştur. Amerika'ya bağlıdır. __registrar (or kaydedici)__ firmalar (örnek: godaddy), ICANN'dan lisans almak zorundalar.

# IANA (or Internet Assigned Numbers Authority)
ICANN için gerekli bazı teknik konuları tamamlayan kuruluştur.

# RIR (yad Regional Internet Registry)
ICANN ve IANA'nın altında dünyanın 5 farklı bölgesinde yetkilendirilmiş kuruluşlar vardır. Bu kuruluşlar kendi bölgelerinden sorumludur ve devlete bağlı kuruluş diillerdir.

- AfriNIC
  
  African Region Internet Registry: Afrika

- APNIC
  
  Asia Pacific Network Information Centre: Asya ve Pasifik

- ARIN
  
  American Registry for Internet Numbers: Kuzey Amerika

- LACNIC

  Latin America and Caribbean Internet Addresses Registry: Latin Amerika ve Karaibler bölgesi

- RIPE NCC
  
  Reseaux IP Européens Network Coordination Centre: Avrupa bölgesi.

RIR alanları yukarıda yazıldığı kadar keskin çizgilerle ayrılmaz. Örneğin, ARIN bölgesi esas olarak Kuzey Amerika olmakla beraber Güney Amerika ve Afrikaya da servis verir. RIPE bölgesi esas olarak avrupa olmakla beraber ortadoğu ve orta-asya içlerine kadar servis vermektedir. Türkiye, RIPE NCC bölgesindedir. RIPE NCC'nin merkezi Hollanda’dadır.

# LIR (or Local Internet Registry)
kullanıcıya IP veren kuruluşlardır. ISP (or Internet Sevice Provider) (turktelekom, superonline...)'lere denk gelir. Yasal anlamda şirketi olan herkes bu görevi alabilir. Türkiyede u servisi sağlayan 100'den fazla kuruluş vardır.

# Web tarayıcının DNS sorgusu
sırası ile:
- web browser dns cache
- OS dns cache
- "hosts" file
- __public dns (or non-authoritative DNS server or recursive DNS server or recursive DNS resolver)__

  örnek google dns 8.8.8.8, 8.8.4.4(google ikinci yedek ip), Cloudflare 1.1.1.1 gibi... Eğer public dns tanımlamazsak ISP bizim yerimize default değeri atar.

  public dns kendi içinde bilgiyi bulamaz ise, kendi gidip root dns server'a sorar.

# hierarchy of DNS system

# 1- root dns servers
  en üstte olan ve en yetkili sunuculardır.

  DNS sunucuları tüm domain bilgilerini saklayamaz. local cache'inde yok ise, ilk önce root server'lara sorar. root server bu bilgiyi local'inde bulundurmuyorsa 2inci seviye root server'ın adresini sorgulayan client'a döndürür.
  
  root serverlar dünyada 12 adettir (yıl 2019). bunlar ICANN tarafından belirlenmiştir. fakat sadece 1 tanesi ICANN kuruluşa direk bağlı bir sunucudur. bu sunucuya __ICANN Managed Root Server (or IMRS)__ deniyor. diğerlerinin ICANN'a bağlı olmamasının sebebi, merkezi yönetimden kaçınmaktır.

  ICANN'ın resmi sayfası olan www.dns.icann.org sitesinde root-servers.org'a referans verilmiştir. buradan 12 server'ı görebiliriz.

  12 adet Root dns server var, fakat bunlarda farklı instance'larla kendilerini çoğaltmışlardır. Yine bu instance'larda root-servers.org sayfasında görülebilir.

  2inci seviye DNS sunucu bilgileri tutar.

# 2- top-level dns server
  2inci seviye dns servler'lardır. her "top-level dns server" ".com", ".org" gibi sorumluluk alanları vardır.

# 3- authoritative DNS server
  3üncü seviye dns server'lardır.

# 4-
  DNS sisteminde 4üncü seviye yoktur. Bu seviyeye istersek public DNS'lerimizi koyabiliriz.

# whois server
registrar'a yeni bir domain eklendiğinde, registrar bu bilgiyi o domainin uzantısının sorumlusu olan "whois server"'a yollar. örneğin .com ve .net alan isimleri için verisign şirketinin whois sunucusu merkezi sunucudur. daha sonra bu bilgi diğer üçüncü parti whois server'lar tarafından klonlanır.

Dolayısı ile; root server'lar dahi .com ve .net için gerekli tüm domain'leri local'lerinde tutmazlar.

Verisign firması ICANN'a bağlıdır ve ICANN tarafından yetkilendirilmiştir.

ICANN'dan her firma godaddy gibi kolayca yetki alamaz. fakat godaddy'ye kolayca aracılık edebilir, yani godaddy'nin bayisi olabilir.

# hostname vs domain name
domain name bir bilgisayara DNS sunucusu tarafından atanmış string'dir. oysa hostname local bir network'te her makinanın kendisini dışarıya tanıttığı isimdir. network içinde hostname kullanılırken, dışarıya gidişlerde domain kullanılır. dışardaki bir yere giderken, oradaki networkteki bir alt makineye erişmek istediğimizde hostname.domainname.com gibi bir adresten yararlanılır. hostname ve domain name aynı görevi görür. www internet tarayıcıları için gerekli varsayılan makinanın hostname'idir.

# subdomain
mail.google.com, map.google.com'deki mail ve map birer subdomain'dir. ayrı IP'leri vardır. fakat istenirse aynı IP'ye de yönlendirilebilir.

# domain'i hosting'e bağlama
wix.com bizim sayfamızı barındırıyor (sunucu hosting firmamız) olsun. godaddy.com'dan da domainimizi almış olalım.

- wix.com'a domain-name'imizi bildiriyoruz.
- wix.com bize wix'in kendi dns'lerini veriyor. bunlar genelde ns1.wix-dns.com tarzında URL'ler oluyor. 
- godaddy'de o domaine ait nameserver'larımızı tanımlıyoruz. bunun için godaddy'ye login oluyor, ilgili domainimizi seçiyor, ayarlarına giriyor ve nameserver alanlarımızı dolduruyoruz. burada birden fazla nameserver olabilir. çünkü yedek nameserver olabiliyor.

Artık domanimize istek yapıldığında, godaddy dns sorgusunu yapanı ns1.wix-dns.com'a yönlendiriyor. ns1.wix-dns.com gelen sorguyu görüyor ve onu sunucu bilgisayarın IP'sini dönüyor.

Bu örnekte godaddy'ye veridğimiz dns sunucuları bizim kendi kişisel sunucularımız olabilir. Genelde büyük firmalar kendi dns suncuularını kullanıyor.

# fully qualified domain name (or FQDN)
hostname + domain name birarada olduğunda verilen isimdir. örnek: tr.wikipedia.com, www.wikipedia.com...

# top-level domain (or TLD)
.com, .org, tr gibi terimlere verilen isimdir. TLD'nin çeşitleri vardır:

- # country code top-level domain (ccTLD)
  .tr, .fr, .de, .us gibi ülke bazlı gruplma için gerekli domain bilgisini ifade eder.

- # generic top-level domains (or gTLD)
  .com, .org gibi kurumların tipini belli eden domain ifadeleridir.

# domain levels
example: mail.google.com

- 1st level domain (or first-level domain)
  
  com

- 2nd level domain (or second-Level domain)

  google

- 3rd level domain (or third-level domain)

  mail

# Ters DNS Çözümlemesi (or Reverse DNS lookup or reverse DNS resolution or rDNS)
  IP'den dns bulma işlemidir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# DNS over TLS (DoT) vs DNS over HTTPS (DoH)
Standart DNS client'lar, DoT ve DoH sunucularına istek yapamazlar. çünkü farklı protokollerdir.

standart dns'te isteğin çoğu açık gider/gelir. oysa DoT ve DoH 'ta istek tamamen şifrelenmiştir.

DoT, TCP soket bağlantısı açıp, o soketi üzerinden TLS ile dns sorgusu atar. DoH ise http protokolünden yararlanarak DNS isteği atar.

Bu iki ptotokolün amacı ISP'lerden gizlenmek değildir. çünkü ISP, dns sorgusundan sonra, gideceğimiz IP adresini zaten görecektir. buradaki amaç;

- man-in-the-middle-attack'ı önlemek
- dns sorgusu yapılıp, cevabı şifreli bir bağlantıda kullanılacak ise güvenliği sağlamış oluruz
- ISP'lerin DNS sunucularındaki yaptığı engellemeleri ortadan kaldırmak

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •