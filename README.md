# ESP32-tzelliot

**ESP32 Arduino IDE Kurulum**


Merhabalar burada ingilizce kaynağının bile az olduğu ESP32 modülü hakkında bilgi vermeye çalışıcam.Öncelikle modülü Arduinp IDE'ye nasıl entegre edicez yani kodlarımızı ESP32 modülüne Arduino uygulamasından yükleyebilir vaziyete nasıl getiricez ondan bahsedicem.

![ESP32 Development Board WiFi+Bluetooth-1000x750](https://user-images.githubusercontent.com/36787074/54149000-55d60680-4446-11e9-95a9-e50eb726bd6d.jpg)

Arduino uygulamasının güncel olduğuna dikkat et.Güncel olmayınca yeni uygulamalarda/projelerde hatalarla karşılaşabilirsin.
Arduno'yu (uygulamayı) daha önce hiç yüklemediysen [buraya](https://www.arduino.cc/en/Main/Software) tıklayarak uygulamayı indirebileceğin siteye ulaşabilirsin.

Şimdi.Arduino'yu indirdiğine göre ESP32 modülünü Arduino IDE'de tanımlamamız lazım.Burdan sonra yapıcağımız işlemi daha önce ESP8266 için bi benzerini göstermiştim.O yazıyı okumuşsan yapacaklarımıza aşina olabilirsin.Değilsen de sıkıntı değil herşeyi en baştan burada yazmaya çalışıcam (Yazının sonuna doğru örnek uygulama ve kod var gözden kaçırmadığına dikkat et :D )okumaya devam.



<p align="center"><img src="https://github.com/Tzelal/ESP32-tzelliot/blob/master/ESP32%20Pics/Annotation%202020-01-28%20162244.png" ></p>


Devamında... ( Additional Board Manager URLs ) yazan yere aşağıdaki resimde olduğu gibi vericeğim linki kopyalayıp yapıştır.

>Eklenicek Kod:**https://dl.espressif.com/dl/package_esp32_index.json**


<p align="center"><img src="https://github.com/Tzelal/ESP32-tzelliot/blob/master/ESP32%20Pics/Annotation%202020-01-28%20162440.png" ></p>

### NOT: Yukarıda paylaştığım link sayesinde sadece Esp32 modülü Arduino IDE'ye tanımlanabiliyor.Eğer daha önceden tanımlamış olduğun Esp8266 modülü varsa veya ileride kullanmayı düşünüyorsan yapman gereken Esp32 ile Esp8266 modüllerinin linklerini bir virgül ile ayırıp 'Additional Boards Manager URLs:' kısmında tanımlamak.Uygulanmış bir görseli aşağıda veriyorum.

Kopyalanıp yapıştırılacak link şu şekilde:
**https://dl.espressif.com/dl/package_esp32_index.json, http://arduino.esp8266.com/stable/package_esp8266com_index.json**



<p align="center"><img src="https://github.com/Tzelal/ESP32-tzelliot/blob/master/ESP32%20Pics/Annotation%202020-01-28%20162553.png" ></p>

Artık modüller Arduino'da tanımlı fakat bir yazılım daha yüklememiz lazım o da basit olmasına rağmen biraz zaman alabiliyor.Şimdi vakit kaybetmeden devam edelim.

<p align="center"><img src="https://github.com/Tzelal/ESP32-tzelliot/blob/master/ESP32%20Pics/Annotation%202020-01-28%20162244.png" ></p>
