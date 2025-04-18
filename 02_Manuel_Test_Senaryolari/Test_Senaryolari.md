#  Manuel Test Senaryoları – Hacktaps

Bu dosya, Hacktaps uygulamasında kullanıcı arayüzü üzerinden manuel olarak uygulanan test senaryolarının listesini içermektedir.

---

##  Test Özeti

| Test ID | Açıklama | Beklenen Sonuç | Gerçek Sonuç | Durum |
|---------|----------|----------------|---------------|--------|
| FT-01 | Tuzaklı Word dosyası oluşturma | Dosya oluşturulmalı | Oluşturuldu | ✅ |
| FT-02 | Dosya farklı cihazda açıldığında iz bilgisi geliyor mu? | IP ve cihaz bilgisi gelmeli | Geldi | ✅ |
| FT-03 | Tuzaklı URL oluşturulup tıklanıyor mu? | Veriler izlenmeli | İzleme gerçekleşti | ✅ |
| NT-01 | Geçersiz dosya (ör. .exe) kullanımı | Sistem reddetmeli | Reddedildi | ✅ |
| NT-02 | Sistem güncelleme sırasında işlem yapılması | Uyarı verilmeli | Sayfa dondu | ❌ |
| NT-03 | Şifreli dosya testi | Test uygulanamamalı | Sistem dışı, uygulanamadı | ⛔ |

---

##  Notlar

- Tüm testler manuel olarak Hacktaps arayüzü üzerinden gerçekleştirilmiştir.
- Test sonuçları gözlem yoluyla belgelenmiş, herhangi bir otomasyon ya da API testi kullanılmamıştır.
- NT-03 numaralı test, sistemin dış kaynaklı dosya kabul etmemesi nedeniyle kapsam dışı bırakılmıştır.
