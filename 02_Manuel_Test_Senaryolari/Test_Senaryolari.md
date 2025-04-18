# 🧪 Manuel Test Senaryoları – Hacktaps

Bu dosya, Hacktaps uygulamasında manuel olarak uygulanan test senaryolarını içermektedir.  
Testler arayüz üzerinden yapılmış ve sızıntı tespit işlevleri gözlemlenmiştir.

---

## 📌 2. TEST SENARYOLARI ve SONUÇLARI

### 2.1 Fonksiyonel Testler

| Test No | Test Adı | Açıklama | Beklenen Sonuç | Gerçekleşen Sonuç | Durum |
|---------|----------|----------|----------------|--------------------|--------|
| 1 | Desteklenen dosya türleri | Uygulamanın ürettiği Word, PDF, QR bait dosyalarının oluşturulması | Dosyalar oluşturulabilmeli | Başarılı | ✅ |
| 2 | Word bait dosyası linkine erişim | Word bait linkine dış kaynaktan erişim denemesi | IP ve sistem bilgisi kaydedilmeli, alarm oluşturulmalı | Başarılı | ✅ |
| 3 | PDF bait dosyası linkine erişim | PDF bait linkine dış kaynaktan erişim denemesi | IP ve sistem bilgisi kaydedilmeli, alarm oluşturulmalı | Başarılı | ✅ |
| 4 | QR Kod ile erişim testi | QR Kod taratılarak linke mobil cihazdan erişildi | IP ve sistem bilgisi kaydedilmeli, alarm oluşturulmalı | Başarılı | ✅ |
| 5 | Onaylı Bait Silme | "Terminate this bait" butonu ile silme işlemi (onay kutusu işaretli) | Bait silinmeli ve sistemde listelenmemeli | Başarılı | ✅ |
| 6 | Onaysız Bait Silme | Onay kutusu işaretlenmeden silme butonuna tıklanması | Bait silinmemeli ve sistemde listelenmeli | Başarılı | ✅ |
| 7 | İzleme Doğruluğu Testi | IP adresi ve konum bilgisinin haritada gösterimi (Test ortamı: Samsung Galaxy A35 5G) | Konum doğru gösterilmeli | Başarısız (Konum yanlış) | ❌ |

---

## 📝 Gözlemler ve Öneriler

- Uygulama tarafından üretilen bait türlerinin tamamı sorunsuz çalışmaktadır.  
- Silme fonksiyonu hem onaylı hem onaysız olarak beklenen şekilde işlemektedir.  
- IP bilgisi izlenebilir durumda olsa da, **konum haritası yanlış sonuç verebilmektedir**.

🔧 **Öneri:**  
Konum doğruluğunun artırılması için IP verisinin daha güncel bir coğrafi veri tabanıyla eşleştirilmesi önerilmektedir.
