#  Hacktaps Test Planı

## 1. Amaç

Bu test çalışmasının amacı, Hacktaps adlı sızıntı tespit uygulamasının temel fonksiyonlarını, güvenilirliğini ve kullanıcıya sunduğu takip mekanizmalarını test etmektir.  

## 2. Kapsam

Bu projede aşağıdaki özellikler test edilmiştir:  
- Tuzaklı dosya (Word/HTML) oluşturma ve açıldığında iz bilgisi iletimi  
- Tuzaklı URL ve QR kod oluşturma  
- Kullanıcıya IP adresi, cihaz bilgisi, lokasyon bildirimi yapılması  
- Bildirim mekanizmasının işleyişi  
- API erişimi (sadece gözlem; dışarıdan dosya yükleme desteklenmiyor)  
- Performans ve sınır testleri  

## 3. Hariç Tutulanlar

- Dış kaynaktan (örneğin Postman) dosya yükleme yapılamamaktadır.  
- Uygulama yalnızca kendi oluşturduğu içerikleri takip edebilmektedir.  
- Otomasyon testleri ve proxy testleri kapsam dışı bırakılmıştır (ayrı olarak yapılacaktır).

 ## 4. Kullanılan Yöntemler

- Manuel Test (fonksiyonel, negatif, pozitif senaryolar)
- API davranışı gözlemi (Postman kullanılarak API testi denemeleri)
- Performans Testi (Siege aracıyla temel yük testi)
- Güvenlik Gözlemi (Burp Suite ile trafik izleme planlanmaktadır)
- Otomasyon Testi (Selenium ile arayüz testi planlanmaktadır)

> Not: Burp Suite ve Selenium testleri, projenin ilerleyen adımlarında bağımsız olarak eklenecektir.
> Burp Suite ile yapılacak güvenlik testleri yalnızca **pasif gözlem düzeyinde** gerçekleştirilecektir. 
Bu testlerde sistemin trafiği izlenecek, ancak doğrudan müdahalede bulunulmayacaktır. Bunun nedeni, uygulamanın sunucu tarafına erişim yetkimizin olmaması ve etik sınırların korunması gerekliliğidir.

> Selenium ile yapılacak testler yalnızca **sınırlı kullanıcı etkileşimi** içerecektir. Uygulamanın temel fonksiyonları (giriş, buton tıklama gibi) test edilecek, ancak dosyanın farklı cihazlarda açılmasıyla oluşan süreçler Selenium kapsamına girmemektedir.


## 5. Test Süreci

| Aşama | Süre | Açıklama |
|-------|------|----------|
| Planlama | 1 gün | Kapsam ve hedeflerin belirlenmesi |
| Senaryo yazımı | 1 gün | Fonksiyonel ve negatif senaryolar |
| Uygulama | 2 gün | Testlerin gerçekleştirilmesi |
| Raporlama | 1 gün | Sonuçların belge haline getirilmesi |

## 6. Roller

- Testçi: AYŞEGÜL SARICA
- Proje türü:  Portföy çalışması

## 7. Riskler

- Hacktaps uygulaması dış kaynaklı dosya yüklemesine izin vermediği için API test kapsamı sınırlıdır.
- Burp Suite gibi araçlarla yapılacak olan güvenlik testleri yalnızca pasif gözlem düzeyinde olacaktır.
- Selenium ile yapılacak otomasyon testleri sınırlı kullanıcı etkileşimini kapsayacaktır.

