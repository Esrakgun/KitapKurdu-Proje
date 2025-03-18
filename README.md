
# useReducer
Bir react hook'u olan useReducer birden fazla state'i daha kolay bir şekilde yönetmek için kullanılır.Bu metot useState ile stateleri yönetmenin zor olduğu durumlarda kullanılır.

useReducer'da bilinmesi gereken bazı kavramlar:

Action:
State'in nasıl değişeceğini ifade eder. (Ekle,sil,güncelle,...)
Dispatch:
Action'ları reducer'a aktaran yapılardır.
Reducer:
State'in nasıl değişeceğine karar veren fonksiyondu

# React Nedir?
React facebook tarafından oluşturulmuş açık kaynaklı javascript tabanlı bir kütüphanedir.
# Bir React Uygulaması Nasıl Oluşturulur?
Terminalde uygulamanın oluşturlması istenen konuma cd ile konumlandıktan sonra npx create-react-app [proje adı] komutu kullanılır ve bir react uygulaması oluşturulur.

Bu komut sayesinde bizim için bazı dosyalardan oluşan bir template gelir.

# React Uygulamasındaki Dosyalar Ve Klasör Yapısı
node-modules: Projenin bağımlılıklarını tutan dosyadır.İndirilen paketlere bağlı olarak gerekli bağımlılıklar bu dosya içerisinde tutulur.Bu dosya içerisine kesinlikle elle müdahele yapmayacağız.Paket indirme,silme işlemlerini bazı komutlar vasutasıyla yapacağız.

public: Projedeki herkes tarafında erişilebilecek dosyaları bir arada tutan klasördür.index.html,resimler,...

src:

.gitignore: Proje githuba gönderildiğinde pushlamak istemediğimiz dosyaları gitignore içerisine yazarız bu sayede ilgili dosyalar githuba pushlanmaz.

package.json: Projede kullanılan kütüphaneleri,projenin bağımlılıklarını proje içerisinde kullanılan bazı komutların yazılı olduğu dosyadır.

package-lock.json: Proje bağımlılıklarının daha detaylı(sürüm,lisans,vs...) şekilde yazıldığı dosyadır.

src: Source- Yani uygulamanın geliştirilmesi noktasında kullanılan klasördür.

-- App.css // index.css ==> Stillendirme

-- App.js ==> Varsayılan olarak oluşan bu dosya ekranda render edilecek contenti belirler.

-- index.js ==> React uygulamasının temel bileşenidir.Bu dosya app.js içerisinde oluşturulan yapıların render edilmesini sağlar.

# React Uygulaması Nasıl Ayağa Kaldırılır ?
npm start komutu terminalde çalıştırılır bu sayede react uygulaması ayağa kaldırılır.
Jsx Nedir?
Jsx bir dosya içerisinde hem html hemde js kodlaması yapmamıza olanak sağlan bir yapıdır.Js'İn dinamik kodlarını {} ler içerisinde yazarız.

Html-Jsx Farkı ?

class yerine className kullanılır

label kısmındaki for yapısı yerine HtmlFor kullanılır

img,input,... gibi self-closing etikelerinde / kullanılması zorunludur.

Jsx uzantılı dosyalarda bir adet parent element bulunmalıdır.

# Stillendirme Nasıl Yapılır ?
Html'de olduğu üzere buradada satır içi ve harici dosyada stillendirme yapılabilir.

Eğer satır içerisinde stillendirme yapılacaksa bunu style={} içerisinde yaparız.Fakat gerekli stillendirme bir obje oluşturulup bunun içerisinde yapılır.

Harici dosyada stillendirme yapılacaksa bunu .css uzantılı bir dosyada yapar ve bu dosyayı jsx dosyasına import ederiz

# React Component Yapısı:
React component tabanlı bir mimariye sahiptir.Uygulamayı farklı farklı componentler ile oluştururuz.

Bir react componenti oluştururken bir js fonkisyonu yazılır.Bu fonksiyon içerisinde return () yapısı oluşturulur.Buradaki () içerisinde html kodlaması yapılır.

Eğer bu komponent içerisinde js özellikleri değişken,obje,fonksiyon tanımlanacaksa bunu return kısmının dışında yapmamız gerekir.

# React projesine bir paket nasıl indirilir ?
React projesine bir paket indirebilmek için npm'e sahip olamamız gerekir.Bu yapı bizim indireceğimiz paketleri yönetimini sağlan bir paket yöneticisidir.

npm install [paket-adı] veya npm i [paket-adı] belirtiilen paket projeye dahil edilir.

npm install [paket-adı]@[istenilen sürüm ] veya npm i [paket-adı]@[istenilen sürüm ] ile bir paketin spesifik sürümü indirilir.Bu şekilde bir paketin sürümüde güncellenebilir.

Eğer bir paket silinmek isteniyorsa bunu npm uninstall [paket adı] komutuyla yaparız.

# Koşullu Renderlama
Render: Ekrana bir contentin basılmasıdır.

Koşullu renderlama nedir ? Renderlama işleminin bir koşula bağlı olarak yapılması işlemidir.

Koşullu renderlama yaparken iki yöntem kullanılır:

# Ternary Operatör(? :):
Bu yöntemle koşullu renderlama yapılırken ilgili koşulun sağlanmaması durumunundada bir contentin renderlanması sağlanır.
Ve Operatörü (&&):
Bu yöntemde koşul sağlanırsa renderlama yapılır ama koşul sağlanmıyorsa renderlama yapılmaz
# Props:
React'da componentlerin dinamik şekilde kullanılması için props kullanılır.Bu kavram sayesinde ilgili component dinamik şekilde kullanılır.

Bir elemanı props ile dinamik hale getirirken ilk olarak bu propsu bu bileşene geçeriz.Sonrasında bileşen içerisinde bu propsu alır ve gereken yerde renderlarız.

# Çoklu Renderlama
Birden fazla elemanı renderlama işlemine çoklu renderlama denir.

Çoklu renderlama işleminde react renderlanan her eleman için bizden benzersiz bir key değeri ister.Bu key değeri reactın VDOM(SANAL DOM) oluşturması noktasında elemanları birbirinden ayırmak için kullanılır.

# State
React'da uygulama içerisinde meydana gelen bir değişime bağlı olarak ekranın güncellenmemesi bizim için sıkıntı oluşturmaktadır.Bunu çözmek için state kullanılır.

State ile bir bileşende veri tutma ve bu veriyi yönetme yetkinliği kazanırız.

# State Nasıl Kullanılır ?
Statei kullanmamız için ilk olarak react içerisinden useState import edilir.Sonrasında bu yapını kurulumu sağlanır.Kurulum yapılırken bir dizi tanımlanır.Bu dizi birinci değer olarak statei ikinci değer olaraks

# Bir react uygulaması ayağa kaldırılırken dikkat edilmesi gerekenler
Bir react uygulaması ayağa kaldırılırken kullanılan npm start komutunın çalışabilmesi için bu kodun yazıldığı terminal package.json dosyasının bulunduğu dizinde çalıştırılmalıdır.Aksi halde hata alınacak ve uygulama ayağa kaldırılayamayacaktır.
# State
React uygulamasında bir değerin değişmesine bağlı olarak arayüzün renderlanmasını sağlayan yapıya state denir.State ile react bileşeni içerisinde verilerimizi kolay bir şekilde yönetebiliriz.
# React Component Türleri
React'da iki tür component bulunur.
Class Component
Function Component
Class componentler function componentlerin atasıdır.Güncel projelerde çok kullanılmaz.Bir class component tanımlarken class kelimesi yazılır sonrasında bu class componente bir isim verilir verilen isim sonrasında extends ile react içerisindeki Component yapısı miras alınır.Bu sayede bir class component tanımlanır.Bir class componentin iki temel yapısı olur.

i.constructor(Kurucu metot)

Bu metot bileşene geçilecek propsların ve state yapılarını kurulumunun yapıldığı kısımdır.

ii.render(Ekranda renderlanacak contenti belirleyen kısım)

Bu metot bileşen içerisinde renderlanacak contenti belirleyen kısımdır.

Class ve Function componentler arasında javascriptdeki var-- let&const arasındaki ilişkiye benzer bir ilişki bulunmaktadır.Class component güncel projelerde daha çok kod yazmamıza sebep olduğundan tercih edilmez.
# Lifecycle (Yaşam Döngüsü)
İnsanlar doğar,gelişir ve ölürler.Bu insanların yaşam döngüsüdür.React bileşenleride tıpkı insanlar gibi bir yaşam döngüsüne sahiptir.componentDidMount,componentDidUpdate,componentWillUnmount metotları ile bir bileşenin yaşam döngüsü izlenir.

# Vite
Klasik react uygulamalarına göre daha güncel olan bu metot sayesinde daha hızlı bir şekilde react uygulamaları oluştururuz.

Vite ile oluşturulan bir react projesi klasik react projesine göre daha az bağımlılık ve dosya içerir.Bu sayede çok daha hızlı bir şekilde uygulama oluşturulur. Bunun yanında vite ile oluşturulan bir react projesi klasik react projesine göre daha performanslı çalışır. Build işlemide klasik react projesine göre daha hızlıdır.

HMR: Vite projesinde yapılan değişiklikleri klasik react projesine göre daha hızlı şekilde renderlama işlemidir.

# useRef
Javascript kısmında yapılan document.querySelector,document.getElementById,document.GetElementsByClassName,... metotlar ile bir elemana erişme işlemini react'da useRef ile yaparız.

Bu react hook'u react içerisinden import edildikten sonra referansı alınır ve alınan bu referans erişilmek istenen elemana ref={} attribute'u olarak verilir.Bu sayede ilgili elemana erişilmiş olur.

# Json-Server
Bir web projesi temelde iki kısımdan oluşur.
Frontend
Backend
Proje geliştirilirken backend'in bize sağladığı verileri alıp arayüzde kullanırız.Fakat elimizde hazır bir api olmadığı durumlarda api'ın oluşturulmasını beklemek yerine json-server adında bir paket indiririr ve localimizde çalışan bir sahte backend elde ederiz.Bu backend tüm http metotlarını(get,post,put,patch,delete) destekler.
# Json-Server kullanarak sahte bir api nasıl oluşturulur
Json server paketini indir.
Proje dizininde package.json ile aynı konumda bir db.json dosyası oluşturulur.
Bu db.json dosyasında bir obje içerisinde herbir endpoint için birer dizi oluştururuz.
npx json-server db.json komutunu çalıştırarak bu api ayağa kaldırılır.
# HTTP Metotları
Server ve client arasında iletişim kurmak için kullanılan metotlara Http metotları denir.
Get:
Server'dan veri çekmek için kullanılır.
Post:
Server'a veri göndermek için kullanılır.Gönderilecek veri isteğin body kısmına eklenmelidir.
Put:
Serverdaki bir veriyi güncellemek için kullanılır.Bu metotda güncellenmek istenen verinin tamamı isteğin body'sine eklenmelidir.
Patch:
Serverdaki bir veriyi güncellemek için kullanılır.Sadece güncellenecek kısım isteğin body'sine eklenmelidir.
Delete:
Serverdaki bir veriyi silmek için kullanılır
# Axios
Güncel projelerin çoğunda kullanılan bu kütüphane bizim için api isteklerini kolaylaştırır.

Gelen isteğin json'dan js nesnesine çevirilmesi işlemini yapar

Gönderilecek verinin js nesnesinde json'a çevirilmesi işlemini yine axios yapar

Parametreleri işler

İsteklere zaman aşımı ekleyebilmemizi sağlar

Uzun uzun url tanımlamaları yerine baseUrl'ler oluşturarak daha az kod yazmamızı sağlar.





# React Route Dom
React router dom kütüphanesi react'ın SPA(Single Page Aplication) a uygun şekilde route'ları ifade etmemizi ve bunlar arasında geçiş yapmamızı sağlar.
# BrowserRouter:
React router dom kütüphanesi'nin çalışması için temel bileşendir.Tüm routing yapısını kapsar.
# Routes:
Tarayıcıdaki url değişimlerini izler ve buna göre hangi path değerindeyse buna uygun elemanı renderlar.
# Route:
Url'e bağlı olarak render edilen herbir sayfa bir route'dur.
# Link:
Proje içerisinde yönlendirmeyi sağlar.Bu eleman html'deki a etiketinin react router dom'daki karşılığıdır.Url'e parametre geçmek için kullanılır.
# NavLink:
Link etiketi gibi routelar arasında geçiş yapmamızı sağlar.Ekstra olarak mevcut sayfadaki NavLink'i aldığı active clası ile özelleştirebiliriz.
# Routelar'daki ortak elemanların renderi
Her route için renderlanacak bileşenleri teker teker import edip kullanmak yerine bunu tek bir seferde yapabiliriz.Bunu yaparkense BrowserRouter içerisinde (!Routes dışarısında) ilgili bileşen çağırılır.Bu sayede tüm route kısımlarında bu yapı kullanılabilir.
# useParams:
url'deki parametrelere erişme ve kullanma imkanı sunar.
# Dynamic Routes:
Bir kitap projesi düşününüz.Bu projede bulunan tüm kitaplar için birer detay sayfası olsun.Bunu her bir kitap için detay sayfası oluşturamayacağımızdan tek bir sayfayı dinamik şekilde renderlarız.Bu işleme dinamik route yapısı denir.
# Nested Routes:
Bir kapsayıcı içerisinde farklı bileşenlerin oluşturulması işlemine Nested Routes denir.

Bu özellik sayesinde sadece belirtilen sayfalar için ortak özellikler gerçekleştirilir.# KitapKurdu-Proje
# KitapKurdu-Proje
# KitapKurdu-Proje
