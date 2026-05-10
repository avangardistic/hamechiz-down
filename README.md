
<div align="center">

# 🍉 Hamechiz‑Down v6.3
### دانلودر جهانی و موتور جستجوی سبک

دانلود خودکار و آرشیو محتوا از صدها وب‌سایت با استفاده از **GitHub Actions**

[![GitHub stars](https://img.shields.io/github/stars/avangardistic/hamechiz-down?style=for-the-badge)](https://github.com/avangardistic/hamechiz-down)
[![GitHub forks](https://img.shields.io/github/forks/avangardistic/hamechiz-down?style=for-the-badge)](https://github.com/avangardistic/hamechiz-down)
[![GitHub license](https://img.shields.io/github/license/avangardistic/hamechiz-down?style=for-the-badge)](LICENSE)
[![GitHub Actions](https://img.shields.io/github/actions/workflow/status/avangardistic/hamechiz-down/hamechiz-down.yml?style=for-the-badge)](https://github.com/avangardistic/hamechiz-down/actions)

</div>

---

<div dir="rtl">

# 📥 درباره پروژه

**همه‌چیزدان (Hamechiz‑Down)** یک ابزار متن‌باز است که با استفاده از **GitHub Actions** امکان دانلود، آرشیو و جستجوی محتوا از اینترنت را فراهم می‌کند.

این ابزار می‌تواند بدون نیاز به سرور اختصاصی:

- 🎬 دانلود ویدیو از **YouTube**
- 📸 دانلود پست و ریل از **Instagram**
- 🎵 دانلود ویدیو از **TikTok**
- 🐦 دانلود ویدیو از **Twitter/X**
- 🤖 دانلود ویدیو از **Reddit**
- 🎧 دانلود موسیقی از **SoundCloud**
- 📱 دانلود فایل از **Telegram**
- 🛍️ دانلود **APK** از **Google Play**
- 🌐 آرشیو کامل صفحات وب
- 🔎 جستجو در یوتیوب و اینستاگرام

را انجام دهد.

تمام این عملیات با استفاده از **GitHub Actions Runner** انجام می‌شود و هیچ سرور جداگانه‌ای نیاز ندارد.

</div>

---

# ✨ ویژگی‌های نسخه 6.3

<div dir="rtl">

| قابلیت | توضیح |
|------|------|
| 📥 دانلود لینک مستقیم | دانلود هر فایل با قابلیت resume |
| 🎬 YouTube | کیفیت 4K، زیرنویس، پلی‌لیست، حذف اسپانسر |
| 📸 Instagram | پست، ریل، استوری، جستجوی هشتگ |
| 🎵 TikTok | دانلود بدون واترمارک |
| 🐦 Twitter/X | دانلود ویدیو و GIF |
| 🤖 Reddit | دانلود ویدیوهای پست |
| 🎧 SoundCloud | دانلود MP3 و پلی‌لیست |
| 📱 Telegram | دانلود فایل از کانال‌های عمومی |
| 🛍️ Google Play | دانلود APK |
| 🌐 Web Archive | ذخیره صفحات به فرمت MHTML |
| 🔎 Search Mode | جستجو در یوتیوب و اینستاگرام |
| 🖼 Thumbnail Gallery | تولید گالری HTML از نتایج |
| ✂️ File Split | تقسیم خودکار فایل‌های بزرگ |

</div>

---

# 🚀 شروع سریع

<div dir="rtl">

## مرحله 1 — فورک پروژه

روی دکمه **Fork** کلیک کنید.

## مرحله 2 — فعال کردن دسترسی نوشتن

```
Settings → Actions → General
```

گزینه زیر را فعال کنید:

```
Read and write permissions
```

## مرحله 3 — اجرای دانلود

</div>

---

# ▶️ اجرای Workflow

## روش 1 — رابط کاربری GitHub

1️⃣ تب **Actions**  
2️⃣ انتخاب **Hamechiz‑Down v6.3**  
3️⃣ کلیک روی **Run workflow**

---

## روش 2 — Commit Message

```bash
# دانلود ویدیو
git commit -m "download https://youtu.be/VIDEO_ID mode:youtube quality:1080" && git push

# دانلود فقط صدا
git commit -m "download https://youtu.be/VIDEO_ID audio-only" && git push

# دانلود از اینستاگرام
git commit -m "download https://instagram.com/p/XXXX mode:instagram" && git push

# جستجو در یوتیوب
git commit -m "search: آموزش پایتون" && git push

# جستجوی هشتگ اینستاگرام
git commit -m "search: #طبیعت" && git push
```

---

## روش 3 — API

```bash
curl -X POST \
-H "Authorization: Bearer TOKEN" \
-H "Accept: application/vnd.github+json" \
https://api.github.com/repos/OWNER/REPO/actions/workflows/hamechiz-down.yml/dispatches \
-d '{"ref":"main"}'
```

---

# 📝 پارامترهای قابل استفاده

<div dir="rtl">

| پارامتر | مثال | توضیح |
|-------|------|------|
| mode | mode:youtube | انتخاب پلتفرم |
| quality | quality:1080 | کیفیت ویدیو |
| subtitles | subtitles:true | دانلود زیرنویس |
| playlist | playlist:true | دانلود پلی‌لیست |
| search | search:python | حالت جستجو |

</div>

---

# 🔎 حالت جستجو

<div dir="rtl">

در حالت `search:` سیستم:

1️⃣ در یوتیوب یا اینستاگرام جستجو می‌کند  
2️⃣ نتایج را استخراج می‌کند  
3️⃣ گالری تصویری می‌سازد

فایل‌های خروجی:

```
search-results.json
gallery.html
```

</div>

---

# 🖼 مشاهده گالری

با فعال کردن **GitHub Pages**:

```
Settings → Pages
Source → main branch
```

گالری در آدرس زیر قابل مشاهده است:

```
https://USERNAME.github.io/REPO/gallery.html
```

---

# 🌐 سایت‌های پشتیبانی شده

- YouTube
- Instagram
- TikTok
- Twitter/X
- Reddit
- SoundCloud
- Telegram
- Google Play
- Twitch
- Vimeo
- Facebook
- Dailymotion
- Pinterest
- LinkedIn
- +1000 سایت دیگر توسط yt‑dlp

---

# 📁 ساختار خروجی

```
downloads/

video_title [id].mp4

video_folder/
video.zip

search-results.json

gallery.html
```

---

# ⚙️ حالت خروجی

| Mode | توضیح |
|-----|------|
| repo | ذخیره در ریپازیتوری |
| artifact | دانلود موقت از Actions |

---

# 🔐 کوکی یوتیوب

برای دانلود ویدیوهای محدود:

1️⃣ نصب افزونه

```
Get cookies.txt LOCALLY
```

2️⃣ استخراج cookies

3️⃣ افزودن در GitHub Secrets

```
Settings → Secrets → Actions
```

نام:

```
YOUTUBE_COOKIES
```

---

# ⚠️ محدودیت‌ها

<div dir="rtl">

- فضای رایگان GitHub حدود **۴GB**
- حداکثر زمان اجرا **۶ ساعت**
- فایل‌های بزرگ **۹۰MB** تقسیم می‌شوند

</div>

---

# 🛠 رفع مشکل

**Permission denied**

فعال کردن:

```
Settings → Actions → Read and write permissions
```

**Age restricted video**

اضافه کردن:

```
YOUTUBE_COOKIES
```

---

# 🤝 مشارکت

اگر ایده‌ای دارید:

- Issue باز کنید
- Pull Request ارسال کنید

---

# ⚠️ سلب مسئولیت

این پروژه برای اهداف آموزشی و شخصی توسعه داده شده است. کاربران مسئول رعایت قوانین پلتفرم‌ها هستند.

---

<div align="center">

اگر این پروژه برای شما مفید بود، به آن ⭐  بدهید.

</div>
```
