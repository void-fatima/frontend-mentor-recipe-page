<div align="center">

# 🍳 Recipe Page

یک صفحه رسپی تمیز، واکنش‌گرا و دسترس‌پذیر؛ پیاده‌سازی‌شده با HTML و CSS خالص.

[![HTML5](https://img.shields.io/badge/HTML5-semantic-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-responsive-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Frontend Mentor](https://img.shields.io/badge/Frontend_Mentor-challenge-3F54A3?style=for-the-badge&logo=frontendmentor&logoColor=white)](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm)

[مشاهده چالش](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm) · [مخزن GitHub](https://github.com/void-fatima/frontend-mentor-recipe-page)

</div>

---

## پیش‌نمایش

![نمای دسکتاپ صفحه رسپی](./design/desktop-design.jpg)

این پروژه راه‌حل چالش **Recipe Page** از Frontend Mentor است. هدف، ساخت صفحه‌ی دستور پخت املت بر اساس طرح مرجع و تمرین ساختار معنایی HTML، طراحی Mobile-first و Responsive Design بوده است.

## ویژگی‌ها

- طراحی واکنش‌گرا برای موبایل و دسکتاپ
- پیاده‌سازی Mobile-first با یک breakpoint مشخص
- استفاده از تگ‌های معنایی مانند `main`، `article`، `header`، `section`، `aside` و `footer`
- جدول معنایی برای نمایش اطلاعات تغذیه‌ای
- استفاده از فونت‌های محلی و بدون نیاز به اینترنت
- رنگ‌بندی مدیریت‌شده با CSS Custom Properties
- نام‌گذاری کلاس‌ها به سبک BEM
- بدون JavaScript، فریم‌ورک یا وابستگی خارجی

## تکنولوژی‌های استفاده‌شده

| تکنولوژی | کاربرد |
|---|---|
| HTML5 | ساختار معنایی محتوا |
| CSS3 | استایل‌دهی، فاصله‌گذاری و طراحی واکنش‌گرا |
| `@font-face` | بارگذاری فونت‌های محلی Outfit و Young Serif |
| CSS Variables | مدیریت یکپارچه پالت رنگ |
| Media Query | تغییر چیدمان در نمایشگرهای بزرگ‌تر |

## ساختار پروژه

```text
frontend-mentor-recipe-page/
├── assets/
│   ├── fonts/
│   │   ├── outfit/
│   │   │   ├── static/                   # وزن‌های ثابت فونت Outfit
│   │   │   ├── Outfit-VariableFont_wght.ttf
│   │   │   ├── OFL.txt                   # مجوز فونت
│   │   │   └── README.txt
│   │   └── young-serif/
│   │       ├── YoungSerif-Regular.ttf
│   │       └── OFL.txt                   # مجوز فونت
│   └── images/
│       ├── favicon-32x32.png             # آیکن تب مرورگر
│       └── image-omelette.jpeg           # تصویر اصلی رسپی
├── design/
│   ├── desktop-design.jpg                # طرح مرجع دسکتاپ
│   └── mobile-design.jpg                 # طرح مرجع موبایل
├── AGENTS.md                             # راهنمای دستیارهای کدنویسی
├── CLAUDE.md                             # راهنمای ابزارهای مبتنی بر Claude
├── index.html                            # ساختار و محتوای صفحه
├── preview.jpg                           # پیش‌نمایش اصلی چالش
├── README.md                             # مستندات اصلی مخزن
├── style-guide.md                        # رنگ‌ها، فونت‌ها و مشخصات طراحی
└── style.css                             # تمام استایل‌های صفحه
```

## ساختار صفحه

```text
body
├── main
│   └── article.recipe
│       ├── img.recipe__image
│       └── div.recipe__content
│           ├── header.recipe__header
│           │   ├── h1
│           │   └── p
│           ├── aside.preparation
│           │   ├── h2
│           │   └── ul
│           ├── section.recipe__section — Ingredients
│           ├── section.recipe__section — Instructions
│           └── section.recipe__section — Nutrition
│               └── table.nutrition-table
└── footer.attribution
```

## اجرای پروژه

این پروژه به نصب هیچ پکیجی نیاز ندارد.

1. مخزن را clone کنید:

   ```bash
   git clone https://github.com/void-fatima/frontend-mentor-recipe-page.git
   ```

2. وارد پوشه پروژه شوید:

   ```bash
   cd frontend-mentor-recipe-page
   ```

3. فایل `index.html` را مستقیماً در مرورگر باز کنید.

برای اجرای پروژه با Live Server نیز می‌توانید در VS Code روی `index.html` راست‌کلیک کرده و **Open with Live Server** را انتخاب کنید.

## رویکرد طراحی

استایل‌های پایه ابتدا برای نمایشگر موبایل نوشته شده‌اند. در عرض‌های `48rem` و بیشتر، media query ظاهر دسکتاپ را فعال می‌کند:

- پس‌زمینه‌ی صفحه به رنگ کرم تغییر می‌کند.
- کارت رسپی در مرکز صفحه قرار می‌گیرد.
- کارت دارای حداکثر عرض، padding و گوشه‌های گرد می‌شود.
- تصویر اصلی نیز گوشه‌های گرد می‌گیرد.

رنگ‌های اصلی پروژه داخل `:root` تعریف شده‌اند تا تغییر و نگهداری آن‌ها ساده باشد:

```css
:root {
  --white: hsl(0, 0%, 100%);
  --stone-100: hsl(30, 54%, 90%);
  --stone-600: hsl(30, 10%, 34%);
  --stone-900: hsl(24, 5%, 18%);
  --brown-800: hsl(14, 45%, 36%);
  --rose-50: hsl(330, 100%, 98%);
  --rose-800: hsl(332, 51%, 32%);
}
```

## نکات آموخته‌شده

- تفاوت بین محتوا در HTML و ظاهر در CSS
- انتخاب تگ مناسب بر اساس معنای محتوا
- ساخت لیست‌های مرتب و نامرتب
- ساخت جدول دسترس‌پذیر با `th` و `scope="row"`
- درک Box Model و مدیریت `margin`، `padding` و `border`
- استفاده از واحدهای نسبی مانند `rem` و `%`
- بارگذاری فونت محلی با `@font-face`
- پیاده‌سازی رابط واکنش‌گرا با media query

## دسترس‌پذیری

- تصویر اصلی دارای متن جایگزین توصیفی است.
- ترتیب عنوان‌ها از `h1` به `h2` ساختار منطقی صفحه را حفظ می‌کند.
- اطلاعات تغذیه‌ای در یک جدول معنایی قرار گرفته‌اند.
- `scope="row"` ارتباط عنوان هر ردیف با مقدار آن را برای screen reader مشخص می‌کند.
- کنتراست رنگ‌ها مطابق پالت ارائه‌شده در چالش در نظر گرفته شده است.

## منابع

- [Frontend Mentor Challenge](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm)
- [MDN Web Docs — HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [MDN Web Docs — CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)

## سازنده

ساخته‌شده توسط [@void-fatima](https://github.com/void-fatima) به‌عنوان بخشی از تمرین‌های Frontend Mentor.

---

<div align="center">

اگر این پروژه برایتان مفید بود، خوشحال می‌شوم به آن ⭐ بدهید.

</div>
