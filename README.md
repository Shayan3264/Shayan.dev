<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>سایت شخصی شایان</title>
  <meta name="description" content="چهار کتاب آموزشی کامل HTML, CSS, Python, JavaScript نوشته شایان – از مقدماتی تا حرفه‌ای با مثال و تمرین" />
  <style>
    /* ====== پایه و دارک‌تم ====== */
    :root{
      --bg:#0e0f13;--panel:#171923;--panel-2:#1f2230;--text:#e6e6eb;--muted:#a2a7b7;--brand:#00c2d7;--brand-2:#4dd0e1;--code-bg:#0a0c12;--accent:#ffb020;--ok:#21d19f;--danger:#ff6b6b;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family:Tahoma, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Noto Sans", sans-serif;
      background:linear-gradient(180deg,var(--bg),#0b0c11 60%);
      color:var(--text); line-height:1.9; -webkit-font-smoothing:antialiased; text-rendering:optimizeLegibility;
    }
    a{color:var(--brand); text-decoration:none}
    a:hover{color:var(--brand-2)}

    header{
      position:sticky; top:0; z-index:10; backdrop-filter:saturate(160%) blur(8px);
      background:linear-gradient(180deg,rgba(23,25,35,.9),rgba(23,25,35,.6));
      border-bottom:1px solid #24273a;
    }
    .container{max-width:1100px; margin:0 auto; padding:1.25rem}
    .hero{display:flex; flex-direction:column; gap:.5rem; align-items:flex-start}
    .title{margin:0; font-size:1.65rem; color:var(--brand)}
    .subtitle{margin:0; color:var(--muted); font-size:.95rem}

    nav.links{display:flex; flex-wrap:wrap; gap:.5rem; margin-top:.5rem}
    nav.links a{background:var(--panel-2); border:1px solid #262a40; padding:.45rem .7rem; border-radius:999px; font-size:.9rem; color:#cdd2e0}
    nav.links a:hover{transform:translateY(-1px); box-shadow:0 6px 18px rgba(0,0,0,.25)}

    main{padding:2rem 0}
    section.book{background:var(--panel); border:1px solid #272a3f; border-radius:20px; padding:1.25rem; margin:1.25rem 0; box-shadow:0 10px 30px rgba(0,0,0,.25)}
    section.book>h2{display:flex; align-items:center; gap:.5rem; margin:.25rem 0 1rem; font-size:1.2rem; color:var(--brand-2)}

    .toolbar{display:flex; gap:.75rem; flex-wrap:wrap; align-items:center; margin-top:.75rem}
    .search{flex:1 1 260px; display:flex; align-items:center; gap:.5rem; background:var(--panel-2); border:1px solid #2a2d44; border-radius:14px; padding:.55rem .75rem}
    .search input{flex:1; background:transparent; border:0; color:var(--text); outline:none}
    .btn{background:var(--panel-2); border:1px solid #2a2d44; color:#e9ecf3; padding:.55rem .8rem; border-radius:12px; cursor:pointer}
    .btn:hover{filter:brightness(1.1)}

    details.chapter{background:#1b1e2b; border:1px solid #2a2d44; border-radius:14px; padding:0; margin:1rem 0; overflow:hidden}
    details.chapter[open]{box-shadow:0 8px 24px rgba(0,0,0,.3)}
    details.chapter summary{list-style:none; cursor:pointer; user-select:none; padding:1rem 1rem; background:linear-gradient(180deg,#1f2230,#1a1d29); display:flex; justify-content:space-between; align-items:center}
    details.chapter summary::-webkit-details-marker{display:none}
    .ch-title{font-weight:700; color:#cfe8ff}
    .badge{font-size:.75rem; color:#9fb1ff; background:#23263a; border:1px solid #2e3350; padding:.2rem .5rem; border-radius:8px}
    .ch-body{padding:1rem 1rem 1.1rem; display:grid; gap:1rem}

    h3{margin:0; color:#9ad5ff}
    p{margin:.2rem 0}
    ul{margin:.2rem 0 .4rem .8rem}

    pre{background:var(--code-bg); border:1px solid #23263d; border-radius:12px; padding:1rem; overflow:auto}
    code{font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace; color:#a9ffe6}

    .exercise{background:#1e2130; border:1px dashed #3a3f66; border-radius:12px; padding:1rem}
    .exercise h4{margin:.2rem 0 .6rem; color:var(--accent)}
    .exercise ol{margin:0 0 0 1rem}
    .tips{background:#15221e; border:1px solid #294a3d; border-radius:12px; padding:.8rem; color:#cfeadd}
    .warn{background:#2a1a1a; border:1px solid #503434; border-radius:12px; padding:.8rem; color:#ffdede}

    footer{border-top:1px solid #24273a; color:#9aa2b5; padding:2rem 0; text-align:center}

    @media (max-width:700px){
      .title{font-size:1.35rem}
      nav.links a{font-size:.85rem}
    }
  </style>
</head>
<body>
  <header>
    <div class="container hero">
      <h1 class="title">📚 کتابخانه آموزشی شایان</h1>
      <p class="subtitle">یادگیری HTML, CSS, Python, JavaScript — از مقدماتی تا حرفه‌ای + تمرین‌های پایانی هر فصل</p>
      <nav class="links">
        <a href="#book-html">HTML</a>
        <a href="#book-css">CSS</a>
        <a href="#book-py">Python</a>
        <a href="#book-js">JavaScript</a>
      </nav>
      <div class="toolbar">
        <div class="search">
          <span>🔎</span>
          <input id="q" placeholder="جستجو در مطالب و فصل‌ها..." />
        </div>
        <button class="btn" id="expand">بازکردن همه فصل‌ها</button>
        <button class="btn" id="collapse">بستن همه فصل‌ها</button>
      </div>
    </div>
  </header>

  <main class="container">
    <!-- ===================== کتاب HTML ===================== -->
    <section class="book" id="book-html">
      <h2>📘 کتاب HTML — از صفر تا حرفه‌ای</h2>
      
      <details class="chapter"><summary><span class="ch-title">فصل ۱: HTML چیست؟ ساختار پایه سند</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p>HTML مخفف <b>HyperText Markup Language</b> است و اسکلت هر صفحهٔ وب را تعریف می‌کند. مرورگرها این تگ‌ها را تفسیر کرده و ساختار محتوای شما را می‌سازند. هر سند HTML5 با <code>&lt;!DOCTYPE html&gt;</code> شروع می‌شود و دارای عناصر ریشه <code>&lt;html&gt;</code>، سربرگ <code>&lt;head&gt;</code> و بدنه <code>&lt;body&gt;</code> است.</p>
          <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="fa" dir="rtl"&gt;
  &lt;head&gt;
    &lt;meta charset="UTF-8" /&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1" /&gt;
    &lt;title&gt;سلام دنیا&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;سلام، من شایان هستم&lt;/h1&gt;
    &lt;p&gt;اولین صفحهٔ HTML من.&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;</code></pre>
          <div class="tips">نکته: ویژگی‌های <code>lang</code> و <code>dir</code> به موتورهای جستجو و فناوری‌های کمکی کمک می‌کند متن فارسی راست‌به‌چپ را درست نمایش دهند.</div>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>یک فایل <code>index.html</code> بساز و اسکلت بالا را پیاده کن.</li>
              <li>در بدنه یک <code>&lt;h1&gt;</code> با نام «شایان» و یک <code>&lt;p&gt;</code> معرفی کوتاه اضافه کن.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۲: متن‌ها، تیترها و عناصر معنایی</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p>تیترها با <code>&lt;h1&gt;..&lt;h6&gt;</code> و پاراگراف‌ها با <code>&lt;p&gt;</code> نوشته می‌شوند. از عناصر معنایی مانند <code>&lt;strong&gt;</code>، <code>&lt;em&gt;</code> و <code>&lt;mark&gt;</code> برای معنابخشی به متن استفاده کنید.</p>
          <pre><code>&lt;h1&gt;تیتر اصلی&lt;/h1&gt;
&lt;h2&gt;زیرتیتر&lt;/h2&gt;
&lt;p&gt;این یک &lt;strong&gt;متن مهم&lt;/strong&gt; با &lt;em&gt;تأکید&lt;/em&gt; است.&lt;/p&gt;
&lt;p&gt;می‌توانید بخشی را &lt;mark&gt;هایلایت&lt;/mark&gt; کنید.&lt;/p&gt;</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>یک صفحه «درباره من» بساز و با تیترها بخش‌بندی کن.</li>
              <li>سه پاراگراف با <code>strong</code> و <code>em</code> و <code>mark</code> اضافه کن.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۳: لینک‌ها، تصاویر و مسیرها</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p>لینک با <code>&lt;a href&gt;</code> و تصویر با <code>&lt;img src alt&gt;</code> نمایش داده می‌شود. از مسیر نسبی برای فایل‌های داخل پروژه و از مسیر مطلق برای آدرس‌های اینترنتی استفاده کنید.</p>
          <pre><code>&lt;a href="https://github.com/shayan" target="_blank" rel="noopener"&gt;گیت‌هاب شایان&lt;/a&gt;
&lt;img src="images/profile.jpg" alt="عکس شایان" width="180" /&gt;</code></pre>
          <div class="tips">از <code>alt</code> توصیفی برای دسترس‌پذیری استفاده کنید؛ صفحه‌خوان‌ها متن جایگزین را می‌خوانند.</div>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>یک گالری ساده با سه تصویر و کپشن زیر هر کدام بساز.</li>
              <li>دو لینک داخلی بساز که به بخش «تماس» و «کتاب‌ها» در همان صفحه بپرند.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۴: لیست‌ها و جدول‌ها</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>از <code>&lt;ul&gt;</code> (بدون ترتیب) و <code>&lt;ol&gt;</code> (دارای ترتیب) همراه با <code>&lt;li&gt;</code> برای آیتم‌ها استفاده می‌کنیم. جدول‌ها با <code>&lt;table&gt;</code>، سطر <code>&lt;tr&gt;</code>، سرستون <code>&lt;th&gt;</code> و سلول <code>&lt;td&gt;</code> ساخته می‌شوند.</p>
          <pre><code>&lt;ul&gt;
  &lt;li&gt;HTML&lt;/li&gt;
  &lt;li&gt;CSS&lt;/li&gt;
  &lt;li&gt;Python&lt;/li&gt;
&lt;/ul&gt;

&lt;table&gt;
  &lt;thead&gt;&lt;tr&gt;&lt;th&gt;کتاب&lt;/th&gt;&lt;th&gt;سطح&lt;/th&gt;&lt;/tr&gt;&lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;&lt;td&gt;HTML&lt;/td&gt;&lt;td&gt;مقدماتی&lt;/td&gt;&lt;/tr&gt;
    &lt;tr&gt;&lt;td&gt;CSS&lt;/td&gt;&lt;td&gt;میانی&lt;/td&gt;&lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>فهرست علاقه‌مندی‌هایت را با <code>ol</code> بساز.</li>
              <li>جدولی با سه ستون (درس، سطح، وضعیت) و چهار ردیف بساز.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۵: فرم‌ها، ورودی‌ها و اعتبارسنجی</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>فرم‌ها قلب تعامل کاربر هستند. از <code>&lt;form&gt;</code> به همراه ورودی‌ها (<code>input</code>، <code>textarea</code>، <code>select</code>) استفاده کنید. ویژگی‌هایی مثل <code>required</code>، <code>minlength</code>، <code>pattern</code> برای اعتبارسنجی سمت کاربر مفیدند.</p>
          <pre><code>&lt;form action="#" method="post"&gt;
  &lt;label&gt;ایمیل: 
    &lt;input type="email" name="email" required placeholder="you@example.com" /&gt;
  &lt;/label&gt;
  &lt;label&gt;پیام:
    &lt;textarea name="msg" minlength="10" required&gt;&lt;/textarea&gt;
  &lt;/label&gt;
  &lt;button type="submit"&gt;ارسال&lt;/button&gt;
&lt;/form&gt;</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>فرم «تماس با شایان» شامل نام، ایمیل، موضوع، پیام بساز.</li>
              <li>برای تلفن از <code>pattern</code> شماره ایرانی استفاده کن.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۶: عناصر HTML5 (ویدیو، صوت، تگ‌های معنایی)</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>HTML5 عناصر رسانه‌ای و معنایی جدیدی آورد: <code>&lt;header&gt;</code>، <code>&lt;nav&gt;</code>، <code>&lt;section&gt;</code>، <code>&lt;article&gt;</code>، <code>&lt;aside&gt;</code>، <code>&lt;footer&gt;</code>، همچنین <code>&lt;video&gt;</code> و <code>&lt;audio&gt;</code>.</p>
          <pre><code>&lt;video controls width="360"&gt;
  &lt;source src="media/intro.mp4" type="video/mp4" /&gt;
  مرورگر شما از ویدیو پشتیبانی نمی‌کند.
&lt;/video&gt;

&lt;audio controls&gt;
  &lt;source src="media/track.ogg" type="audio/ogg" /&gt;
&lt;/audio&gt;</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>صفحهٔ فرود با ساختار معنایی کامل بساز.</li>
              <li>یک ویدیوی معرفی ۱۰–۲۰ ثانیه‌ای اضافه کن.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۷: سئو پایه و دسترس‌پذیری (A11y)</span><span class="badge">حرفه‌ای</span></summary>
        <div class="ch-body">
          <p>برای سئو از عنوان توصیفی، توضیحات متا و سلسله‌مراتب صحیح تیترها استفاده کنید. برای دسترس‌پذیری: متن جایگزین تصاویر، نسبت کنتراست مناسب، و ترتیب فوکوس را رعایت کنید. ویژگی <code>aria-*</code> به درک بهتر نقش عناصر کمک می‌کند.</p>
          <pre><code>&lt;meta name="description" content="آموزش وب شایان" /&gt;
&lt;nav aria-label="ناوبری اصلی"&gt;...&lt;/nav&gt;
&lt;button aria-expanded="false" aria-controls="menu"&gt;منو&lt;/button&gt;</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>کنتراست رنگ‌ها را در صفحاتت بررسی کن (نسبت 4.5:1).</li>
              <li>برای سه دکمهٔ تعاملی صفت‌های ARIA مناسب قرار بده.</li>
            </ol>
          </div>
        </div>
      </details>
    </section>

    <!-- ===================== کتاب CSS ===================== -->
    <section class="book" id="book-css">
      <h2>🎨 کتاب CSS — از پایه تا حرفه‌ای</h2>

      <details class="chapter"><summary><span class="ch-title">فصل ۱: مبانی انتخاب‌گرها، واحدها و آبشار</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p>CSS ظاهر صفحه را کنترل می‌کند. مفاهیم کلیدی: انتخاب‌گر (selector)، ویژگی (property) و مقدار (value). آبشار (Cascade) و <i>Specificity</i> تعیین می‌کنند کدام قانون اعمال شود. از واحدهای واکنشی مثل <code>rem</code> و <code>%</code> استفاده کنید.</p>
          <pre><code>h1{color:#00c2d7}
.card{background:#1f2230; padding:1rem; border-radius:12px}
#main{max-width:1100px; margin:0 auto}</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>سه قانون با انتخاب‌گر نوع، کلاس و شناسه بنویس.</li>
              <li>تفاوت <code>px</code> و <code>rem</code> را با یک مثال نشان بده.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۲: Box Model، نمایش، جایگذاری</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p>هر عنصر یک جعبه است: <code>content → padding → border → margin</code>. ویژگی <code>box-sizing: border-box</code> مدیریت اندازه‌گیری را ساده‌تر می‌کند. با <code>display</code> نوع نمایش (block/inline/inline-block) و با <code>position</code> جایگذاری کنترل می‌شود.</p>
          <pre><code>.card{box-sizing:border-box; padding:16px; border:1px solid #2a2d44; margin:12px}</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>دو کارت بساز که اندازهٔ برابر ولی <code>padding</code> متفاوت دارند.</li>
              <li>یک نوار بالایی چسبان با <code>position: sticky</code> پیاده‌سازی کن.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۳: Flexbox در عمل</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>Flexbox چینش یک‌بعدی را آسان می‌کند: محور اصلی (main) و عمود (cross). از <code>display:flex</code>، <code>justify-content</code> و <code>align-items</code> استفاده کنید.</p>
          <pre><code>.row{display:flex; gap:12px; justify-content:space-between; align-items:center}
.row .item{flex:1 1 0; background:#1b1e2b; padding:1rem; border-radius:10px}</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>گرید کارت ۳ ستونه بساز که در موبایل ۱ ستونه شود.</li>
              <li>نوار ناوبری با آیتم‌های فاصله‌گرفته با <code>space-between</code> بساز.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۴: CSS Grid – گرید دو بعدی</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>Grid برای چینش دوبعدی عالی است. ردیف‌ها و ستون‌ها را با <code>grid-template-rows/columns</code> تعریف کنید و از <code>gap</code> برای فاصله‌ها بهره ببرید.</p>
          <pre><code>.grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:14px}
.card{background:#1e2130; padding:1rem; border-radius:12px}</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>صفحهٔ گالری واکنش‌گرا با Grid بساز.</li>
              <li>سربرگ دو ستونه (لوگو/منو) با ریسپانسیو گرید پیاده کن.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۵: تایپوگرافی، رنگ، متغیرها و تم تیره</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>از متغیرهای CSS برای مدیریت رنگ و تم استفاده کنید. نسبت کنتراست را رعایت کنید و از <code>@media (prefers-color-scheme)</code> برای همگام‌سازی با سیستم بهره ببرید.</p>
          <pre><code>:root{--bg:#0e0f13; --text:#e6e6eb}
@media (prefers-color-scheme: light){:root{--bg:#ffffff; --text:#111}}
body{background:var(--bg); color:var(--text)}</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>یک سوئیچر ساده «روشن/تاریک» با تغییر کلاس روی <code>body</code> بساز.</li>
              <li>خط‌کشی و سلسله‌مراتب تایپوگرافی برای h1..h6 تعریف کن.</li>
            </ol>
          </div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۶: انیمیشن و ترنزیشن، Performance</span><span class="badge">حرفه‌ای</span></summary>
        <div class="ch-body">
          <p>برای انیمیشن‌های روان از transform/opacity و <code>will-change</code> استفاده کنید. از <code>transition</code> برای تعاملات ظریف بهره ببرید و انیمیشن‌های سنگین را محدود کنید.</p>
          <pre><code>.btn{transition:transform .2s ease}
.btn:hover{transform:translateY(-2px)}</code></pre>
          <div class="exercise">
            <h4>تمرین</h4>
            <ol>
              <li>برای کارت‌ها انیمیشن ورود بساز (fade & slide).</li>
              <li>با DevTools هزینهٔ Repaint/Composite را بررسی کن.</li>
            </ol>
          </div>
        </div>
      </details>
    </section>

    <!-- ===================== کتاب Python ===================== -->
    <section class="book" id="book-py">
      <h2>🐍 کتاب Python — از مقدماتی تا حرفه‌ای</h2>

      <details class="chapter"><summary><span class="ch-title">فصل ۱: شروع سریع، نصب، اجرا</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p>پایتون زبانی خوانا و چندمنظوره است. کد را در فایل <code>.py</code> ذخیره و با دستور <code>python file.py</code> اجرا کنید.</p>
          <pre><code>print("سلام شایان!")
name = "Shayan"
print(f"Hello {name}")</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>برنامه‌ای بنویس که نام کاربر را بگیرد و خوش‌آمد بگوید.</li>
            <li>جمع دو عدد ورودی را نمایش دهد.</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۲: انواع داده، عملگرها، ورودی/خروجی</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p>انواع پایه: <code>int</code>، <code>float</code>، <code>str</code>، <code>bool</code>. تبدیل نوع با <code>int()</code>/<code>str()</code>. ورودی با <code>input()</code>.</p>
          <pre><code>a = int(input("عدد اول: "))
b = int(input("عدد دوم: "))
print("جمع:", a + b)</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>مبدل دما: سلسیوس ↔ فارنهایت.</li>
            <li>حسابگر مساحت دایره با ورودی شعاع.</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۳: شرط‌ها، حلقه‌ها و فهرست‌ها</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>با <code>if/elif/else</code> تصمیم‌گیری و با <code>for/while</code> تکرار انجام می‌شود. ساختارهای داده‌ای مانند <code>list</code> و <code>dict</code> بسیار پراستفاده‌اند.</p>
          <pre><code>nums = [1,2,3,4]
sq = [n*n for n in nums if n%2==0]
print(sq)  # [4, 16]</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>لیست اعداد ۱..۱۰۰ که بر ۳ بخش‌پذیرند تولید کن.</li>
            <li>یک فرهنگ‌لغت دانش‌آموز (نام→نمره) بساز و میانگین بگیر.</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۴: توابع، ماژول‌ها و مدیریت خطا</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>توابع با <code>def</code> تعریف می‌شوند. برای سازمان‌دهی از ماژول‌ها و پکیج‌ها استفاده کنید. خطاها را با <code>try/except</code> مدیریت کنید.</p>
          <pre><code>def safe_div(a,b):
    try:
        return a/b
    except ZeroDivisionError:
        return None</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>ماژولی با دو تابع ریاضی و یک تست کوتاه بنویس.</li>
            <li>ورودی کاربر را ایمن بخوان (اعتبارسنجی عدد صحیح).</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۵: برنامه‌نویسی شی‌ءگرا (OOP) و فایل‌ها</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>کلاس‌ها با <code>class</code> تعریف می‌شوند. برای کار با فایل‌ها از <code>with open()</code> استفاده کنید تا بسته‌شدن خودکار انجام شود.</p>
          <pre><code>class Book:
    def __init__(self, title, author):
        self.title=title; self.author=author
    def __repr__(self):
        return f"{self.title} - {self.author}"

with open('data.txt','w', encoding='utf-8') as f:
    f.write('سلام شایان')</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>کلاس «دانشجو» با متد محاسبهٔ معدل بساز.</li>
            <li>لیست کارها را از فایل بخوان و مرتب چاپ کن.</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۶: مجازی‌سازی، کتابخانه‌ها و پکیجینگ</span><span class="badge">حرفه‌ای</span></summary>
        <div class="ch-body">
          <p>بسته‌ها را با <code>pip</code> نصب کنید و محیط مجازی با <code>venv</code> بسازید. ساخت CLI ساده با <code>argparse</code>.</p>
          <pre><code># ساخت محیط مجازی
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install requests rich</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>ابزار خط‌فرمان ساده‌ای بساز که یک URL را گرفته و وضعیت پاسخ را چاپ کند.</li>
            <li>یک پکیج کوچک با ساختار استاندارد ایجاد کن.</li>
          </ol></div>
        </div>
      </details>
    </section>

    <!-- ===================== کتاب JavaScript ===================== -->
    <section class="book" id="book-js">
      <h2>⚡ JavaScript — از مقدماتی تا حرفه‌ای</h2>

      <details class="chapter"><summary><span class="ch-title">فصل ۱: آشنایی، اجرا در مرورگر و کنسول</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p>جاوااسکریپت زبان تعامل در وب است. کد را داخل تگ <code>&lt;script&gt;</code> یا فایل جداگانه قرار دهید.</p>
          <pre><code>&lt;script&gt;
  console.log('سلام شایان');
  alert('خوش آمدی!');
&lt;/script&gt;</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>پیغامی در کنسول چاپ کن و یک هشدار نمایش بده.</li>
            <li>دکمه‌ای بساز که روی کلیک شمارنده را افزایش دهد.</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۲: متغیرها، توابع و دامنه</span><span class="badge">مقدماتی</span></summary>
        <div class="ch-body">
          <p><code>let</code> و <code>const</code> را جایگزین <code>var</code> کنید. توابع معمولی و پیکانی هر دو کاربردی‌اند. دامنهٔ بلاک با <code>let/const</code> ایمن‌تر است.</p>
          <pre><code>const PI = 3.14;
let count = 0;
const add = (a,b) =&gt; a + b;</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>تابع پیکانی «حداکثر سه عدد» بنویس.</li>
            <li>تفاوت <code>let</code> و <code>const</code> را با نمونه نشان بده.</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۳: DOM و رویدادها</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>DOM نمای درختی از HTML است. با <code>querySelector</code> به عناصر دسترسی بگیرید و رویدادها را با <code>addEventListener</code> مدیریت کنید.</p>
          <pre><code>// HTML: &lt;button id="btn"&gt;کلیک&lt;/button&gt; &lt;p id="out"&gt;0&lt;/p&gt;
const btn = document.querySelector('#btn');
const out = document.querySelector('#out');
let n = 0;
btn.addEventListener('click', () =&gt; { out.textContent = ++n; });</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>Todo List ساده با افزودن/حذف آیتم بساز.</li>
            <li>ورودی متن را به‌صورت زنده در یک پیش‌نمایش نشان بده.</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۴: Async/Await و فراخوانی API</span><span class="badge">میانی</span></summary>
        <div class="ch-body">
          <p>با <code>fetch</code> داده بگیرید و با <code>async/await</code> کد خواناتر بنویسید. خطاها را با <code>try/catch</code> بگیرید.</p>
          <pre><code>async function load(){
  try{
    const res = await fetch('https://jsonplaceholder.typicode.com/todos/1');
    const data = await res.json();
    console.log(data);
  }catch(e){ console.error('خطا', e); }
}
load();</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>لیست پست‌ها را از یک API عمومی بخوان و در صفحه رندر کن.</li>
            <li>بارگذاری اسکلتی (Loading) برای انتظار شبکه اضافه کن.</li>
          </ol></div>
        </div>
      </details>

      <details class="chapter"><summary><span class="ch-title">فصل ۵: ماژول‌ها، بسته‌سازی و الگوهای کدنویسی</span><span class="badge">حرفه‌ای</span></summary>
        <div class="ch-body">
          <p>از ماژول‌های ES با <code>type="module"</code> استفاده کنید و کد را به فایل‌های کوچک‌تر تقسیم کنید. الگوهای رایج: ماژول، فکتوری، Observer.</p>
          <pre><code>// main.js
import {sum} from './util.js';
console.log(sum(2,3));
// util.js
export const sum = (a,b) =&gt; a+b;</code></pre>
          <div class="exercise"><h4>تمرین</h4><ol>
            <li>پروژهٔ کوچک ماژولار با دو ماژول ابزار و یک ماژول UI بساز.</li>
            <li>الگوی Observer را برای سیستم اعلان ساده پیاده کن.</li>
          </ol></div>
        </div>
      </details>
    </section>
  </main>

  <footer>
    ساخته شده با ❤️ توسط شایان — ۲۰۲۵ · <a href="https://github.com/" target="_blank" rel="noopener">GitHub Pages</a>
  </footer>

  <script>
    // جستجوی زنده در همه فصل‌ها
    const q = document.getElementById('q');
    const chapters = Array.from(document.querySelectorAll('details.chapter'));
    q.addEventListener('input', () => {
      const term = q.value.trim().toLowerCase();
      chapters.forEach(d => {
        const txt = d.innerText.toLowerCase();
        const hit = txt.includes(term);
        d.style.display = hit ? '' : 'none';
      });
    });

    // باز/بستن همه فصل‌ها
    const expand = document.getElementById('expand');
    const collapse = document.getElementById('collapse');
    expand.addEventListener('click', () => chapters.forEach(d => d.open = true));
    collapse.addEventListener('click', () => chapters.forEach(d => d.open = false));
  </script>
</body>
</html>
