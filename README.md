# CodeStorm Eğitim Platformu Angular17

![GitHub Repo stars](https://img.shields.io/github/stars/berkerertan/Tobeto3A-BootcampProject-Angular)
![GitHub forks](https://img.shields.io/github/forks/berkerertan/Tobeto3A-BootcampProject-Angular)
![GitHub issues](https://img.shields.io/github/issues/berkerertan/Tobeto3A-BootcampProject-Angular)
![GitHub contributors](https://img.shields.io/github/contributors/berkerertan/Tobeto3A-BootcampProject-Angular)
![GitHub last commit](https://img.shields.io/github/last-commit/berkerertan/Tobeto3A-BootcampProject-Angular)

[Backend API ReadMe](https://github.com/berkerertan/Tobeto3A-NArchitecture.BootcampProject)

## Proje Açıklaması
Bu eğitim platformu, kullanıcılara çeşitli konularda online kurslar sunmak için tasarlanmıştır. Platform, kullanıcıların kayıt olmalarına, kurslara katılmalarına ve ilerlemelerini takip etmelerine olanak tanır.
## Özellikler
<table>
  <tr>
    <td>-Responsive Tasarım</td>
    <td>-Kullanıcı kayıt ve giriş sistemi</td>
  </tr>
  <tr>
    <td>-Hesap Güvenliği için Authorization</td>
    <td>-Rol Bazlı Erişim Kontrolü(Eğitmen, Öğrenci, Admin)</td>
  </tr>
  <tr>
    <td>-3 Kullanıcı türü tek giriş ekranı</td>
    <td>-Kurslar için Dinamik Arama, Pagination, Eğitmene göre listeleme</td>
  </tr>
  <tr>
    <td>-Kurs içeriklerini görüntüleme ve ilerlemeyi takip etme</td>
    <td>-Kullanıcı profili</td>
  </tr>
  <tr>
    <td>-Eğitim sonunda bitirme sertifikası</td>
    <td>-Admin ve Eğitmen Paneli</td>
  </tr>
  <tr>
    <td>-Karanlık Mod</td>
    <td>-Global Error Handler</td>
  </tr>
  <tr>
    <td>-Authorization Interceptor</td>
    <td>-Refresh Token ve Token Yenileme</td>
  </tr>
  <tr>
    <td>-Token İptali (Revoke Token)</td>
    <td>-JWT</td>
  </tr>
</table>

## Mimari Yapı
Bu proje, Özellik Bazlı Modüler Mimari (Feature-based Modular Architecture) yaklaşımını benimsemektedir. Bu mimari yapı, projenin daha iyi organize edilmesini ve yönetilmesini sağlar.

## Angular Dosya Yapısı
<p float="left">
  <img src="https://i.imgur.com/GJvxKJr.png" alt="Proje Görseli 1" width="400"/>
</p>

## Global Error Handler
<p float="left">
  <img src="https://i.imgur.com/cfZRgJK.png" alt="Proje Görseli 1" width="200"/>
</p>
Uygulamada oluşabilecek tüm hataları merkezi bir noktada yakalayarak kullanıcıya uygun mesajlar gösteriyoruz. Bu sayede hata yönetimi ve loglama işlemleri daha etkin bir şekilde yapılabiliyor. Kullanıcıya API'den gelen hata mesajları Toastr olarak gösterilir.

## Auth Interceptor
Authorization interceptor'ı, her HTTP isteğine otomatik olarak JWT token ekler ve yetkilendirme süreçlerini yönetir.

## Refresh Token/Token Yenileme ve Revoke Token
<p float="left">
  <img src="https://i.imgur.com/2RB0TbY.png" alt="Proje Görseli 1" width="800"/>
</p>
Refresh token kullanarak, kullanıcıların oturum sürelerini uzatıyoruz. Böylece kullanıcılar tekrar giriş yapmak zorunda kalmıyor.Kullanıcı çıkış yaptığında veya güvenlik ihlali durumunda, token iptal edilerek erişim engellenir. Refresh Token, HttpOnly Cookie olarak tutulur.

## Admin Panel Guard
<p float="left">
  <img src="https://i.imgur.com/9Crsfo2.png" alt="Proje Görseli 1" width="650"/>
</p>
AdminPanelGuard, admin yetkisine sahip kullanıcıların sadece yönetici paneline erişimini sağlamak için kullanılır. Bu guard, kullanıcının yetkilerini kontrol eder ve yetkisi olmayan kullanıcıları yönlendirir.

## Ana Sayfa ve Hakkımızda
<p float="left">
  <img src="https://i.imgur.com/5tyHvdt.png" alt="Proje Görseli 1" width="400"/>
  <img src="https://i.imgur.com/XYSdy6i.png" alt="Proje Görseli 2" width="400"/>
</p>

- Kullanıcılar için platform hakkında istatistiklerin ve bazı eğitimlerin gösterildiği sayfalar

## Tüm Kursların Listelenmesi ve Kurs Detay Sayfaları
<p float="left">
  <img src="https://i.imgur.com/9iiMo7s.png" alt="Proje Görseli 1" width="400"/>
  <img src="https://i.imgur.com/6SN7He1.png," alt="Proje Görseli 1" height="250"/>
</p>

- Dinamik arama, Eğitmen ismine göre listeleme, Pagination, tek sayfada gözüken kurs sayısını seçme özellikleri
- Sadece öğrenci statüsündeki hesap türlerinin ve başvuru süresi açık olan kurslara başvurma izini

## İletişim ve S.S.S 
<p float="left">
  <img src="https://i.imgur.com/TIxxXSz.png" alt="Proje Görseli 1" width="400"/>
  <img src="https://i.imgur.com/wWc5PWX.png" alt="Proje Görseli 2" width="400"/>
</p>

- Kullanıcıların site üzerinden iletişim için mail gönderebilme özelliği

## Giriş 
<p float="left">
  <img src="https://i.imgur.com/kRBAuUt.png" alt="Proje Görseli 1" width="400"/>
  <img src="https://i.imgur.com/sxFuC0Y.png" alt="Proje Görseli 2" width="400"/>
</p>

- 3 kullanıcı türü ile aynı yerden giriş yapabilme, Gece ve gündüz mod seçeneği LocalStorage'da depolanır kullanıcı tekrar giriş yaptığı zaman seçili mod ile devam eder.

## Öğrenci Kayıt Sayfası
<p float="left">
  <img src="https://i.imgur.com/CZoFjVj.png" alt="Proje Görseli 1" width="263"/>
  <img src="https://i.imgur.com/ogmGHp9.png" alt="Proje Görseli 1" width="263"/>
  <img src="https://i.imgur.com/dLBZDRC.png" alt="Proje Görseli 2" width="263"/>
</p>

- Dinamik Validasyon ile kullanıcının girdiği değerler anlık olarak takip edilir.

## Kullanıcı Türüne Göre Değişen NavBar 
<p float="left">
  <img src="https://i.imgur.com/iHjjBsC.png" alt="Proje Görseli 1" width="250"/>
  <img src="https://i.imgur.com/LM9334q.png" alt="Proje Görseli 2" width="250"/>
</p>

- LocalStorage'da JWT içerisinde ki role göre navbar değişir

## Mail
<p float="left">
  <img src="https://i.imgur.com/PdnjkZ1.png" alt="Proje Görseli 1" width="263"/>
  <img src="https://i.imgur.com/AdDGgLD.png" alt="Proje Görseli 1" width="263"/>
  <img src="https://i.imgur.com/arZn9sl.png" alt="Proje Görseli 2" width="263"/>
</p>

- Yeni kayıt olan öğrenci için Email doğrulama, Her giriş yapıldığında iki faktörlü kimlik doğrulaması, Şifremi Unuttum gibi durumlarda kullanıcıya mail gönderilir

## Admin ve Eğitmen Paneli
<p float="left">
  <img src="https://i.imgur.com/ZTg5828.png" alt="Proje Görseli 1" width="400"/>
  <img src="https://i.imgur.com/BYVWkx8.png" alt="Proje Görseli 2" width="400"/>
</p>

- Eğitmen ve Admin rollerine göre değişen panel yapısı
- Kurs, Eğitmen, Öğrenci, Chapter gibi tüm nesnelerin CRUD işlemlerinin yapılması

## Şifremi Unuttum ve Şifre Sıfırlama
<p float="left">
  <img src="https://i.imgur.com/54tpgVM.png" alt="Proje Görseli 1" width="400"/>
  <img src="https://i.imgur.com/ZtnfaJJ.png" alt="Proje Görseli 2" width="400"/>
</p>

- Şifresini unutan kullanıcılar için üzerinde Jwt token barındıran bir url oluşturulur ve kullanıcıya mail yoluyla gönderilir. Kullanıcı maildeki bu link üzerinden şifre sıfırlama sayfasına yönlendirilir. Yeni şifre oluşturulurken dinamik validasyon ile kullanıcı şifrenin uygunluğunu anlık olarak görebilir.

### İletişim
Bu proje hakkında herhangi bir sorunuz veya geri bildiriminiz varsa, lütfen bizimle iletişime geçin.

### Katkı
Bu projeye katkıda bulunmak istiyorsanız, lütfen aşağıdaki adımları izleyin:

Depoyu fork edin.
Yeni bir dal (branch) oluşturun: git checkout -b my-new-feature
Yaptığınız değişiklikleri commit edin: git commit -am 'Add some feature'
Dalınıza (branch) push edin: git push origin my-new-feature
Bir Pull Request oluşturun.

## Teşekkürler
