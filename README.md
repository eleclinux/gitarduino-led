![arduino-led](https://user-images.githubusercontent.com/64849090/153049451-71a9f955-9e89-4214-a9d4-3811beed0b8b.png) 



پروژه بسیار ساده توسط میکروکنترلر Arduino Uno جهت یادگیری ابتدایی کار با این میکروکنترلر
در این پروژه یک LED 5mm قرمز رنگ به همراه یک مقاوت محدود کننده جریان توسط پایه شماره ۳ میکروکنترلر مدیریت خواهیم کرد

چرا گفته شد LED 5mm قرمز رنگ؟
میتوان از هر رنگ LED 5mm یا LED 3mm استفاده کرد فقط باید توجه داشت که هر رنگ از LED چه قرمز چه سبز ویا آبی یک میزان جریان تحمل می کنند بنابراین در درجه اول چه کار 
با LED و یا هر قطعه الکترونیکی باید به دیتاشیت آن قطعه که توسط سازنده آن تولید شده مراجعه و مطالعه کرد . وقی به دیتاشیت LED 5mm قرمز رنگ مراجعه میکنید متوجه میشید
که تحمل جریان هر رنگ با هر نوع ولتاژ مشابه متفاوت است.

چرا از مقاومت محدود کننده استفاده می کنیم؟
ابتدا اجازه دهید درباره جریان یا آمپر بیشتر بدانیم . جریان عبور بارهای الکتریکی از نقطه دارای انرژی پتانسیل بالاتر به نقطه دارای انرژی پتانسیل پایین تر گفته می شود
بگزارید با یک مثال ساده تر گفته بالا را آسان تر کنیم . تصور کنید یک مقدار آب جاری که از بالاترین نقطه (ولتاژ بیشتر) به سمت نقطه پایین تر (زمین یا ولتاژ کمتر) در حال 
جاری شدن است مثال آب جاری همان جریان است . حال چرا از محدود کننده جریان استفاده کنیم؟ در مثال بالا آب جاری را با سرعت بالا تصور کنید بنابراین اگر مابین دو نقطه پل
قرار داشته باشد به خاطر شدت بالای جریان آب پل ویران می شود چرا؟چون پل بر اساس یک میزان فشار آب طراحی و ساخته شد . حال برگردیم به برنامه اصلی در دیتا شیت LED 5mm 
گفته شده این نوع LED ها جریانی حدود 20 میلی آمپر را می توانند تحمل کنند و ولتاژ بین پایه ها حدود ۳ ولت است . LED همان پل روی آب است و آب همان جریان الکتریکی
پایه های Arduino Uno ولتاژی بین 0 تا 5 ولت می توانند تولید و خروج دهند اما در دیتاشیت LED گفته شد نهایتا 3 ولت پس بنابراین اگر LED را مستقیم به پایه متصل کنیم LED 
خواهد سوخت برای جلوگیری از سوختگی از محدود کننده جریان استفاده خواهیم کرد.

چطور تشخیص دهیم یک LED چه مقاومتی احتیاج دارد؟
قانونی هست به نام قانون اهم که هر مهندس برق و یا الکترونیک باید آن را بداند
قانون اهم فرمولی دارد    R=V/I
ولتاژ را با V    جریان را با I     و مقاومت را با R بر حسب اهم
در داده برگ LED گفته شد ولتاژ قابل تحمل 3 ولت است و میزان تحمل جریان آن 20 میلی آمپر
طبق فرمول    R=3v/20mA
جواب می شود 0.15 حال باید این عدد را تبدیل کنیم 3v/0.02A=150 ohm
برای تبدیل میل آمپر به آمپر به این صورت عمل می کنیم.
بنابراین مقاوت مورد نیاز جهت روشنایی LED طبق استاندار گفته شده 150ohm می باشد


