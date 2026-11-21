# بازی تایم | Bazi Time

اپلیکیشن اندرویدی مدیریت گیم‌نت و بوفه؛ برای ثبت و مدیریت دستگاه‌ها، زمان بازی، هزینه‌ها، فروش بوفه و گزارش درآمد.

## ساخت APK با GitHub Actions

1. محتوای همین پوشه را در ریشه یک مخزن GitHub قرار دهید.
2. از تب **Actions** اجرای workflow با نام **Build Bazi Time Android APK** را بررسی کنید.
3. فایل `BaziTime-Android.apk` در بخش **Artifacts** قابل دریافت است.

برای انتشار نسخه رسمی با تگ (مثلاً `v1.1.0`)، ابتدا کلید امضای اندروید را بسازید و چهار Secret زیر را در مسیر **Settings → Secrets and variables → Actions** ثبت کنید:

- `ANDROID_KEYSTORE_BASE64`
- `ANDROID_KEYSTORE_PASSWORD`
- `ANDROID_KEY_ALIAS`
- `ANDROID_KEY_PASSWORD`

برای ساخت کلید روی ویندوز (یک‌بار اجرا کنید):

```powershell
keytool -genkeypair -v -keystore bazitime-release.jks -alias bazitime -keyalg RSA -keysize 2048 -validity 10000
[Convert]::ToBase64String([IO.File]::ReadAllBytes("bazitime-release.jks")) | Set-Clipboard
```

مقدار کپی‌شده را در `ANDROID_KEYSTORE_BASE64` قرار دهید؛ رمزها و نام مستعار را نیز در سه Secret دیگر وارد کنید. فایل keystore را در مخزن قرار ندهید. همان کلید باید برای تمام نسخه‌های بعدی حفظ شود تا به‌روزرسانی روی نسخه قبلی نصب شود.

## پیش‌نمایش

![نمای بازی تایم در محیط گیم‌نت](docs/bazitime-preview.png)
