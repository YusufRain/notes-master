############################

############################
# AGILE SCRUM
############################

############################

# Systems development life cycle (or SDLC or application development life-cycle)

genel bir terimdir. aşağıdakilerin kümesini kapsar.

# Agile (Çevik) proje yönetimi

bir proje (yazılım projesi olmak zorunda diil) yönetim (işleyiş) biçimidir.  Gereksinimleri açıkça belirli olmayan, değişime açık, karmaşık projelerin yönetimi için uygulanmaktadır. agile manifestosu şu şekildedir:

türkçe:
```
Bizler daha iyi yazılım geliştirme yollarını

uygulayarak ve başkalarının da uygulamasına yardım ederek ortaya çıkartıyoruz.

Bu çalışmaların sonucunda:

Süreçler ve araçlardan ziyade bireyler ve etkileşimlere

Kapsamlı dökümantasyondan ziyade çalışan yazılıma

Sözleşme pazarlıklarından ziyade müşteri ile işbirliğine

Bir plana bağlı kalmaktan ziyade değişime karşılık vermeye

değer vermeye kanaat getirdik.

Özetle, sol taraftaki maddelerin değerini kabul etmekle birlikte,

sağ taraftaki maddeleri daha değerli bulmaktayız.
```

ingilizce:
```
 We are uncovering better ways of developing

software by doing it and helping others do it.

Through this work we have come to value:

Individuals and interactions over processes and tools

Working software over comprehensive documentation

Customer collaboration over contract negotiation

Responding to change over following a plan

That is, while there is value in the items on

the right, we value the items on the left more.
```

# Scrum
kelime anlamı: itişip kakışma, saldırı

Agile'ın bir türevidir. Sprint (kelime anlamı: sürat koşusu), backlog (kelime anlamı: rezerv, birikim), daily meeting gibi kavramlar bunun içindedir. Sadece yazılım projelerinde uygulanmak için tasarlanmıştır. Scrum'ın türkçe kelime anlamı itişip kakışma anlamına gelir fakat özel türkçe karşılığı yoktur.

Scrum temel olarak agile'a göre, sürecin nasıl işleyeceği ile ilgili detaylandırılmış şeklidir. Agile ise işin felsefik/üst seyiveyi/soyut kısmıdır. örneklerden gidersek:
- agile'da yüzyüze iletişim olması gerektiği belirtiltilir; scrumda ise, müşteri ile birlikte çalışmak çok verimli olduğu belirtilir.
- Agile'da iterasyonlarlar bahsedilir, scrumda sprint ile detaylandırılmıştır.
- agile'da visualizing önemli denir, scrumda, scrum board'dan bahsedilir.

sprint içerisinde analistler her zaman yeni sprint belirmeden önce analizleri hazırlamış ve teknik ekibe yollamış olmalı. teknik ekip retro-toplantısı ile yeni sprint puanları verilmeden önceki arada bunları okumalıdır.

Scrum'ın yıllar içinde klavuzu güncellenmektedir. akışta ve ifadelerde değişiklikler yapılmaktadır. 2020 sürümü buradadır:

(source-id: 81)

(source-id: 82)

Diğer sürümlerdeki değişikler burada: (source-id: 83)

# Scrum çalışmalarında geçen kavramlar

# scrum'daki kişiler

- __scrum master__: sadece scrum sürecini ve teknik olmayan konularda yaşanan engelleri çözmek için ilgili kişidir. bu kişi; taskların içeriği değilde, scrum süreçinin işlediğinden emin olmalıdır.

- __project manager (proje yöneticisi)__: bazı agile sistemlerde bu role varken, bu rolde bir kişi scrum'da yoktur. çünkü srum'da takım self-organized'dır.

- __team leader (or takım lideri)__: klasik proje yönetimlerinde bu vardır. scrumda böyle bir role yoktur. çünkü team self organized'dir.

- __scrum team__: product owner, scrum master ve development'lardan oluşan kümedir.

- __development team__: 2020 yılı sürümünde sadece "__developers__" olarak adlandırılır. sprint içerisinmdeki taskları yapacvak olan kişilerdir. alt kümelere ayrılamazlar. eğer ayrılması gerekiyor ise, farklı/bağımsız bir scrum takımı kurulmalıdır. analistler ve testçiler dahil ayrı grup olarak görülmemelidir.

  3'ten az veya 9'dan fazla kişi olması tavsiye edilmez.

- __product owner (or PO or ürün sahibi)__: tüm kararlardan/araştırmalardan sonra en son ürün için yapılacak taskları onaylayan, üründe hangi geliştirmeleri yapılacağını söylemeye yetkili kişi. PO sürekli müşteri ile temas halindedir. müşterinin isteklerini anlar ve backlog'daki tasklara business value'ları set eder. backlog'daki tasklardaki istekleri yazar/detaylandırır. teknik bilgisi olan kişi değildir. sadece business odaklıdır.

  PO tüm işlerini development team'e de yaptırabilir. fakat sorumlulukları ona aittir.

  sprint iptalini sadece product owner verebilir. fakat stackeholder'lar, scrum master ve geliştirici takımda bu kararı yönlendirmede etkili olabilir. sprint iptal edilirse, yarım kalan tüm tasklar gözden geçirilir ve yeni sprint'e başlamak için gerekli toplantılar ayarlanır.

  sprint sonlarındaki DEMO'lar product owner'a yapılır.

# scrum events
retropektif, grooming gibi toplantıların tümünü kapsayan kümedir. her toplantı mutlaka önceden belirlenmiş kısıtlı sürelerde (time-boxed) yapılmalıdır.

- __sprint__: 1 aydan uzun olmamalıdır.

- __sprint planning (or Sprint Planlama)__: bu toplantıda:

  - hangi taskların başlayacak olan sprint'e alınacağı belirlenir.
  - eğer bilinmiyorsa yüzeysel olarak o işlerin teknik anlamda nasıl/ne şekilde yapılacağı belirlenir.
  - her task için yapılmamış ise "Defination of done" belirlenir.

  Bu sorular sprint planning'de cevaplandırılmalıdır:

  - Bu Sprint Neden Değerlidir? (bu 2020-November tarihli scrum sürümünde geldi)
  - Bu Sprint’te ne tamamlanabilir?
  - Seçilen iş nasıl yapılacak?

  1 aylık sprint için 8 saat ile sınırlıdır. daha kısa sprint'ler için daha kısa olmalıdır.

- __günlük toplantılar (or daily scrum meeting)__: her gün yapılmalıdır. sadece; dün ne yaptım, bugün ne yapacam ve engelim varmı konuşulmalıdır. toplam 15 dk olmalıdır.

- __sprint review (or sprint değerlendirme)__: bu toplantı herkesin katılabileceği bir toplantıdır. sprint sonunda yapılır. biten her taskın demo'su yapılır. sprint içerisinde hangi engellerle karışalıldı, nasıl çözüldü konuları tartışılır. biten tasklar ile ilgili sorular varsa onlar cevaplanır. scrum team ve stackeholder'lar genel görüşlerini bildirir. stackeholder'lar; scrum team'i dışında kalan ve ürün hakkında yorum, öneri yapabilen tüm kişilerdir.

  bu toplantının scrum terminologisinde resmi bir yeri yoktur.

  1 aylık sprint için max 4 saat olmalıdır. daha kısa sprinmt'ler için daha kısa olmalıdır. 

- __retrospective (retrospektif) toplantısı__: retrospektif kelime anlamı: 'dünden bugüne', 'geriye dönük'. her sprint sonu takımın ve scrum master'ın toplanarak yağtığı başarısızlıkları ve başarıları konuştukları toplantı. 3 saat veya daha az olmalıdır. burada hem teknik hemde scrum süreci hakkındaki değerlendirmeler yapılır. fakat ideal olan scrum/agile süreci hakkında konuşmaktır. fakat teknik konulara da girilmez diye kural yok. süreç ne kadar başarılı gitsede her süreçte geliştirme amaçlı şeyler konuşulmalıdır. aksi durumda iyiye gidiş olmaz. bu toplantıda herkes şu 3 başlıkta maddeleri toplar:
  - neleri daha iyi yapabilirdik?
  - neleri iyi yaptık?
  - neleri kötü yaptık?

  bu toplantıya sadece 'scrum team'in katılması beklenir.

  'Sprint Değerlendirme'den sonra ve 'Sprint Planlama'dan önce yapılır.

- __Product Backlog refinement__: 

  refinement kelime anlamı: iyileştirme.

  bu toplantı __Grooming toplantıları__ olarak kullanılıyor fakat bu yanlış. "grooming" kelime anlamı: prepare or train (someone) for a particular purpose or activity.

  Product Backlog refinement, resmi olarak scrum doc'unda yazıyor fakat "scrum events" bağlığı altında diil.

  bu toplantıda backlog'daki herhangi bir item için süre ve detay verilir.

  süre olarak tüm ekibin sprint zamanının %10'unu aşmamalı.

# scrum artifacts (or scrum eserleri)
- __increment__: tüm projenin hayatı boyunca hedefe ulaşmak için yapılan her katkıya denir. somut bir adım olması şarttır. __Done (or bitti)__ olmayan iş increment olamaz. increment, kağıt üzerinde sayılabilen bir değer diildir.

- __Product Backlog (or ürün iş listesi)__: Product Owner tarafından yönetilen sprint dışındaki tüm task'lar kümesidir.

- __sprint backlog (or spint iş listesi)__: sprint içerisindeki tüm iş listesi kümesidir.

# scrum için diğer terimler

- __Planning poker (or Scrum poker)__: ekipçe her taska süre verirken uygulanan bir tekniktir. herkes kapalı kağıtları ile her taska süre verir.

  resmi scrum doc'unda geçen bir terim diildir.

- __çapraz fonksiyonlu takım (or cross-functional team)__: farklı becerilerde/alanlardan geliştiriciler olabilir ve hepsi birlikte sprint'in amacına ulaşabilmesi için yeterli olmalıdırlar. "cross functional" terimimi farklı becerilerde insanlar olması gerektiğini belirtmektedir. çünkü scrum takımı dışarıya bağımlı olmamalıdır. sprint'im amacı için gerekli tüm yetkinliğe sahip olmalıdır.

  çaprazdan kasıt şu diildir: development team içindeki her kişi, diğer herkesin işini yapabilecek yetkinlikte olmalıdır.

  resmi scrum doc'unda geçen bir terimdir.

- __business Value__: iş önceliği. product owner'ın karar verdiği değer. product owner için iş ne kadar önemli.

  resmi scrum doc'unda geçen bir terim diildir.

- __Story points__: estimation ve işin zorluk (komplekslik) değeri çarpımıdır. alabildiği değerler: Fibonacci-like değerleridir: 0, 0.5, 1, 2, 3, 5, 8, 13, 20, 40, 100. Daha yüksek değer verilmemelidir. eğer daha yüksek değer vermek gerekiyor ise; sub-tasklara bölünmelidir. bug veya teknik elemanların açtığı task'larda story point olmalıdır. sonuçta product owner onaylıyor ve bunlar sprint'te çalışılıyor.

  resmi scrum doc'unda geçen bir terim diildir.

- __story point vs hour__: bir işin ne kadar süreceği net olaraka belli olmaz. bu sebeple karşılaştırma tekniği ile ölçüm yapılması alternatif bir çözüm olarak sunulmuştur. story point'i karılaştırma değeri olarak  alırız. her sprint bir önceki sprint'te alınan toplam story point ile karşılaştırılarak her taska story point atanır. birçok agile master'ı projelerde saat yerine, story point ile değerlendirildiğinde, bir süre sonra story point'lerin saate göre daha doğruyu yansıttığı gözlemlenmiştir.

- __Estimation__: işin bir kişi tarafından bitirilmesi süresidir. resmi scrum doc'unda geçen bir terim diildir.

- __Burn-down Chart__: resmi scrum doc'unda geçen bir terim diildir. spring içerisinde kalan işleri gösteren grafiktir.

- __Burn-up Chart__: resmi scrum doc'unda geçen bir terim diildir. sprint içerisinde biten işleri gösteren grafiktir.

- __Definition of Done (or DoD)__: resmi scrum doc'unda geçen bir terimdir. bir taskın kapanması için gerekli tüm definitionlar. burada o taskın production'a çıkması için gerekli tüm bilgiler olmalıdır.

- __spike__: spike kelime anlamı: sivri uç. bazı taskların çıktısı olmaz ve ya olması için önce araştırma gerektirir. bu araştırma tasklarına verilen genel isimdir.

# The Chicken and the Pig
It is a business fable. It was also mentioned in the official "Scrum Guide" but it has been removed.

The chicked and pig decided to open a restaurant. They both should serve a food to customer as partners. the chicked had to serve his eggs and the pig had to serve meat which will be part of itself. In the bottom line; The Chicken is involved, but the Pig commits. This situation is simulated on scrum framework as: the Development Team, Product Owners & Scrum Masters are considered as people who are committed to the project while stakeholders, customers and executive management are considered as involved but not committed to the project.

# Kanban

Agile'ın bir türevidir. Sadece yazılım projelerinde uygulanmak için tasarlanmıştır.

Kaban, scrum ile karşılaştırıldığında;

kambanda; toplantılar ve belirli aktiviteler bulunmamaktadır. Fakat yaşanan darboğaz durumlara göre aksiyonlar alınmaktadır. Her projede, süreç kendini geliştirmektedir.

kambanda; Yazılımcıların estimation vermesi opsiyoneldir.

kambanda; Agile'daki gibi roller (scrummaster gibi) belirlenmemiştir.

Kambanda; iterasyon opsiyoneldir. Agile'da sprint (iterasyona denk geliyor) zorunludur.

# Extreme programming (or XP)
Agile'ın bir türevidir. Sadece yazılım projelerinde uygulanmak için tasarlanmıştır. Bu metodda kaliteli kod ön plandadır. Gerektiğinde ufak/büyük refactoring'ler yapılmalıdır. Merkezde sürekli çalıştırılabilir kod olmalı ve ufak ufak parçalar halinde geliştirmeler yapılıp bu koda eklenmelidir. Testler kodda önce yazılmalıdır. Basit tasarım ve kodlama standardı gibi kavramlara önem verilir.

# WaterFall Model (or Şelale modeli)
Kod baştan sona analize göre tasarlanır ve müşteriye teslim edilir. Günümüz şartlarına pek uygun değildir. Zira tüm yazılım detaylandırılması önceden uzun bir zaman ve maliyet alması bir yana, analiz sürecinde de gelişmeler meydana gelmektedir. Bunları o süreçte yakalama ve ona göre analiz yapmak neredeyse imkansızdır. Aynı zamanda müşteri bazen ne istediğini tam olarak bilemez. Geliştirme sürecine müşteri katılır ve zaman ile gelişimini inceler ise (diğer modellerde olduğu gibi), ürün teslimi sonunda müşterinin beklenmedik şeylerle karşılaşması zorlaşır.

Tüm proje boyunca bazen proje önmeli süreçlere bölünebiliyor (scrum'daki sprint sonu gibi). bu noktalara waterfall modelinde; milestone (kilometre taşı, dönüm noktası) diye isimlendiriliyor.

# Lean software development (or yalın yazılım geliştirme)
Lean ürün geliştirme süreci ilk olarak Toyota firmasının üretim bölümünde kullanılan kültüre verilen isimdir. Daha sonra Mary Poppendieck ve Tom Poppendieck 2003'te yazdıkları "lean software development" kitabında bu konu yazılıma uyarlandı.

Lean prensipleri genel olarak optimize çalışmaya dayanan, sadec egerekli işi yapmaya odaklı (kullanılmayan özellikler içermeyen) üretim sistemlerine dayanır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •