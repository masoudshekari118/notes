---
dg-publish: true
---

<div id="interactive-box">
  <h2>موضوع را انتخاب کنید</h2>
  <div class="button-row">
    <button class="interactive-btn" onclick="showContent('item1', this)">موضوع اول</button>
    <button class="interactive-btn" onclick="showContent('item2', this)">موضوع دوم</button>
    <button class="interactive-btn" onclick="showContent('item3', this)">موضوع سوم</button>
  </div>
  <div id="content-display">لطفاً یکی از موضوعات بالا را انتخاب کنید.</div>
</div>

<style>
  #interactive-box {
    font-family: Tahoma, sans-serif;
    direction: rtl;
    max-width: 600px;
    margin: 20px auto;
    padding: 20px;
    background: #f9f9f9;
    border-radius: 12px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  }
  #interactive-box h2 {
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
  #content-display {
    padding: 15px;
    background: white;
    border-radius: 8px;
    min-height: 80px;
    line-height: 1.8;
    color: #444;
    border: 1px solid #e0e0e0;
  }
</style>

<script>
  const contents = {
    item1: "این توضیحات مربوط به موضوع اول است. می‌توانی هر متنی اینجا بنویسی.",
    item2: "این توضیحات مربوط به موضوع دوم است. کاملاً قابل تغییر است.",
    item3: "این توضیحات مربوط به موضوع سوم است. هر تعداد موضوع می‌توانی اضافه کنی."
  };

  function showContent(key, btn) {
    document.querySelectorAll('.interactive-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    document.getElementById('content-display').innerHTML = contents[key];
  }
</script>
