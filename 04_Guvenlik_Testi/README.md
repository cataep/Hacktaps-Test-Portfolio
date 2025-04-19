# 04_Guvenlik_Testi

Bu klasör, Hacktaps uygulamasının temel güvenlik kontrollerine yönelik yapılan testleri içermektedir. Özellikle CSRF (Cross-Site Request Forgery) koruması sistem üzerinde manuel olarak test edilmiştir.

---

## 🛡️ Amaç
- Uygulamanın güvenlik mekanizmalarını anlamak
- CSRF korumasını test ederek form ve cookie token eşleşmesinin denetlenip denetlenmediğini gözlemlemek

---

## 🔧 Uygulanan Testler
- Geçerli token ile bait oluşturma isteği (200/302 beklenen)
- Token uyuşmazlığı içeren istek (403 Forbidden beklenen)
- Cookie içinde otomatik gelen `csrftoken` ile elle girilen `csrfmiddlewaretoken` farklıysa sistemin davranışı
- Postman'in Cookies sekmesi ile manuel header değerlerinin çakışması durumundaki sonuçlar

---

## 📊 Bulgular
- Uygulama, CSRF korumasını etkin şekilde uygulamaktadır
- Token uyumsuzluğu olduğunda sunucu 403 Forbidden yanıtı vermektedir
- Postman tarafından otomatik atanan token, testleri yanıltabileceği için console ve cookie gözlemi zorunludur

---

## 📁 Klasör İçeriği

| Dosya Adı | Açıklama |
|-------------|-----------|
| `csrf_guvenlik_testi.md` | Postman ve Burp Suite ile yapılan CSRF testinin detaylı açıklaması |
| (isteğe bağlı) `screenshots/` | Ekran görüntülerinin saklandığı dizin |

---

## 📚 Not
Bu test, manuel olarak yürütülen bir güvenlik testidir ve sistemde herhangi bir zaafiyet gözlemlenmemiştir. CSRF kontrollerinin başarıyla çalıştığı gözlemlenmiştir.

