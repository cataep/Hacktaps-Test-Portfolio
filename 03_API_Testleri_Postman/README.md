#  03_API_Testleri_Postman

Bu klasör, Hacktaps uygulamasına yönelik olarak Postman kullanılarak gerçekleştirilen API testlerini içermektedir.

Testler, uygulamanın alarm bildirim endpoint'i (`alarmuse/`) ve bait dosyalarına ait bağlantıların (`PDF`, `Word`, `QR`) erişilebilirliğini ölçmek amacıyla yapılmıştır.  
Ayrıca hata durumları ve sistemin yanıt davranışları da gözlemlenmiştir.

---

##  Klasör Özeti

|  Klasör | Test Türü |  Test Yöntemi |  İçerik |
|-----------|--------------|------------------|----------|
| 03_API_Testleri_Postman/ | API Testi | Postman ile manuel istekler | alarmuse/ POST, bait linklerine GET, hata senaryoları |

---

##  Klasör İçeriği

| Dosya Adı | Açıklama |
|-----------|----------|
| `api_test_senaryolari.md` | API test senaryoları ve sonuçlarının tablo halinde listesi |
| `hacktaps_api_collection.json` *(isteğe bağlı)* | Postman koleksiyonunun dışa aktarılmış hali |
| (isteğe bağlı) `postman_screenshot/` | Postman çıktılarının ekran görüntüleri klasörü |

---

##  Uygulanan Testler

- `alarmuse/` endpointine POST isteği gönderildi
- Bait PDF, Word ve QR bağlantılarına GET ile erişim testleri yapıldı
- Silinmiş bait bağlantısına yapılan erişimde 404 yanıtı alındı
- Body’siz POST isteği ile sistemin hata yanıtı verdiği gözlemlendi
- Sahte User-Agent header’ı ile yapılan GET çağrısı test edildi

---

##  Notlar

- Testler yalnızca `GET` ve `POST` metodlarını kapsar.  
- PUT/DELETE gibi metodlar veya dosya yüklemeleri uygulama yapısında desteklenmediğinden kapsam dışıdır.
- Tüm testler Postman üzerinden **manuel olarak** gerçekleştirilmiştir.
