بازی تایم - نسخه اندروید

شناسه بسته: com.bazitime.app
نسخه: 1.1

ساخت APK با GitHub Actions:
1) پوشه‌ها و فایل‌های این پروژه را مستقیماً در ریشه Repository قرار دهید.
2) وارد زبانه Actions شوید.
3) گردش‌کار Build Bazi Time Android APK را اجرا کنید.
4) پس از موفقیت، فایل BaziTime-Android.apk را از بخش Artifacts دریافت کنید.

ساخت محلی:
پوشه android را در Android Studio باز کنید، Gradle Sync را انجام دهید و task زیر را اجرا کنید:
assembleDebug

فایل خروجی:
app/build/outputs/apk/debug/app-debug.apk

نکته:
- رابط برنامه از فایل android/app/src/main/assets/index.html بارگذاری می‌شود.
- داده‌های برنامه در فضای ذخیره‌سازی WebView روی همان دستگاه نگهداری می‌شوند.
- برای نگهداری امن اطلاعات، از قابلیت دریافت و بازیابی فایل پشتیبان داخل برنامه استفاده کنید.
