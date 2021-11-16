############################

############################
# DATABASE NOSQL TERMINOLOGY
############################

############################

# NoSQL (or Not Only SQL or nonrelational or non-SQL) vs Relational Database Management System (or RDBMS or İlişkisel veri tabanı yönetim sistemi)
ilişki olmamasından yola çıkılarak optimize edilmiş veritabanlarıdır. fakat bazı db'ler ilişki destekler. örnek: mongodb'deki "DBRef" özelliği. dolayısı ile aslında olayın çıkış noktası ilişki olmaması olsada, ilişki kurup daha fazlı özelliklerden feragat ederek optimize edilen veritabnaları da NoSQL grubunun içindedir.

Nosql veritabanları kendi içlerinde çok farklı mantıklarda çalışabilmektedirler. bazılarında bir özellik yok iken, diğerinde mevcut olabilir. işleyiş, data tutma biçimleri çok çok farklı olabiliyor.

piyasada no-sql'lerin scallable olduğu söylenir. Oysa RDBMS'lerde scallable'dır. Fakat RDBMS'in scallale olmasını zorlaştıran etkenler çok daha fazladır. en önemli sebeplerden biri, distrubuted transaction lock ve foreign key feature'leridir. Çünkü bu feature'ler tüm cluster'daki tüm node'lara aynı anda bilgi iletimi gerektirir. Dolayısı ile scallable sistemde yeni node ekleme çıkarma gibi işlemlerde, runtime sırasında binlerce farklı satırda lock olduğunu düşünürsek işimizi zorlaştığını göreceğiz. Aslında RDBMS'lerde "Horizontal Scaling (or Yatay Ölçeklendirme)" no-sql'e göre zordur (imkansız diil). "Vertical Scaling (or Diken Ölçeklendirme)" ise hem RDBMS hemde NoSQL'lerde aynı kompleklikle olduğunu söyleyebiliriz.

# nosql database tipleri

- # Document-Oriented store
Her nesneyi (id'si olan bir nesneyi) ayrı birer (tek) döküman gibi saklar. örnek sistemler: MongoDB

- # Key-Value store
Bilgiler bir anahtar ve karşılığında bir değer şeklinde saklanıyor. genelde çok fazla işlem ama ufak verileri saklamak için kullanılan sistemlerde kullanılıyor (örneğin; caching).

key-value sistemler farklı veri yapıları (hash-map gibi) da içerebilir, yada verilerin (value'ların) tipini (int, string...)'de yönetebilir.

örnek sistemler: Redis

- # Graph store
Kayıtlar, graph(structure çeşidi) ile ilişkilendirilmiş şekilde tutulmaktadır. bu ilişkiler, relational database'lerdeki ilişkilerle aynıdır fakat foreign key tarzı kavramlar yoktur.

sosyal network ağı gibi bilgilerin tutulmasında kullanılırlar. ahmet'in like'ladıkları, ahmetin dislike'ladığı, ahmetin arkadaşları...

örnek sistemler: Neo4J, Giraph

- # others (which includes "column" word)
bu gruba giren örnek sistemler: HBase, Cassandra.

burada terminoloji karmaşası söz konusudur. Bu kaynakta yorumları da dahil olmak üzere çok verimli bilgiler mevcut: (source-id: 407)

"column" terimi içeren no-sql terimleri aşağıda açıklanmıştır:

  - # column-oriented
    bu terim RDBMS dünyasında farklı amaçla kullanılan bir terimdir.

  - # column-store
    column-store bir sutun'a ait (belli range'lerdeki veya tüm) dataların fiziksel olarak ardarda kayıtlı olduğu sistemlerdir. daha doğrusu; her hücrenin hangi satıra ait olduğu bilgisinin direk olarak store'a yazılmayan sistemlerdir. bu tarz sistemlerde bir hücrenin hangi satır'a ait olduğunu farklı hesaplamalarla bulabiliriz. column-store fiziksel olarak data'yı bu şekilde kaydeder:

    ```
    (ID) 1, 2, 3, 4, 5, 6
    (First Name) Joe, Jack, Jill, James, Jamie, Justin
    (Last Name) Smith, Williams, Davis, Miller, Wilson, Taylor
    (Phone) 555-1234, 555-5668, 555-5432, NULL, 555-6527, 555-8247
    (Email) jsmith@gmail.com, jwilliams@gmail.com, NULL, jmiller@yahoo.com, NULL, jtaylor@aol.com
    ```

    Örneğin Cassandra column-store diildir. zaten resmi github sayfasında "partitioned row-store" olduğu yazar. çünkü eğer bir hücreye erişmek istiyorsak; cassandra, önce row-key'i buluyor, sonra o satırdan istediğimiz column-name'i ulup, ilgili sututun değerini buluyor.

  - # column family
    column family database'de, RDBMS'teki tablo column-family'ye denk gelmektedir. column family yapısında developer'ın sorgudan döndürmek istediği her sutun için farklı tablo yapması gerekir/beklenir. (not: "one-table-per-query pattern" buradan gelir). bu sebeple "tablo" yerine "column-family" terimi kullanılır. yani 1 tablo, bir column grubuna denk gelir. "family" suffix'i buradan gelir. family suffix'i; bir nevi multi-column, yada column-group terimlerine denk gelir.

    Bu kısmı farklı bir dille açıklamak gerekirse: user_by_name ve user_by_id tablomuz olsun. RDBMS'te bunları tek 1 taloda tutardık. Column-family yapısında ayrı ayrı tutuyoruz. İşte bu sebeple sutunları family'lere ayrılmış varsayıyoruz. terim buradan geliyor.

    Column family yapısında fiziksel olarak, her column-family data tek bir dosyada tutulur. kaynak: (source-id: 263) title: "Columnar data stores", 5th paragraph.

    dosyanın logical yapısı bu şekildedir:

    ```
                  column-1      column-2
    row-key-1     value-1       value-2


                  column-1      column-2
    row-key-2     value-3       value-4
    ```
    
    table ile column-family karşılaştırıldığında, fiziksel olarak data tutuş biçiminin farketmemesini bekleriz. fakat ikisi arasında şu farklar söz konusu:
    - kavramsal/logical farklılık
    - veriye erişimde, genelde farklı öncelikler tercih edildiği için, data'nın tutuş biçimi structural olarak farklı optimize ediliyor. örneğin column-family mantığında (genelde) data fiziksel olarak sorted oluyor. tablo ile karşılaştırıldığında, bu gibi optimizasyonlar/farklılıkar söz konusu oluyor.

    cassandra dünyasında eskiden column-family terimi kullanılırdı. fakat daha CQL'e geçiş ile "tablo" terimi kullanılmaya başlandı. fakat cassandra hala column-family bir database'dir.

  - # wide-column store (or extensible record store)
    column family'nin türevidir diyebiliriz.

    __wide-column__ sistem; her cell (hücre)'nin value'su için farklı sürüm değerleri saklar. time-series pattern'i de buradan gelir. Bu sebeple; __wide-column__ store'lar  "__three-dimensional structure__ (bazen "__multi-dimensional__" denir)" olarak, document-based store'lar ise "two-dimensional structure" olarak nitelendirilirler. çünkü document-store'da her column'un farklı sürümlerini saklayamayız (json formatını düşünürsek bunu hayal edebiliriz).

    ```
                  column-1   column-1@01-01-2020       column-2
    row-key-1     value-1    value-2                   value-3


                  column-1   column-1@02-02-2022       column-2
    row-key-2     value-4    value-5                   value-6
    ```

Yukarıdaki no-sql tiplerine bakıldığında, aslında, herhangi bir db ile kaydettiğimiz ve çektiğimiz bilgiyi diğeri ile de yapabiliriz. örneğin; Document tabanlı sistemdeki kaydı, Key-Value ile de tutabiliriz. fakat seçimimizi datamızı nasıl çekeceğimize (nerelere sorgu atıp çekmek isteyeceğimize), nasıl kaydedeceğimize göre karar vermeliyiz.

örnek:

ilişkisel veritabanı gibi data kaydedecek isek, fakat ilişkiye ihtiyacımız yok ise, Document tabanlı database bu iş için uygun. çünkü ilerdeki zamanlarda her data sutunu'na göre sorgu atmak isteyebiliriz. oysa bu data'yı Key-Value database'de saklıyor olsaydık, sorgularımızda büyük problem yaşardık. çünkü Key-Value database value'da ne olduğu ile pek ilgilenmez. Key-Value genelde value'su tek bir değer olan datalar için uygundur. bu şekilde daha hızlı okuma ve yazma yapabiliriz. Hatta bu sebepten genelde RAM üzerinde çalışırlar.
