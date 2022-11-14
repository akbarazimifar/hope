# نصب پلتفرم Xray 
در این مقاله کوتاه آموزش می‌دهیم که چگونه می‌توانیم پلتفرم Xray را بر روی لینوکس نصب کنیم. اگر دسترسی به لینوکس ندارید، می توانید برای تهیه سیستم لینوکسی به مستندات ما در این زمینه رجوع کنید.

پیش از پرداختن به قسمت بعدی لازم است اشاره کنیم که Xray به خودی خود هیچگونه رابط کاربری (User Interface) ندارد و ما مجبور خواهیم بود که برای ساخت اکانت به صورت دستی فایل‌های تنظیمات را تغییر دهیم. از آنجا که انجام این کار برای کاربران تازه‌کار کمی سخت خوهد بود، ما به جای نصب مستقیم Xray، [اپلیکیشنی به نام X-UI](https://github.com/vaxilu/x-ui) را نصب خواهیم کرد که در کنار نصب Xray به ما یک رابط کاربری بسیار راحت برای مدیریت کاربران خواهد داد. به طور مثال، در عکس زیر، داشبورد X-UI به شما خواهد گفت که منابع سیستم چگونه در حال استفاده هستند.

![image](https://user-images.githubusercontent.com/118040490/201552920-ed6eca0d-b89c-47ee-a4b3-c65a0b36b90a.png)

# نصب اپلیکیشن X-UI
خب، رسیدیم به اصل ماجرا. مجددا تاکید کنیم که از اینجا به بعد پیش‌فرض ما این هست که شما سیستم لینوکسی خود را تهیه کرده، آدرس IP سرور خود را می‌دانید و موفق شدید به آن SSH کنید. در اینجا فرض می‌کنیم آدرس IP شما مثلا 24.30.41.50 می‌باشد.

۱. ابتدا با دستور زیر، سطح اختیارات را بالا می‌بریم.

```bash
sudo -i
```


۲. با دستور زیر، بانک اطلاعاتی اپلیکیشن‌های لینوکس را به روز می‌کنیم.



```bash
apt update && apt upgrade -y
```


۳. با دستور زیر، فایل نصب X-UI را دانلود می‌کنیم.


```bash
wget https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh
```


۴. با دستور زیر، فایل نصب را اجرا می‌کنیم.


```bash
bash install.sh
```

۵. در جواب سوال 确认是否继续 (آیا مایل به ادامه هستید؟) دکمه y را بزنید.

۶. در جواب سوال 请设置您的账户名 (نام کاربری را مشخص کنید.) باید نام کاربری برای ورود به X-UI بسازید. می‌توانید از نامی مثل admin استفاده کنید.

۷. در جواب سوال 请设置您的账户密码 (رمز عبور را مشخص کنید.) باید رمزعبور را مشخص کنید. هر رمز عبور دلخواهی می‌توانید تعریف کنید. نام‌کاربری و رمزعبور را یادداشت کنید تا بعدا از آن برای ورود به X-UI استفاده کنیم.

۸. در جواب سوال 请设置面板访问端口 (پورت را مشخص کنید.) باید پورتی را مشخص کنیم که از آن برای وصل شدن به X-UI استفاده خواهیم کرد. پورت می‌تواند هر عددی بین 8000 تا 64000 باشد. مثلا می‌توانید پورت 34567 را انتخاب کنید.

۹. تمام. در اینجا کار تمام هست و شما X-UI را نصب کرده‌اید. پیامی شبیه زیر بر روی صفحه باید ظاهر شده باشد.

۱۰. در صورتی که همه چی موفقیت آمیز پیش‌ رفته باشد، حالا باید بتوانیم که X-UI را بر روی مرورگر Chrome و Edge باز کنیم. مثلا اگر آدرس IP سرور ما 24.30.41.50 باشد و پورت را 34567 انتخاب کرده باشیم، آنگاه آدرس http://{IP}:{PORT} را در مرورگر می‌توانیم وارد کنیم.



```bash
http://24.30.41.50:34567
```