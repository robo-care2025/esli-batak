# Eşli Batak — Android uygulaması

Bu klasör, Eşli Batak oyununun Android projesidir. Oyun telefonda tam ekran açılır, internetsiz çalışır, dikey ekranda kalır ve kapatıp açınca kaldığın elden devam eder. Telefonun geri tuşu açık pencereyi kapatır.

APK'yı iki yoldan biriyle oluşturabilirsin. Bilgisayarına bir şey kurmak istemiyorsan 1. yol daha kolay.

## 1. yol: GitHub ile (kurulum gerektirmez)

1. github.com'da ücretsiz bir hesap aç.
2. Sağ üstteki **+** düğmesinden **New repository** seç. Ad olarak `esli-batak` yaz ve **Create repository** de.
3. Açılan sayfada **uploading an existing file** bağlantısına tıkla. Bu klasördeki her şeyi (gizli `.github` klasörü dahil) sürükleyip bırak, sonra **Commit changes** de.
   - Mac'te gizli klasörleri görmek için Finder'da `Cmd + Shift + .` tuşlarına bas.
4. Üstteki **Actions** sekmesine geç. "APK oluştur" işi kendiliğinden başlar. Başlamazsa soldan "APK oluştur"u seçip **Run workflow** de.
5. Yaklaşık 3–5 dakika sonra iş yeşil tik alır. İşe tıkla, sayfanın altındaki **Artifacts** kısmından `esli-batak-apk` dosyasını indir.
6. İnen zip'i aç, içindeki `app-debug.apk` dosyasını telefonuna at ve aç. Telefon "bilinmeyen kaynak" izni isterse bu dosya için izin ver.

## 2. yol: Android Studio ile

1. developer.android.com/studio adresinden Android Studio'yu kur.
2. **Open** ile bu klasörü aç. İlk açılışta gerekli dosyaları kendisi indirir (birkaç dakika sürebilir).
3. Telefonu USB ile bağla (telefonda Geliştirici seçenekleri > USB hata ayıklama açık olmalı) ve yeşil **Run** düğmesine bas. Ya da **Build > Build APK(s)** ile APK dosyası al.

## Oyunu değiştirmek

Oyunun tamamı tek bir dosyada: `app/src/main/assets/index.html`. Bu dosyayı değiştirip APK'yı yeniden oluşturman yeterli.

## Google Play'e koymak istersen

Buradaki APK kişisel kullanım içindir. Google Play için Android Studio'da **Build > Generate Signed Bundle / APK** ile imzalı bir paket (.aab) oluşturman ve bir Google Play geliştirici hesabı açman gerekir. Uygulama kimliği `com.eslibatak.app`; yayınlamadan önce kendine özel bir kimlikle değiştirmen iyi olur (`app/build.gradle` içindeki `applicationId`).
