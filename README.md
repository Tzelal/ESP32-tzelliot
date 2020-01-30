<h1 align="center">ESP32-tzelliot-</h1>

<h2 align="center">ESP32 Arduino IDE kurulum ve ilk kodlar</h2>




Merhabalar burada ingilizce kaynağının bile az olduğu ESP32 modülü hakkında bilgi vermeye çalışıcam.Öncelikle modülü Arduinp IDE'ye nasıl entegre edicez yani kodlarımızı ESP32 modülüne Arduino uygulamasından yükleyebilir vaziyete nasıl getiricez ondan bahsedicem.

![ESP32 Development Board WiFi+Bluetooth-1000x750](https://user-images.githubusercontent.com/36787074/54149000-55d60680-4446-11e9-95a9-e50eb726bd6d.jpg)


Arduino uygulamasının güncel olduğuna dikkat et.Güncel olmayınca yeni uygulamalarda/projelerde hatalarla karşılaşabilirsin.
Arduno'yu (uygulamayı) daha önce hiç yüklemediysen [buraya](https://www.arduino.cc/en/Main/Software) tıklayarak uygulamayı indirebileceğin siteye ulaşabilirsin.

Şimdi.Arduino'yu indirdiğine göre ESP32 modülünü Arduino IDE'de tanımlamamız lazım.Burdan sonra yapıcağımız işlemi daha önce ESP8266 için bi benzerini göstermiştim.O yazıyı okumuşsan yapacaklarımıza aşina olabilirsin.Değilsen de sıkıntı değil herşeyi en baştan burada yazmaya çalışıcam (Yazının sonuna doğru örnek uygulama ve kod var gözden kaçırmadığına dikkat et :D )okumaya devam.


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20162244.png" width="550"></p>


Devamında... ( Additional Board Manager URLs ) yazan yere aşağıdaki resimde olduğu gibi vericeğim linki kopyalayıp yapıştır.

>Eklenicek Kod:<br/>**https://dl.espressif.com/dl/package_esp32_index.json**


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20162440.png" width="550"></p>


 NOT: Yukarıda paylaştığım link sayesinde sadece Esp32 modülü Arduino IDE'ye tanımlanabiliyor.Eğer daha önceden tanımlamış olduğun Esp8266 modülü varsa veya ileride kullanmayı düşünüyorsan yapman gereken Esp32 ile Esp8266 modüllerinin linklerini bir virgül ile ayırıp 'Additional Boards Manager URLs:' kısmında tanımlamak.Uygulanmış bir görseli aşağıda veriyorum.

Kopyalanıp yapıştırılacak link şu şekilde:
**https://dl.espressif.com/dl/package_esp32_index.json, http://arduino.esp8266.com/stable/package_esp8266com_index.json**




<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20162553.png" width="550"></p>


Artık modüller Arduino'da tanımlı fakat bir yazılım daha yüklememiz lazım o da basit olmasına rağmen biraz zaman alabiliyor.Şimdi vakit kaybetmeden devam edelim.


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20193918.png" width="550"></p>


Yukardaki resimde olduğu gibi 'Boards Manager' kısmına tıkladığında karşına çıkıcak sayfada arama kısmına 'Esp' yazdığında Esp32 modülünü indirebileceğin seçenek direkt karşına çıkıcak.İlk aşamalardan biri olan 'Additional Board Manager URLs' kısmına yazdığın linke göre karşına Esp8266 modülünün indirme seçeneği de çıkabilir.İstersen ikisini de indirebilirsin,ben konu gereği sadece Esp32 modülünü indiricem (İkisini de indirmen ilerleyen aşamalarda sıkıntı yaratmaz).


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20195851.png" width="550"></p>


'İnstall' butonuna tıkladıktan sonra biraz süre alıyor fakat Esp32 modülü kullanmaya hazır.<br/>
Evet.Şimdi Esp32 modülünü test etmek amaçlı Arduino IDE'de halihazırda yüklü olan 'wifi' örneğini deneyebiliriz.Fakat bunu için öncelikle 'ESP32 Dev Module' şıkkını seçmemiz lazım ki Arduino IDE'miz hangi modüle kodü atıcağını bilebilsin (Bu arada eğer farklı bir modül kullanıyorsan onu da burdaki seçeneklerden bulup seçebilirsin.Türkiye piyasasında bu modülün genelde sadece bir modülü satılıyor o da yukarıda yazdığım model.)


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20162946.png" width="550"></p>


Modülü seçtikten sonra olması gereken değerler aşağıdaki gibidir:


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20201638.png" width="550"></p>


Herşeyin yolunda gittiğini düşünüyorum.Deniyceğimiz örneğin bulunduğu yer aşağıdaki gibi:


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20164013.png" width="550"></p>


Karşımıza yeni bir sayfa çıkıcak.Çıkan sayfada hazır bir kod var ve çalıştırdığımız zaman çevredeki wifi ağlarını çekim güçleriyle birlikte göstericek.


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20164152.png" width="550"></p>


### NOT:ESP32 modülüne kod atılacağı zaman Arduino IDE'de çalıştır (Upload) butonuna bastıktan sonra pencerenin alt kısmında 'Connecting..._____.....___' gibi bir bilgi çıkıcak.


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-28%20230749.png" width="550"></p>


### O esnada Esp32 modülünün üzerindeki 'Boot' butonunu basılı tutman gerek.Yüzdelik değerler (%4 gibi) çıkmaya başladığında bırakabilirsin.Yazdığım gibi yapmazsan kod modüle yüklenmezo yüzden bu kısma dikkat.İlk önce boot butonunun nerede olduğunu paylaşıyorum.


<p align="center"><img src="ESP32%20Pics/esp32_LI.jpg" width="550"></p>


### Kodun yüklendikten sonraki hali aşağıdaki gibi:


<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-29%20175155.png" width="550"></p>


Herşey yolunda gitmişse yukarıda paylaştığım görseller gibi bir sonuç alman gerek.Son olarak bu kod için Serial Monitor'ü açıp etraftaki wifi ağlarına bakman gerek (Serial Monitor'dan örnek görüntü aşağıda).


<p align="center"><img src="ESP32%20Pics/InkedAnnotation%202020-01-28%20164333_LI.jpg" width="550"></p>







