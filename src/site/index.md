<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>مسعود شکری | تفکر سیستمی، هوش مصنوعی و کار دانشی</title>
  <meta name="description" content="سیستم مدیریت دانش شخصی درباره تفکر سیستمی، هوش مصنوعی، خلاقیت، نوشتن، پژوهش و توسعه فردی.">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://cdn.jsdelivr.net/gh/rastikerdar/vazirmatn@v33.003/Vazirmatn-font-face.css" rel="stylesheet">

  <style>
    /* ============================================================
       ROOT VARIABLES
       ============================================================ */
    :root {
      --green-900: #0f3d2e;
      --green-800: #14503b;
      --green-700: #1a6b4d;
      --green-600: #218a63;
      --green-500: #2fa377;
      --green-400: #5cbf98;
      --green-200: #b9e4d2;
      --green-100: #dff2e9;
      --green-50: #f2faf6;

      --ink: #16241f;
      --ink-soft: #42574f;
      --ink-mute: #6d837b;

      --bg: #ffffff;
      --bg-soft: #f7fbf9;
      --line: #e2efe8;

      --radius: 18px;
      --radius-sm: 12px;
      --shadow-sm: 0 1px 2px rgba(15,61,46,.06), 0 4px 14px rgba(15,61,46,.05);
      --shadow-md: 0 10px 30px rgba(15,61,46,.10);
      --max: 1120px;
    }

    /* ============================================================
       RESET & BASE
       ============================================================ */
    *, *::before, *::after { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: 'Vazirmatn', system-ui, -apple-system, 'Segoe UI', Tahoma, sans-serif;
      background: var(--bg);
      color: var(--ink);
      line-height: 1.9;
      font-size: 16px;
      -webkit-font-smoothing: antialiased;
    }
    a { color: var(--green-700); text-decoration: none; }
    a:hover { color: var(--green-600); }
    .wrap { max-width: var(--max); margin: 0 auto; padding: 0 24px; }

    /* ============================================================
       HEADER
       ============================================================ */
    header {
      position: sticky; top: 0; z-index: 50;
      background: rgba(255,255,255,.85);
      backdrop-filter: saturate(180%) blur(12px);
      border-bottom: 1px solid var(--line);
    }
    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 68px;
    }
    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 800;
      font-size: 20px;
      color: var(--green-900);
    }
    .logo .mark {
      width: 34px; height: 34px; border-radius: 10px;
      background: linear-gradient(135deg, var(--green-600), var(--green-400));
      display: grid; place-items: center;
      color: #fff; font-size: 17px;
      box-shadow: var(--shadow-sm);
    }
    .nav-links {
      display: flex;
      gap: 26px;
      align-items: center;
    }
    .nav-links a {
      color: var(--ink-soft);
      font-size: 15px;
      font-weight: 500;
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--green-700); }
    .menu-btn {
      display: none;
      background: none;
      border: 1px solid var(--line);
      border-radius: 10px;
      padding: 8px 10px;
      cursor: pointer;
    }

    /* ============================================================
       HERO
       ============================================================ */
    .hero {
      background:
        radial-gradient(900px 420px at 85% -10%, var(--green-100), transparent 60%),
        radial-gradient(700px 380px at 10% 0%, #eaf7f1, transparent 60%),
        var(--bg);
      padding: 86px 0 72px;
      border-bottom: 1px solid var(--line);
      text-align: center;
    }
    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--green-100);
      color: var(--green-800);
      border: 1px solid var(--green-200);
      padding: 7px 16px;
      border-radius: 999px;
      font-size: 13.5px;
      font-weight: 600;
      margin-bottom: 22px;
    }
    .badge .dot {
      width: 7px; height: 7px;
      border-radius: 50%;
      background: var(--green-500);
    }
    h1 {
      font-size: clamp(30px, 4.6vw, 50px);
      line-height: 1.45;
      margin: 0 auto 20px;
      font-weight: 800;
      color: var(--green-900);
      letter-spacing: -.4px;
      max-width: 800px;
    }
    h1 .hl {
      background: linear-gradient(180deg, transparent 62%, var(--green-200) 62%);
      padding: 0 4px;
    }
    .lead {
      font-size: clamp(16px, 2vw, 19px);
      color: var(--ink-soft);
      max-width: 760px;
      margin: 0 auto 16px;
    }
    .quote {
      border-right: 4px solid var(--green-500);
      background: var(--bg-soft);
      padding: 18px 22px;
      border-radius: var(--radius-sm);
      max-width: 760px;
      color: var(--green-900);
      font-weight: 600;
      font-size: 17px;
      margin: 26px auto 32px;
      text-align: right;
    }
    .cta {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
      justify-content: center;
    }
    .btn {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 13px 26px;
      border-radius: 12px;
      font-weight: 700;
      font-size: 15px;
      transition: .2s;
      border: 1px solid transparent;
      cursor: pointer;
    }
    .btn-primary {
      background: var(--green-700);
      color: #fff;
      box-shadow: var(--shadow-sm);
    }
    .btn-primary:hover {
      background: var(--green-800);
      color: #fff;
      transform: translateY(-2px);
      box-shadow: var(--shadow-md);
    }
    .btn-ghost {
      background: #fff;
      color: var(--green-800);
      border-color: var(--green-200);
    }
    .btn-ghost:hover {
      background: var(--green-50);
      color: var(--green-900);
      transform: translateY(-2px);
    }

    /* ============================================================
       SECTIONS
       ============================================================ */
    section { padding: 76px 0; }
    .sec-head {
      margin-bottom: 42px;
      max-width: 720px;
      margin-left: auto;
      margin-right: auto;
      text-align: center;
    }
    .kicker {
      color: var(--green-600);
      font-weight: 700;
      font-size: 14px;
      letter-spacing: .5px;
      margin: 0 0 10px;
    }
    h2 {
      font-size: clamp(24px, 3vw, 32px);
      margin: 0 0 12px;
      color: var(--green-900);
      font-weight: 800;
    }
    .sec-head p {
      color: var(--ink-soft);
      margin: 0;
      font-size: 16.5px;
    }

    /* ============================================================
       PILLARS — طراحی جدید به صورت لیست عمودی
       ============================================================ */
    .pillars-list {
      display: flex;
      flex-direction: column;
      gap: 16px;
      max-width: 900px;
      margin: 0 auto;
    }
    .pillar-item {
      display: flex;
      align-items: center;
      gap: 18px;
      background: #fff;
      border: 1px solid var(--line);
      border-radius: var(--radius-sm);
      padding: 16px 24px;
      transition: all .2s;
      text-decoration: none;
      color: inherit;
    }
    .pillar-item:hover {
      border-color: var(--green-400);
      box-shadow: var(--shadow-sm);
      transform: translateX(-4px);
    }
    .pillar-item .ico {
      font-size: 28px;
      width: 48px;
      text-align: center;
      flex-shrink: 0;
      color: var(--green-600);
    }
    .pillar-item .content {
      flex: 1;
    }
    .pillar-item .content h3 {
      margin: 0 0 4px;
      font-size: 18px;
      font-weight: 700;
      color: var(--green-900);
    }
    .pillar-item .content p {
      margin: 0;
      font-size: 15px;
      color: var(--ink-soft);
      line-height: 1.7;
    }
    .pillar-item .go {
      font-weight: 700;
      color: var(--green-600);
      font-size: 14px;
      white-space: nowrap;
    }
    .pillar-item:hover .go {
      color: var(--green-800);
    }

    /* ============================================================
       CONNECT — طراحی جدید با دو ستون و آیکون
       ============================================================ */
    .connect-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 48px;
      align-items: start;
    }
    .connect-text h2 {
      margin-top: 0;
    }
    .connect-text p {
      color: var(--ink-soft);
      font-size: 16.5px;
    }
    .connect-items {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px 24px;
    }
    .connect-item {
      display: flex;
      align-items: flex-start;
      gap: 10px;
    }
    .connect-item .icon {
      font-size: 22px;
      color: var(--green-500);
      line-height: 1.4;
    }
    .connect-item .text b {
      display: block;
      color: var(--green-900);
      font-size: 16px;
    }
    .connect-item .text span {
      color: var(--ink-soft);
      font-size: 14px;
      line-height: 1.6;
    }

    /* ============================================================
       PHD PANEL
       ============================================================ */
    .panel {
      background: linear-gradient(135deg, var(--green-800), var(--green-600));
      color: #fff;
      border-radius: 24px;
      padding: 48px 44px;
      box-shadow: var(--shadow-md);
    }
    .panel h2 { color: #fff; margin-bottom: 16px; }
    .panel p {
      color: rgba(255,255,255,.9);
      font-size: 16.5px;
      max-width: 820px;
    }
    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 26px;
    }
    .tag {
      background: rgba(255,255,255,.14);
      border: 1px solid rgba(255,255,255,.24);
      color: #fff;
      padding: 7px 16px;
      border-radius: 999px;
      font-size: 14px;
      font-weight: 600;
    }

    /* ============================================================
       LATEST NOTES — به صورت لیست متنی
       ============================================================ */
    .latest-list {
      max-width: 800px;
      margin: 34px auto 0;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .latest-item {
      display: flex;
      align-items: baseline;
      gap: 16px;
      padding: 12px 20px;
      border-bottom: 1px solid var(--line);
      transition: background .2s;
      border-radius: var(--radius-sm);
    }
    .latest-item:hover {
      background: var(--bg-soft);
    }
    .latest-item .date {
      font-size: 14px;
      color: var(--ink-mute);
      white-space: nowrap;
      min-width: 90px;
    }
    .latest-item .title {
      font-size: 17px;
      font-weight: 600;
      color: var(--green-900);
      flex: 1;
    }
    .latest-item .title a {
      color: inherit;
      text-decoration: none;
    }
    .latest-item .title a:hover {
      color: var(--green-600);
    }
    .latest-item .arrow {
      color: var(--green-400);
      font-weight: 700;
    }

    /* ============================================================
       CTA BAND
       ============================================================ */
    .band {
      background: var(--green-50);
      border: 1px solid var(--green-200);
      border-radius: 24px;
      padding: 44px;
      text-align: center;
    }
    .band h2 { margin-bottom: 10px; }
    .band p {
      color: var(--ink-soft);
      max-width: 640px;
      margin: 0 auto 26px;
    }

    /* ============================================================
       FOOTER
       ============================================================ */
    footer {
      background: var(--green-900);
      color: rgba(255,255,255,.75);
      padding: 52px 0 26px;
      margin-top: 80px;
    }
    .f-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      gap: 40px;
      padding-bottom: 34px;
      border-bottom: 1px solid rgba(255,255,255,.12);
    }
    footer h4 {
      color: #fff;
      font-size: 16px;
      margin: 0 0 14px;
    }
    footer a {
      color: rgba(255,255,255,.72);
      display: block;
      margin-bottom: 9px;
      font-size: 14.5px;
    }
    footer a:hover { color: var(--green-400); }
    .f-bottom {
      padding-top: 22px;
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 10px;
      font-size: 13.5px;
      color: rgba(255,255,255,.55);
    }

    /* ============================================================
       RESPONSIVE
       ============================================================ */
    @media (max-width: 900px) {
      .connect-grid {
        grid-template-columns: 1fr;
        gap: 32px;
      }
      .connect-items {
        grid-template-columns: 1fr;
      }
      .f-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 640px) {
      .nav-links {
        display: none;
      }
      .menu-btn {
        display: block;
      }
      .f-grid {
        grid-template-columns: 1fr;
      }
      .hero {
        padding: 60px 0 52px;
      }
      .panel {
        padding: 34px 24px;
      }
      .band {
        padding: 32px 20px;
      }
      section {
        padding: 56px 0;
      }
      .quote {
        font-size: 15px;
        padding: 14px 18px;
      }
      .pillar-item {
        flex-wrap: wrap;
        padding: 16px;
      }
      .pillar-item .go {
        margin-top: 8px;
        width: 100%;
        text-align: left;
      }
      .latest-item {
        flex-wrap: wrap;
        gap: 8px;
      }
      .latest-item .date {
        min-width: unset;
        width: 100%;
        font-size: 13px;
      }
    }
  </style>
</head>
<body>

<!-- ================= HEADER ================= -->
<header>
  <div class="wrap nav">
    <a href="/" class="logo">
      <span class="mark">◈</span>
      <span>مسعود شکری</span>
    </a>
    <nav class="nav-links">
      <a href="#pillars">حوزه‌ها</a>
      <a href="#connect">نخِ مشترک</a>
      <a href="#phd">پژوهش</a>
      <a href="#latest">آخرین نوشته‌ها</a>
      <a href="#contact">ارتباط</a>
    </nav>
    <button class="menu-btn" onclick="document.querySelector('.nav-links').style.display='flex'">☰</button>
  </div>
</header>

<!-- ================= HERO ================= -->
<div class="hero">
  <div class="wrap">
    <span class="badge"><span class="dot"></span> سیستم مدیریت دانش شخصی — همیشه در حال رشد</span>
    <h1>بهتر فکر کنیم، بهتر یاد بگیریم،<br><span class="hl">بهتر بنویسیم</span> و بهتر پژوهش کنیم.</h1>
    <p class="lead">
      من دانشجوی دکتری <b>مدیریت سیستم‌ها</b> هستم و این‌جا نسخه‌ی عمومیِ یادداشت‌ها،
      تجربه‌ها و آموخته‌هایم را منتشر می‌کنم؛ از تفکر سیستمی و هوش مصنوعی
      تا خلاقیت، نوشتن، روش پژوهش و توسعه‌ی فردی.
    </p>

    <div class="quote">
      همه‌ی این موضوعات، شاخه‌های یک درخت‌اند — نه جنگل‌هایی جدا از هم.
      نخِ مشترکشان یک چیز است: <b>روش‌مند بودن در کارِ فکری.</b>
    </div>

    <div class="cta">
      <a class="btn btn-primary" href="#pillars">شروع کاوش ↓</a>
      <a class="btn btn-ghost" href="#latest">آخرین نوشته‌ها</a>
      <a class="btn btn-ghost" href="#contact">کانال نوفکر</a>
    </div>
  </div>
</div>

<!-- ================= PILLARS (حوزه‌های دانشی) ================= -->
<section id="pillars">
  <div class="wrap">
    <div class="sec-head">
      <p class="kicker">حوزه‌های دانشی</p>
      <h2>این‌جا درباره‌ی چه می‌نویسم؟</h2>
      <p>هر حوزه دروازه‌ای است به مجموعه‌ای از یادداشت‌های به‌هم‌پیوسته.</p>
    </div>

    <div class="pillars-list">
      <a class="pillar-item" href="#">
        <span class="ico">◎</span>
        <div class="content">
          <h3>تفکر سیستمی</h3>
          <p>کتاب‌ها، افراد تأثیرگذار، مجلات و همایش‌ها، و روش‌شناسی‌های سیستمی مثل VSM و SSM. عینکی برای دیدن کلیت، روابط و بازخوردها.</p>
        </div>
        <span class="go">ورود →</span>
      </a>

      <a class="pillar-item" href="#">
        <span class="ico">◆</span>
        <div class="content">
          <h3>هوش مصنوعی و کار دانشی</h3>
          <p>ابزارها، پرامپت‌های آزموده‌شده، ترفندهای کاربردی — و یک نگاه انتقادی: چطور از AI استفاده کنیم بدون آن‌که اصالتِ فکر کردن را از دست بدهیم.</p>
        </div>
        <span class="go">ورود →</span>
      </a>

      <a class="pillar-item" href="#">
        <span class="ico">✦</span>
        <div class="content">
          <h3>خلاقیت و نوآوری</h3>
          <p>هم مفهوم، هم تکنیک‌های عملی. میراث سایت «نوخلاق» به‌همراه تجربه‌ی یک ترم تدریس این درس.</p>
        </div>
        <span class="go">ورود →</span>
      </a>

      <a class="pillar-item" href="#">
        <span class="ico">◈</span>
        <div class="content">
          <h3>توسعه فردی</h3>
          <p>عادت‌سازی، سیستم‌سازی شخصی، هدف‌گذاری، مدیریت توجه و تمرکز — فقط آنچه خودم تجربه کرده‌ام و واقعاً کار کرده است.</p>
        </div>
        <span class="go">ورود →</span>
      </a>

      <a class="pillar-item" href="#">
        <span class="ico">✎</span>
        <div class="content">
          <h3>نوشتن و نویسندگی</h3>
          <p>نوشتن نه فقط ابزار انتقال ایده، که <b>روشی برای فکر کردن</b>. چرایی، تکنیک‌ها و جای نوشتن در فرآیند یادگیری و پژوهش.</p>
        </div>
        <span class="go">ورود →</span>
      </a>

      <a class="pillar-item" href="#">
        <span class="ico">⌕</span>
        <div class="content">
          <h3>پژوهش و روش‌شناسی</h3>
          <p>روش‌ها، شیوه‌ها و ابزارهای پژوهشی؛ خلاصه‌ی آنچه در مسیر دکتری یاد می‌گیرم و به کار می‌بندم.</p>
        </div>
        <span class="go">ورود →</span>
      </a>

      <a class="pillar-item" href="#">
        <span class="ico">▤</span>
        <div class="content">
          <h3>تدریس</h3>
          <p>یادداشت‌ها و طرح‌درس‌های مبانی سازمان، بازاریابی، رفتار سازمانی، مهارت‌های حرفه‌ای، تجزیه و تحلیل سیستم‌ها و خلاقیت و نوآوری.</p>
        </div>
        <span class="go">ورود →</span>
      </a>

      <a class="pillar-item" href="#">
        <span class="ico">✧</span>
        <div class="content">
          <h3>تجربه‌ها و درس‌ها</h3>
          <p>روایت صادقانه از مسیرها — از جمله شکست‌ها. چون آنچه جواب نداده، به‌اندازه‌ی موفقیت‌ها آموزنده است.</p>
        </div>
        <span class="go">ورود →</span>
      </a>

      <a class="pillar-item" href="#">
        <span class="ico">☷</span>
        <div class="content">
          <h3>نقشه‌ی کل یادداشت‌ها</h3>
          <p>فهرست کامل MOCها و نقطه‌ی ورود به شبکه‌ی پیوندخورده‌ی همه‌ی یادداشت‌های این باغچه.</p>
        </div>
        <span class="go">دیدن نقشه →</span>
      </a>
    </div>
  </div>
</section>

<!-- ================= CONNECT (نخِ مشترک) ================= -->
<section id="connect" class="connect">
  <div class="wrap connect-grid">
    <div class="connect-text">
      <p class="kicker">نخِ مشترک</p>
      <h2>چرا این موضوعات کنار هم‌اند؟</h2>
      <p>
        شاید در نگاه اول پراکنده به‌نظر برسند؛ اما هرکدام یک لایه از یک پرسش واحدند:
        <b>چطور می‌شود کارِ فکری را روش‌مندتر انجام داد؟</b>
        این‌جا نه مجموعه‌ای از موضوعات جدا، بلکه یک ذهن با یک دغدغه‌ی مشترک را می‌بینید.
      </p>
    </div>

    <div class="connect-items">
      <div class="connect-item">
        <span class="icon">◉</span>
        <div class="text">
          <b>تفکر سیستمی</b>
          <span>عینکِ نگاه: دیدن کلیت، روابط و بازخوردها به‌جای اجزای جدا.</span>
        </div>
      </div>
      <div class="connect-item">
        <span class="icon">◉</span>
        <div class="text">
          <b>توسعه فردی</b>
          <span>همان تفکر سیستمی، اما در مقیاس فردی؛ وقتی خودم موضوعِ سیستم‌ام.</span>
        </div>
      </div>
      <div class="connect-item">
        <span class="icon">◉</span>
        <div class="text">
          <b>خلاقیت و نوآوری</b>
          <span>دیدن الگوهای تازه در همان روابط — خروجیِ طبیعی نگاه سیستمی.</span>
        </div>
      </div>
      <div class="connect-item">
        <span class="icon">◉</span>
        <div class="text">
          <b>هوش مصنوعی</b>
          <span>قدرتمندترین ابزار امروز برای تقویت فکر — به شرط استفاده‌ی سنجیده.</span>
        </div>
      </div>
      <div class="connect-item">
        <span class="icon">◉</span>
        <div class="text">
          <b>نوشتن</b>
          <span>ابزاری که همه‌ی این‌ها را به هم وصل می‌کند؛ نوشتن یعنی فکر کردن.</span>
        </div>
      </div>
      <div class="connect-item">
        <span class="icon">◉</span>
        <div class="text">
          <b>پژوهش و تدریس</b>
          <span>محل آزمون و انتقالِ همه‌ی آنچه در بالا آمد.</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ================= PHD PANEL ================= -->
<section id="phd">
  <div class="wrap">
    <div class="panel">
      <p class="kicker" style="color:var(--green-200)">پژوهش جاری</p>
      <h2>رساله‌ی دکتری: توسعه‌ی یک روش‌شناسی ترکیبی</h2>
      <p>
        در رساله‌ام روش‌شناسی جدیدی را توسعه می‌دهم که از ترکیب
        <b>مدل سیستم زنده (VSM)</b> با <b>چارچوب چندسطحی (MLP)</b> به دست می‌آید
        و قرار است در <b>صنعت برق</b> پیاده‌سازی شود. هدف، ساختن ابزاری برای فهم و مدیریتِ
        گذارهای پیچیده در سیستم‌های بزرگ‌مقیاس است.
      </p>
      <div class="tags">
        <span class="tag">مدیریت سیستم‌ها</span>
        <span class="tag">VSM</span>
        <span class="tag">MLP</span>
        <span class="tag">گذار سیستمی</span>
        <span class="tag">صنعت برق</span>
        <span class="tag">روش‌شناسی ترکیبی</span>
      </div>
    </div>
  </div>
</section>

<!-- ================= LATEST NOTES (متنی) ================= -->
<section id="latest" style="padding-top:0">
  <div class="wrap">
    <div class="sec-head">
      <p class="kicker">تازه‌ترین نوشته‌ها</p>
      <h2>از آخرین یادداشت‌ها دیدن کنید</h2>
      <p>هر نوشته یک قدم در مسیر روش‌مندتر شدنِ فکر است.</p>
    </div>

    <div class="latest-list">
      <div class="latest-item">
        <span class="date">۱۴۰۴/۰۲/۱۵</span>
        <span class="title"><a href="#">چرا VSM را برای رساله‌ام انتخاب کردم؟</a></span>
        <span class="arrow">←</span>
      </div>
      <div class="latest-item">
        <span class="date">۱۴۰۴/۰۲/۱۰</span>
        <span class="title"><a href="#">پرامپت‌نویسی برای پژوهشگران</a></span>
        <span class="arrow">←</span>
      </div>
      <div class="latest-item">
        <span class="date">۱۴۰۴/۰۲/۰۵</span>
        <span class="title"><a href="#">عادت نوشتن روزانه؛ چگونه شروع کردم</a></span>
        <span class="arrow">←</span>
      </div>
    </div>
  </div>
</section>

<!-- ================= CTA BAND ================= -->
<section id="contact" style="padding-top:0">
  <div class="wrap">
    <div class="band">
      <p class="kicker">همراه شوید</p>
      <h2>نوفکر | پژوهش، یادگیری و ابزارهای هوشمند</h2>
      <p>
        اگر دانشجو، پژوهشگر، مدرس، نویسنده، تولیدکننده‌ی محتوا یا صرفاً کنجکاوی هستید
        که دوست دارد بهتر فکر کند و بهتر یاد بگیرد — خوش‌آمدید.
      </p>
      <div class="cta" style="justify-content:center">
        <a class="btn btn-primary" href="https://ble.ir/nofekr_ir">عضویت در کانال نوفکر</a>
        <a class="btn btn-ghost" href="mailto:mshekari95@gmail.com">ارسال ایمیل</a>
      </div>
    </div>
  </div>
</section>

<!-- ================= FOOTER ================= -->
<footer>
  <div class="wrap">
    <div class="f-grid">
      <div>
        <h4>مسعود شکری</h4>
        <p style="margin:0;font-size:14.5px;max-width:380px;color:rgba(255,255,255,.65)">
          نسخه‌ی عمومیِ سیستم مدیریت دانش شخصی من در Obsidian.
          تلاشی برای فکر کردنِ بهتر و انتقالِ صادقانه‌ی آنچه در این مسیر یاد گرفته‌ام.
        </p>
      </div>
      <div>
        <h4>حوزه‌ها</h4>
        <a href="#">تفکر سیستمی</a>
        <a href="#">هوش مصنوعی</a>
        <a href="#">خلاقیت و نوآوری</a>
        <a href="#">توسعه فردی</a>
        <a href="#">نوشتن</a>
      </div>
      <div>
        <h4>بیشتر</h4>
        <a href="/about">درباره من</a>
        <a href="#">نقشه یادداشت‌ها</a>
        <a href="#">پژوهش و روش‌ها</a>
        <a href="#">تدریس</a>
        <a href="#">کانال نوفکر</a>
      </div>
    </div>
    <div class="f-bottom">
      <span>© 1405 — تمام یادداشت‌ها با ♥ در Obsidian نوشته شده‌اند.</span>
      <span>آخرین به‌روزرسانی: 1405</span>
    </div>
  </div>
</footer>

</body>
</html>
