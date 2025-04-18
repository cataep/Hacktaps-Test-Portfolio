#  02_Manuel_Test_Senaryolari

Bu klasör, Hacktaps uygulamasında kullanıcı arayüzü üzerinden manuel olarak gerçekleştirilmiş test senaryolarını ve sonuçlarını içermektedir.

Testler, uygulamanın sızıntı tespiti işlevlerini doğrulamak amacıyla farklı bait türleri (Word, PDF, QR) ve erişim yolları kullanılarak uygulanmıştır.  
Tüm testler manuel olarak yürütülmüş, otomasyon veya API aracı kullanılmamıştır.

---

##  Klasör Özeti

|  Klasör |  Test Türü |  Test Yöntemi |  İçerik |
|-----------|--------------|------------------|----------|
| 02_Manuel_Test_Senaryolari/ | Fonksiyonel, Negatif | Manuel test (kullanıcı arayüzü üzerinden) | Bait oluşturma, erişim testleri, silme fonksiyonu, izleme doğruluğu |

---

##  Klasör İçeriği

| Dosya Adı | Açıklama |
|-----------|----------|
| `Test_Senaryolari.md` | Markdown formatında tüm manuel test senaryoları ve sonuçları |
| `manuel_test_raporu` | Tüm senaryoları içeren kapsamlı Word formatlı test raporu |


---

## Uygulanan Testler

- Word, PDF ve QR formatında bait dosyalarının oluşturulması
- Bu dosyalara farklı cihaz ve bağlantılarla erişilerek sistemin izleme davranışının test edilmesi
- Bait silme fonksiyonunun onaylı/onaysız davranışlarının test edilmesi
- IP adresine göre konum bilgisinin haritada doğru gösterilip gösterilmediğinin test edilmesi

---

##  Notlar

- Tüm testler manuel olarak, doğrudan Hacktaps arayüzü üzerinden gerçekleştirilmiştir.
- Bu bölümde **otomasyon, API ya da performans testi** yer almamaktadır.
- Uygulamanın harita üzerindeki IP-konum eşlemesi hatalı sonuç vermiştir. Bu test başarısız olarak işaretlenmiştir.

