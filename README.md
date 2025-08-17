# Shayan.dev
Shayan.devیک سایت شخصی برای آموزش فناوری
<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <title>Shayan.dev</title>
  <style>
    body {
      font-family: 'Tahoma', sans-serif;
      background-color: #121212;
      color: #f0f0f0;
      margin: 0;
      padding: 0;
      direction: rtl;
    }

    nav {
      background-color: #1f1f1f;
      padding: 10px;
      position: relative;
    }

    .menu-icon {
      font-size: 24px;
      cursor: pointer;
      display: inline-block;
    }

    #menu-toggle {
      display: none;
    }

    .menu {
      display: none;
      list-style: none;
      padding: 0;
      margin-top: 10px;
    }

    #menu-toggle:checked + .menu-icon + .menu {
      display: block;
    }

    .menu li {
      padding: 8px 0;
    }

    .menu a {
      color: #f0f0f0;
      text-decoration: none;
    }

    section {
      padding: 20px;
      border-bottom: 1px solid #333;
    }

    h2 {
      color: #00ffcc;
    }

    h3 {
      color: #ffcc00;
    }

    p, li {
      line-height: 1.8;
    }
  </style>
</head>
<body>

  <nav>
    <input type="checkbox" id="menu-toggle">
    <label for="menu-toggle" class="menu-icon">&#9776;</label>
    <ul class="menu">
      <li><a href="#intro">معرفی</a></li>
      <li><a href="#htmlcss">HTML و CSS</a></li>
      <li><a href="#python">پایتون برای امنیت</a></li>
      <li><a href="#network">درک شبکه</a></li>
      <li><a href="#servers">سرورها</a></li>
      <li><a href="#linux">لینوکس</a></li>
      <li><a href="#security">امنیت سایبری</a></li>
    </ul>
  </nav>

  <section id="intro">
    <h2>Shayan.dev</h2>
    <p>من شایان هستم. اینجا سایت شخصی منه برای آموزش برنامه‌نویسی، امنیت، شبکه، و لینوکس. همه‌ی مطالب اینجا به زبان ساده و فارسی نوشته شدن تا هر کسی بتونه وارد دنیای واقعی فناوری بشه. خوش اومدی!</p>
  </section>

  <section id="htmlcss">
    <h2>کتاب اول: HTML و CSS</h2>
    <h3>فصل ۱: ساختار HTML</h3>
    <p>HTML زبان نشانه‌گذاریه که ساختار صفحه وب رو می‌سازه. با تگ‌هایی مثل &lt;p&gt;، &lt;img&gt;، &lt;a&gt; می‌تونی متن، تصویر و لینک بسازی.</p>
    <h3>فصل ۲: استایل‌دهی با CSS</h3>
    <p>CSS ظاهر صفحه رو کنترل می‌کنه. رنگ، فونت، فاصله، سایه، همه با CSS تنظیم می‌شن. مثال:</p>
    <pre>p { color: red; font-size: 18px; }</pre>
    <h3>فصل ۳: طراحی فرم‌ها</h3>
    <p>با تگ &lt;form&gt; می‌تونی فرم بسازی برای ورود اطلاعات. مثل ایمیل، رمز، دکمه ارسال.</p>
    <h3>فصل ۴: ریسپانسیو کردن سایت</h3>
    <p>با media query می‌تونی سایت رو برای موبایل و دسکتاپ بهینه کنی.</p>
  </section>

  <section id="python">
    <h2>کتاب دوم: پایتون برای امنیت</h2>
    <h3>فصل ۱: ساخت اسکریپت ساده</h3>
    <p>پایتون برای نوشتن ابزارهای امنیتی عالیه. مثال:</p>
    <pre>print("در حال تست رمز")</pre>
    <h3>فصل ۲: تست رمز با لیست</h3>
    <pre>
passwords = ["123456", "admin"]
for p in passwords:
    print("تست رمز:", p)
    </pre>
    <h3>فصل ۳: کار با فایل‌ها</h3>
    <p>می‌تونی فایل‌های متنی رو بخونی و بررسی کنی:</p>
    <pre>
with open("rockyou.txt") as f:
    for line in f:
        print(line.strip())
    </pre>
    <h3>فصل ۴: ارتباط با شبکه</h3>
    <p>با کتابخانه socket می‌تونی به سرور وصل بشی و داده بفرستی.</p>
  </section>

  <section id="network">
    <h2>کتاب سوم: درک شبکه</h2>
    <h3>فصل ۱: IP و DNS</h3>
    <p>IP آدرس هر دستگاهه. DNS مثل دفترچه تلفنه که اسم دامنه رو به IP تبدیل می‌کنه.</p>
    <h3>فصل ۲: Router و Port</h3>
    <p>Router مسیر رو مشخص می‌کنه. Port درگاه ارتباطیه. مثلاً پورت 80 برای وب.</p>
    <h3>فصل ۳: پروتکل‌ها</h3>
    <p>HTTP، FTP، SSH، TCP/UDP از پروتکل‌های مهم شبکه‌ان.</p>
  </section>

  <section id="servers">
    <h2>کتاب چهارم: سرورها</h2>
    <h3>فصل ۱: سرور چیه؟</h3>
    <p>سرور یه کامپیوتره که همیشه روشنه و درخواست‌ها رو جواب می‌ده. مثل سایت‌ها، ایمیل‌ها، دیتابیس‌ها.</p>
    <h3>فصل ۲: انواع سرور</h3>
    <ul>
      <li>Web Server</li>
      <li>Database Server</li>
      <li>Mail Server</li>
    </ul>
    <h3>فصل ۳: نصب سرور</h3>
    <p>با لینوکس و ابزارهایی مثل Apache یا Nginx می‌تونی سرور راه بندازی.</p>
  </section>

  <section id="linux">
    <h2>کتاب پنجم: لینوکس</h2>
    <h3>فصل ۱: لینوکس چیه؟</h3>
    <p>سیستم‌عاملی رایگان، امن، و قابل کنترل با ترمینال. مناسب برای سرورها و هکرها.</p>
    <h3>فصل ۲: دستورات پایه</h3>
    <pre>
ls      # لیست فایل‌ها
cd      # رفتن به پوشه
rm      # حذف فایل
mkdir   # ساخت پوشه
sudo    # اجرای دستور با دسترسی بالا
    </pre>
    <h3>فصل ۳: توزیع‌ها</h3>
    <p>Ubuntu، Kali Linux، Debian، Arch از معروف‌ترین توزیع‌ها هستن.</p>
  </section>

  <section id="security">
    <h2>کتاب ششم: امنیت سایبری</h2>
    <h3>فصل ۱: امنیت یعنی چی؟</h3>
    <p>یعنی جلوگیری از نفوذ، خرابکاری، یا دزدی اطلاعات. هکر خوب کسیه که ضعف‌ها رو پیدا کنه.</p>
    <h3>فصل ۲: حملات رایج</h3>
    <ul>
      <li>XSS</li>
      <li>SQL Injection</li>
      <li>Brute Force</li>
    </ul>
    <h3>فصل ۳: ابزارهای تست نفوذ</h3>
    <p>Kali Linux، Nmap، Burp Suite، Hydra، John the Ripper</p>
    <h3>فصل ۴: اخلاق هک</h3>
    <p>هک باید با اجازه و برای آموزش یا محافظت باشه. هک بدون اجازه = جرم.</p>
  </section>

</body>
</html>
