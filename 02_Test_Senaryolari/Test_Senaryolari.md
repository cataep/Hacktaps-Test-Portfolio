# 🧪 Test Senaryoları

Hacktaps uygulaması için uygulanan test senaryoları aşağıdaki gibidir:

---

## ✅ 1. Fonksiyonel Testler

| Test ID | Açıklama | Beklenen Sonuç | Gerçek Sonuç | Durum |
|---------|----------|----------------|---------------|--------|
| FT-01 | Tuzaklı Word dosyası oluşturma | Dosya başarıyla oluşturulmalı | Oluşturuldu | ✅ |
| FT-02 | Oluşturulan dosyayı başka cihazda açma | IP, cihaz bilgisi alınmalı | Bilgiler geldi | ✅ |
| FT-03 | Tuzaklı URL oluşturma ve tıklama | Kullanıcı bilgileri yakalanmalı | Yakalandı | ✅ |

---

## ❌ 2. Negatif Testler

| Test ID | Açıklama | Beklenen Sonuç | Gerçek Sonuç | Durum |
|---------|----------|----------------|---------------|--------|
| NT-01 | Geçersiz formatta dosya yükleme (.exe) | Reddedilmeli | Reddedildi | ✅ |
| NT-02 | Sistem güncellemesi sırasında işlem | Uyarı verilmeli | Sayfa dondu | ❌ |
| NT-03 | Şifreli dosya açıldığında | Takip edilememeli | Takip edilmedi | ✅ |

---

## 🔄 3. API Testleri (Postman)

| Test ID | Açıklama | Beklenen Sonuç | Gerçek Sonuç | Durum |
|---------|----------|----------------|---------------|--------|
| API-01 | API endpoint gözlemi (GET /status) | 200 OK dönmeli | 200 OK | ✅ |
| API-02 | Dışarıdan dosya yükleme denemesi | 403 veya hata dönmeli | 403 Forbidden | ✅ |

---

## 🔁 4. Performans Testleri

| Test ID | Açıklama | Beklenen Sonuç | Gerçek Sonuç | Durum |
|---------|----------|----------------|---------------|--------|
| PT-01 | 1000 eş zamanlı kullanıcı yükü (Siege) | Sunucu yanıt vermeye devam etmeli | %97 başarılı istek | ⚠️ |
| PT-02 | Büyük dosya yükleme (100 MB) | Reddedilmeli veya zaman aşımı | Zaman aşımı | ✅ |

---

## 🛡️ 5. Güvenlik Testleri (Burp Suite - planlandı)

| Test ID | Açıklama | Beklenen Sonuç | Gerçek Sonuç | Durum |
|---------|----------|----------------|---------------|--------|
| SEC-01 | İzleme sırasında veri analizi | Trafik görüntülenebilmeli | Planlandı | ⏳ |
| SEC-02 | Header manipülasyonu | Sistem engellemeli | Planlandı | ⏳ |

---

## 🤖 6. Selenium Testleri (planlandı)

| Test ID | Açıklama | Beklenen Sonuç | Gerçek Sonuç | Durum |
|---------|----------|----------------|---------------|--------|
| SEL-01 | Giriş ekranı test | Doğru şifreyle giriş yapılmalı | Planlandı | ⏳ |
| SEL-02 | “Dosya oluştur” butonu tıklanabilirliği | Buton çalışmalı | Planlandı | ⏳ |
