---
{"dg-publish":true,"dg-permalink":"/scroll-until-infinity","permalink":"/scroll-until-infinity/","tags":["سبک_زندگی_دیجیتال"],"dg-note-properties":{"tags":["سبک_زندگی_دیجیتال"]}}
---


![تصویر مرتبط](https://dinu.ir/wp-content/uploads/2023/11/32434.jpg)
تا حالا شده برای یه لحظه گوشی‌تون رو بردارید و قبل از اینکه به خودتون بیاید، نیم‌ساعت گذشته باشه؟ این دقیقاً همون جادوی «اسکرول بی‌نهایت» یا _infinite scroll_ ـه. قابلیتی که در اکثر شبکه‌های اجتماعی مثل اینستاگرام، تیک‌تاک، توییتر و حتی یوتیوب به شکلی از اون استفاده می‌شه. اما پشت این طراحی، فقط راحتی کاربر نیست؛ بلکه یه سازوکار دقیق و هدفمند پنهان شده که ما رو به صفحه‌نمایش میخ‌کوب می‌کنه.

---
### پشت صحنه‌ی اسکرول بی‌نهایت: طراحی برای اعتیاد

اسکرول بی‌نهایت اولین بار توسط یک طراح UX به نام _آزا راسکین_ در سال ۲۰۰۶ ابداع شد؛ اما خودش بعدها اعتراف کرد که از اختراعش پشیمونه! چرا؟ چون فهمید این قابلیت تبدیل به یکی از عوامل اصلی اعتیاد دیجیتالی شده.

ایده خیلی ساده‌ست: وقتی شما به انتهای محتوا می‌رسید، به جای اینکه مجبور باشید روی دکمه‌ای برای رفتن به صفحه بعدی کلیک کنید، بلافاصله محتوای جدید ظاهر می‌شه. این فرآیند بی‌وقفه، ساختاری شبیه به دستگاه‌های اسلات کازینو داره: شما نمی‌دونید که بعدی چی قراره بیاد، و این «عدم قطعیت پاداش» دقیقاً همون چیزیه که مغز ما رو تحریک می‌کنه برای تکرار بیشتر.

---
### چرا از اسکرول لذت می‌بریم؟

مغز ما عاشق تازگیه. هر بار که یه محتوای جدید (تصویر، ویدیو یا حتی یه توییت ساده) رو می‌بینیم، مقداری _دوپامین_ در مغزمون ترشح می‌شه. این ماده شیمیایی حس لذت، انگیزه و پاداش رو به همراه میاره. بنابراین هر اسکرول، یه پاداش کوچیک به ما می‌ده. حالا تصور کن این چرخه صدها بار در روز تکرار بشه...

---
### هزینه‌هایی که نمی‌بینیم

- **کاهش تمرکز:** ذهن شما مدام در حالت پردازش محتوای جدید قرار می‌گیره و فرصت بازیابی نداره.
    
- **اختلال خواب:** اسکرول شبانه، نور آبی و هیجان‌های پیاپی، کیفیت خواب رو پایین میاره.
    
- **کاهش عزت‌نفس:** مقایسه بی‌وقفه با ظاهر زندگی دیگران، بدون دیدن پشت‌صحنه‌ی واقعی.
    
- **افزایش اضطراب و بی‌قراری ذهنی.**
    





```dataviewjs
const container = dv.el("div", "");

container.innerHTML = `
<style>
  .interactive-box {
    font-family: Tahoma, sans-serif;
    direction: rtl;
    max-width: 600px;
    margin: 20px auto;
    padding: 20px;
    background: #f9f9f9;
    border-radius: 12px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  }
  .interactive-box h2 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
  }
  .button-row {
    display: flex;
    gap: 10px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 20px;
  }
  .interactive-btn {
    padding: 10px 20px;
    border: none;
    border-radius: 8px;
    background: #4a90d9;
    color: white;
    cursor: pointer;
    font-size: 14px;
    transition: background 0.3s;
  }
  .interactive-btn:hover {
    background: #357ab8;
  }
  .interactive-btn.active {
    background: #2c5f8a;
  }
  .content-box {
    padding: 15px;
    background: white;
    border-radius: 8px;
    min-height: 80px;
    line-height: 1.8;
    color: #444;
    border: 1px solid #e0e0e0;
  }
</style>

<div class="interactive-box">
  <h2>موضوع را انتخاب کنید</h2>
  <div class="button-row">
    <button class="interactive-btn" data-target="item1">موضوع اول</button>
    <button class="interactive-btn" data-target="item2">موضوع دوم</button>
    <button class="interactive-btn" data-target="item3">موضوع سوم</button>
  </div>
  <div class="content-box" id="content-display">
    لطفاً یکی از موضوعات بالا را انتخاب کنید.
  </div>
</div>

<script>
  const contents = {
    item1: "این توضیحات مربوط به موضوع اول است. می‌توانی هر متنی اینجا بنویسی.",
    item2: "این توضیحات مربوط به موضوع دوم است. کاملاً قابل تغییر است.",
    item3: "این توضیحات مربوط به موضوع سوم است. هر تعداد موضوع می‌توانی اضافه کنی."
  };

  const buttons = document.querySelectorAll(".interactive-btn");
  const display = document.getElementById("content-display");

  buttons.forEach(btn => {
    btn.addEventListener("click", () => {
      buttons.forEach(b => b.classList.remove("active"));
      btn.classList.add("active");
      const target = btn.getAttribute("data-target");
      display.innerHTML = contents[target];
    });
  });
</script>
`;
```
