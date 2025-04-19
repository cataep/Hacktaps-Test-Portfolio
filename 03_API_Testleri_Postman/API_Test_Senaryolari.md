# API Test Senaryoları – Postman

Bu dosya, Postman kullanılarak Hacktaps uygulaması üzerinde gerçekleştirilen API test senaryolarını içermektedir.

---

## API Testleri

| Test No | Test Adı | Açıklama | API Yöntemi | Beklenen Sonuç | Gerçekleşen Sonuç | Durum |
|---------|----------|----------|-------------|----------------|--------------------|--------|
| TC01 | Yeni Bait Oluşturma | Kullanıcı, bait ismi girerek form aracılığıyla bait oluşturduğunda, sistem POST /en/triggers/ endpointini kullanarak kaydı tamamlar.| POST | 302 FOUND | 302 FOUND | ✅ |
| TC02 | PDF Dosya Linkine GET Çağrısı | Oluşturulan bait PDF linkine GET ile erişim | GET | 200 OK | 200 OK | ✅ |
| TC03 | Word Dosya Linkine GET Çağrısı | Oluşturulan bait Word linkine GET ile erişim | GET | 200 OK | 200 OK | ✅ |
| TC04 | QR Kod Linkine GET Çağrısı | Oluşturulan QR bait linkine GET ile erişim | GET | 200 OK | 200 OK | ✅ |
| TC05 | Silinmiş Dosya Linkine Erişim | Terminate edilen bait dosyasının linkine GET çağrısı yapılması | GET | 404 Not Found | 200 OK | ⚠️ |
| TC06 | Boş POST İsteği | `triggers/` endpointine body’siz POST isteği gönderildi | POST | 400 Bad Request | 200 OK | ⚠️ |
| 7 | Sahte Header ile GET | GET isteğine özel User-Agent eklendi | GET | 200 OK (beklenen), davranış gözlemlenir | 200 OK | ✅ |

---

## 🔐 Ek Gözlem: CSRF Token Uyumsuzluğu ve Güvenlik Davranışı

- Repeater ile elde edilen geçerli CSRF token'lar (`csrftoken` ve `csrfmiddlewaretoken`) Postman'de kullanıldığında 403 Forbidden yanıtı alındı.
- Postman’in kendi Cookies sekmesinden gönderdiği token değerleri, manuel girilenlerle çakıştığı için bu hata oluştu.
- Hata mesajında görülen gerçek `csrftoken` değeri hem Cookie hem de Body'de eşleştirildiğinde sistem 302 FOUND ile başarılı yanıt verdi.
- Bu test, uygulamanın aktif CSRF korumasına sahip olduğunu ve sahte ya da uyumsuz token'lı isteklere karşı etkili olduğunu göstermektedir.

  Test Stratejisi Notu

Yönlendirme (302 Found) içeren linklerde Postman’in "Automatically follow redirects" ayarı duruma göre değiştirilmiştir.

Redirect davranışı gözlemlenecekse: Ayar kapatılmıştır. Böylece doğrudan 302 yanıtı analiz edilmiştir.

Dosya içeriğine erişim amaçlıysa: Ayar açık bırakılmış ve nihai 200 OK yanıtı alınması hedeflenmiştir.

---

## Notlar

- API testleri sadece `GET` ve `POST` yöntemleri üzerinden yapılmıştır.
- Dış kaynaklı dosya yükleme gibi işlemler uygulama tarafından desteklenmediği için kapsam dışı bırakılmıştır.
- Tüm testler Postman uygulaması kullanılarak manuel olarak uygulanmıştır.
- ---

### 🔍 Test Notu:

- **TC02-TC03-TC04** testleri sırasında sistem, bait erişimini başarıyla algılamış ve **Alert Count** + **New Alert** alanlarında uyarı göstermiştir.
- Bu durum, sistemin alarm tetikleme ve izleme mekanizmasının **doğru çalıştığını pasif olarak doğrulamaktadır**.

 ### 🛑 TC05-Önemli Güvenlik Notu:
 Bait terminate edildikten sonra bağlantıya erişim hâlâ sağlanabilmektedir. Bu, uygulamanın dosya erişim yetkilendirmesi veya silme sonrası kaynak temizliği mekanizmalarının eksik olduğunu gösterebilir. Güvenlik açığı olarak değerlendirilebilir.

 ### TC06 Test Notu:

İlk denemede body tamamen boş bırakıldığında ve CSRF token da eksik olduğunda, sistem 403 Forbidden yanıtı vermiştir. Bu, güvenlik kontrolünün CSRF öncelikli olduğunu göstermektedir.

İkinci denemede geçerli bir csrfmiddlewaretoken gönderilmiş fakat body’de zorunlu alanlar (desc_text, submit vb.) eksik bırakılmıştır. Buna rağmen sistem 200 OK yanıtı vermiştir.

Bu durum, form doğrulamasının (validation) eksik olabileceğini veya yalnızca frontend seviyesinde kontrol yapıldığını göstermektedir.


