<h1 align="center">ESP32-tzelliot-</h1>

<h2 align="center">ESP32 Arduino IDE kurulum ve ilk kodlar</h2>




Merhabalar burada ingilizce kaynağının bile az olduğu ESP32 modülü hakkında bilgi vermeye çalışıcam.Öncelikle modülü Arduinp IDE'ye nasıl entegre edicez yani kodlarımızı ESP32 modülüne Arduino uygulamasından yükleyebilir vaziyete nasıl getiricez ondan bahsedicem.

![ESP32 Development Board WiFi+Bluetooth-1000x750](https://user-images.githubusercontent.com/36787074/54149000-55d60680-4446-11e9-95a9-e50eb726bd6d.jpg)

Arduino uygulamasının güncel olduğuna dikkat et.Güncel olmayınca yeni uygulamalarda/projelerde hatalarla karşılaşabilirsin.
Arduno'yu (uygulamayı) daha önce hiç yüklemediysen [buraya](https://www.arduino.cc/en/Main/Software) tıklayarak uygulamayı indirebileceğin siteye ulaşabilirsin.

Şimdi.Arduino'yu indirdiğine göre ESP32 modülünü Arduino IDE'de tanımlamamız lazım.Burdan sonra yapıcağımız işlemi daha önce ESP8266 için bi benzerini göstermiştim.O yazıyı okumuşsan yapacaklarımıza aşina olabilirsin.Değilsen de sıkıntı değil herşeyi en baştan burada yazmaya çalışıcam (Yazının sonuna doğru örnek uygulama ve kod var gözden kaçırmadığına dikkat et :D )okumaya devam.




![Annotation 2020-01-28 162244](https://github.com/Tzelal/ESP32-tzelliot/blob/master/ESP32%20Pics/Annotation%202020-01-28%20162244.png)



Devamında... ( Additional Board Manager URLs ) yazan yere aşağıdaki resimde olduğu gibi vericeğim linki kopyalayıp yapıştır.

>Eklenicek Kod:<br/>**https://dl.espressif.com/dl/package_esp32_index.json**


![Annotation 2020-01-28 162440](https://user-images.githubusercontent.com/36787074/73452487-0c9ee600-437b-11ea-8c69-9edaa5164ca1.png)


 NOT: Yukarıda paylaştığım link sayesinde sadece Esp32 modülü Arduino IDE'ye tanımlanabiliyor.Eğer daha önceden tanımlamış olduğun Esp8266 modülü varsa veya ileride kullanmayı düşünüyorsan yapman gereken Esp32 ile Esp8266 modüllerinin linklerini bir virgül ile ayırıp 'Additional Boards Manager URLs:' kısmında tanımlamak.Uygulanmış bir görseli aşağıda veriyorum.

Kopyalanıp yapıştırılacak link şu şekilde:
**https://dl.espressif.com/dl/package_esp32_index.json, http://arduino.esp8266.com/stable/package_esp8266com_index.json**



![Annotation 2020-01-28 162553](https://user-images.githubusercontent.com/36787074/73452560-2dffd200-437b-11ea-8f49-a181375a64f9.png)


Artık modüller Arduino'da tanımlı fakat bir yazılım daha yüklememiz lazım o da basit olmasına rağmen biraz zaman alabiliyor.Şimdi vakit kaybetmeden devam edelim.

![Annotation 2020-01-28 193918](https://user-images.githubusercontent.com/36787074/73452614-4374fc00-437b-11ea-9486-4d49ae53cdd5.png)



Yukardaki resimde olduğu gibi 'Boards Manager' kısmına tıkladığında karşına çıkıcak sayfada arama kısmına 'Esp' yazdığında Esp32 modülünü indirebileceğin seçenek direkt karşına çıkıcak.İlk aşamalardan biri olan 'Additional Board Manager URLs' kısmına yazdığın linke göre karşına Esp8266 modülünün indirme seçeneği de çıkabilir.İstersen ikisini de indirebilirsin,ben konu gereği sadece Esp32 modülünü indiricem (İkisini de indirmen ilerleyen aşamalarda sıkıntı yaratmaz).

![Annotation 2020-01-28 195851](https://user-images.githubusercontent.com/36787074/73452640-525bae80-437b-11ea-8a20-d03c2e99baf8.png)


'İnstall' butonuna tıkladıktan sonra biraz süre alıyor fakat Esp32 modülü kullanmaya hazır.<br/>
Evet.Şimdi Esp32 modülünü test etmek amaçlı Arduino IDE'de halihazırda yüklü olan 'wifi' örneğini deneyebiliriz.Fakat bunu için öncelikle 'ESP32 Dev Module' şıkkını seçmemiz lazım ki Arduino IDE'miz hangi modüle kodü atıcağını bilebilsin (Bu arada eğer farklı bir modül kullanıyorsan onu da burdaki seçeneklerden bulup seçebilirsin.Türkiye piyasasında bu modülün genelde sadece bir modülü satılıyor o da yukarıda yazdığım model.)

![Annotation 2020-01-28 162946](https://user-images.githubusercontent.com/36787074/73452678-67384200-437b-11ea-9fe1-117d5dfeb222.png)


Modülü seçtikten sonra olması gereken değerler aşağıdaki gibidir:

![Annotation 2020-01-28 201638](https://user-images.githubusercontent.com/36787074/73452696-761ef480-437b-11ea-8ff1-4b1dcc9afd5d.png)


Herşeyin yolunda gittiğini düşünüyorum.Deniyceğimiz örneğin bulunduğu yer aşağıdaki gibi:

![Annotation 2020-01-28 164013](https://user-images.githubusercontent.com/36787074/73452720-89ca5b00-437b-11ea-8e97-03fba0f513b4.png)


Karşımıza yeni bir sayfa çıkıcak.Çıkan sayfada hazır bir kod var ve çalıştırdığımız zaman çevredeki wifi ağlarını çekim güçleriyle birlikte göstericek.

![Annotation 2020-01-28 164152](https://user-images.githubusercontent.com/36787074/73452751-98187700-437b-11ea-888c-ac5cf253f523.png)


### NOT:ESP32 modülüne kod atılacağı zaman Arduino IDE'de çalıştır (Upload) butonuna bastıktan sonra pencerenin alt kısmında 'Connecting..._____.....___' gibi bir bilgi çıkıcak.

![Annotation 2020-01-28 230749](https://user-images.githubusercontent.com/36787074/73452774-a797c000-437b-11ea-9ec5-d3325e60e87c.png)


### O esnada Esp32 modülünün üzerindeki 'Boot' butonunu basılı tutman gerek.Yüzdelik değerler (%4 gibi) çıkmaya başladığında bırakabilirsin.Yazdığım gibi yapmazsan kod modüle yüklenmezo yüzden bu kısma dikkat.İlk önce boot butonunun nerede olduğunu paylaşıyorum.

![esp32_LI](https://user-images.githubusercontent.com/36787074/73452801-b41c1880-437b-11ea-9896-7f283099ca19.jpg)


### Kodun yüklendikten sonraki hali aşağıdaki gibi:

![Annotation 2020-01-29 175155](https://user-images.githubusercontent.com/36787074/73452837-cc8c3300-437b-11ea-95dd-a9ca0bfbe789.png)

<p align="center"><img src="ESP32%20Pics/Annotation%202020-01-29%20175155.png" width="550"></p>


Herşey yolunda gitmişse yukarıda paylaştığım görseller gibi bir sonuç alman gerek.Son olarak bu kod için Serial Monitor'ü açıp etraftaki wifi ağlarına bakman gerek (Serial Monitor'dan örnek görüntü aşağıda).

![InkedAnnotation 2020-01-28 164333_LI](https://user-images.githubusercontent.com/36787074/73452852-d877f500-437b-11ea-8155-b5233ad5341e.jpg)








