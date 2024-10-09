<p align="center">
  <a href="https://github.com/oXIIIo/marzban-template/" target="_blank" rel="noopener noreferrer">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Gozargah/Marzban-docs/master/screenshots/logo-dark.png">
      <img width="160" height="160" src="https://raw.githubusercontent.com/Gozargah/Marzban-docs/master/screenshots/logo-dark.png">
    </picture>
  </a>
</p>
<h1 align="center"/>تمپلیت های مختلف برای پنل  <a href="https://github.com/Gozargah/Marzban">مرزبان</a></h1>

# مقدمه
لیستی از تمپلیت های شخصی سازی شده برای مرزبان

# لیست تمپلیت ها
- [تمپلیت برای V2ray](https://github.com/mdjvd/marzban-template/tree/master/v2ray)
- [تمپلیت برای V2ray (with IPv6)](https://github.com/mdjvd/marzban-template/tree/master/v2rayWithIPv6)
- [تمپلیت برای Sing-Box](https://github.com/mdjvd/marzban-template/tree/master/singbox)
- [تمپلیت برای Sing-Box (with IPv6)](https://github.com/mdjvd/marzban-template/tree/master/singboxWithIPv6)
- [تمپلیت برای Clash](https://github.com/mdjvd/marzban-template/tree/master/singbox)
- [تمپلیت برای Mux](https://github.com/mdjvd/marzban-template/tree/master/mux)
- [صفحه سابسکریپشن (MuhammadAshouri)](https://github.com/mdjvd/marzban-template/tree/master/subscription)


# مراحل نصب
برای نصب هر تمپلیت به صفحه مربوط به آن مراجعه کنید

# نصب همه
برای نصب همه تمپلیت های موجو دستورات زیر را در ترمینال سرور خود اجرا کنید:
1. دانلود فایل های تمپلیت
```sh
sudo wget -N -P /var/lib/marzban/templates/v2ray/ https://raw.githubusercontent.com/mdjvd/marzban-template/master/v2ray/default.json
sudo wget -N -P /var/lib/marzban/templates/singbox/ https://raw.githubusercontent.com/mdjvd/marzban-template/master/singbox/default.json
sudo wget -N -P /var/lib/marzban/templates/clash/ https://raw.githubusercontent.com/mdjvd/marzban-template/master/clash/default.yml
sudo wget -N -P /var/lib/marzban/templates/mux/ https://raw.githubusercontent.com/mdjvd/marzban-template/master/mux/default.json
sudo wget -N -P /var/lib/marzban/templates/subscription/ https://raw.githubusercontent.com/mdjvd/marzban-template/master/subscription/index.html

```
2. دستورات زیر رو تو ترمینال سرورتون بزنید:
```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'V2RAY_SUBSCRIPTION_TEMPLATE="v2ray/default.json"' | sudo tee -a /opt/marzban/.env
echo 'SINGBOX_SUBSCRIPTION_TEMPLATE="singbox/default.json"' | sudo tee -a /opt/marzban/.env
echo 'CLASH_SUBSCRIPTION_TEMPLATE="clash/default.yml"' | sudo tee -a /opt/marzban/.env
echo 'MUX_TEMPLATE="mux/default.json"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
echo 'USE_CUSTOM_JSON_DEFAULT=True' | sudo tee -a /opt/marzban/.env
```
یا مقادیر زیر رو در فایل `.env` در پوشه `/opt/marzban` قرار بدین
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
V2RAY_SUBSCRIPTION_TEMPLATE="v2ray/default.json"
SINGBOX_SUBSCRIPTION_TEMPLATE="singbox/default.json"
CLASH_SUBSCRIPTION_TEMPLATE="clash/default.yml"
MUX_TEMPLATE="mux/default.json"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
USE_CUSTOM_JSON_DEFAULT=True
```

3. ری استارت مرزبان
```sh
marzban restart
```

## بروزرسانی
برای بروزرسانی تمپلیت ها فقط کافیست مرحله 1 را تکرار کنید.
