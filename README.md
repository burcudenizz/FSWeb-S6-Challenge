# React Sprint Challenge

**Talimatları dikkatlice okuyun.Sprint Challenge için tam olarak neler istendiğini iyice anlamadan başlamayın.**

Bu challenge, geçmiş sprint boyunca öğrenilen kavramları ve teknikleri uygulamanıza ve bunları somut bir projede uygulamanıza olanak tanır. Bu sprint boyunca **React'a giriş** yaptık. Bu sprint sırasında **React bileşenleri ve gelişmiş stilleme** üzerinde çalıştınız.

Bu Challenge'da, bir API'den alınan verileri kullanarak **bir Star Wars sayfası** oluşturarak bu becerilerdeki ustalığınızı göstereceksiniz.

Bu tek başına yapılması gereken bir projedir. Tüm çalışmayı tek başınıza yapacaksınız.

### Proje Kurulumu

- [ ] Forklayarak bir kopyasını oluşturun
- [ ] Forkunuzu klonlayın
- [ ] main branch üzerinde çalışın
- [ ] Push commits: `git push origin main`

## Proje Talimatları

### Giriş

Bu challenge'da, bir API'den elde edilen stilize edilmiş bir karakter listesi sunan bir web sayfası oluşturacaksınız. Verileri bir web sayfasına aktarabilmek, JavaScript geliştiricilerinin yaptığı işin büyük bir bölümünü oluşturur; bu meydan okuma, böyle bir görevi başarabilitenizi sınar.

Minimum Uygulanabilir Ürünü oluşturmak için (MVP) gereklilikler aşağıda sıralanmıştır, projeniz aşağıdaki çıktılara benzemelidir:

[Örnek](/ornek/ornek1.png)

[Diğer örnek](/ornek/ornek2.png) [çalışan hali]https://ergineer.com/assets/materials/as7fwyf-star-wars/

### Talimatlar

Bitmiş projeniz aşağıdaki tüm özelliklere sahip olmalıdır:

- [ ] Karakterleri çağırmak için şu endpointi(uç noktası) kullanın `[GET] https://swapi.dev/api/people/` ([msw](https://github.com/mswjs/msw)).
- [ ] Çekilen karakter listesini bir state e yazın.
- [ ] Karakterlerinizi DOM'a aktarın:

  1. Her bir karakteri render etmek için 'Karakter' isminde bir React bileşeni oluşturun.
  1. map metoduyla statedeki verileri listeleyin, ve tüm karakterleri Karakter bileşenini kullanarak sayfaya yazdırın.
  1. Tüm yazdırılan karaklerlerin ismi DOM'da mutlaka yer almalıdır (örnek. "Luke Skywalker").
  1. Karakterlerin isimleri HTML'ye sabit olarak yazılamaz. Bu veriler mutlaka API'den çekilmelidir.
  1. Bileşenler **styled-components** kullanılarak stillenmelidir.

  **Notlar:**

- Tarayıcı tarafından JavaScript kullanılarak uç noktadan elde edilen veriler, [msw](https://github.com/mswjs/msw). MSW'nin yaptığı her şeyi anlamanız şu an için gerekli değildir, yalnızca şimdilik axios'u `https://swapi.dev/api/people/` adresine istek göndermek için kullandığınızda gerekli verileri nasıl çekeceğinizi bilmeniz yeterlidir.
- Uç noktayı HTTPie veya Postman kullanarak test ederseniz, MSW isteği engellemeyeceğinden farklı sonuçlar elde edersiniz.
- Ek dosyalar oluşturabilirsiniz ancak **mevcut dosyaları veya klasörleri taşımayın veya ismini değiştirmeyin**.
- Ekstra kitaplıklar kurmak dışında `package.json` dosyanızı değiştirmeyin.
- "start" işlemi bazen yeni bağımlılıklar eklendikten sonra tıkanabilir ve yeniden başlatılması gerekebilir.
- Çözümünüzde en iyi yöntemleri kulanmanız, temiz ve profesyonel sonuçlar üretmeniz önemlidir.
- Yazım denetimi ve syntax denetimi de dahil olmak üzere çalışmanızı gözden geçirmek için zaman planlayın.
- MVP'yi karşılayan bir meydan okuma göndermek, çok fazla detay içerip de sonuç içermeyenbir meydan okuma göndermekten daha iyidir.

### Ek Hedefler

Gerekli şeyleri bitirdikten sonra çalışmanızı daha da ileri götürebilirsiniz. Bu hedefler, bu modülde öğrendiğiniz şeyler olabilir veya olmayabilir, ancak az önce çalıştığınız proje üzerine inşa edilirler. Zaman tanıyın, sınırlarınızı zorlayın ve aşağıdaki isteğe bağlı hedeflerden herhangi birini gerçekleştirip gerçekleştiremeyeceğinize bakın:

- [ ] Karakter bileşenini daha karmaşık hale getirin ve birkaç alt bileşene bölün.
- [ ] Karakterlerle işlenecek film bilgilerini elde etmek için `[GET] https://swapi.dev/api/films/` (msw) uç noktasını kullanın.
- [ ] State'e eklemeden önce API verilerinden gereksiz bilgileri kaldırmak için ayrı bir modülde bir yardımcı fonksiyon oluşturun.
- [ ] Stil bileşenleri ile effektler veya animasyonlar oluşturun.
- [ ] Bir dizi promise'ini çözmek için Promise.all'ı kullanın.

## Esnek Mülakat Soruları

1. React JS nedir ve hangi sorunları çözer? Yanıtınızı sınıfta tanıtılan kavramlarla ve web'deki kişisel araştırmanızla destekleyin.
1. Bileşen statelerini tanımlayın.
1. Propları açıklayın.
1. Side effektler nelerdir ve bir React bileşenindeki efektleri belirli state veya prop değişiklikleriyle nasıl senkronize edersiniz?

Yanıtlar:

1. React.js web uygulamaları için hızlı ve interaktif bir ui(kullanıcı arayüzü) oluşturmaya sağlayan bir JavaScript kütüphanesidir. Component(bileşen) tabanlı bir yaklaşım izler ve her bileşen kendi içindeki durumu yönetebilir. Böylece modüler bir uygulama tasarlanmasını sağlar.
   React virtual DOM oluşturur, böylece webteki değişiklikler direkt DOM'a uygulanmaz, sadece yapılan değişiklikler güncellenir. Bu da uygulama performansını arttırır.

2. React state bir componentin dinamik verilerini depolayan ve bileşenin davranışlarını belirleyen bir JS nesnesidir. State dinamiktir ve componentin etkişelimli olmasını sağlar.
   3.Props’lar , bir componentten başka bir componente veri aktarımı yapmamızı sağlar.
   Props’lar salt okunur (read-only) dir. Değiştirilemezler. Bu veri aktarımı; ana componentten alt componentlere geçerken alt componentler tarafından herhangi bir değişime uğramaz.
3. API kullanımlarınıda ve DOM'un manuel olarak değiştirilmesi gibi işlemlere side effects denir. Çünkü bu tarz yan etkiye sahip işlemler rendering sırasında tamamlanmayabilir veya diğer bileşenlere etki etmesi gerekiyor olabilir.
   React bileşenlerinde side effect'leri yönetmek için useEffect() hooku kullanılır. Bu hookun componentte bir değişiklik olduğunda dış dünyadaki işlemleri senkronize eder.
   useEffect() hooku, iki parametre alır:
   birinci parametre, side effect işlevi ve ikinci parametre ise side effect'in senkronize edileceği durumlar ve/veya props'lar dizisidir.
