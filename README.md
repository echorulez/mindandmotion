# Mind & Motion

**Daha sağlıklı bir zihin için günlük alışkanlıklar.**

Mind & Motion; bilişsel egzersizleri, fiziksel hareketi ve günlük alışkanlık takibini bir araya getiren Türkçe bir web uygulamasıdır. PWA desteği sayesinde uyumlu cihazlarda ana ekrana eklenebilir ve ilk çevrimiçi açılışta önbellek hazırlandıktan sonra çevrimdışı kullanılabilir.

## Özellikler

- **Bugün:** Günlük program ve haftalık hedefler.
- **Çift Odak:** Görsel dikkat ve işlem hızı egzersizi.
- **Hafıza Sarayı:** Bellek stratejileri ve hatırlama çalışmaları.
- **Dizi Bulmaca:** Sayı ve harf dizileriyle akıl yürütme.
- **Yol Ustası:** Çoklu görev egzersizi.
- **Hareket rutini:** Yaşa ve kullanıcı geri bildirimine göre ayarlanan kuvvet ve denge hareketleri.
- **Yaşam:** Günlük alışkanlıklar ve risk faktörü kontrol listeleri.
- **İlerleme:** Bilişsel ölçümler ve egzersiz geçmişi.
- **Bilgi:** Uygulamanın amacı, bilimsel dayanakları ve sınırlılıkları.
- Mobil ekran desteği ve açık/koyu tema.

## Teknoloji ve dosyalar

HTML, CSS ve JavaScript ile geliştirilmiştir. Derleme adımı, sunucu tarafı uygulama veya veritabanı gerektirmez.

- [mindandmotion.html](./mindandmotion.html): Uygulamanın arayüzü ve işleyişi.
- [index.html](./index.html): Site kökünden uygulamaya yönlendirme.
- [manifest.webmanifest](./manifest.webmanifest): PWA adı, açılış adresi ve simgeleri.
- [sw.js](./sw.js): Çevrimdışı önbellek ve güncelleme yönetimi.
- [icons/](./icons): Kurulum simgeleri.
- [icon.svg](./icon.svg): Vektör simge.

## Yerelde çalıştırma

Python yüklüyse proje klasöründe:

```shell
python -m http.server 8000 --bind 127.0.0.1
```

Tarayıcıda <http://localhost:8000> adresini açın. Sunucuyu durdurmak için terminalde `Ctrl+C` kullanın.

PWA özelliklerini test etmek için dosyayı doğrudan açmak yerine localhost veya HTTPS üzerinden çalıştırın.

## GitHub Pages ile yayınlama

1. Proje dosyalarını GitHub deposunun köküne yükleyin. `icons` klasörünün yapısını koruyun.
2. Depoda **Settings → Pages** bölümünü açın.
3. **Source:** `Deploy from a branch` seçin.
4. Dosyaların bulunduğu dalı (örneğin `main`) ve `/(root)` klasörünü seçip kaydedin.
5. Yayın tamamlanınca Pages bölümündeki HTTPS adresini açın.

Proje deposu için adres genellikle `https://KULLANICI_ADI.github.io/DEPO_ADI/` biçimindedir. İlk ziyaret internet bağlantısı gerektirir.

## Telefona ekleme

- **Android / Chrome:** Tarayıcı menüsünden “Uygulamayı yükle” veya “Ana ekrana ekle”.
- **iPhone / Safari:** Paylaş menüsünden “Ana Ekrana Ekle”.

Menü adları cihaz ve tarayıcı sürümüne göre değişebilir. Çevrimdışı kullanım öncesinde uygulamayı internet bağlantısıyla açıp önbelleğin hazırlanmasını bekleyin.

Dış kaynak bağlantıları internet gerektirir. Google Fonts yüklenemezse cihazdaki yedek yazı tipleri kullanılır. Zamanlamaya duyarlı egzersizleri gerçek cihazda ve pil tasarrufu ayarlarını dikkate alarak test edin.

## Veriler ve gizlilik

Profil, egzersiz geçmişi ve takip bilgileri cihazdaki tarayıcının yerel depolamasında saklanır. Uygulama bu kayıtları bir sunucuya göndermez ve cihazlar arasında otomatik eşitlemez.

Tarayıcı/site verileri silinirse kayıtlar kaybolabilir. Farklı bir site adresinde veya tarayıcıda aynı kayıtlar otomatik olarak görünmez.

Yazı tipleri Google Fonts üzerinden yüklenir; bu nedenle uygulama çevrimiçiyken üçüncü taraf ağ istekleri oluşabilir.

### Ad değişikliği ve mevcut kayıtlar

Mevcut kullanıcı verilerini korumak için `brain-booster-v1` yerel depolama anahtarı değiştirilmemiştir. Önceden kurulmuş PWA'nın kimliğini korumak için manifestin `id` alanı da sabittir; bu alan bir açılış bağlantısı değildir. Yeni açılış dosyası `mindandmotion.html` dosyasıdır.

Kayıtların korunması için siteyi aynı protokol, alan adı ve port üzerinde kullanmaya devam edin. Uygulamanın adının veya dosya adının değişmesi tek başına kayıtları silmez.

## Güncellemeler

Uygulama dosyalarını güncelledikten sonra [sw.js](./sw.js) içindeki `CACHE_NAME` sürümünü artırın. Eski önbellekleri temizlemek için kullanılan `brain-booster-` öneki teknik uyumluluk amacıyla korunmuştur.

Çevrimiçi açılışlarda uygulama sayfası ağdan alınır; bağlantı yoksa önbellekteki kopya kullanılır. Yayın sonrası uygulamayı bir kez çevrimiçi açıp ardından uçak modunda yeniden açarak çevrimdışı kullanımı doğrulayın.

## Önemli not

Mind & Motion tanı koymaz, tedavi yerine geçmez ve herhangi bir hastalığı önleyeceğini garanti etmez. Ölçümler kişisel takibe yöneliktir; klinik değerlendirme yerine kullanılmamalıdır.

Günlük yaşamı etkileyen bilişsel belirtiler için bir sağlık uzmanına başvurun.
