
############################

############################
# PATTERN MVC 
############################

############################

# MVC vs MVP vs MVVM vs Redux vs Flux vs Presentation Model (or Application Model)

Redux ve flux pattern'leri detaylı şekilde farklı başlıkta anlatılıyor.

bu konuya girmeden önce birkaç terimi incelemek gerekli:

- # concern
    concern türkçe kelime anlamı: ilgi, endişe, ait olmak

    yazılım projelerinde concern her bir fonksiyonalitenin yazılım tarafındaki katmanıdır. örneğin loggining layer'ı bir concern'dir.

- # Cross-Cutting Concern
    yazılımımızın bir katmanında diğer concern'lere ihtiyaç duyabiliyoruz. "loggining", "security" gibi concern'ler diğer tüm katmanlar tarafından ihtiyaç duyulmaktadır. başka katmanlardan çağrılan concern'lere "Cross-Cutting Concern" denir. bazı örnekler:

    - security
    - configuration management
    - logging
    - communication between services (protocols, dto standarts...)
    - monitoring (healt check, metrics, distributed tracing)
    - persistence management
    - caching
    - data validation
    - business rules (common rules which are using by independed services)
    - exception handling
    - performance/memory management -> performans cross-cutting concern'dür. fakat her yere kod yazmayı gerektiren bir durum olmayabilir. yada bunun altına sub-category olarak caching'i ekleyebiliriz.

- # Separation Of Concern
    SoC concern'lerin birbirinden ayrılması için tasarlanmış pattern'lerdir/çözümlerdir.

    aşağıdakilerin her biri SoC çözümü için geliştirilmiş birer patterndir:

    - CQRS
    - MVC
    - MVP
    - MVVM
    - Presentation Model (or Application Model)

    MV ile başlayan patternler ailesine __Model-View-\* (or MV\*)__ denir.

    Bu patternler hem server hem client tarafta kullanılabilir.

    React, angular, android gibi framework'lerin sadece 1 tanesi ile yukarıdaki istediğimiz pattern ile yazabiliriz. Önemli olan yazım tarzımızdır. Fakat framework'ün best practice'leri bizi bir pattern'e yaklaştırabilir.

- # aspect oriented programming (or cephe yönelimli programlama or AOP)
    bu konu başka yerde de anlatılıyor.

    AOP, concern'leri birbirinden ayırmayı temel alan programlama felsefesidir.

# JSP model 1 Architecture vs JSP model 2 Architecture
model 1:

```
Client <--> JSP <--> Java-Bean(s) <--> Database
```

On above architecture, both JSP and Java-Bean(s) may have the responsibility of "Controller" (C of MVC). For that reason model 1 does not fit to MVC architecture.

model 2:

```
Client <--> Controller(Servlet) <--> JSP <--> Java-Bean(s) <--> Database
```

Model 2 fit in MVC architecture. On this model:
- Java-Bean(s) are representation of model (M of MVC)
- JSP is the View of MVC
- Controller(Servlet) is the C of MVC

In model-2 architecture, JSP's and Java Beans may contain business logic but it's not mostly recommended.

# MVC (or Model-View-Controller)
flux vs mvc başka başlıkta anlatılıyor.

Smalltalk firması 1980'lerde MVC denilen yapıyı ortaya atmıştır.

mvc'de controller dolaylı yoldan view'a bağımlıdır. controller'ın bir metodunu çağrırıken, view yoksa muhtemelen exception alırız. çünkü örneğin; muhasebe sayfamızda kullanıcının parası bittiyse "0 tl" kırmızı ile gösterilecektir. bu sebeple unit test controller'ların metodlarını çağırarak yapamıyoruz. (Bu sebeple MVP, MVC'den türetilmiştir.)

bir android projesinde ilk düşünüldüğünde MVC şunlara karşılık gelebilir:
- M: herhangi bir sınıftaki data sınıfı yada objesi
- V: layout dizinindeki xml dosyamız
- C: activity sınıfımız

oysa bu bakış açısı her zaman doğru diildir. programı yazarken mimariyi biz tasarlamaktayız. örneğin; layout.xml oluşturmayıp, tüm GUI elementlerini activity'mizde (java kodumuzda) dinamik oluşturabiliriz. araştırma yapılırsa MV* ailesinden birçok pattern'in de android porojelerinde kullandığı görülebilir.

MV* ailesindeki pattern'ler sadece önyüz için tasarlanmamıştır. Bir projenin bütünü iyice incelenirse birçok kısmında MV* ailesinden patternler görebiliriz. Örneğin suncu tarafta REST controllerımızda da MVC görebiliriz.

Model sınıfı, sadece dataların tutulduğu sınıf diildir. business logic'te burada olduğu unutulmamalıdır. Controller sadece view ve model arasında bir aracıdır.

Aşağıda MVC'nin temel şeması çizilmiştir. View, Model'dan data'ları gözlemlemek (observe) etmekle yükümlü. Controller ise Model'de update'ler gerçekleştiriyor.

Aşağıdaki şekilde yıldız (*) prefixine sahip olan text, ok işaretinin yaptığı örnek bir aksiyondur.

```
*show
 > > > >  User > > > > >*click
^                      v
^                      v
View               Controller
v                      v
v                      v 
> > > > > Model < < < <  *write
*observe
```

Şekil için kaynak: (source-id: 409) "A Pattern Language for MVC Derivatives", authors: Takashi Kobayashi and Sami Lappalainen.

Yukarıdaki şekilde "View" ile "model" arasındaki ok işaretinin yönünü diğer türlü çizenler de var. Bu biraz çizimin nasıl algılanacağı ile alakalı bir durum. Arkaplanda herkesin bahsetmek istediği şey aynı oysa.

Yukarıdaki şekilde tam gösterilmesede "view", controller'daki event'leri tetikliyor. Aslında user view'a tıklamış oluyor. (Şekilden farklı anlaşılabilir.)

Yine yukarıdaki şekilde controller ile view arasına şu görevi gören çizgi çizilebilir: User event'lerine göre Controller, farklı view'ı initialize edebilir.

# MVP (or Model-View-Presenter)

MVC'deki "controller" yerine "Presenter" gelir, ve MVC'deki "View" artık daha çok View değişikliklerinden de sorumludur. örnekle ilerleyelim:

```java
class MyPresenter {

    MyPresenter(MyView view, MyModel model) {
        this.view = view;
        this.model = model;
    }

    void onEventX(int buttonNumber) {
        model.change("999");
        view.showWarning("You create an event!"); //it does not cares what views does. view can show alertbox or can show small text inside screen.
    }
}
```

Burada MyView bir interface. MyView'ın View tarafında implemente edilmesi gerekiyor. Yani view, her olayda kendinde nelerin güncelleneceğini belirlemesi gerekiyor. Dolayısı ile view'ı mock'layıp, presenter'ın metodlarını çağıran Unit testler yazabiliriz.

Yukarıdaki kod örneği;
- 'MVC model 2'de olsaydık:

   view.showRedAlertBox("You create an event!") olacaktı. Yani; MVC'de view'a daha spesifik ne yapması gerektiğini söylüyorduk. Oysa MVP'de View'ın abstract/interface'ini yönetiyoruz, yani daha genel/yüzeysel bir View-API'si kullanabiliyoruz.

- MVC'de olsaydık:

  hiçbir view metodunu çağıramıyor olacaktık.

Bu konu burada sade kod örnekleriyle açıklanmış: (source-id: 411) Linkteki projelerin gerçek kod örnekleri burada: (source-id: 412)

MVP ikiye ayrılıyor:

- # Passive View

  Presenter, modeli güncelledikten sonra view'a yeni model'i yollar. örnek:

  ```java
  view.showAlert("paranız azaldı:" + model.getMoney() );
  ```

  view'ın model değişikliğinden haberdar olabilmesi için, Presenter'ın view'a bunu bildirmesi gerekir.

  Aşağıdaki şekilde yıldız (*) prefixine sahip olan text, ok işaretinin yaptığı örnek bir aksiyondur.

  ```
        User
        ^ v 
  *show ^ v *click
        ^ v
        ^ v
        ^ v
        ^ v   *onEventX
        View  > > > > >  Presenter
              < < < < <         v
              *showAlert        v
                                v
                                v
                                v
        Model  < < < < < < < < *write
  ```

  Şekil için kaynak: (source-id: 409) "A Pattern Language for MVC Derivatives", authors: Takashi Kobayashi and Sami Lappalainen.

- # Supervising Controller

  passive'dekinin tersine, modelde yapılan bir değişiklik otomatik olarak view tarafından bilinir. view kendini update eder. bunun için binding yapılması şarttır.

  Aşağıdaki şekilde yıldız (*) prefixine sahip olan text, ok işaretinin yaptığı örnek bir aksiyondur.

  ```
        User
        ^ v
  *show ^ v *click
        ^ v
        ^ v
        ^ v   *onEventX
        View  > > > > >  Presenter
        v     < < < < <          v
        v     *showAlert         v
        v                        v
        v                        v
        v *read                  v
        Model  < < < < < < < < < < *write
  ```

  Şekil için kaynak: (source-id: 409) "A Pattern Language for MVC Derivatives", authors: Takashi Kobayashi and Sami Lappalainen.

# MVVM (or Model View ViewModel)
Bazı kaynaklarda __Model–View–Binder__ olarakta isimlendirilir.

Presentation Model'den sonra, Microsoft yazılımcısı John Gossman tarafından, 2005 yılında ortaya atılmıştır.

KnockoutJS MVVM yapısı üzerine kuruludur.

MVVM'de Presenter yerine ViewModel kullanılıyor.

MVVM'de data binding (yada reactive tarzı streamler) kullanmak şart. Çünkü; View, ViewModel'a erişiyor fakat tersi yapılamıyor. ViewModel, modele erişebiliyor fakat tersi yapılamıyor. Bu sebeple MVVM projelerinde çoğunlukla MVVM altyapısı sunan framework'lerden yararlanılır. örnek olarak; data binding özelliği android tarafından destekleniyor: (source-id: 415).

View, model'deki verilere data binding yapar. Ve event'leri ViewModel'a bildirir. ViewModel, model'i günceller. modelde olan değişiklik, view'a, viewModel aracılığı ile binding olduğu için otomatik yansır.

View code:

```html
<Button
  style="red"
  onClick="@{viewModel.detailEventClicked()}"
  text='@{viewModel.winner} + Click see the winner details'
/>
```

Yukarıda görüldüğü gibi "winner"(model) bilgisi, "viewModel" içerisinde tutuluyor ki, view buna erişebilsin.

```
      User
      ^ v
*show ^ v *click
      ^ v
      ^ v
      ^ v      *onClick
      View  > > > > > > > > > > > > > ViewModel
                                      v  ^
                              *write  v  ^ *on-model-change-event
                                      v  ^
                                      Model
```

Şekil için kaynak: (source-id: 409) "A Pattern Language for MVC Derivatives", authors: Takashi Kobayashi and Sami Lappalainen.

# Comparison Table

| Pattern  | Project size            | Separation of Concerns | Code complexity | Modifi-ability | Testability | Requires view sync framework |
|----------|-------------------------|------------------------|-----------------|----------------|-------------|------------------------------|
| MVC      | Small/Medium            | Fair                   | Low             | Low            | Fair        | Yes                          |
| MVC2     | Medium/Enterprise       | Good                   | Medium/High     | Low            | Good        | No                           |
| MVP (SC) | Medium/Enterprise       | Fair                   | High            | High           | Fair        | Yes                          |
| MVP (PV) | Small/Medium/Enterprise | Good                   | High            | High           | Good        | No                           |
| MVVM     | Medium/Enterprise       | Good                   | Medium/High     | Low            | Very good   | Yes                          |

kaynak: (source-id: 409) "A Pattern Language for MVC Derivatives", authors: Takashi Kobayashi and Sami Lappalainen.

# Presentation Model (or Application Model)
Bu MVC ve türevlerine alternatiftir.

Martin Fowler tarafından 2004 yılında ortaya atılmıştır. MVP'den sonra ortaya atılmış, MVP'ye çok benzemektedir.
