# بررسی قیمت و تعداد اگهی هر موبایل برای انتخاب موبایل ارزان قیمت و با برند محبوب 

> **دانشجو:** حسین حصاری 
> **تاریخ:** 1405/3/25  
> **ابزارها:** Python · Pandas · BeautifulSoup · Matplotlib · BashScript · Seabor · CSV 

---
 🎯 داستان پروژه
 
برای خرید یک موبایل می خواهم بدانم که کدام برند ارزان تر و تعداد اگهی آن کمتر است؟
>برای همین بجای بررسی در ساعت ها با گرفتن اطلاعات و تحلیل آنها این موضوع را بفهمم.
---

## 📦 داده‌ها

- **منبع:** سایت دیوار — دسته بندی موبایل و تبلت
- **تعداد آگهی:** XXX سطر پس از پاک‌سازی
- **ستون‌ها:** `قیمت` `عنوان` `ادرس اگهی`
- **روش جمع‌آوری:** BeautifulSoup + Requests (اجرا به‌صورت Local)

---

## 🔍 نتایج کلیدی
### تعداد اگهی
پیدا کردن تعداد اگهی هر برند:

<img width="1200" height="600" alt="brand_counts_bar_plot" src="https://github.com/user-attachments/assets/79bfe6fc-c3f4-4046-a03f-dc4e3aebc33c" />

میانگین قیمت های هر برند:
<img width="1200" height="600" alt="average_prices_bar_plot" src="https://github.com/user-attachments/assets/cd2ffe8e-3129-4859-9949-b6c6c99bf9ae" />
---

## 🗂️ ساختار فایل‌ها

```
_example/HosseinHesari
├── scraper.py       ← مرحله ۱: استخراج داده (اجرا روی سیستم Local)
├── notebook.ipynb        ← مرحله ۲: Cleaning + EDA (اجرا در Google Colab)
├── dataset_sample.csv    ← نمونه خروجی scraper
├── run.sh ← فایل اجرای پروژه
├── README.md           
└── charts/
    ├── average_prices_bar_plot.png
    └── brand_counts_bar_plot.png
└── divar_requests_data/
  ├──ads_data_clean.json
  └── data.csvdata.csv
```

---

## ▶️ نحوه اجرا

### مرحله ۱ — استخراج داده (روی سیستم خودتان)

> ⚠️ این مرحله را **در Colab اجرا نکنید** — سایت‌های ایرانی IP خارجی را مسدود می‌کنند.

```bash
bash run.sh <-- اینجا میتوانید مدیریت کنید پروژه را
# نصب پیش‌نیازها
```

خروجی: با زدن گزینه های 1 و 2 که 1: اسکرپینگ سایت دیوار هست
2: ساخت فایل csv می باشد که فایل json ایجاد شده را تبدیل به csv می کند.
فایل ایجاد شده data.csv
### مرحله ۲ — تحلیل داده (در Google Colab)

1. فایل `data.csv` را در **Google Drive** آپلود کنید
2. فایل `notebook.ipynb` را در **Google Colab** باز کنید
3. مسیر فایل را در سلول بارگذاری تنظیم کنید
4. سلول‌ها را به ترتیب اجرا کنید
