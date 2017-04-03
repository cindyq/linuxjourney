# وضعیت‌های Power

## محتوای درس

باورش سخت است که ما از راه‌های کنترل وضعیت سیستم از طریق خط فرمان صحبت نکرده‌ایم‌،
اما وقتی از init صحبت می‌کنیم‌، در کنار مد‌هایی که به شروع سیستم می‌انجامند باید به
مد‌های مربوط به توقف سیستم نیز اشاره کنیم.

برای خاموش (shutdown) سیستم‌:

```
$ sudo shutdown -h now
```

سیستم را خاموش می‌کند، و می‌توانید تعیین کنید که در چه زمانی این اتفاق بیافتد.
می‌توانید زمان را به صورت چند دقیقه بعد از الان مشخص کنید که دستور عمل کنید:

```
$ sudo shutdown -h + 2
```

این دستور سیستم را دو دقیقه بعد خاموش می‌کند. همین‌طور شما می‌توانید سیستم را
restart هم بکنید:

```
$ sudo shutdown -r now
```    

و یا تنها از دستور reboot استفاده کنید:

```
$ sudo reboot
```

## تمرین

فکر می‌کنید وقتی سیستم‌تان را خاموش می‌کنید‌، چه اتفاقی برای init رخ می‌دهد؟

## سوالات آزمون

دستور مناسب برای خاموش کردن سیستم در ۴ دقیقه بعد چیست؟

## پاسخ آزمون

```
sudo shutdown -h +4
```