<p align="center">
  <a href="https://github.com/oXIIIo/marzban-template/" target="_blank" rel="noopener noreferrer">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Gozargah/Marzban-docs/master/screenshots/logo-dark.png">
      <img width="160" height="160" src="https://raw.githubusercontent.com/Gozargah/Marzban-docs/master/screenshots/logo-dark.png">
    </picture>
  </a>
</p>
<h1 align="center"/>MUX template for <a href="https://github.com/Gozargah/Marzban">Marzban</a></h1>

## فهرست مطالب
- [مقدمه](#مقدمه)
- [ویژگی‌ ها](#ویژگی-ها)
- [مراحل نصب](#مراحل-نصب)

# مقدمه
تمپلیت MUX

# ویژگی ها
- این تمپلیت خود مرزبانه که بعدش میتونید فایل رو با توجه به نیازتون تغییر بدین
و ...

# مراحل نصب
1. دانلود فایل template
```sh
sudo wget -N -P /var/lib/marzban/templates/mux/ https://raw.githubusercontent.com/mdjvd/marzban-template/master/mux/default.json
```
2. دستورات زیر رو تو ترمینال سرورتون بزنید:
```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'MUX_TEMPLATE="mux/default.json"' | sudo tee -a /opt/marzban/.env
```
یا از این طریق فایل را ادیت کرده و اضافه کنید
```sh
sudo nano /opt/marzban/.env
```
و مقادیر زیر رو در فایل `.env` در پوشه `/opt/marzban` قرار بدین
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
MUX_TEMPLATE="mux/default.json"
```

3. ری استارت مرزبان
```sh
marzban restart
```
در ادامه با این دستور میتونید ادیتش کنین ری استارت مرزبان هم نمی خواد
```sh
sudo nano /var/lib/marzban/templates/mux/default.json
```

## بروزرسانی
برای بروزرسانی تمپلیت فقط کافیست مرحله ۱ را تکرار کنید.

