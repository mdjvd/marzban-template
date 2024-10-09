<p align="center">
  <a href="https://github.com/oXIIIo/marzban-template/tree/master/clash" target="_blank" rel="noopener noreferrer">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Clash-Mini/Clash.Mini/master/icon/Clash.Mini.ico">
      <img width="160" height="160" src="https://raw.githubusercontent.com/Clash-Mini/Clash.Mini/master/icon/Clash.Mini.ico">
    </picture>
  </a>
</p>
<h1 align="center"/>Clash Meta Config Example for <a href="https://github.com/Gozargah/Marzban">Marzban</a></h1>

## فهرست مطالب
- [ویژگی‌ ها](#ویژگی-ها)
- [مراحل نصب](#مراحل-نصب)
- [لینک دانلود کلش متا](#لینک-دانلود-کلش-متا)

# مقدمه
کلش متا یک پروکسی مبتنی بر قوانین است که به شما این امکان را می‌دهد که تنظیمات مربوط به برنامه از قبیل DNS و مسیریابی و ... را از سمت سرور انجام دهید. به عنوان مثال، می‌توانید از سمت سرور، کلش را به گونه‌ای تنظیم کنید که اتصال به سایت‌های ایرانی به صورت مستقیم انجام شود.

# ویژگی ها
- وصل شدن به سریع ترین کانفیگ
- وصل شدن به اولین کانفیگ سالم
- لودبالانس
- وصل شدن مستقیم به وب‌سایت‌های ایرانی هنگامی که فیلترشکن روشن است
- بلاک کردن تبلیغات
و ...

# مراحل نصب
1. دانلود فایل template
```sh
sudo wget -N -P /var/lib/marzban/templates/clash/ https://raw.githubusercontent.com/mdjvd/marzban-template/master/clash/default.yml
```

2. دستورات زیر رو تو ترمینال سرورتون بزنید:
```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'CLASH_SUBSCRIPTION_TEMPLATE="clash/default.yml"' | sudo tee -a /opt/marzban/.env
```
یا مقادیر زیر رو در فایل `.env` در پوشه `/opt/marzban` قرار بدین
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
CLASH_SUBSCRIPTION_TEMPLATE="clash/default.yml"
```

3. ری استارت مرزبان
```sh
marzban restart
```

## بروزرسانی
برای بروزرسانی تمپلیت فقط کافیست مرحله 1 را تکرار کنید.

# لینک دانلود کلش متا
- Android:
   - [FlClash](https://github.com/chen08209/FlClash/releases/latest)
   - [Clash. Meta for Android](https://github.com/MetaCubeX/ClashMetaForAndroid/releases/latest)
- iOS:
  - [MFI](https://t.me/meta_for_ios)
- Windows：
  - [FlClash](https://github.com/chen08209/FlClash/releases/latest)
  - [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev/releases/latest)
  - [clashN](https://github.com/2dust/clashN/releases/latest)
  - [v2rayN](https://github.com/2dust/v2rayN/releases/latest)
  - [Clash.Mini](https://github.com/MetaCubeX/Clash.Mini/releases/latest)
- Mac OS：
  - [FlClash](https://github.com/chen08209/FlClash/releases/latest)
  - [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev/releases/latest)
  - [ClashX.Meta](https://github.com/MetaCubeX/ClashX.Meta/releases/latest)
- Linux：
  - [FlClash](https://github.com/chen08209/FlClash/releases/latest)
  - [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev/releases/latest)
