## Android Nedir? 
Giriş olarak vikipedik bir tanım yapmamız gerekirse Android; Google ve Open Handset Alliance tarafından mobil cihazlar için geliştirilen ve geliştirilmekte olan açık kaynak kodlu bir işletim 
sistemidir.
Normal bir kullanıcı iseniz; Android işletim sistemli bir telefona sahip olmak sizi uygulama geliştiricilerin yazdığı uygulamalara erişip onları kullanabilmenizi sağlar. Her uygulama farklı platformlara farklı şekilde yazıldığı için Android için yazılmış programları bu işletim sistemine sahip cihazlarda kullanabilirsiniz.
Peki biz program geliştiriciler Android işletim sistemine neden ihtiyaç duyar? İşletim sistemlerinin hepsi uygulama geliştiricilere çeşitli avantajlar sağlar. Bunlardan birisi hızlı ve kolay uygulama geliştirmek. Android işletim sistemi de bize bunu sağlıyor, normalde 1 yılda bol hatalı bir uygulama çıkarmak yerine size daha kolay geliştirecek birçok araç sunarak bu geliştirme süresini 1 haftaya kadar düşürebiliyor.
Android işletim sistemi içerisinde JVM adı verilen bir sanal makine bulunduruyor. Bu sanal makine ise belirli dosyaların belleğe yüklenip çalıştırılmasını sağlıyor. Sizin yazdığınız programı yorumlayarak makinenin anlayabildiği bir dile çeviriyor. Kısacası siz İngilizce bilmiyor olsanız dahi yurtdışına gittiğinizde bir çevirmen ya da program aracılığıyla Türkçe çeviri almanız gibi düşünebilirsiniz bu sanal makineyi. Biz Türkçe konuşuyoruz, aracı İngilizceye çevirip diğer kişiye söylüyor; diğer kişi İngilizce bir şey söylediğinde de aracı bize Türkçe halini söylüyor.
Şimdi gelelim bu iki tarafın konuştuğu dile. Android işletim sisteminde bir uygulama yazmak için genel olarak Java kullanılıyor, hatta biraz geriye (2017 yılına) gidersek Androidde Java dışında pek bir programlama dili kullanılmadığını görüyoruz. Şuan ise genel olarak Java ve Kotlin kullanılıyor.
Bilgisayara gelirsek; bilgisayarın anladığı tek dil makine dili (evet şu 1010li falan olan). Aşağıya koyacağım şemada Java ya da Kotlin programlama dilinin hangi aşamalardan geçip makineyle anlaştığını anlatacağım. 

![Kaynak Kodundan Makine Diline](https://github.com/Ritotwo/Android-Egitimi/blob/master/Androide%20giri%C5%9F/Androide%20Giri%C5%9F%201%20-%20Genel%20Tan%C4%B1mlar/java-to-machine.png)

Öncelikle Java ve Kotlin dosyaları okunuyor tabiki de bilgisayar tarafından. Daha sonra bu okunan dosyalar, compiler (derleyici) tarafından bytecode’a çevirme işlemine tabi tutulur. Bu işlem sırasında Java ve Kotlin dosyaları .class uzantılı dosyalara dönüştürülür. Bunları okumak isterseniz okuyamazsınız çünkü bytecode adı verilen ve önceden de adından bahsettiğimiz JVM adı verilen sanal makine tarafından daha kolay okunacak hale gelmiştir yani “02AB”li bir dile dönüşmüştür (Küçük bir bilgi; bu dosyaları bir bir metin düzenleyici ile açarsanız dosyanın “cafe babe” kelimeleri ile başladığını görebilirsiniz :P). Daha sonra bunlar paketlenip uygulamaya (android için .apk uzantılı dosyalara) çevrilir. Daha sonra bu uygulamayı alıp sisteminize kurup ardından çalıştırmak istediğinizde ise JVM yine devreye girer ve bu bytecode dediğimiz rastgele gözüken harf ve rakam topluluğundan oluşan metni alıp analiz eder ve sizin verdiğiniz emirleri makineye tercüme eder. Daha önce örneğini verdiğimiz aracı işte budur. Sizin verdiğiniz kodu alıp makine diline çevirerek makineye işlem yaptırır.

## Java Nedir? 
Daha önceden bahsetmiştik Java’nın nasıl çalıştığından fakat şimdi gelelim Java gerçekten nedir. Yine giriş olarak vikipedik bir tanım yapmamız gerekirse eğer Java; Sun Microsystems tarafından geliştirilen, nesne tabanlı, yüksek seviye bir programlama dilidir. Hatta mottoları da; “bir kere yaz, her yerde çalıştır”dır. Bu da demek oluyor ki siz bir Java kodu yazdığınızda bunu diğer platformlarda da çalıştırabilirsiniz.

## JVM Nedir? 
JVM(Java Virtual Machine) bytecode dan oluşan paketleri (yani uygulamaları) makineyle haberleştiren aracıdır. JVM platformlara özel olarak yazılır (Linux, Windows ve Mac gibi).

## JRE Nedir? 

JRE(Java Runtime Environment) Java ile yazılmış olan uygulamaların çalışmasını sağlayan kütüphaneleri JVM e sağlayan bileşendir. Bir uygulama çalışmak için JREnin sağladığı paketlere ihtiyaç duyar. Tek başına JVM uygulamayı çalıştırmaya yetmez.

## JDK Nedir? 

JDK(Java Development Kit) Java ile yazılmış olan uygulamaların derlenmesini sağlayan bileşenleri barındırır. Aynı zamanda JDK kuruluyken bir uygulamaya hata ayıklama da yapabiliriz.
JDK içerisinde JRE ve geliştirme kitlerini barındırır. JRE içerisinde JVM ve kütüphaneleri barındırır.

RESIM 

## Compiler (Derleyici) Nedir? 

Kaynak kodunu kullanarak bir dili başka bir dile çeviren araçtır. JDK içerisinde javac adı verilen bir derleyici bulundurur ve bu derleyici Java dilindeki kaynak kodunu bytecode a çevirir.

## IDE nedir? 

IDE(Integrated Development Environment) yazılmış olan kodu kendi içerisinde bulundan derleyici ile derleyerek uygulama paketleri oluşturmaya yarayan uygulamalardır. İçerisinde metin düzenleyici barındırır ve kodu buraya yazdıktan sonra belirli prosedürler ile uygulamanızı derleyerek size verir.

## Android Studio Nedir? Nasıl Kurulur? 

Android Studio, Android uygulamalarını geliştirmek için kullanılan yegane IDE dir. Biz kodlarımızı bu IDEnin içindeki  metin düzenleyiciye yazıp Çalıştır a tıklarız ve o kendi içinde derleme işlemlerini halledip uygulamayı çalıştırır.
Şimdi gelelim Android Studio kurulumuna. Android Studio kurulumunu ayrıntılı bir biçimde anlatan bir sürü kaynak olduğu için sizi oralara yönlendireceğim. Çok faydalı olduğunu düşündüğüm bir linki takip etmeniz için aşağıya bırakıyorum. Daha sonraki yazılarda görüşmek üzere.

## Tanımlar 

+bytecode: Taşınabilir kod olarak da bilinir. JVM gibi sanal makinelerin daha kolay yorumlaması için minik karakterlerden oluşur.
+kaynak kodu: Bir program oluşturmak için yazdığımız insanların okuyabildiği (human-readable) kod satırları. Bir kişi bir uygulamanın kaynak kodunu alırsa eğer bu programı derleyerek ve değiştirerek istediği biçimde çalıştırabilir.

## Kaynakça ve İleri Okuma 
#### [Android Studio Nasıl Kurulur?](https://gelecegiyazanlar.turkcell.com.tr/konu/android/egitim/android-201/android-studionun-windows-uzerinde-kurulumu) 
#### [JVM, JRE ve JDK Nedir?](https://medium.com/@kplnosmn94/jvm-jre-ve-jdk-nedir-6cfee2727812) 
#### [Kotlin Nedir? Vikipedi](https://tr.wikipedia.org/wiki/Kotlin) 
#### [JIT Compiler Nedir? Bir java dosyası ne aşamalardan geçerek çalışır?](https://aboullaite.me/understanding-jit-compiler-just-in-time-compiler/) 
#### [Kotlin ve Java kaynak kodunun çalışmaya geçme aşamaları.](https://tedhagos.com/posts/kotlin-getting-started/) 
#### [Derleyici Nedir?](http://bilgisayarkavramlari.sadievrenseker.com/2008/01/03/derleyici-compiler/) 
#### [Derleyici Nedir? Vikipedi](https://tr.wikipedia.org/wiki/Derleyici) 
