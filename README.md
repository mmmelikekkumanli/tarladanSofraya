# tarladanSofraya

**Tarladan Sofraya**, Melike Kumanlı ve Beyza Girgin tarafından oluşturulan bir projedir. Bu uygulama, doğa dostu ürünlerin satışını yapmayı amaçlar. Hem kendi bayimizin bulunduğu şehirlerde hizmet verirken, Türkiye genelinde kargo imkânı sunarak 81 ilden kullanıcılara ulaşmaktadır.

## Motivasyon

Bu projenin motivasyonu, organik ve doğa dostu ürünlere olan talebin arttığı günümüzde insanlara sağlıklı ve doğal yaşamı destekleyen ürünlere kolay erişim sağlamaktır. Uygulama, çevre dostu ürünlerin daha geniş bir kitleye ulaşmasını hedefler. Ayrıca, Türkiye’nin her köşesindeki kullanıcılara, kendi bayinizin bulunduğu şehirlerde olduğu gibi kaliteli ve doğal ürünler sunmayı amaçlar.

## Yapı Durumu

### Kullanıcı Arayüzü (UI)
- Ana ekran tasarımı tamamlandı.
- Ürün kategorileri ve detay sayfası işlevsel.
- Sepet ve ödeme işlemleri için temel tasarımlar mevcut.

### Kullanıcı Kayıt ve Giriş
- E-posta ile kullanıcı kaydı ve giriş işlemleri tamamlandı.

### Sipariş ve Kargo Takibi
- Sipariş oluşturma işlemi mevcut.
- Kullanıcılar, siparişlerini takip edebilir.

### Ödeme Sistemi
- Kredi kartı ile ödeme entegrasyonu sağlandı.

### Harita ve Lokasyon Özelliği
- Kullanıcılar, teslimat bölgesini seçerek ürünlerin gönderileceği şehirleri görebilir.
- Türkiye’nin 81 iline kargo gönderimi yapılabiliyor.
- Kullanıcılar, teslimat bölgesini ana ekran üzerinden yazarak kendileri oluşturabiliyor.

### Kod Stili
# main.dart
Main fonksiyonunda, asenkron işlemler yapılacağı için async/await kullanımı ile Firebase'in başlatılma süreci yönetilmiştir. Özellikle Firebase.initializeApp() işleminin tamamlanmasının beklenmesi, uygulamanın Firebase ile düzgün bir şekilde çalışmasını sağlamaktadır. Ayrıca, WidgetsFlutterBinding.ensureInitialized() çağrısı, Flutter'ın başlatılmadan önce gerekli işlemleri yapmasını sağlar ve bu sayede uygulamanın doğru bir şekilde başlatılması sağlanır.

<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/2d3981e3-0c28-4038-b3a8-de9a6362ca26" width="400" />
</div>

# home_page.dart
<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/cb6f0fd2-bdf9-4a0d-939b-34bea2373e14" width="400" />
</div>

Widget yapısında, **AppBar** widget'ındaki **Row** kullanımı, logo görselinin düzgün bir şekilde ortalanmasını sağlamaktadır. `mainAxisAlignment: MainAxisAlignment.center` ve `mainAxisSize: MainAxisSize.min` kullanımı, logonun doğru şekilde merkezde yer almasını sağlar. Ayrıca, **Drawer**, **body** ve **NestedScrollView** yapıları, kullanıcı arayüzünün düzenli ve kullanıcı dostu bir şekilde ayarlanmasına yardımcı olmuştur.

Renkler ve temalar açısından, `backgroundColor: Theme.of(context).colorScheme.surface` kullanımı, uygulamanın temaya bağlı renklerini doğru bir şekilde uygular ve böylece kullanıcı deneyimini tutarlı hale getirir.

### Fotoğraflarla Uygulama Çerçevesi
<h1> Giriş Kısmı </h1>
 Giriş ekranımız iki şekilde tasarlandı; üyeliği bulunanlar ve üyeliği bulunmayanlar için. Mail ile giriş yapan kullanıcının datası Firebase user kısmına kaydediliyor, bu kullanıcının aynı mail üzerinden iki defa kayıt olmasını engelliyor.
<p float="left">
  <img src="https://github.com/user-attachments/assets/2677f6c7-8f5c-4994-87ec-dc199861bb65" width="200" />
  <img src="https://github.com/user-attachments/assets/dfc48248-ec7c-405c-844d-a6808d195373" width="200" />
  <img src="https://github.com/user-attachments/assets/8f677c6a-3da8-487e-9b4d-857011aaf421" width="200" />
</p>
<h1>Drawer Kısmı </h1>
<p>
  Uygulamanın drawer kısmı oldukça sade ve net kullanıma uygun oluşturuldu. Logoyla bordo temaya renk verirken anasayfaya dönüş, ayarlar ve çıkış butonuyla işlevsellik oluşturuldu.
</p>
<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/7ac771a9-0b7d-4572-8f26-adc1135fe6f4" width="200" />
</div>
<h1>Home Page </h1>
<p> Ana sayfamız (home page) app barında logomuz ve sloganımıza yer verdik. Alt kısımdaysa kategörilerine  göre ürünlerimizi sıraladık. Anasayfada ürünler kullanıcıya fotoğrafları , isimleri ve fiyat bilgileri ve gramajlarıyla sunulmuştur. </p>
<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/724499d1-5948-40fc-9bc4-081749ad1f8e" width="200" />
</div>
<h1>Ürünlerimiz </h1>
<p> Alınacak ürün seçildiğinde kişinin karşısına ana sayfadan farklı olarak iki ayrı teslimat seçeneği sunulur. Seçtiği teslimat seçeneğine göre ekle kısmına tıklanarak sizi ödeme sayfasına atar.  </p>
<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/16f008f4-e8e3-444d-8c39-73ffcd1d8c3c" width="200" />
</div>
<h1>Ödeme Sayfası </h1>
<p> Kart bilgilerini doldurduğunuz halde onay alınarak ödemeniz alınır. Bu da Firebase de Firestore Database Siparişler kısmına kaydolur.  </p>
<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/332f66b0-31f2-4062-a125-ae85d4cebf37" width="200" />
</div>
<h1>Ödeme Onayı ve Fiş </h1>
<div style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/82ff5df7-68d2-45d4-bff7-a0fc2ce295f5" width="200" />
  <img src="https://github.com/user-attachments/assets/aa481291-0fd4-48d0-bc1e-15cdf9af032f5" width="200" />
 
### Kurulum
Bu projeyi çalıştırabilmek için aşağıdaki adımları takip edebilirsiniz.
### Gereksinimler
Flutter SDK: Flutter geliştirme ortamı yüklü olmalıdır.
Dart SDK: Flutter, Dart dilini kullanarak çalışır, bu nedenle Dart SDK da yüklü olmalıdır.
IDE (Entegre Geliştirme Ortamı): Flutter uygulamaları geliştirmek için bir IDE (örneğin, Visual Studio Code veya Android Studio) kullanmanızı öneririz.
### Lisans
Bu proje MIT Lisansı altında lisanslanmıştır. Daha fazla bilgi için LICENSE dosyasına göz atabilirsiniz.

### İlgili Projenin Drive ve Youtube Videosu Linki 

[<p> https://drive.google.com/drive/home </p>](https://drive.google.com/file/d/1AoDFl2lY0ooNZB6t54z9OdXohBBEch1O/view?usp=drive_link)](https://drive.google.com/file/d/1AoDFl2lY0ooNZB6t54z9OdXohBBEch1O/view?usp=drive_link)
https://www.youtube.com/watch?v=pn_d_GP-jwY](https://youtu.be/Dv9-WcPGFis)
</div>









