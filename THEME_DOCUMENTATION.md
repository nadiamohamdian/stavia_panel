# استاویتا - تم پنل فروشنده

## نمای کلی

این تم برای پنل فروشنده استاویتا طراحی شده است و از Bootstrap 5 با پشتیبانی کامل از RTL (راست به چپ) و فونت‌های فارسی استفاده می‌کند.

## ویژگی‌ها

- ✅ **Bootstrap 5**: آخرین نسخه Bootstrap با تمام کامپوننت‌ها
- ✅ **RTL Support**: پشتیبانی کامل از راست به چپ
- ✅ **Bootstrap Icons**: آیکون‌های Bootstrap
- ✅ **Dark Mode**: حالت تاریک و روشن
- ✅ **Persian Fonts**: فونت‌های فارسی (IRANYekan, Vazirmatn)
- ✅ **Responsive**: طراحی واکنش‌گرا
- ✅ **Accessibility**: دسترسی‌پذیری

## فایل‌های تم

### 1. `theme-tokens.css`
فایل اصلی توکن‌های طراحی که شامل:
- رنگ‌های برند
- رنگ‌های متن
- رنگ‌های پس‌زمینه
- شعاع‌های مرزی
- سایه‌ها
- تایپوگرافی
- فاصله‌گذاری

### 2. `bootstrap-theme.css`
فایل تم Bootstrap 5 که شامل:
- متغیرهای CSS سفارشی Bootstrap
- پشتیبانی RTL
- کامپوننت‌های سفارشی
- حالت تاریک
- کلاس‌های کمکی

### 3. `vendor-panel-demo.html`
نمونه کامل استفاده از تم

## نصب و راه‌اندازی

### 1. اضافه کردن فایل‌های CSS

```html
<!-- Bootstrap 5 CSS -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

<!-- Custom Theme Files -->
<link rel="stylesheet" href="theme-tokens.css">
<link rel="stylesheet" href="bootstrap-theme.css">

<!-- Persian Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;700&display=swap" rel="stylesheet">
```

### 2. تنظیم HTML

```html
<html lang="fa" dir="rtl" data-bs-theme="light">
```

### 3. اضافه کردن JavaScript

```html
<!-- Bootstrap 5 JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
```

## رنگ‌های تم

### رنگ‌های اصلی
- **Brand**: `#0560FD` (آبی اصلی)
- **Brand Glow**: `#0091D0` (آبی درخشان)
- **Text**: `#0F1723` (متن اصلی)
- **Muted**: `#606060` (متن کم‌رنگ)
- **Background**: `#FFFFFF` (پس‌زمینه)
- **Elevated**: `#F6F7FB` (پس‌زمینه برجسته)
- **Soft**: `#ECF0FF` (پس‌زمینه نرم)
- **Border**: `#E5E7EB` (مرز)
- **Danger**: `#ED1C24` (خطر)

### شعاع‌های مرزی
- **Small**: `8px`
- **Medium**: `10px`
- **Large**: `20px`
- **Pill**: `9999px`

### سایه‌ها
- **Card**: `0 6px 16px rgba(0,0,0,.06)`
- **Brand Glow**: `0 0 10px #0091D0`

## کلاس‌های سفارشی

### دکمه‌ها

```html
<!-- دکمه برند -->
<button class="btn btn-brand">دکمه برند</button>

<!-- دکمه نرم -->
<button class="btn btn-soft">دکمه نرم</button>

<!-- دکمه با سایه برند -->
<button class="btn btn-brand brand-glow">دکمه درخشان</button>
```

### کارت‌ها

```html
<!-- کارت برجسته -->
<div class="card card-elevated">
  <div class="card-body">محتوای کارت</div>
</div>

<!-- کارت نرم -->
<div class="card card-soft">
  <div class="card-body">محتوای کارت</div>
</div>
```

### فرم‌ها

```html
<!-- ورودی برند -->
<input type="text" class="form-control form-control-brand" placeholder="متن...">

<!-- ورودی نرم -->
<input type="text" class="form-control form-control-soft" placeholder="متن...">
```

## حالت تاریک

### فعال‌سازی با JavaScript

```javascript
function toggleTheme() {
  const html = document.documentElement;
  const currentTheme = html.getAttribute('data-bs-theme');
  const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
  
  html.setAttribute('data-bs-theme', newTheme);
  localStorage.setItem('theme', newTheme);
}

// مقداردهی اولیه
document.addEventListener('DOMContentLoaded', () => {
  const savedTheme = localStorage.getItem('theme') || 'light';
  document.documentElement.setAttribute('data-bs-theme', savedTheme);
});
```

### فعال‌سازی با HTML

```html
<html data-bs-theme="dark">
```

## پشتیبانی RTL

تم به طور کامل از RTL پشتیبانی می‌کند:

```html
<html lang="fa" dir="rtl">
```

### تنظیمات RTL خودکار
- متن‌ها راست‌چین می‌شوند
- دکمه‌ها جهت‌بندی صحیح دارند
- منوهای کشویی در سمت راست باز می‌شوند
- فرم‌ها راست‌چین هستند

## آیکون‌ها

از Bootstrap Icons استفاده کنید:

```html
<i class="bi bi-house-door"></i>
<i class="bi bi-person"></i>
<i class="bi bi-gear"></i>
```

## نمونه‌های استفاده

### نوار ناوبری

```html
<nav class="navbar navbar-expand-lg navbar-light bg-white border-bottom">
  <div class="container-fluid">
    <a class="navbar-brand fw-bold" href="#">
      <i class="bi bi-shop me-2"></i>
      استاویتا
    </a>
    
    <div class="navbar-nav me-auto">
      <a class="nav-link active" href="#">
        <i class="bi bi-house-door me-1"></i>
        داشبورد
      </a>
    </div>
  </div>
</nav>
```

### کارت آمار

```html
<div class="card card-soft h-100">
  <div class="card-body text-center">
    <i class="bi bi-box-seam text-brand fs-1 mb-2"></i>
    <h5 class="card-title">۱۲۵</h5>
    <p class="card-text text-muted">محصول فعال</p>
  </div>
</div>
```

### جدول

```html
<div class="table-responsive">
  <table class="table table-hover">
    <thead>
      <tr>
        <th>شماره سفارش</th>
        <th>مشتری</th>
        <th>تاریخ</th>
        <th>وضعیت</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>#۱۲۳۴۵</td>
        <td>احمد محمدی</td>
        <td>۱۴۰۲/۱۰/۱۵</td>
        <td><span class="badge bg-success">تکمیل شده</span></td>
      </tr>
    </tbody>
  </table>
</div>
```

## سفارشی‌سازی

### تغییر رنگ‌ها

در فایل `theme-tokens.css`:

```css
:root {
  --brand: #0560FD;        /* رنگ اصلی */
  --brandGlow: #0091D0;    /* رنگ درخشان */
  --text-base: #0F1723;    /* متن اصلی */
  --bg-base: #FFFFFF;      /* پس‌زمینه */
}
```

### اضافه کردن کلاس جدید

در فایل `bootstrap-theme.css`:

```css
.btn-custom {
  --bs-btn-color: #FFFFFF;
  --bs-btn-bg: #YOUR_COLOR;
  --bs-btn-border-color: #YOUR_COLOR;
  /* سایر تنظیمات... */
}
```

## دسترسی‌پذیری

تم شامل ویژگی‌های دسترسی‌پذیری زیر است:

- پشتیبانی از `prefers-reduced-motion`
- پشتیبانی از `prefers-contrast: high`
- کلاس‌های `sr-only` برای متن‌های مخفی
- فوکوس قابل مشاهده
- پشتیبانی از چاپ

## مرورگرهای پشتیبانی شده

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## مجوز

این تم برای استفاده در پروژه استاویتا طراحی شده است.

## پشتیبانی

برای سوالات و پشتیبانی، با تیم توسعه تماس بگیرید.
