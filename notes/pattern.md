
############################

############################
# PATTERN
############################

############################

# GOF (or Gang of Four)
1994'te "Design Patterns: Elements of Reusable Object-Oriented Software" isimli kitap Erich Gamma, Richard Helm, Ralph Johnson ve John Vlissides tarafından yazılmıştır. bu kitapta birçok objcet orianted pattern anlatılmaktadır. kitap birçok yazılımcı tarafından bilinir. bu kitabın yazarlarına "Gang of Four" takma adı verilmiştir. işlenen bazı konular:
- genel object orianted felsefesi
- Structural patterns (adapter, bridge, composite, decorator, facade, proxy...)
- Creational patterns (abstract factory, builder, factory method, prototype, singleton...)
- Behavioral patterns (observer...)
- c++ üzerinden örnekler

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# pattern types
- Creational Pattern

  bir veya birden fazla objenin init edilmesi ile ilgili konuları ele alır.

- structural pattern

  Sınıfların birbirleri arasındaki ilişki yapılarını ve birbirlerini nasıl kullandıkları ile ilgili konuları ele alır.

- Behavioral pattern

  Objelerin birbiri ile olan ilişkilerinden ziyade, birbirleri arasında haberleşmlerini veya birbirlerini ne zaman kullanmaları gerektiği (rolleri/görevleri) konuları ele alır.

- Concurrency pattern

  Multi-thread uygulamalar için geliştirilen patternlerdir.

- Architectural pattern

  Daha çok üst seviyeli (yani; sınıf diil, yazılımlar veya modüller seviyesinde) olan patternlerdir. 

- Database pattern

- Anti-Pattern

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Pattern list by types

Aşağıdaki tüm liste, bu dökümanda sıra ile anlatılmıştır. Farklı dökümanda anlatılmış olan pattern'lerin yanına link eklenmiştir.

Aşağıdaki listede bazı ana başlıklar direk olarak pattern olarak sayılmayabilirler. Fakat dizayn yaklaşımlarıdır. Bu dizayn yaklaşımlarını implemente etmeye çalışırsak mutlaka bazı patternlerden yararlanıyor olacağız.

- Creational pattern
  - Prototype pattern
  - Singleton pattern
  - Builder pattern
  - Factory pattern + Factory method pattern + abstract factory pattern (or Factory of Factory pattern)
  - [file"java_bean.md" - title:"DI (or Dependency Injection)"](https://github.com/ysf0/notes/blob/master/notes/java_bean.md#di-or-dependency-injection)
  - object pool pattern ("Thread pool pattern" başlığının içinde anlatılıyor.)
  - Lazy Initialization Pattern
- Structural pattern
  - Private class data pattern
  - Facade pattern
  - Proxy Pattern (or vekil deseni)
  - Delegation Pattern
  - Adapter pattern
  - Composite pattern
  - Bridge pattern
  - Decorator pattern
- Behavioral pattern
  - command pattern
  - Iterator pattern
  - Null object pattern
  - Observer pattern (or Gözlemci deseni)
  - State pattern vs strategy pattern vs Template method pattern
  - Specification pattern
  - Memento pattern
  - Chain Of Responsibility
- Concurrency patterns
    - Thread pool pattern (Aynı zamanda "Creational pattern" altındadır. Çünkü "object pool pattern"'in biri türevidir.)
- Architectural patterns
  - çoğunlukla microservis tabanlı sistemde uygulanabilecek pattern'ler
    - Decomposition patterns: "Decomposition by domain capabilities" vs "Decomposition by business capabilities"
    - Sidecar pattern (or sidekick pattern)
    - database per service pattern
    - Shared database
    - microservice pattern (or mikroservis deseni) vs Monolithic pattern (or monolitik desen)
    - SOA (or Service-oriented architecture)
      - Enterprise application integration
      - service bus (or enterprise service bus or ESB)
    - Externalized configuration pattern
    - api gateway pattern
    - api composition pattern
    - Circuit Braker (or devre kesici)
    - CQS (or Command Query Separation) vs CQRS (or Command Query Responsibility Segregation)
    - two-phase commit (or 2PC)
    - saga pattern
    - Transactional outbox pattern
      - Polling publisher pattern
      - Transactional Log Tailing
    - event sourcing pattern
    - Service registry pattern
    - Client-side Service Discovery Pattern vs Server-side Service Discovery Pattern
    - Self Registration pattern
    - 3rd Party Registration
    - Blue-Green Deployment Pattern
    - Microservice chassis
    - Service Template
    - Self-contained service
    - [file:"pattern_mvc.md" - title:"micro-frontends (or micro frontends)"](https://github.com/ysf0/notes/blob/master/notes/web_custom_elements.md#micro-frontends-or-micro-frontends)
  - [file:"pattern_ddd.md" - title:"Domain-driven design (or DDD) vs data-centric design (or database-centric design or data-driven design)"](https://github.com/ysf0/notes/blob/master/notes/pattern_ddd.md#domain-driven-design-or-ddd-vs-data-centric-design-or-database-centric-design-or-data-driven-design)
  - MVC vs MVP vs MVVM vs Redux vs Flux vs Presentation Model (or Application Model) [file:"pattern_mvc.md"](https://github.com/ysf0/notes/blob/master/notes/pattern_mvc.md)
  - Data Access Object (or DAO) pattern (Bu pattern "Structural" grubu altında da sayılabilir)
  - Repository pattern
  - Front Controller pattern
  - Backend For Frontend
  - multitier architecture (or n-tier architecture) vs multilayer architecture (or n-layer architecture)
- Database pattern
  - [file:"database_cassandra.md" - title:"one table per query pattern (or one-table-per-query pattern) vs query-first approach (or query-driven modelling)"](https://github.com/ysf0/notes/blob/master/notes/database_cassandra.md#one-table-per-query-pattern-or-one-table-per-query-pattern-vs-query-first-approach-or-query-driven-modelling)
  - [file:"database_cassandra.md" - title:"time series pattern"](https://github.com/ysf0/notes/blob/master/notes/database_cassandra.md#time-series-pattern)
  - [file:"database_cassandra.md" - title:"wide partition pattern (or wide row pattern)"](https://github.com/ysf0/notes/blob/master/notes/database_cassandra.md#wide-partition-pattern-or-wide-row-pattern)
- Uncategorized
  - [file:"javascript_react.md" - title:"Higher-Order Components (or HOC)"](https://github.com/ysf0/notes/blob/master/notes/javascript_react.md#higher-order-components-or-hoc)
- Anti-Pattern
  - Don't Use Exceptions For Flow Control
  - Blob (or Monster Class or god bean or god object or god class or Winnebago)
    - God Method (or god function)
  - Dependency hell
  - Spaghetti code
  - Reinventing the square wheel (or Reinventing the wheel)
  - Tester-driven development (or bug-driven development) (Anlatılmasına gerek duyulmadı)
  - Programming by permutation (or programming by accident or shotgunning) (Anlatılmasına gerek duyulmadı)
  - Copy and paste programming (or Copy-and-paste programming or Cut-And-Paste Programming or Clipboard Coding or Software Cloning or Software Propagation) (Anlatılmasına gerek duyulmadı)
  - law of the instrument (or law of the hammer or Maslow's hammer or golden hammer or Old Yeller or Head-in-the sand)
  - Softcoding vs Hardcoding
  - magic string
  - Lava Flow (or Dead Code)
  - boat anchor (or boatanchor)
  - Error hiding
  - Busy waiting
  - Overengineering (or over-engineering or over-kill) (Anlatılmasına gerek duyulmadı)
  - Calling super (or call super)
  - Cargo cult programming
  - vendor lock-in (or proprietary lock-in or customer lock-in)
  - Functional Decomposition (or No Object-Oriented AntiPattern or No OO)
  - Don't repeat yourself (or DRY or do not repeat yourself)
  - Silver Bullet
  - micromanagement (Anlatılmasına gerek duyulmadı)

# Other Architectural Patterns
"Microservices patterns" kitabının yazarı Chris Richardson, kendisinin katkıda bulunduğu microservices.io/patterns sayfası altında "patterns" olarak aşağıdakileri ayrı ayrı birer pattern olarak listelemiştir (source-id: 461). Aşağıdaki konuları kişisel olarak bildiğim için bu dökümanda anlatma gereği duymadım.

- Multiple service instances per host - deploy multiple service instances on a single host
- Service instance per host - deploy each service instance in its own host
- Service instance per VM - deploy each service instance in its VM
- Service instance per Container - deploy each service instance in its container
- Serverless deployment - deploy a service using serverless deployment platform
- Service deployment platform - deploy services using a highly automated deployment platform that provides a service abstraction (kubernetes, openshift...)
- Service per team - Each team of organization manages one or more services independently.
- Access Token - security konusu
- Health Check API - each servis opens a health endpoint. An independed servis checks periodically all services.
- Application metrics - merkezi bir serviste, tüm servislerin mtriklerinin toplanması yöntemidir. 2 çeşittir: ya tüm servisler buraya bilgiyi kendileri yollar, yada merkezi metrik servisi tüm diğer servislerden periyodik olarak bu bilgileri bir endpoint aracılığı ile okur/toplar. 
- Exception tracking - All services reports all exceptions to a centralized exception tracking service that aggregates and tracks exceptions and notifies developers.
- Distributed tracing - zipkin gibi tool'lar ile isteklerin yönünü ve harcadığı zamanı görebilmek için merkezi bir monitoring tool'u kullanma yöntemidir. urada her servis her http request alıp attığın merkezi service (örneğin zipkin'e) haber verir.
- Log deployments and changes - deployment yapılan herşeyi detaylı şekilde loglandığı yapılardır. Burada sadece deployment'ın ne olduğu diil, aynı zamanda öncesi ve sonrası metric'lerin ortalamaları gibi bilgiler de olmalıdır. Bu şekilde her deployment2ın etkileri ve sorunları gözlemlenebilmiş olur.
- Audit logging - user activity'nin database'e loglandığı ve takip edilmesinin sağlanmasıdır. audit log'unda temel olarak user'ın activity'leri ve bu activity'lerin tetikleriği activitiy'ler takip edilir. diğer log'lar genel log mekanizmalarından takip edilmelidir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# prototype pattern
Prototip deseni belirli nesnelerin kopyasını oluşturarak daha sonra yapılacak işlemler için, oluşturulan kopyanın kullanılmasını sağlayan yaratımsal desendir.

```java
User user2 = user1.clone();
user2.setName("mehmet");
```

Örneğin biyolojik bir hücre kendini iki parçaya bölüyor ve aynı hücreden iki tane oluyor.

Bazı durumlarda new ile obje yaratmak, her değeri tek tek set edileceğinden çok maliyetli olabiliyor. Bu gibi durumlarda tercih edilebilir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# singleton pattern
bir objeyi, tüm uygulamada aynı instance'ı kullandırma yöntemidir.

Bu sık kullanıldığında veya dependency-injection yerine kullanıldığında anti-pattern olabilmektedir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# builder pattern

```java
User myUser = User.UserBuilder("ahmet", "agaogli")

                  .age(30)

                  .phone("1234567")

                  .address("Fake address 1234")

                  .build();
```

avantajlar:
- okunaklılığı arttırıyor. bir constuctor'da 10 tane parametre olursa, hangi parametre nedir anlaşılmaz.
- constuctor'lara tüm parametreleri vermek istemeyiz. null göndermek yerine bu yapı tercih edilir. 10 adet alabilen bir constuctor için tüm kombinasyonları hazırlamak maliyetli olacaktır ve kod kalabalığı yaratacaktır.

# Chaining Methods (or method chaining or Cascading or named parameter idiom)
bir metodun kendi instance'ını veya bir sonraki çağıracağımız metodun instance'ını döndürmesi durumudur. böylece zincirleme metodları üstüste çağırabiliriz. "chaining" sadece builder pattern'inden kullanılmaz.
- QueryDSL ve builder pattern'ler bunu kullanır.

# Fluent API
fluent kelime anlamı: akıcı.

metod chaining yaparak kompleks operasyonların yapılabilmesini sağlayan API'lerdir. 
- QueryDSL Fluent API kullanır.
- Builder pattern sadece kendi nesnesini döndüren setter'lar sunar. Özel bir API sunmasına gerek olmadığı için Fluent API kullanır diyemeyiz.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# factory pattern (or simple factory pattern)
tek bir metod ile; new MyClass(param1, param2...) gibi bir yapıya ihtiyaç duymadan yeni sınfıları türetme yöntemidir. örneğin; sadece getMyClass(param1, param2...) yazıp aynı ihtiyacı giderebiliriz.

Bu pattern'de bir factory sınıfı vardır ve bu sınıfın içinde factory metodları vardır. factory metodlar dışında public metodlar olmamalıdır.

# Factory Method pattern
"factory pattern" ile aynıdır. tek farkı abstract bir sınıf döndürmesidir.

```java
interface Interviewer
{
    askQuestions();
}

class Developer implements Interviewer
{
    askQuestions()
    {
        print('hey developer!');
    }
}

class Manager implements Interviewer
{
    askQuestions()
    {
        print('hey Manager!');
    }
}

abstract class HiringManager
{
    // Factory method
    abstract Interviewer makeInterviewer();

    doInterview()
    {
        Interviewer interviewer = this.makeInterviewer();
        interviewer.askQuestions();
    }
}
```

Now "HiringManager" should be implemented like "DevelopmentManager", "MarketingManager"...

# abstract factory pattern (or Factory of Factory pattern)
2 farklı implementasyon/kullanım mevcut:

1- Burada factory dönen metod bize factory tarafından sunuluyor:

```java
public interface Shape {
   void draw();
}

public class RoundedRectangle implements Shape {
   @Override
   public void draw() {
      System.out.println("Inside RoundedRectangle::draw() method.");
   }
}

public class RoundedSquare implements Shape {
   @Override
   public void draw() {
      System.out.println("Inside RoundedSquare::draw() method.");
   }
}

public class Rectangle implements Shape {
   @Override
   public void draw() {
      System.out.println("Inside Rectangle::draw() method.");
   }
}

public abstract class AbstractFactory {
   abstract Shape getShape(String shapeType) ;
}

public class ShapeFactory extends AbstractFactory {
   @Override
   public Shape getShape(String shapeType){
      if(shapeType.equalsIgnoreCase("RECTANGLE")){
         return new Rectangle();
      }else if(shapeType.equalsIgnoreCase("SQUARE")){
         return new Square();
      }	 
      return null;
   }
}

public class RoundedShapeFactory extends AbstractFactory {
   @Override
   public Shape getShape(String shapeType){    
      if(shapeType.equalsIgnoreCase("RECTANGLE")){
         return new RoundedRectangle();
      }else if(shapeType.equalsIgnoreCase("SQUARE")){
         return new RoundedSquare();
      }	 
      return null;
   }
}

public class FactoryProducer {
   public static AbstractFactory getFactory(boolean rounded){   
      if(rounded){
         return new RoundedShapeFactory();
      }else{
         return new ShapeFactory();
      }
   }
}
```

2- İlişkili Factory metodlarını aynı class içerisinde bulundururuz. örnek kapımız ve kapıyı montaj edecek uzman (door fitting expert) olsun. bu kisinin ilişkili olması gerekli.

```java
interface DoorFactory
{
    public Door makeDoor();
    public DoorFittingExpert makeFittingExpert();
}

class WoodenDoorFactory implements DoorFactory
{
    public Door makeDoor()
    {
        return new WoodenDoor();
    }

    public DoorFittingExpert makeFittingExpert()
    {
        return new Wooden_Door_Fitting_Expert();
    }
}

class IronDoorFactory implements DoorFactory
{
    public Door makeDoor()
    {
        return new IronDoor();
    }

    public DoorFittingExpert makeFittingExpert()
    {
        return new Iron_Door_Fitting_Expert();
    }
}
```

# static factory method vs constructor

örnek: 

```java
new BigInteger("3")
```

vs

```java
BigInteger.valueOf("3")
```

- static'lerin avantajları:

  - constuctor'da metod ismi kullanmaz. sınıf ismi kullanır. bu sebeple constructor'ı çağırdığımızda yapılacak işin amacı için dökümantasyona bakmak şarttır. koddan direk anlaşılmaz.

  - static metod bize zaten varolan instance'ı dönebilir. oysa consctuctor'ın yeni instance yaratması şarttır.

  - bazı diller constructor overload'a izin vermiyor. eğer SL4J, SLF.net gibi tüm cross-language facada hazırlanacaksa static factory kullanmak gerekebilir.

  - static factory metod'lar aldığı parametreye göre (uygunluğu varsa) farklı bir sınıfta dönebilir. bunu constructor'da yapamayız.

- static'lerin dezavantajları:

  - OOP felsefesine aykırı

  - constructor'u olmayan sınıflar'dan subclass yaratılamaz. bu sebeple sadece static metod yaratıp, constructor'ları yazmaktan kaçamayız. fakat hem static hem constructor olunca, API'mizi kullanan developer'lara çok fazla seçenek sunmuz oluruz. 
  
    constructor'larımızı protected yaratabiliriz. fakatbu sefer başka paketlerden kendimiz çağıramayız. bu dezavantajı gidermek için, sub-class yaratmak yerine "composition over inheritance" yapabiliriz. yada constructor'ları çok basit tutarız ve kullandırtmak istemiyorsak bunu DOC'lara not düşeriz.

genelde kullanılan static factory metod isimlendirmeleri:

- from: örnek Date.from(instant); isntant birçok formatta olabilir. from bize istediğimiz sınıf yada subclass'a cast edecek.

- of: Set\<Rank> faceCards = EnumSet.of(JACK, QUEEN, KING); birçok parametre alarak bize uygun olan classı döner.

- valueOf: from ile aynı.

- getInstance veya instance: Calendar.getInstance(); getInstance bazen ekstra paramere isteyebilir.

- create or newInstance: Array.newInstance(classObject, arrayLen); yeni bir instance döndürür. ayarları prametre olarak alır.

Yukarıdaki isimlendirmeler zorunlu diildir. fakat genelde bu isimlendirme kullanılır. örneğin; Calendar.getInstance() aynı instance'yi döndürmüyor. singleton pattern'de getInstance metodu aynı instance'yi döndürür. fakat calendar buna uymamış. calendar bu metodu şu amaçla böyle isimlendirmişler: önce default Locale'i bul ve bana instance'yi oluştur.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Lazy Initialization Pattern
Dependency injection framework'leri bunu kolaylaştırsada manuel de (aspect gibi gelişmiş teknolojiler kullanmadan da) uygulanabilir bir pattern'dir.

Manuel uygulamak istediğimizde:
- bir class'ın constructor'ında, class'a ait private field'larımızı init etmeyiz.
- class'ımızdan bir metod çağrıldığında, ilgili metodda kullanılan ve init olmamış bir field var ise önce onları init edebiliriz.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Private class data pattern
bir java sınıfında sınıf değişkenleri tamamen dışarıya kapatılmak istenebilir. bunun için tüm değişkenleri private yapıp setter'larını kaldırmamız gerekecek.
Fakat buda yetmez bu dataların o sınıftan dahi değiştirilmemesini isteyebiliriz. Bunun için tüm data'yı yine sınıf değişkeni olarak; bütün dataları içeren tek bir sınıf yaratabiliriz. Bu oluturduğumuz yeni sınıf consctuctor haricinde setter'a sahip olmamalıdır.

```java
class Math{
  private int kose1;
  private int kose2;

  alanHesapla(){....}
  
  //getters
}
```

Bu yapılması daha iyi olacaktır:

```java
class MathData{
  private int kose1;
  private int kose2;

  MathData(kose1, kose2){...}

  //getters
}

class Math{
  private MathData data;
  alanHesapla(){....} // can call: data.getKose1();
  .....
}
```

Artık Math sınıfımızda data.setKose1(); çağıramayız. Oysa ilk Math sınıfımızda kose1=3; yapabilirdik.

Yani dışarıya kapattığımız yetmezmiş gibi; ilgili sınıfımızda da önlem almış oluyoruz.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Facade pattern
facade kelime anlamı: cephe, Bir yapının ön tarafta bulunan bölümü

birden fazla sınıfın işlevini birleştirip çağırmak durumunda kalabiliyoruz. örneğin; getComputer() işlemi kendi içerisinde %90 getKlavye(); getMotherBoard(); gibi işlemleri yapması gerekiyor. Bunları tek tek çağırmak yerine facada sınıfı yaratıp, sadece facada sınıfından yararlanma metodolojisidir.

örnek: Simple Logging Facade for Java (SLF4J). SLF bir interface ile tüm implementasyonların değil, birçok log kütüphanelerinin kullanılabilmesi için arayüz sunmaktadır. burada SLF4J kütüphanesinin init() metodunu çağırdığımızda:
- A log kütüphanesi için 2 adet metod
- B log kütüphanesi için ise 1 metod çağrıyor olabilir.

Patternin tanımında belirttiğimiz gibi; bir metod (init metodu) diğer tüm ihtiyaçlarımızı görecek metodları çağırmaktadır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Proxy Pattern (or vekil deseni)

- CommandExecuter --> Interface olsun
- CommandExecuterImpl --> türemiş sınfımız olsun
- CommandExecuterProxy --> türemiş sınfımız olsun

- CommandExecuterProxy sınıfının içinde CommandExecuterImpl otomatik initialize olsun.
- CommandExecuterProxy sınıfının runCommand(String commandStr) metodunu çağırdığımızda bizim için CommandExecuterImpl metodunun runCommand'ını çağırır. fakat ek olarak önce komutu koşturabilicek yetki olup olmadığı kontrol edilir. Bunun gibi birçok kontrol yapılabilir. Benzer şekile otomatik CommandExecuterImpl initialize edilirken ona gerekli parametreleri geçer. 

Proxy pattern'i CommandExecuterImpl 'ın kullanımına aracılık ediyor ve bize kolaylaştırıyor. Spesifik bir örnek verirsek; CommandExecuterProxy yerine CommandExecuterUser yada CommandExecuterAdmin isimli 2 proxy yapabiliriz. Bu proxy'ler CommandExecuterImpl'ı initialize ederken parametrelerini biliyor olucak ve komutu çalıştırmadan doğru yetkilerle kontrol edeceklerdir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Delegation Pattern (or Delegator Pattern)
bazı kaynaklarda "__proxy chains__" olarakta geçmektedir.

proxy pattern'e çok benzer.

Bazen kalıtım yerine, composition tercih edilir. işte bu durumda, super class'ların metodlarını, sınıfımızın içinde oluşturduğumuz instance üzerinden çağırırız. bu gibi durumlarda Delegator pattern kullanılabilir.

proxy ile farkı şudur: Delegator pattern, referans olduğu sınıfın metodlarını aynen çağırırken, proxy pattern arada loglama, kontrol gibi birçok işlev görebilmesi söz konusudur.

kaynak: (source-id: 152)

```java
class MyClass {

  Delegator d; // Delegator birden fazla olabilir.

  method1(){
    d.method1();
  }

  method2(String a){
    d.method2(String a);
  }
}
```

Eğer yukarıdakini yapmasaydık şunu yapacaktık:

```java
class MyClass extends Delegator {

}
```

Bazı diller multiple inheritance desteklemiyor (örnek java). Bu gibi durumlarda bu pattern kullanılabilir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# adapter pattern

adapter is a bridge between two incompatible interfaces.

örnek;

```
- Reader         (Interface)
  - PpdfReader   (Implementation)
  - DocReader    (Implementation)
  - PhotoReader  (Implementation)
```

Yukarıda Photo, pdf ve doc'tan çok farklı bir media dosyası. örneğin; Reader interfacesi getAllAsText(); metoduna sahip. Fakat bunu photoda nasıl implemente edeceğiz?

Öncelikle getAllText yerine fotonun meta-data bilgilerini text olarak döndüreceğimizi kabul ederek ilerleyelim.

Foto'dan meta-data'ları döndüren sınıfımız olsun:

```
PhotoMetaDataReader   (Interface)
 - getPhotoDate()     (Method)
 - getPhotoId()       (Method)
```
 
Yeni bir adapter sınıfı yaratırız:

```java
class PhotoReaderAdapter {

    PhotoMetaDataReader p;

    getAllMetaData(){

       return p.getPhotoDate() + p.getPhotoId();
    }
}
```

Artık PhotoReaderAdapter'ı PhotoReader içinde kullanabiliriz.

Böylece PhotoReader ile PhotoMetaDataReader'ı PhotoReaderAdapter ile birbirine bağlamış olduk.
Burada adaptee rolünde olan PhotoMetaDataReader interface'sidir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# composite pattern

- örnek;

Data clasımız olsun. Folder ve File implementasyonumuz olsun. File sadece tek bir "Data" Objesi barındıracaktır. Oysa Folder, bir Data Listesi barındıracaktır. Bu "Data" listesi içinde file yada folder olabilir.

Şimdi main class'ımızda ;

```java
Folder root = new Folder();
root.add(new Folder());
root.add(anotherSubFolder);
```

yukarıdaki kod akışında içiçe dizinler yaratabiliyoruz. İşte bu tarz bileşik data tutulup ağaç yapısı hazırlabilicek tasarımlara "composite pattern" denir. 

- örnek;

```java
class Employee {

  String name;
  List<Employee> subEmployees;
}
```

YUkarıdaki obje ile tüm şirketin hiyerarşisi bile yaratılabilir. en üstte genel müdür employee'si olacaktır.

- örnek;

AritmeticExpression sınıfı. Bu sınıf büyük bir denklemi barındırıyor. List\<Operand\> barındırıyor. Her operan yine kendi içinde operand listesi barındırıyor.

1 # ( 2 + ( 3 + 4 ) ) denklemimizi örnek alabilir. bir Operand 1,# ve X'i barındırıyor olacak. X operand'ı ise içinde; 2, + ve Y operandını bulunduracak. Y operandı ise; 3, + 4 ü barındırıyor olucak gibi...

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# bridge pattern

Satış raporlarının çıktısı alan kodlarımız olsun:

```
- Rapor         (Interface)
  - Internet    (Interface)
    - PDF       (Implementation)
    - Doc       (Implementation)
  - Magaza      (Interface)
    - PDF       (Implementation)
    - Doc       (Implementation)
```

Bridge pattern'i diyorki; ilgili sınıftan soyut olan bir yapıyı ayırın. Bizim sistemde soyut olan kavram "format" (pdf, doc) olmasıdır. PDF ve doc'u soyutlaştırmamız gerek.

Sonuçta bu olması isteniyor:

```
- Rapor         (Interface)
  - Internet    (Implementation)
  - Magaza      (Implementation)

- Format      (Interface)
  - PDF       (Implementation)
  - Doc       (Implementation)
```

Artık yeni rapor yaratmak istediğimizde yaratılacak rapor nesnesine Format sınıfını parametre geçeceğiz.

Köprü rolünde olan sınıf Format'tır. FormatBridge diye adlandırabilirdik.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Decorator pattern

```java
interface Cloud_Computer_Service
{
  getCost();
  getDescription();
}

class Simple_Cloud_Computer_Service implements Cloud_Computer_Service
{
  getCost(){
      return 10;
  }

  getDescription(){
      return 'Simple Cloud Computer Service';
  }
}

class VIP_Cloud_Computer_Service implements Cloud_Computer_Service
{
  private Cloud_Computer_Service service;

  getCost(){
      return service + 5; // VIP computers has 5 GB more ram. the cost increased.
  }

  getDescription(){
      return 'VIP Cloud Computer Service (+5 more GB RAM)';
  }
}
```

Yukarıda, VIP bilgisayarlar, simple'lara göre her zaman 5 $ fazla olacak. Bu dinamik olarak şekilde ayarlanmış. Bu inherit edilerekte yapılabilirdi, fakat inheritance yerine composition tercih etmiş olduk.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# command pattern
Yapılacak bir işin detaylarını, bu işi tetikleyen taraftan soyutlamak için kullanılan bir pattern'dir. örnek:

```java
class RemoveThingsFromDB implements Runnable {
    public void run() {
        System.out.println("Removing things from DB...");
        // add here many code
    }
}
 
class EditThingsOnDB implements Runnable {
    public void run() {
        System.out.println("Editing values on DB...");
        // add here many code
    }
}

public class MainApp {
    public static void main(String[] args) {
        Thread thread = new Thread(new RemoveThingsFromDB());
        thread.start();
         
        Thread thread1 = new Thread(new EditThingsOnDB());
        thread1.start();
    }
```

Yukarıdaki kod örneğinde; main thread'in diğer thread'lerde yapılan işlemlerden hiç bilgisi yok. Sadece ne yapmak istediğini söylüyor ve işi iligli sınıfın ilgili metodu hallediyor. Böylece işleri biribirinden soyutlamış oluyoruz.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Iterator Pattern 
for loop yerine iterator objesi ile dönmemizi sağlayan pattern'dir.

Iteratorler'in avantajı şudur:
- uygulamamızda tüm koleksiyon nesnelerimiz aynı iterator interfacesinden türemiş sınıfları kullanır. bu şekilde bize gelen koleksiyon tipini düşünmeden o koleksiyonda işlem yapabiliriz (döngü kurma gibi).
- koleksiyon sınıfımızdaki iterator objesi bize filtreli dönüşte yapabilir. örnek:

Radyo dinleme cihazımız olsun.

```java
Kanal {
   Frekans;
   Language;
}

class KanalListesi {

   kanalEkle(Kanal);
   kanalSil(Kanal);
   
   iterator(Language);
}
```

Yukarıdaki KanalListesi koleksiyonumuzun döndüreceği iterator'ın next(); metodu bize aldığı Language parametresine göre filtrelenip dönecektir. Zaten iterator'ın next() metodunun implementasyonunu KanalListesi sınıfını yazan yazılımcı yazacaktır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Null Object Pattern
Bir AbstractUser class'ımız olsun. Bundan 2 tane implementasyon olsun. 1 tanesi normal koşullarda yapacağımızı User implementasyonumuz, diğeri ise NullUser implementasyonumuz. NullUser'ın metodları hiç null pointer döndürmesin. örnek: NullUser.getName(); --> "User not available" dönsün. gibi. 

Gerçek hattan kullanım örnekleri:
# 1
Bir ekran koruyucu yazılımımız olsun. Bu yazılım ekranda toplar gösterecek olsun. Toplar için efect'lerimiz olsun. Efectler biz dizinden yükleniyor olsun. dizinde hiçbir dosya olmadığında NullEffect sınıfımız devreye girecek ve default olarak ekranın efektsiz çalışmasını sağlayacaktır.

# 2
logger impelementasyonlarımız olsun:
  - db-logger --> gelen her logu db'ye kaydeder
  - file-logger --> gelen her logu dosyaya kaydeder
  - system-out-logger --> gelen her logu ekrana basar
  - null-logger --> gelen her logu ignore eder (/dev/null gibi)

# 3
https://github.com/j-easy/easy-random/wiki/excluding-fields Bu sayfada da yazdığı gibi SkipRandomizer sınıfı Null Object Pattern'i implemente eder.

org.jeasy.random.randomizers.misc.SkipRandomizer sınıfının içeriğine bakarsak şunu görürüz:

```java
public class SkipRandomizer implements Randomizer<Object> {

    @Override
    public Object getRandomValue() {
        return null;
    }
}
```

Randomizer'den türemiş diğer bazı sınıfılar bu listede: https://github.com/j-easy/easy-random/tree/0426dcd8b2df555d276a16513ab92d79f99f8de5/easy-random-core/src/main/java/org/jeasy/random/randomizers/misc

Bu listeden bazıları:
- BooleanRandomizer.java --> Random boolean döndürüyor
- ConstantRandomizer.java --> Sabit döndürüyor
- UUIDRandomizer.java --> random UUID döndürüyor
- SkipRandomizer.java --> hiçbir şey döndürmüyor. Null olmasını istediğimiz objeleri SkipRandomizer aracılığı ile setliyoruz.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Observer pattern (or Gözlemci deseni)

Observer tasarım deseni; birbirleri ile bire çok (yani bir nesnenin içinde başka bir nesnenin listesinin bulunması olarak düşünebiliriz) ilişki olan nesneler arasında olay bazlı bir etkileşim olduğu durumları düzenler. Örnek senaryolar:

- Bir e-ticaret sitesinde bir üründeki stok değişiminde o ürünü takip eden üyelere haber verilmesi" 

- facebookta bir paylaşıma yapılan yorumlar için paylaşımcıya ve diğer yorumculara bildirim gitmesi

İlk senaryodan gidelim;

- "Observer (or consumer)" yapısına denk gelen sınıf "Üye" sınıfı olsun. 

- "Observable (or Subject or object)" yapısına denk gelen sınıf "Ürün" sınıfı olsun. 

ürün içinde, üyelerin listesi olsun.

Urun.updateFiyat(int newFiyat) metodunun içinde tum uye listesine email ile fiyatın değiştiğini haber veren işlem yapılmalıdır.

Observer tasarım desenei, Open-Closed Prensibine çok güzel bir örnektir. Yeni observer class'ları yarattığımızda, subject'i değiştirmeye gerek kalmıyordu.

# publish-subscribe vs Observer
publish-subscribe sistemlerde arada event bus (or sistemde adlandırabileceğimiz herhangi bir mekanizma: broker, message broker, event bus) vardır. oysa observer sistemde event bus yoktur. Observer'da, subject direk Observer'ların metodlarını çağırır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# state pattern vs strategy pattern
iki patern de birbirine çok benzerdir. fakat temel farklılık hangi nesnelerin hangi bilgiyi içerdiği ile ilgilidir.

iki patternde de ayrı nesneler yaratılıp, akışın her duruma göre davranışlarını bu yarattığımız nesnelerde bulundurabiliriz. Bu şekilde if/else gibi durumlardan kısmen kurtulmuş oluruz.

Aşağıdaki koda bakıldığında da tahmin edileceği gibi; state pattern için nesnenin NE olduğu önemlidir. Strategy için nesnenin NASIL çalıştığı önemlidir.

state pattern için örnek:

```java
Context context = new Context();

// StartState and StopState implements a common interface.

StartState startState = new StartState();
startState.doAction(context);

StopState stopState = new StopState();
stopState.doAction(context);
```

strategy pattern için örnek:

```java
Context context = new Context(new OperationAdd());		
ontext.executeStrategy(10, 5);

context = new Context(new OperationSubstract());		
context.executeStrategy(10, 5);
```

# Template method pattern
template kelime anlamı: şablon

Spring'deki restTemplate gibi *template sınıfıları bu patterni baz almaktadır.

Bir süper class'ta bir iş akışını belirleriz. Bu iş akışı birçok farklı implementasyon için çalışır. Eğer isterse implementasyonlar bu akışı değiştirebilir. Fakat büyük resimde ne olacağı bellidir. böylece kod tekrarından kurtulmuş oluruz.

Template implementasyonlarına Concrete Class denir. Concrete kelime anlamı: somut, belirgin, elle tutulur.

# Template method pattern vs ( state pattern vs strategy pattern )
Template pattern'de compile time'da class seçimi söz konusudur. Oysa state pattern ve strategy pattern runtime'da class seçimi söz konusudur.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Specification pattern

```java
Spec vip_specification = new VIP_Product_Spec();
Product product = productRepository.getUsersBasket();
boolean isValidForThisUser = vip_specification.isSatisfied(product);
```

Yukarıdaki gibi spesifikasyonlar yaratıp, business logic'lerimizi tek bir noktadan karar verebilmemizi sağlar.

__Composite Specification__ ise birden fazla isSatisfied metodunu birlikte kullanabilmemiz (or, and...) üzerine kurulu bir patterndir.

Spesification objelerimizi repository'den data çekerken filtreleme amaçlı da kullanabiliriz. örnek:

```java
Spec vip_specification = new VIP_Product_Spec();
productRepository.filterBySpec(vip_specification);
```

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Memento Pattern
Bir calss'ın her durumunu saklamak için kullanacağımız bir pattern'dir. Örneğin text editor geliştiriyoruz. Undo, redo yaptığımızda, hem cursor'un pozisyonu hemde text'in kendisi değişmektedir.

- Memento: Saklamak istediğimiz nesnemizin tamamını ya da bir kısmını tutan sınıftır.
- CareTaker: Memento'ların (saklanan nesnelerin) referansının tutulduğu sınıftır.
- Originator: Değerleri tutulacak olan ve önceki değerlerine geri dönebilen sınıftır.

```java
TextMementoCollection coll = new TextMementoCollection(); // TextMementoCollection --> CareTaker

TextEditor editor = new TextEditor(); // TextEditor --> Originator
editor.type('111');
editor.type('222');

TextMemento saved1 = editor.save(); // TextMemento --> Memento
coll.add(saved1);

editor.type('333');

editor.restore(saved); 
// or 
// editor.restore(coll.get(0)); 
```

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Chain Of Responsibility
java servlet'ler buna en iyi örnektir. zincir gibi kimlk doğrulama, loggining-, compression gibi birçok işlem zincirleme yapılır ve herkesin sorumluluğu farklıdır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Thread pool pattern
İlgili uygulamada thread sayısının merkezi bir modülden limitlenerek sırası ile çalıştırılma patternidir. Merkezi modülümüz isterse thread'leri önceden işletim sisteminde hazır tutabilir, yada işi biten thread'leri kapatmadan, sıradaki thread'e direk teslim edebilir. Fakat bu detaylar pattern'de opsiyoneldir.

# Object pool pattern
Thread pool pattern'in atasıdır.

JVM'in en sık kullanılan Integerları önceden hazır tutması gibi birçok pooling yöntemi, 'Object pool pattern'e güzel bir örnek olabilir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Decomposition patterns: "Decomposition by domain capabilities" vs "Decomposition by business capabilities"
"Decomposition by domain capabilities" bazı kaynaklarda "__Decomposition by subdomain capabilities__" olarakta geçmektedir.

Hybrit olan bir yazılımı, parçalara bölme yöntemleridir. Örneğin bu patternlerde birer decomposition pattern'dir:
- Sidecar pattern
- Service per team
- Self-contained Service

Bir hybirt uygulamayı mikro parçalara bölmek için ya domain bazlı yada business işleyişine göre böleriz.

- # Decomposition by domain capabilities

DDD'de bahsedilen patternler, hep bu patern'i uygulamamız

Aşağıdaki listede * ile başlayanlar bizim domainimiz. Altında da bu domainde sağladığımız hizmetler mevcut. domain yada altında yazan hizmetlerimiz ayrı microserviser olabilir veya olmayabilir. Fakat 1 yıldız'ın tümü bir grup olarak bağımsız çalışabilecek şekilde tasarlanmalıdır.

```
* IT
- network team
- software developer team
- mobile-device provider team
- laptop provider team

* Administrative Management
- Human resource
- table/chair provider
```

- # Decomposition by business capabilities

```
* provider
- mobile-device provider team
- laptop provider team
- table/chair provider

* IT
- network team
- software developer team

* Administrative Management
- Human resource
```

Not: Diğer bir örnekler: şunlar olabilir:
- Her birimin kendi 'Insan Kaynakları' mı olacak (Decomposition by domain capabilities), yoksa 1 insan kaynakları tüm birimlere eleman mı sağlayacak (Decomposition by business capabilities).
- Her birimin kendi yazılım ekibi mi olcak yoksa tek bir yazılım birimi, tüm diğer birimlere mi hizmet verecek?
- Tek bir devops ekibimi tüm projelern deployment'larını yapacak? yoksa her projenin kendi devops ekibi mi olcak?

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Sidecar pattern (or sidekick pattern)
Bu bir çeşit decomposition pattern'dir. Çünkü birçok işlevi asıl uygulamamızdan ayrıştırmış oluruz.

Bir uygulama yanında sidecar dediğimiz farklı bir uygulamayı bulundurur. Sidecar, asıl uygulamamızın yapması gerekn bazı işlevleri onun için yerine getirecektir. Bunun avantajını direk örnek üzerinden inceleyelim:

Spring Cloud Eureka (discovery server) client'leri java için yazılmış durumda. Peki cloud'da nodejs microservisimiz nasıl eureka'ya bağlanacak. işte böyle bir durumda sidecar pattern aklımıza gelir.

- Yeni bir microservis yaratırız.
- spring-cloud-netflix-sidecar bağımlılığını ekleriz.
- sidecar projesinin config dosyasına da nodejs'in healt-check url'sini veririr.
- nodejs uygulamamızın bir portundan sürekli olarak healtcheck (spring cloud doc'unda standardı yazıyor) status OK cevabı döneriz.

Proje ayağa kaldırıldığında sidecar sürekli olarak healcheck'e request atacak ve cevap aldığı sürece asıl eureka server'ımıza register olacak. sidecar eurekaya register olması için nodejs'e aracılık etmiş oluyor.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# database per service pattern
her microservisin kendi database'i olması mimarisidir. temel olarak şu tarz alt çözümlere gidilebilir:

  - Private-tables-per-service – each service owns a set of tables that must only be accessed by that service
  - Schema-per-service – each service has a database schema that’s private to that service
  - Database-server-per-service – each service has it’s own database server.

tablolar arası ilişkilerin nasıl tutulacağı konusu için çözümler aşağıdadır. aşağıdaki listedeki her 2 durum içinde ilişkiler db tarafında tutulduğubda, kolonlarda foreign key olamayacak.

  - 1- ilişki tablosu sadece 1 veritabanında olacak.
  - 2- ilişki tablosu ilgili tüm servislerde tutulacak.

Yukarıda 1'inci durumda bir servis eğer ilişki tablosunu içermiyor ise; her defasında ilişki tablosunu kullanan microservice istek yapacaktır. bu da network yavaşlığına sebep olacaktır.

2inci maddede ise, ilişkiler iligli servislerin veritabanlarında olacağı için 2 dezavantaj var:
  - dublicate veriler oluyor (ilişkiler birçok veritabanında saklanıyor)
  - update ve add işlemleri tüm veritabanlarında güncelleniyor. bu yavaşlık sebebi.

avantajı ise:
  - 1inci çözümde olduğu gibi her ilişki tablosuna erişim gerektiğinde diğer servislere istek yapılmıyor. direk db'den okunuyor.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Shared database
database per service pattern'in tersidir. Brden fazla servisin ortak DB kullanmasıdır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# microservice pattern (or mikroservis deseni) vs Monolithic pattern (or monolitik desen)

microservice'lerde bağımlılıkların neredeyse hiç olmaması (veya minimum olması) gerekiyor. bu da ortak kod bloklarının microservisler arasında hiç olmamasını gerektiriyor. genelde kullanılan ortak kod bloklarını gruplandırarak incelersek;

- database model
  
  her microservis kendi db'sine gitmesi gerekir. örneğin user ve adres modellerimiz olsun. her servis kendi db'sinde verileri ve ilişkileri tutmalıdır. ilikşikler arası bağlantı kurmak gerekirse, diğer servise runtime sırasında sorgu atması gerekecektir.

  bu konu "database per service pattern" başlığında daha detaylı anlatılıyor.

- utility kodları

  bir borsa uygulaması düşünelim. para çevrimi aşaması neredeyse her servis tarafından kullnılır. klasik mimarilerde olsa common sınıfa utility olarak yazılır ve herkes bu kod parçasına depend olur. oysa microservislerde 'money-converter' isimli bir servisimiz olur ve herkes runtime sırasında bu servise sorgu atarak para çevrimi yapması beklenir.

- 3party dependencies

  tabiki apache-common-utils gibi servisleri her projemizde kullanabiliriz.

- config strings

  config'ler farklı bir config micro-servisinden okunmalıdır.

- common maven configs + common maven dependencies + common codes

  runtime sırasında olmayan konfigler pom.xml gibi config dosyalarında tanımlanır. bunları standart tutmak istiyorsak, template'ler haline getirip, bu template'leri hızlıca kopyalanabilir şekilde ayarlayıp, her projeye ayrı ayrı atabiliriz. bu konu "Microservice chassis" patterni başlığında anlatılıyor.

  bu son madde için bazı developer'lar common dependency yapılabilir olduğunu düşünüyor. bu konuda farklı görüşler var. burada görüş ayrılığı olmasının sebebi şu: business logic olan kısımlarda bağımlılık olmazsa genelde sorun olmayacağı düşünülür. çünkü business logic olmayan kodlar teknoloji için gerekli utility sınıflarıdır. aynı apache-commons-util'de olduğu gibi. dolayısı ile bizde kendi şirketimiz içinde bir utility yazmış sayılıyoruz.

  shared lib olabilmesi için örnek: (source-id: 153) "Exceptions" başlığı

  Bazı developer'lar ise kod dublikasyonu olsa bile common lib yapılmaması görüşünde. kaynak: (source-id: 154) "Do you share anything?" başlığı.

  Bu konu burada da cevaplanmış: (source-id: 155)

  Fakat genel olarak; teknik ortak kodların olmasında pek sakınca görülmezken, business logic olan kodların kesinlikle ortak olmaması öneriliyor.

# avantajlar

- bir projede bir kütüphane değiştirildiğinde diğer kütüphanelerin zarar görmediğinden emin olabilir. örneğin; springmvc kullanırken aynı projede, spring'in  bir modülünü ekleyeceğiz. yeni kütüphaneyi eklerken springmvc dependency'leri ile çakışmıyor görünse de, her zaman beklendiği gibi olmayabiliyor. bu durumun önüne geçilmiş oluyor. docker gibi her proje/yazılım birbirinden bağımsız olmuş oluyor.

- her proje farklı dillerde yazılabiliyor.

- projelerde aynı kütüphanenin farklı sürümleri kullanılabiliyor

- projeler çok ufak ve fazla parçalara bölünmüş olacağından; deploymentlar daha ufak parçalar şeklinde ve daha az riskli şekilde yapılabilecektir. yani; tüm paketi birden çıkmak zorunda kalmıyoruz. continuous delivery'yi kolaylaştırıyor.

- projeler çok ufak ve fazla parçalara bölünmüş olacağından; doğası gereği modülerliği arttırmaya yöneltiyor.

- bir modülde sorun çıkınca tüm sistem çökmemiş oluyor. sadece o modül kullanılamıyor.

- update işlemleri için tüm sistemi durdurmaya gerek yok.

- localde development için tüm sistemi açmaya gerek yok.

- operasyonler işlerde startup süreçleri hızlanır.

- devre dışı bırakılacak modüller için sistemi kapatmaya gerek yok. sadece o servisleri kapatmak yeterli.

# dezavantajlar

- her projenin farklı databasesi olması, özel sorgular ve atomic işlemler için zorluk çıkarabiliyor (transactional işlemlerdeki zorluklar)

- Complex communication:
  - network ağı sürekli haberleşme ihityacı arttırığında yoruluyor
  - hangi business akışında, hangi servisin nereye gittiğini bulmak ve bir servisteki değişikliğin, diğer hangi serviste etki yaratabileceği ancak e2e testlerinde görülebiliyor.

- mikroservis, monolitike göre çok sonradan çıkan bir pattern. dolayısı ile şu anda piyasada olan birçok uygulama monolitik. bunları mikroservis yapısına geçirmek çok zorlu bir süreç gerektirebiliyor.

- Infrastructure requirements. tüm servisleri (özellikle farklı DC'ler var ise) manuel yönetmek çok zor. bunun için çoğu proje kubernetes/openshfit/istio gibi çözümlere para vermek veya depend olmak zorunda kalıyor. Aynı zamanda bunları yönetecek bilgi sahibi birilerine ihtiyaç duyuluyor.

- daha tecrübeli yazılımcı ihtiyacı doğuruyor:
  - dependency olmaması gerektiğinden, tecrübeli yazılımcılar olmazsa, dublicate kodların sonucunda code smell'ler oluşabiliyor.
  - genel olarak bakıldığında; daha fazla infrastructure requirement bilgisi gerektiriyor. en basitinden lokal ortamda bağımsız development yapmak için bile kuberntes kaldırmak gerekebiliyor.

- iyi optimize edilmezse, bazı durumlarda sistem requirement'leri (RAM gibi...) daha fazla harcayabiliyor (özellikle ufak projelerde dezavantaj yaratıyor).

# cloud native architecture
bir mimaridir. "native", doğal anlamına gelir. 'cloud native'den kasıt; cloud yapısına en uygun olandır.

spring'in cloud native'i karşılayan modülleri vardır. "Spring cloud netflix" ismi ile geçer çünkü tüm implementasyonlar netfix'in spring'den bağımsız geliştirdiği uygulamaları kullanabilmek için yapılmıştır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# SOA (or Service-oriented architecture) vs web service
SOA kabaca bir mimarisel paradigmadır. Bu paradigma; birden fazla/farklı web servisini entegre ederek (veya gruplayarak) tek bir sistem gibi işlemesini sağlamaya dayanır. Her servis direk veritabanına erişirse, birçok servis aynı anda aynı veritabanında işlem yapmaya kalkar. Fakat bunun yerine, servis tabanlı bir yaklaşım ile her business işleten servis kendi işini arkaplanda yapmalı ve veritabanındaki değişikliği yapmalıdır.

Bu açıdan bakıldığında, biraz microservis mantığına benzer bir yapı vardır. Fakat SOA'nın temelinde microservisler gibi bağımsız uygulama geliştirme, scallable gibi fikirler yatmaz. SOA, biraz daha enterprise ve yüksek seviyede bir yakşalım biçimidir. kaynak: (source-id: 463) 1st Footnote, last sentence.

web servis ise, web teknolojileri kullanarak, dışarıya API açarak, hizmet veren servislere verilen genel bir terimdir. web servis bir yaklaşım diildir, bir teknolojidir.

SOA paradigmasını birçok teknoloji ile gerçekleyebilir (implemente edebiliriz):
- web servisler
- CORBA
- REST
- gRPC
- EJB
- SOAP

# Enterprise application integration (or EAI)
monolitik uygulamalar'ın birbirleri ile haberleşebilmesi için gerekli entegrasyonlardır. Tam olarak neleri kavradığı belli olmayan (resmi şekilde yazılı olmayan) fakat piyasada sıkça kullanılan bir terimdir.

EAI pattern'lerini implemente etmemize yarayan bazı framework'ler:
- Spring Integration
- Apache Camel
- Red Hat Fuse
- Mule ESB
- Guarana DSL 

Gregor Hohpe ve Bobby Woolf, 'Enterprise application integration' için gerekli 65 pattern'i "Enterprise Integration Patterns" isimli kitapta anlatmıştır. Bu kitaptaki patternleri burada bulabiliriz: (source-id: 156) enterpriseintegrationpatterns.com'a apache camel'ın resmi sitesinden referans verilmiştir. kaynak: (source-id: 157) 1st sentence.

Bu kitaptaki bazı patternler:
- File Transfer
- Shared Database
- Remote Procedure Invocation
- Point-to-Point Channel
- Publish-Subscribe Channel
- Message Bus
- Synchronous (Web Services)

# service bus (or enterprise service bus or ESB)
ESB birçok monolitik uygulamanın birbiri ile haberleşebilmesi ve entegrasyonunu sağlamak için merkezde olan bir component'tir. ESB'ler ek olarak, mesaj formatını değiştirme, filtreleme, yönlendirme, bazı business logic içerme gibi özellikleri de vardır.

Bu şekil EBS'yi güzel şekilde açıklamaktadır: (source-id: 462)

"Enterprise application integration" içinde önerilen mimarilerden biridir.

ESB'nin dezavantajları:
- Adding additional step/call in the service flow and add a slight delay to the response time. 
- Additional cost to setup ESB servers, VPNs, and other infrastructure
- All services are routed through a single place; it will have a single point of failure. 
- Not having too much options to scale up a single service in ESB infrastructure. 

# ESB vs SOA vs microservice vs Monolithic
tam olarak birbirlerine alternatif olmasalarda, karşılaştırma yapılabilir. Fakat içiçe de kullanılmaktadırlar. Örnekler;
- ESB kullanıp her servisimizi micro seviyede yapabiliriz. Fakat tam olarak microservis yapamayacağız, çünkü ortak/merkezi olanbir service bus kullanmış olacaklar.
- Zaten ESB, SOA olan bir ortam için tasarlanmıştır.
- Sadece SOA kullanıp, ESB olmayan bir ortamda servislerimiz çok ufak ve scallable yaptıkça, microservis ortamını hazırlamış olamktayız.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Externalized configuration
config server pattern'idir. servislerin tek bir servisten tüm configleri çekebilmesidir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# api gateway
bir sunucu yazılımdır. edge server gibi çalışır. özellikleri:

- Farklı protokoller arası dönüşüm. örnek: SOAP->REST, TCP->SOAP
- darboğaz (throttling) yönetimi. her user'dan gelen istekleri sınırlandırmak. yani; belli zamana dilimlerinde, bazı isteklere limit getirebilmek.
- kimlik doğrulama
- api versiyonlama
- api grubu devreye alım/kapatma/açma
- Loglama, izleme, bildirim
- Servis birleştirme (service composition). birden fazla iç servisi tek bir servis olarak dışarıya açabilme.
- caching

piyasadaki bazı api gateway'ler: tyk, Kong

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# API Composition
api gateway uygulamaları bunu bizim için yapabilir. edge proxy diye adlandırılan bu sunucular api'lerimizi dışarıdan erişime açarken tek bir endpoint'ten açar.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# CQS (or Command Query Separation) vs CQRS (or Command Query Responsibility Segregation)
Segregation kelime anlamı: ayırma

ikisi çok benzerdir fakat farklı patternlerdir.

2 pattern de metodları iki farklı gruba alınmasını önerir:

- Commands: Objenin veya sistemin durumunu değiştirir. Void dönüş yapar.

  'command' yerine modifier veya 'mutator' terimleri de kullanılır. kaynak: (source-id: 158)

- Queries: Sadece sonucu geriye döner herhangi bir objenin veya sistemin durumunu değiştirmez.

Bir command metodu (eğer dönüş yapmasının yan etkisi olmayacaksa), dönüş yapabilir. fakat bu pek tercih edilen bir yöntem olmamalıdır.

CQS daha çok mikro seviyede, CQRS  ise makro seviyede sistemi ele alan pattern'lerdir. CQS büyük resimden bakıldığında sistemdeki herhangi bir fonksiyonun ya query yada read işlemi yapmasını önerir. kaynak: (source-id: 158)

oysa CQRS (büyük resimden bakarak) bunların da ayrılmasını önerir:
- fonksiyonlara yollanan ve response alınan modeller/objeler
- microservislerin sadece query veya command olarak ayrılması
- sadece fonksiyon seviyesinde değil, sınıflar bazında ayrılması (yani; bir sınıftaki tüm metodlar ya query yapacak yada command yapacak)

kaynak: (source-id: 160) Luke Puplett'in cevabında açıklama mevcut. Mesajın altında Greg Young cevap yazmış fakat Greg web projelerinde kullanımı hakkında yorum düşmüş.

CQRS ilk "Greg Young" tarafından ortaya atılmıştır.

## query ve command'lar için DB modellerinin ayrılması
DB modelleri ayrılmaz ise classic CRUD işlemleri yapan sistemin metodlarını ayırmış gibi oluruz. Bu durumda sadece command servislerimizi scale ettiğimizi düşünelim. DB server instance sayımız aynı olacağı için bunun faydasını görmeyeceğiz. Çünkü darboğaz olarak DB karşımıza çıkacaktır. Fakat eğer command ve query'lerimiz ayrı modeller olursa, ayrı DB'lere kaydedebiliriz. Hepsine ayrı çözüm uygulayabiliriz. örneğin; sadece query microservislerimizi scale ettikten sonra, sadece query yapacağımız DB instnce'larınıda scale edebiliriz. Oysa tersi durumda; tüm sistemi scale etmemiz gerekecekti.

CQRS bir sistemde kesinlikle query ve read modelleri ayrı olacak diye bir kesinlik yotkur. kaynak: (source-id: 161) 9uncu paragraf.

## View Models (or Projections or Query Models)
Query fonksiyonlarımız data okur (veritabanından). bu data'lar yansıtılmak için kullanılan datalar olduğu için, CQRS pattern'i dökümanlarında bu şekilde isimlendirilmiştir.

Bu patternin faydaları:
- CQRS yapıldığında "event sourcing"'de kolaylaşacaktır. çünkü sadece "Commands" servisimize gelen istekleri loglamamız yeterli olacaktır.
- Bazı servislerimiz sadece database'ye read yetkisi olduğundan o servislerimizde güvenliği arttırmış oluruz. (secure by design)
- Sistemimizi micro servislere bölüştürmemiz kolaylaşacaktır.
- Read only query metodlarımız, yazma işlemi yapan metodlarla aynı sınıflarda olmayacağı için büyük DAO'lar karşımıza çıkmayacak. Çünkü command modeli ile view model'leri aynı olmak zorunda diil.
- Database'yi değiştiren servislerin hangileri olduğunu bildiğimizden hata tespiti kolaylaşabilir.
- read ve write yapan DB'ler aynı olmak zorunda diil. Zira write yapıldıktan sonra async bir thread'de de farklı bir DB'ye raporlama için (query servislerinin yararlanması için) kayıt atılabilir. Dolayısı ile; query ve command'lerin kullandıkları db'ler farklı. bununda sonucunda; farklı db çözümleri sunabiliriz. örneğin; kayıt command'ler kayıt atarken mongdo kullanıp, raporları okurken oracle kullanmalarını performance açısından verimlilik sağlayacak ise bu şekilde kullanılmasına olanak sağlar.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# two-phase commit (or 2PC)

database/network sistemlerinde transaction işlemi yapacak yazılım karşıya önce "prepare for commit" mesajı iletir. eğer OK dönüşünü alırsa "commit" mesajını, her servise ayrı ayrı gönderir. Bu yaklaşım genelde uzakta birden fazla birbirinden bağımsız veritabanlarında işlem çalıştırılacağı zaman yapılır. böylece atomic işlem daha garantiye alınmış olunur.

2PC'de yazılım, diğer servise yada veritabanı servisine "prepare for commit" mesjaını atması ve dönüşünü alması fazına __voting phase__ denir.

Klasik sistemlerde ise direk olarak ilk işlemde "commit" mesajını gönderilir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# saga pattern
türkçe kelime anlamı: destan

Saga pattern önyüzde de kullanılan bir pattern'dir. örnek redux-saga; saga'larımızın yönetimini sağlar.

2PC'ye alternatiftir. 2PC senkron bir çözümdür. saga asenkron ve reaktiftir. saga'nın asenkron olabilmesi için, tüm servislerin ortak bir event bus'a bağlı olmaları gerekir. bu şekilde saga, global yürüyen transaction sürecinden haberdar olabileceklerdir. kaynak: (source-id: 162) "saga pattern" başlığındaki ilk paragraf.

2PC'deki gibi birçok dağıtık servisimiz olsun. birçok servisimiz kendi bağımsız veritabanına kayıt/güncelleme işlemi yapıyor olsun. ortak bir event bus ile birbirleri arasında haberleşebiliyor olsun. son kullanıcı global bir transaction işlemini tetiklesin. transaction'ın ilk adımı (yani ilk event) event bus'a yollansın. bu event'i ilgili servis kendine çekecek ve işletmeye başlayacak. ilgili event'ler tamamlandıkça diğer event'lerde çağrılacak.

peki hata olursa ne olacak? işlemler geri alınacak. işte 2PC ile fark burada. saga'da işlemin sonucu, isteği yapan service, isteği gerçekleştiren servis tarafından döndürülür. isteği yapan servis, business logic'e göre tekrar aynı servise geri alma işlemini yollayacaktır. 2PC'de geri alma işlemi veritabanına hiç yazmamaktır, oysa saga'da geri alma işlemi güncelleme yada (event sourcing kullanılıyor ise) yeni bir event state'i oluşturmak olacaktır. kaynak: (source-id: 162) "Two-phase commit (2pc) pattern" balığında ikinci resimde görülmektedir ki, bir işlem abort edildiğinde, ilgili servise verilerin veritabanına kayıt edilmemesi isteği yollanmakta. Diğer kaynak: (source-id: 164) "All transactions in the sequence complete successfully or compensating transactions are ran to amend a partial execution." yani; compensating (telafi) transaction'ları yine sequence içerisinde tanımlanır.

Saga ile işletilen transaction büyük resme bakıldığında "__long-lived transaction (or LLT or long-running transaction)__" olarak kabul edilir. çünkü logic olarak bakıldığında atomik birçok işlem başka servislere yaptırılır. Bu durumda birçok ufak işlemleri birbiri ardına çağıran servis uzun süreli bir işlem olacaktır. kaynak: (source-id: 165) "Long-running business activity" başlığı. Diğer kaynak: 'saga' teriminin ilk ortaya atıldığı belge: (source-id: 166)

Aslında ilk çıkan makalede uzun süreli vakit ihtiyacı olan tasklardan bahsediliyordu. fakat bu pattern kısa süreli olanlarda uygulanamayacaı anlamına gelmiyor.

saga'nın debug'ı, 2PC'e göre daha zordur. kaynak: (source-id: 162) "saga pattern" başlığındaki ilk paragraf. "Disadvantages of the Saga pattern" başlığı.

benzer şekilde saga'nın reactif olması da bir avantajdır. reactif olmasından kasıt şu: tüm event'lerin çağrılıp daha sonra thread'in kapatılması ve callback'in çağrılması yeteneği. 2PC'de işlemler bitene kadar thread'imiz açıkken, saga'da işlemler çağrılıp thread sonlanabilir. event'ler bittiğinde, bir callback metod tetikletebiliriz. 

2PC'de bir transaction sadece bir servisin kendi içinde (seviyesinde) değil, tüm servisler (sistem) seviyesinde kullanılır. dolayısı ile transaction'ın başladığı andan, bittiği ana kadar veritabanında bazı değerler kilitli kalacaktır. bu durum saga'da değildir. çünkü saga'da; 'transaction' sadece servislerin kendi içlerinde(seviyelerinde) gerçekleşecektir.

2PC'de kaynakların (örnek veritabanı) kilitlenmesi, 2PC'nin reactif manifestosuna uymamadığını gösterir. kaynak: (source-id: 168) "The Saga Pattern in a Reactive Microservices Environment", authors: "Martin Stefanko", "Ondrej Chaloupka", "Bruno Rossi", title: "INTRODUCTION" başlığında ikinci paragrafın ortasında.

transaction yönetimleri saga ile 2 farklı şekilde yönetilebilir (implemente edilebilir):

- __Choreography (or tr:Koreografi)__

  bazı kaynaklarda "event" yöntemi olarak adlandırılıyor. fakat bu çok doğru diil.
  
  Koreografi kelime anlamı: Bir dans gösterisini oluşturan adım, figür ve anlatımların bütünü.

  her event diğer event'leri tetiklemesi için event bus'a mesaj gönderir. dolayısı ile tüm sistem merkezi bir noktadan yönetilmez. örnek: bir servis tetikledi, o servis diğer servisleri de tetikleyebilir. yani bir orchestrator yoktur. kaynak: (source-id: 170) "Choreography-Based Saga" başlığındaki ilk paragraf.

- __Orchestration__

  bazı kaynaklarda "command" yöntemi olarak adlandırılıyor. fakat bu çok doğru diil.

  merkezi bir servisten tüm event'ler/servisten çağrılır ve revert servisleri de aynı orchestrator tarafından çağrılır.
  
  Orchestration biraz daha çok 2PC'e benzemektedir.

  Orchestration'da, orchestrator servisi runtime'ı catch edilemeyen exception ile karşılaşıp kapanırsa, o zaman saga yarıda kalmış olacak ve revert işlemleri yapılamayacak. 2PC'de transactional olduğu için tüm saga'nın yarım kalma gibi bir durumu yoktu. Çünkü tüm transaction merkezi bir yerden geri alınıyordu (daha doğrusu veritabanına comitlenmiyordu). Saga'da buna çözüm olarak, saga-orchestrator-instance'ının yakalanamayan bir sebepten kill olması durumunda, hangi adımda kaldığını algılayacak bir yapı gerekmektedir. Bunu "eventuate tramp", "axon", BPM gibi yapılar hazır olarak sağlıyor. Burada saga işleminin ne kadar önemli olduğu da önemli. Eğer saga işlemi önemli ise (örneğin finansal hizmetlerde) bu recover durumlarını sağlam şekilde desteklememiz gerekmektedir. Oysa yarıda kalabilmesinde bir mahsur olmayan bir işlem ise, saga'nın nerde kaldığını tutan bir yapıya ihtiyacımız olmayabilir.

- __hybrid__
  Yukarıdaki Koreografi ve Orchestration, hibrit olarakta kullanılabilir. Bir sistemde Orchestration kullanıldığı her saga'nın öyle olacağı anlamına gelmez. bazı saga'larda Orchestration, bazı saga'larda Koreografi kullanılabilir.

# backward recovery vs forward recovery
backward recovery, saga herhangi bir adımda fail olduğunda, companse event'leri çağırma yöntemidir.

forward recovery ise, saga fail olduğuda, kalan kısımlarının saga'nın resume/restart edilmesi ile yapılan recovery çözümüdür.

forward/backward recovery mode ise snapshot alarak yapılan mix bir yöntemdir. yani saga tümüyle restart edilmez veya resume da edilmez. saga'nın belli adımlarında sistemin state'i bi yerde saklanır. Böylece eğer saga fail olursa, ilgili snapshot'a kadar olan kısım revert edilir (backward recovery) yapılır, ve daha sonra saga devam ettirilir (forward recovery).

# event-driven architecture vs saga
(source-id: 171) sayfasında event driven architecture'ın deprecated ve saga ile replace olduğu yazmaktadır. bunun sebebi şudur:

event-driven architecture bir sistem çok genel bir terim kalıyor. saga ise bunun biraz daha spesifik hali olarka düşünebiliriz. fakat her # event-driven bir sistem zaten saga olmak zorunda. çünkü; saga reversable işlemlerden bahseder. event-driven daha geneldir ve reversable olmasından bahsetmez. fakat pratikte reversable olmayan event'ler nerdeyse hiç yoktur. bu sebeple saga daha net ve daha gerçekçi bir şekilde ihtiyaçları karşılayan bir pattern'dir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Transactional outbox pattern
bir servis atomic olarak hem DB'ye kayıt hemde message event'i atmak isteyebilir. Bu işlemlerin atomic olduğunu garanti edebilmek için outbox pattern kullanılır. İlgili servis DB işlemlerini yapar ve aynı DB-transaction'ında DB'de farklı bir tabloya da yazar (bu tabloya "Outbox table" denir). DB'ye yazıldıktan sonra, DB'den sürekli olarak kafka veya bağımsız bir servis event kayıtlarını okur ve işletmeye başlar. Yani direk olarak kafka'ya diil, arada DB vardır.

2 şekilde implemente edilebilir:

- # Polling publisher pattern
  Bağımsız bir service (scheduled job) sürekli olarak outbox table'ı okur. Buradan sonra ilgili event'i kafka'ya fırlatır.

- # Transactional Log Tailing
  DB seviyesinde transaction-log'lardaki değişiklikler takip edilir. Her değişiklikle kafka'ya direk DB tarafından kayıt atılır.

  Bu patterni uygulayan yazılımlara "__Change data capture (or CDC)__" deniliyor. örnek sistemler: Debezium, Kafka Connect (with a connector).

Outbox pattern, "dual write" problemine bir çözüm olabilir. "dual write"; hem db hem kafka'ya atomik yazmamız gereken fakat yazamadığımzı durumlarda (hata aldığımzıdan ötürü) görülebilen bir hatadır. tekrar aynı flow'lar, aynı request-data'sı ile çağrıldığında işlem yarım kaldığı için, sistemin tekrar benzeri kayıtları atması durumunda "dual write" oluşur.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# event sourcing pattern
order tablosundan gidelim. order'ın tamamlanması için birçok aşama vardır. işleme alınma, ödeme alınma, kargoya verilme gibi... bunların her biri event'tir bu event'ler "event store" da tutulmalı.

böylece;
- order'ın son haline event'leri takip ederek bile ulaşabiliriz.

  not: order'ın son halini sadece query'lerimiz (CQRS pattern'indeki query'lerimiz) için bir tabloda tutarız. fakat her event sonunda bu order tablomuzu güncellemeyiz. sadece tüm event'ler tamamlandığında order tablomuzu güncelleriz.

- event-driven architecture sağlar (reactive sistemler için ideal bir yapı)

- her event ne yapacağına kendi karar verecektir. bu da daha modüler/mikro servis mimarisine geçişimizi uygun kılacaktır.

# isimlendirme
event isimler geçmiş zaman olmalı ve fiil içermelidir. uygulamanın hangi durumda olduğunu net bir şekilde açıklamalıdır. örnekler: 

| Badly named     | Well named      |
|-----------------|-----------------|
| AccountInserted | AccountCreated  |
| AccountUpdated  | FeeCharged      |
| AccountUpdated  | MoneyWithdrawn  |
| AccountUpdated  | AccountCredited |
| AccountDeleted  | AccountClosed   |

# Event storming
domain expertlerin ve devleoper'ların bir araya gelerek yaotığı toplantıdır. bu toplandıda event'lerin ne olduğuna karar verilir.

# domain events vs event-sourcing

domain event'leri microservislerimiz arasındaki haberleşmede kullanılan event'ler olarak düşünülebilir. event sourcing ise her microservisin kendi içinde tuttuğu event'lerdir. bu 2 event'ler ayrı ayrı tablolarda tutulması önerilir. böylece her node bağımsızca test edilebilir ve geliştirilebilir olacaktır.

domain event'lere örnekler:

- A user has registered
- An order has been received
- The payment deadline has expired

Domain event'leri, event sourcing event'lerine göre daha yüksek seviyelidir. Domain expertleri tarafından anlaşılırlar. Bu sebeple teknik olmamalıdırlar. Oysa evet sorucing eventleri daha alt seviyeli ve yazılım teknik elemanları tarafından anlaşılabilirler.

bu durumu bu linkteki: (source-id: 172) "Events from Event Sourcing ≠ Domain Events" başlığındaki bu resim iyi açıklamaktadır: (source-id: 173)

Martin'in bloğunda bu geçmektedir: (source-id: 174) "Event Sourcing ensures that all changes to application state are stored as a sequence of events." Dolayısı ile her event sourcing işlemi application'ın state'inde değişiklik yapmaktadır. Her değişiklik sonrası state veritabanında saklanmalıdır.

# snapshots
event'lerin sayısı çok artabilir ve bir command birçok event çalıştırabilir. dolayısı ile, bir her event son durumu (state'i) okumak için sürekli ilk event'in log'undan son event'in loguna kadar okuyup, hesaplama yapması gerekebilir. örneğin; aynı kullanıcı toplu transaction işlemleri üstüste yapıyor. her event; yani transaction öncesi bakiyede para kalıp kalmadığını kontrol edeceğiz. tüm eventlerin ne kadar harcadğını bulmak zorundayız. bunu yapmak yerine 10 adet işle sonrası yeni bir snapshot yaratabiliriz. bu snapshot'ta soon durumun özeti olabilir. bu snapshotları event tablosunda da tutabiliriz yada farklı bir tabloda sadece snapshot'ları tutabiliriz.

her snapshot'un event tablosunda tutulduğu bir örnek: (source-id: 175)

snapshot'ların ne aralıklarda alınacağı, sistemin mimarisi, uygulamanın domaini ve performans ölçekleri gibi birçok parametreye bağlıdır. snapshot almak; hem maliyetli hemde kod logici ve karmaşıklığı getrdiği unutulmamalıdır.

# Compensation events
Compensation kelime anlamı: azminat, telafi.

revert işlemi için attığımız event'lere verilen genel isim.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Circuit Braker pattern (or devre kesici deseni)
başka başlıkta anlatılıyor (Hystrix ile birlikte anlatılıyor).

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Service registry
"discovery server" konusu altında (başka başlıkta) anlatılıyor.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Client-side Service Discovery Pattern vs Server-side Service Discovery Pattern
her iki pattern'de de, service discovery'ye her node kendi ip'sini bildiriyor.

Client-side pattern'inde her node, service discovery'ye erişerek, diğer node'lara gideceği ip adreslerini alır.

Server-side pattern'de ise her node direk olarak sistemdeki "load balancer"'a istek yaparak gitmek istediği servise erişir. 

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Self Registration pattern
her node'un kendini service regisrty'ye kaydetmesi gerekmektedir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# 3rd Party Registration
Her nodun kendisini servis registry'ye kaydetmesi yerine sidecar gibi üçüncü parti yazılımların bizim yerimize kaydetmesi pattern'idir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Blue-Green Deployment Pattern
tüm mikroservisleri durdurup yeni sürüm çıkmak ve hata olma durumunda geri alınmasını beklemek çok zaman alabilir. bunun önüne geçmek için bir ortamda daha yeni sürüm sistem ayağa kaldırılır. eski sistem hala ayaktadır. yeni sistem sadece tek bir yönlendirme yapılarak canlıya alınmış olur. bu yönteme Blue-Green Deployment denir.

yönlendirme yapılmadan önce yeni ortamda happy path testler koşulması önerilir.

"green"; o anda "production" ortamını, "blue" ise "staging" ortamını ifade etmek için kullanılan renklerdir.

Netflix bu renkleri red/black olarak kullanıyor. kaynak: (source-id: 176) title: "Blue/Green Deployment".

# canary releasing (or canary deployment)
release kelime anlamı: 1.serbest bırakmak 2. gösterime sokmak/yayına sunmak

"canary" terimi yazılım dünyasında "early version of software" anlamında kullanılıyor. bunun hikayesi; kömür madencilerinin önceden ortam havasından hastalanmalarını engellemek için kanarya kuşunu kullanmaları hikayesi olan 'canary in the coal mine'dan geliyor.

canary releasing bu tekniğinde; hem yeni, hemde eski ortam ayağa kaldırılır. canlı'nın trafiği azar azar yeni ortama açılır. burada monitoring mekanizlamalarımızın çok iyi şekilde tasarlanmış olmalıdır. çıkacak hata oranlarının eskisi ile karşılıştırılması ile yenisinin trafiği yavaş yavaş arttırılır.

# Rolling release (or rolling update or rolling deployment)
büyük paketler çıkarak güncellemek yerine, ufak ufak güncellemeler çıkılarak gerçekleştirilen deployment'lardır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Microservice chassis
chasis türkçe karşılığı: şasi (Motorlu kara taşıtlarının iskelet bölümü)

her yeni mikroservis oluşturulduğunda bir framework'ten yararlanıp, cross-cutting concern'lerin (loggining, security...) tekrar tekrar yazılmaması ve bununla zaman kaybedilmemesi gerekmektedir. örnek spring boot-starter bunun için ideal bir örnektir. spring boot starter yerine bizde onu wrap edip common bir base dependency yapabiliriz.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Service Template
Microservice chassis'te dependency olarak base bir proje kullanılırken, burada base proje direk olarak copy/paste (fork) yöntemi ile kullanılmaktadır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Self-contained service
her microservisin availability'sini arttırmak için uygulanabilecek bir pattern'dir. Order servisini düşünelim. gelen isteği senkron olarak önce güvenlik servisine, sonra product servisine, işlem atammalnınca da raporlama servisine bilgi yollayıp olması ve sonra son kullanıcıya dönüş yapması gerekir. Diğer servisler cevap vermediği zaman bu serviste işlem yapamayacaktr. İşte bunu engellemek için şöyle çözümlere gidilebilir: 
- Gelen request jwt içerirse, jwt'yi kendi açıp onaylayabilir.
- product datasını doğrulayabilmek için product listesininin veritabanının klonunu kendinde barındırabilir.
- raporlama servislerine de hiç syncron istek atmaz. channel üzerinden asenkron mesaj bırakır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# data access object (or DAO) pattern
örneğin Employee sınıfı modelimiz olsun. bunun erişimi için gerekli aşağıdaki sınıfları bir EmployeeDAO isimli sınıfına koyabiliriz:

```java
List<Employee> findById();

List<Employee> findByName();

boolean insertEmployee(Employee employee);

boolean updateEmployee(Employee employee);
```

Bazıları pattern olmadığını, sadece "seperate of logic" temeline uyduğunu belirtiyor. Bazıları ise "Structural" pattern altında olduğunu belirtmektedir.

# repository pattern
DAO sadece persistence odaklıdır ve persistence işlemlerinin ayrılmasını sağlar. "repository" ise ona çok benzerdir fakat farklı kavramlardır.

Repository, sadece aggregate root'ları yönetmek için kullanılırken, DAO direk DB objeleri manipüle eder.

Repository, "collection of objects" olarak düşünülmelidir. Yani bir collection (liste) var ve biz bu collection'a ekleme çıkarma, o collection'da arama (query) gibi işlemler yapıyoruz. Aynı arrayList'in metodlarında yaptığımız gibi. collection tek tipte bilgi store ettiğinden, repository tek tip model üzerine odaklanır, örnek: UserRepository, OrderRepository gibi...

Repository; Eric Evans'ın DDD kitabında anlatılıyor. kaynak: "Domain-Driven Design: Tackling Complexity in the Heart of Software", 2013, page 106.

Her aggregate veya aggregate root için sadece 1 repository class'ı kullanmamız önerilir. kaynak: (source-id: 178) "Define one repository per aggregate" başlığı, 1inci cümle. İşin aslına bakıldığında; bir aggregate altındaki tüm entity'ler aggregate root'lar tarafından update edilmektedir. Yani aggregate için yazılan repository aslında aggregate root için yazılmış oluyor (aynı kapıya çıkıyor). Aggregate altındaki diğer entity'ler için ayrı repository yazılmamalı. Bu durum tüm aggregate'in consistency'si için önemli.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Front controller pattern
Spring MVC'deki dispatcher-servlet bir Front controller örneğidir. tüm request'ler buradan geçer. Bu şekilde ortak olan concern'ler (security, internationalization, and providing particular views for certain user...) burada halledilir.

"Martin Fowler", "Patterns of Enterprise Application Architecture" isimli kitabında bu pattern'den bahsetmiştir. kaynak: (source-id: 179)

Burada da detaylı şekilde anlatılmaktadır: (source-id: 180)

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Backend For Frontend
Back-end servislerinin önüne facade gibi diğer servisleri çağıran servisler yazılır. Bu yeni servisler sadece son kullanıcının kullandığı client'a hizmet etmek için vardır. Bu client'lar daha az servis çağırarak daha çok iş yaptırabilir ve bu servisler buna göre optimize edilmiştir. Çünkü son kullancının kullandığı cihazlarda pil kullanımı gibi parametreler önemlidir.

Her client çeşidi için (ATM, mobile, web...) farklı servisler yazılabilir.

Bu yeni servislerde ne gibi optimizasyonlar yapılabilir:
- client'a dönen response'ta tarih gibi data'lar formatlıdır. client'ın tekrar formatlamasına gerek yoktur.
- Client'ın parse etmesi daha hızlı olan response biçimlerinde dönüş yapabilmelidir (örneğin client ortamında json, xml'e göre daha hızlı parse ediliyorsa, bu servisler json dönebilmelidir)
- Client'ın yapacağı X http isteğinden sonra %90 Y isteği de yapılıyorsa, X ve Y isteğini aynı request'te karşılayabilmelidir.
- Cache'lenebilen hard-coded data'lar birçok microservisten ayrı ayrı çekilmesi yerine, tek bir servisten sunan servis yazılmalıdır.
- no-sql'deki gibi client'a tüm data'yı tek hamlede yollayabilmek için, response de-normalize edilmiş olabilir.
- Bazı servisler çok fazla gereksiz data dönebilir. örneğin user servisi, user2ın yaşını dönüyordur. fakat Bu ATM'yi ilgilendirmez. Bu sebeple ATM servislerine yaş bilgisi dönmemelidir. Bu şekilde network ve client'ın response parser'ı daha az yorulacaktır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# multitier architecture (or n-tier architecture) vs multilayer architecture (or n-layer architecture)
tier ve layer'ın kelime anlamları birbirine çok yakın (aynı denebilir, fakat belki detaylarda ayrılıyordur. tam bilmiyorum.). bu sebeple piyasada birbiri yerine kullanılıyor. fakat "layer", logical olarak aynı runtime'da birbirinden ayrılmış iş katmanlarını temsil eder. Örneğin; business layer, database-crud-services layer gibi... Sadece business ve database-crud-services olan bir yazılım 2-layered application'dır.

Oysa "tier" terimi fiziksel olarak ayrı olan katmanları temsil etmek için kullanılıyor. Örneğin; UI layer, busines service...

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Don't Use Exceptions For Flow Control (Anti-Pattern)
Exception kullanımının kodun akışını belirlememesi gerektiğini savunana bir görüştür. Bu durum dil'den dile değişmektedir. yani; bu öneri her dil için geçerli değildir. kaynak: (source-id: 145) 7'inci bölüm (her bölüm çizgi ile ayrılmış).

Örneğin; aşağıdaki gibi for-loop içinde bir döngümüzde kullanmamız önerilmez:

```java
try {
	for (int i = 0; i++){
		array[i]++;
    // Do naything here with "array[i]"
  }
} catch (ArrayIndexOutOfBoundsException e) {
  // exit from for-loop at this point or add any logic here
}
```

kaynak: (source-id: 145) 2'inci bölüm (her bölüm çizgi ile ayrılmış).

Ancak, bizim yazmadığımı herhangi bir kütüphane exception fırlatıyor ise; o zaman elden birşey gelmez ve onu yakalamak gerekir: 

```java
} catch(RedirectException e) {
	response.sendRedirect(e.getURL());
}
```

kaynak: (source-id: 145) 5'inci bölüm (her bölüm çizgi ile ayrılmış).

Aşağıdaki örneklerden birinde exception kullanılmış, diğerinde kullanılmamış:

```cs
if (conn.State != ConnectionState.Closed)
{
    conn.Close();
}
```

```cs
try
{
    conn.Close();
}
catch (InvalidOperationException ex)
{
    Console.WriteLine(ex.GetType().FullName);
    Console.WriteLine(ex.Message);
}
```

Yukarıda hangisini kullanmak önerilir? Eğer çoğunlukla exception case'ine düşülüyor ise; if bloğu ile kontrol etmek gerekli. Eğer nadir düşülecek bir case ise exception kullanmak gerekir. Çünkü eğer nadir karşılaşılıyor ise; if bloğu olmayacağı için hç if-kontrolü yapılmamış olacak. kaynak: (source-id: 148) "Handle common conditions without throwing exceptions" başlığı.

# performans etkileri
Exception kullanmak, performance konusunda bazen avantaj sağlarken bazen dezavantaj sağlayabilir. Bu dilden dile ve kod akışının durumuna göre değişiklik gösterebilir. 

Artık JIT kavramı da Java dünyasına geldiği için, bu durum (performance) birçok faktörden etkileniyor. Burada (kaynak: (source-id: 149)) yazan tüm cevaplarda; java dünyasında; try bloğuna girmenin neredeyse hiçbir maliyeti olmadığı belirtilmiş. Fakat asıl maliyet exception olduğunda ortaya çıktığı belirtilmiş.

Java'daki bu durum şundan kaynaklanıyor: bytecode içerisinde try bloğu yoktur. Kod akışı aynen devam etmektedir. Fakat exception-table olarak isimlendirilen bir tabloda try catch gibi blokların meta bilgileri tutulmaktadır. Dolayısı ile herhangi bir exception olduğunda, JVM, bu tabloyu incelemekte ve buna göre akışı yönetmektedir. İşte maliyet burada ortaya çıkmaktadır. Eğer thread'in başlangıç noktasına kadar olan stack-trace'imiz büyükse (yani içiçe metodlar çağrılmış ise), bu durumda her metod için exception-table JVM tarafından okunup kontrol edilecektir. kaynak: (source-id: 150) "The Non-Heap Exception Table" başlığı. + bu kaynakta bytecode örneği verilmiş. bu örnekteki bytecode'da try-catch olmadığı da örneğin içerisinde yazmaktadır: (source-id: 149) Kingshuk Bandyopadhyay'nin cevabı.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Blob (or Monster Class or god bean or god object or god class or Winnebago) (Anti-Pattern)
Single Responsibility principle'a uymayıp birçok işi üstlenen, gereğinden fazla üyümüş olan class'lar için kullanılan bir terimdir.

# God Method (or god function)
God Class'taki gibi tüm iş yükününün sadece 1 fonksiyona düştüğü durumlardır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Dependency hell (Anti-Pattern)

bu terim genelde Dependency'lerden kaynaklı sorunlar olduğunda kullanılır. bazen platfrom spesifik terimler kullanılır. örnek: jar hell, dll hell gibi.

Dependency hell birkaç çeşit formda karşımıza çıkabilir:

- __Long chains of dependencies__

  açıklama: dependency ağacının derinliğinin çok uzaması. Aslında bu direk olarak bir problem değil, fakat farklı bir dependency problemi ile karşılaştığımızda, sorunun çözümünü çok zorlaştıracak bir tehlike arz eden bir durumdur.

  muhtemel çözüm: 
  - microservisler. bir projeyi farklı executable paketlerle kullanılabilir halde ayırmak. belki portable uygulamacıklar sunmak.
  - yada farklı dependency tercihlerinde bulunmak.

- __too many dependencies__

  muhtemel çözüm: 
  - microservisler. bir projeyi farklı executable paketlerle kullanılabilir halde ayırmak. belki portable uygulamacıklar sunmak.
  - ortak super pom'lardan kurtulmak içi super pom'ları da ayırmak.

- __version collusion (or version conflict or sürüm çakışması)__

  açıklama: yürüteceğimiz bir programın bir bağımlılığı diğer yürüteceğimiz bir programın bağımlılığı ile sürüm çakışması yaşamaktadır. örnek: x programı Dependency-A'yı max 3 sürümü kabul ederken, Y programı min 4 kabul etmektedir.

  muhtemel çözüm: container (örnek docker)

- __cyclic dependency (or circular dependency)__:

  açıklama: birbirine depend eden projeler.
  
  muhtemel çözüm:
  - projeleri birleştirmek
  - ortak kodları başka üçüncü bir projeye taşımak

# tree vs flat Dependency store management

nix ve yarn paket yöneticileri paketleri/bağımlılıkları bir dizinde tutar. buna store biçimine flat adı verilir. bu dizinde X paketi olsun. X paketinin bağımlılıkalrı X dizini içinde değildir. X ile aynı dizindedir. bu paket yönetim sistemi daha az yer kaplar. çünkü ortak bağımlılıklar ortak dizine referans eder.

tree'de ise her paket/Dependency kendi Dependency'lerini kendi içinde barındırır. ağaç şeklindedir. bu yöntem flat'e göre daha çok yer kaplar. fakat paketler taşınabilirdir. bir paketi başka sisteme kopyalayıp kullanabilirsiniz. çünkü herşey kendi içindedir. npm tree yöntemini kullanır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Spaghetti code (Anti-Pattern)
Özellikle kod akışının takibinin zor olduğu yazılımlarda kullanılan bir terimdir. Bu durum genelde "goto" kullanımlarında veya kod akışı tek yönlü olmadığında olur. farklı bir değişle; kodu çağıran fonksiyon, tekrar kodu çağıranı çağırdığı durumlar fazla olduğunda Spaghetti terimi kullanılır. En temelde kodun bakımının çok maliyetli olduğu durumlarda bu terim kullanılır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Reinventing the square wheel (or Reinventing the wheel)
Biz yapmadan önce ilgili sorunumuza/isterimize çözüm üretilmiş olabilir. Özel bir sebep olmamasına rağmen, daha önceden üretilmiş bu çözümü kullanmıyorsak bu bir anti-pattern'dir.

# "Not invented here"
"Not invented here" terimi genelde dışarıdan ürün almama eğilimini temsil etmek için kullanılır. "Not invented here" sendromu in-house geliştirme çok daha verimsiz olmasına rağmen şirketin sürekli bu politikayı izlemesi durumunda kullanılan bir terimdir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# law of the instrument (or law of the hammer or Maslow's hammer or golden hammer or Old Yeller or Head-in-the sand)
hammer kelime anlamı: çekiç

Kişinin bildiği ve sevdiği favori framework/tool/çözümün en geçerli olan olduğu veya en iyisi olduğu yaklaşımıdır. Bu yaklaşım bri anti-pattern'dir. Zira kişinin tüm yeniliklere kapalı olmasına sebep olur.

çekiç terimi şuradan geliyor: bir çocuğa çekiç verdiğinizde, tüm problemleri çözmek için o çekici kullanır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Softcoding
Hardcoding'in zıttıdır. Businness'in kodda diil, config dosyalarında olmasıdır. Tabiki ihityaçlar gereği uygulanabilir fakat debug etmeyi aşırı zorlaştırdığı gibi, sürekli çok fazla generic kod yazmaya sebep oluyor.

# Hardcoding
Kodun konfigurasyonlarının sabit olarak kodun içine gömülmesidir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# magic string
yazılımcılar arasında "hardcode string" olarakta adlandırılır. enum, yada final static olmayan kod içine direk olarak yazılmış string'lere verilen isimdir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Lava Flow (or Dead Code)
Optimum koşullarda geliştirilmemiş kodun, canlıya alınması durumunda kullanılan terimdir. bu kodun en önemli sıkıntılarından biri bazı kısmının kullanılmıyor (Dead Code) veya amacının olmaması durumu olduğu içi anti-pattern'e aynı zamanda "Dead Code" denilebiliyor.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# boat anchor (or boatanchor)
boat anchor kelime anlamı: tekne çapası

kodun içerisinde ilerde ihtiyacımız olabilecek fakat şu anda kullanılmayan özelliklerin olmasıdır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Error hiding
Catch edilen ahtanın hiçir yere log'lanmaması veya kaydedilmemesi yada son kullanıcıya dönülmemesi durumlarıdır. Hata catch edildiğinde, farklı bir iş logic'i uygulanıyor olailir fakat her türlü bunların lolanması gerekmektedir. Yoksa hata yok olur.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Busy waiting
bir bilgi beklerken, cpu'yu meşgul edilmesi durumudur. Bunun yerine reactive çözümler uygulanmalıdır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Calling super (or call super)
Super class'ın metodunu çağırmak bir anti-pattern'dir. Biz abstract/interface'deki (super class'taki) metodları override etmeliyiz fakat super çağırmamalıyız. Api'mizi kullanan client zaten super class'taki metodları çağırmalı ve bu metodlarda override etmemiz beklenen metodları çağırmalıdır.

Bunun en temel sebebi, alt implementasyonların, üst sınıfları işleyişini iyi bilmeleri gereksinimidir. Ne zaman super çağrılacak ne zaman çağrılmayacak gibi konuları implementasyonlar bilmemelidir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Analysis Paralysis
Paralysis kelime anlamı: felç

Proje analizinde gereğinden fazla kynak harcanmasında ortaya çıkan sorundur.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Cargo cult programming
Pattern'leri veya çözümleri anlamadan sadece uygulamak için uygulayıp progra geliştirme tekniğidir.

Cargo cult terimi şuradan geliyor: 2inci dünya savaşında Pasafik adasında bir grup kitle sürekli olarak onlara kargo ile yemek getiren yüce insanları bekliyordu. Fakat arkada ne olup bittiğinden haberleri yok ve sorgulamıyorlardı.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# vendor lock-in (or proprietary lock-in or customer lock-in)
Bir yazılımın bir altyapıya/ürüne çok fazla bağımlı olacak şekilde geliştirilmesi. Böyle olunca farklı bir ürüne geçiş çok maliyetli, hatta geçiş yerine projenin tümüyle yeniden yazılmasına sebebiyet verebiliyor.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Functional Decomposition (or No Object-Oriented AntiPattern or No OO)
bir sınıfın bir metodunun olması, tüm elemenlarının private olması, sadece 1 işi ir metod ile yapması, onu prosedürel dilmişçesine kullanılmasına sebep olan metodolojidir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Don't repeat yourself (or DRY or do not repeat yourself) 
tekrar yazılan kodları ortak yere alma prensibidir. Bu uygulanmadığında bir anti-pattern olur ve birçok kod sürekli farklı yerlerde tekrar yazılır.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

# Silver Bullet
kelime anlamı: gümüş kurşun

Bir teknolojinin (kütüphane, dil, pattern, çözüm...) her duruma göre çözüm sunamayacağı ortadadır. Fkata bunu byle düşünmeyip, ilgili çözümü sürekli ve her duruma uygulandığı zaman olumsuz sonuçlar yaşanmaktadır. Yani; hiçbir teknoloji "silver bullet" değildir.

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •

• • • • • • • • • • • • • • • • • • • • • • • •