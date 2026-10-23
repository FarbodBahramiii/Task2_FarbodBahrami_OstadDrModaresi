پروژه نُوا — ورود و ثبت‌نام با HTML/CSS/JavaScript و Supabase

فایل‌ها:
- LoginPage.html: صفحه ورود
- SignupPage.html: صفحه ثبت‌نام
- Dashboard.html: داشبورد محافظت‌شده
- style.css: طراحی ظاهری مشترک و واکنش‌گرا
- config.js: تنظیمات اتصال Supabase
- database.sql: نمونه ساخت جدول profiles و سیاست‌های دسترسی (RLS)

راه‌اندازی:
1) در Supabase یک پروژه بساز.
2) از Project Settings > API، Project URL و Publishable key را بردار.
3) فایل database.sql را در بخش SQL Editor پروژه Supabase اجرا کن تا جدول profiles و trigger ذخیره نام کاربری ساخته شود.
4) در config.js مقدار YOUR_SUPABASE_URL و YOUR_SUPABASE_PUBLISHABLE_KEY را با اطلاعات پروژه خودت جایگزین کن.
5) فایل‌ها را با VS Code باز کن و با افزونه Live Server اجرا کن (از روی file:// اجرا نکن).
6) برای ساخت حساب، SignupPage.html را باز کن. سپس با همان ایمیل و رمز در LoginPage.html وارد شو.

ذخیره اطلاعات:
- ایمیل و رمز عبور توسط Supabase Auth مدیریت می‌شوند.
- نام کاربری در user_metadata حساب Auth ذخیره می‌شود و در داشبورد خوانده می‌شود.
- فایل database.sql یک جدول profiles جداگانه با RLS نمونه دارد، اما نسخه فعلی صفحات به آن جدول متصل نیست؛ برای ذخیره نام کاربری در جدول profiles باید عملیات insert/select را به کد اضافه کرد یا trigger سمت دیتابیس ساخت.

نکته:
- اگر تأیید ایمیل در Supabase فعال باشد، پس از ثبت‌نام باید ایمیل را تأیید کنی و سپس وارد شوی.
- Publishable key برای کد مرورگر است؛ هرگز کلید secret/service_role را داخل فایل‌های HTML یا JavaScript قرار نده.
- این پروژه ساده و آموزشی است و شامل بازیابی رمز عبور یا تأیید ایمیل سفارشی نیست.
