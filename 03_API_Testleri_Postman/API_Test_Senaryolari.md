#  API Test Senaryoları – Postman

Bu dosya, Postman kullanılarak Hacktaps uygulaması üzerinde gerçekleştirilen API test senaryolarını içermektedir.

---

## API Testleri 

| Test No | Test Adı | Açıklama | API Yöntemi | Beklenen Sonuç | Gerçekleşen Sonuç | Durum |
|---------|----------|----------|-------------|----------------|--------------------|--------|
| 1 | Bait Oluşturma | Kullanıcının bait oluşturma işlemi sırasında, 'triggers/' API’sine POST isteği gönderildi| POST | 200 OK | 200 OK | ✅ |
| 2 | PDF Dosya Linkine GET Çağrısı | Oluşturulan bait PDF linkine GET ile erişim | GET | 200 OK | 200 OK | ✅ |
| 3 | Word Dosya Linkine GET Çağrısı | Oluşturulan bait Word linkine GET ile erişim | GET | 200 OK | 200 OK | ✅ |
| 4 | QR Kod Linkine GET Çağrısı | Oluşturulan QR bait linkine GET ile erişim | GET | 200 OK | 200 OK | ✅ |
| 5 | Silinmiş Dosya Linkine Erişim | Terminate edilen bait dosyasının linkine GET çağrısı yapılması | GET | 404 Not Found | 404 Not Found | ✅ |
| 6 | Boş POST İsteği | `alarmuse/` endpointine body’siz POST isteği gönderildi | POST | 400 Bad Request | 400 Bad Request | ✅ |
| 7 | Sahte Header ile GET | GET isteğine özel User-Agent eklendi | GET | 200 OK (beklenen), davranış gözlemlenir | 200 OK | ✅ |

---

##  Notlar

- API testleri sadece `GET` ve `POST` yöntemleri üzerinden yapılmıştır.
- Dış kaynaklı dosya yükleme gibi işlemler uygulama tarafından desteklenmediği için kapsam dışı bırakılmıştır.
- Tüm testler Postman uygulaması kullanılarak manuel olarak uygulanmıştır.
