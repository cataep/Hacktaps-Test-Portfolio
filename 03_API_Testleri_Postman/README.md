# 03_API_Testleri_Postman

Bu klasör, Hacktaps uygulamasına yönelik olarak Postman kullanılarak gerçekleştirilen API testlerini içermektedir.

Testler, uygulamanın alarm bildirim endpoint'i (`alarmuse/`) ve bait dosyalarına ait bağlantıların (`PDF`, `Word`, `QR`) erişilebilirliğini ölçmek amacıyla yapılmıştır.  
Ayrıca hata durumları, sistemin yanıt davranışları ve CSRF koruma mekanizması da gözlemlenmiştir.

---

## Klasör Özeti

| Klasör | Test Türü | Test Yöntemi | İçerik |
|-----------|--------------|------------------|----------|
| 03_API_Testleri_Postman/ | API Testi | Postman ile manuel istekler | alarmuse/ POST, bait linklerine GET, hata senaryoları, CSRF gözlemi |

---

## Klasör İçeriği

| Dosya Adı | Açıklama |
|-----------|----------|
| `api_test_senaryolari.md` | API test senaryoları ve sonuçlarının tablo halinde listesi |
| `hacktaps_api_collection.json` *(isteğe bağlı)* | Postman koleksiyonunun dışa aktarılmış hali |
| (isteğe bağlı) `postman_screenshot/` | Postman çıktılarının ekran görüntüleri klasörü |

---

## Uygulanan Testler

- `alarmuse/` endpointine POST isteği gönderildi
- Bait PDF, Word ve QR bağlantılarına GET ile erişim testleri yapıldı
- Silinmiş bait bağlantısına yapılan erişimde 404 yanıtı alındı
- Body’siz POST isteği ile sistemin hata yanıtı verdiği gözlemlendi
- Sahte User-Agent header’ı ile yapılan GET çağrısı test edildi
- CSRF koruma mekanizmasının aktif olduğu gözlemlendi: `csrftoken` ile `csrfmiddlewaretoken` eşleşmezse 403 Forbidden döndü
- Postman’in kendi Cookies sekmesinden gönderdiği token ile manuel girilen token çakışırsa istek başarısız oluyor

---

## Notlar

- Testler yalnızca `GET` ve `POST` metodlarını kapsar.  
- PUT/DELETE gibi metodlar veya dosya yüklemeleri uygulama yapısında desteklenmediğinden kapsam dışıdır.
- Tüm testler Postman üzerinden **manuel olarak** gerçekleştirilmiştir.
- CSRF gözlemi sırasında, sistemin token uyumsuzluğuna karşı 403 dönmesi güvenlik açısından olumlu değerlendirilmiştir.
- ### 🔍 Ek Gözlem:

- GET ile erişilen bait bağlantılarında sistemin izleme mekanizması tetiklenmiştir.
- `TC02-TC03-TC04` gibi baitlerde, sistem **alarm count** ve **alert icon** bilgilerini güncellemiştir.
- Bu testler, uygulamanın **pasif saldırı algılama mekanizmasının da işlediğini göstermektedir.**
- `TC05` testinde Bait terminate edildikten sonra bağlantıya erişim hâlâ sağlanabilmektedir. Bu, uygulamanın dosya erişim yetkilendirmesi veya silme sonrası kaynak temizliği mekanizmalarının eksik olduğunu gösterebilir. Güvenlik açığı olarak değerlendirilebilir.


