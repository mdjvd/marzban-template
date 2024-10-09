<p align="center">
  <a href="https://github.com/oXIIIo/marzban-template/" target="_blank" rel="noopener noreferrer">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Gozargah/Marzban-docs/master/screenshots/logo-dark.png">
      <img width="160" height="160" src="https://raw.githubusercontent.com/Gozargah/Marzban-docs/master/screenshots/logo-dark.png">
    </picture>
  </a>
</p>
<h1 align="center"/>xray custom config with IPv6 for <a href="https://github.com/Gozargah/Marzban">Marzban</a></h1>

## فهرست مطالب
- [مقدمه](#مقدمه)
- [ویژگی‌ ها](#ویژگی-ها)
- [مراحل نصب](#مراحل-نصب)

# مقدمه
تمپلیت کاستوم کانفیگ بهینه شده برای کاربران داخلی
اگه همه سروراتون IPv6 داره و می‌خواید فعال بشه براتون این کانفیگ به کارتون میاد

# ویژگی ها
- وصل شدن مستقیم به وب‌سایت‌های داخلی هنگامی که فیلترشکن روشن است
- بلاک کردن تبلیغات
و ...

# مراحل نصب
1. دانلود فایل template
```sh
sudo wget -N -P /var/lib/marzban/templates/v2ray/ https://raw.githubusercontent.com/mdjvd/marzban-template/master/v2rayWithIPv6/default.json
```
2. دستورات زیر رو تو ترمینال سرورتون بزنید:
```sh
echo 'USE_CUSTOM_JSON_DEFAULT=True' | sudo tee -a /opt/marzban/.env
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'V2RAY_SUBSCRIPTION_TEMPLATE="v2ray/default.json"' | sudo tee -a /opt/marzban/.env
```
یا از این طریق فایل را ادیت کرده و اضافه کنید
```sh
sudo nano /opt/marzban/.env
```
و مقادیر زیر رو در فایل `.env` در پوشه `/opt/marzban` قرار بدین
```sh
USE_CUSTOM_JSON_DEFAULT=True
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
V2RAY_SUBSCRIPTION_TEMPLATE="v2ray/default.json"
```

3. ری استارت مرزبان
```sh
marzban restart
```

## بروزرسانی
برای بروزرسانی تمپلیت فقط کافیست مرحله ۱ را تکرار کنید.
