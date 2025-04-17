# 🔍 Test Türleri – Hacktaps Uygulaması

Bu çalışmada aşağıdaki test türleri uygulanmıştır veya planlanmaktadır:

---

## 1. Fonksiyonel Testler

### 🎯 Amaç:
Uygulamanın temel işlevlerini doğru şekilde yerine getirip getirmediğini test etmek.

### 🧪 Hacktaps’e Uygulanışı:
- Tuzaklı dosya, URL ve QR kod oluşturulabiliyor mu?
- Bu içerikler başka cihazlarda açıldığında sistem doğru bilgi topluyor mu?
- Kullanıcıya doğru bildirim geliyor mu?

---

## 2. Negatif Testler

### 🎯 Amaç:
Sistem beklenmeyen veya hatalı durumlarda nasıl davranıyor? Hataları doğru yönetiyor mu?

### 🧪 Hacktaps’e Uygulanışı:
- Desteklenmeyen dosya formatları yüklendiğinde sistem uyarı veriyor mu?
- Sistem güncellemesi sırasında işlem yapılabiliyor mu?
- Şifreli dosyalar işlendiğinde sistem ne tepki veriyor?

---

## 3. API Testleri (Sınırlı)

### 🎯 Amaç:
API uç noktalarının doğru çalışıp çalışmadığını test etmek.

### 🧪 Hacktaps’e Uygulanışı:
- Postman kullanılarak API uç noktaları gözlemlendi.
- Sistem dışarıdan dosya kabul etmediği için doğrudan test yapılamadı.
- Yanıt kodları, veri biçimi ve hata mesajları incelendi.

---

## 4. Performans Testi

### 🎯 Amaç:
Sistem yüksek yük altında nasıl davranıyor? Yanıt süreleri ve hata oranları nelerdir?

### 🧪 Hacktaps’e Uygulanışı:
- Siege aracıyla 1000 eş zamanlı bağlantı testi yapıldı.
- Ortalama yanıt süresi, hata oranı gözlemlendi.
- Sistem belirli sınırların üzerinde yavaşlamaya başladı.

---

## 5. Güvenlik Testleri (Pasif Gözlem)

### 🎯 Amaç:
Sistemin temel güvenlik davranışlarını izlemek.

### 🧪 Hacktaps’e Uygulanışı:
- Burp Suite ile gelen/giden HTTP trafiği gözlemlendi (planlandı).
- İz bilgisi sunucuya giderken ne tür veri taşındığı gözlemlenecek.
- Aktif müdahale yapılmadan sadece gözlem yapılacaktır.

---

## 6. Otomasyon Testleri (Selenium)

### 🎯 Amaç:
Web arayüzünde tekrarlanan işlemleri otomatikleştirerek test etmek.

### 🧪 Hacktaps’e Uygulanışı:
- Giriş ekranı ve buton tıklama gibi temel arayüz işlemleri Selenium ile test edilmesi planlanmaktadır.
- Dosya açılması sonrası oluşan izleme süreçleri Selenium kapsamı dışındadır.
