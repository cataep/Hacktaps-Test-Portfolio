#  02_Manuel_Test_Senaryolari

Bu klasör, Hacktaps sızıntı tespiti uygulamasının manuel olarak test edildiği senaryoları ve test raporlarını içermektedir. Tüm testler kullanıcı arayüzü (UI) üzerinden uygulanmış, herhangi bir otomasyon veya API testi yapılmamıştır.

---

## 📌 Genel Bilgi

| 📂 Klasör | 🧪 Test Türü | 🔧 Test Yöntemi | 📄 İçerik |
|-----------|--------------|------------------|----------|
| 02_Manuel_Test_Senaryolari/ | Fonksiyonel, Negatif | Manuel, kullanıcı arayüzü üzerinden | Dosya oluşturma, link izleme, geçersiz dosya senaryoları |

---

## 🧪 Uygulanan Testler

Bu bölümde test edilen başlıca işlevler şunlardır:

- Tuzaklı dosya (Word/HTML) oluşturulması
- Oluşturulan dosyanın farklı cihazlarda açılması
- Kullanıcının IP ve cihaz bilgilerinin Hacktaps tarafından izlenmesi
- QR kod ve URL takibi
- Şifreli ve geçersiz dosyaların sistem tarafından nasıl ele alındığı (Not: Hacktaps uygulaması sadece sistemin kendi oluşturduğu dosyalar üzerinden çalıştığı için harici dosya yüklemeye dayalı negatif senaryolar bu çalışmada kapsam dışı bırakılmıştır.)
- Sistem güncellemesi sırasında işlem yapılmaya çalışılması

---

## 📄 İçerikler

| Dosya Adı | Açıklama |
|-----------|----------|
| `test_senaryolari.md` | Markdown formatında tüm manuel test senaryolarının listesi |
| `test_raporu.docx`    | Resmî ve kapsamlı Word raporu (içindekiler, gözlemler, tablo vs.) |


---

## 🧭 Test Yöntemi

- Tüm testler, kullanıcı gibi davranılarak, Hacktaps arayüzü üzerinden manuel olarak gerçekleştirilmiştir.
- Her testte beklenen ve gerçek sonuçlar ayrı ayrı değerlendirilmiş, test sonuçları raporda tablo olarak sunulmuştur.
- Otomasyon ve API testleri bu bölümün dışında tutulmuş, ayrı klasörlerde ele alınacaktır.
