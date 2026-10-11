<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BANKET | اسناد رسمی</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700;800&display=swap');

:root{
  --black:#11120f;
  --gold:#b69754;
  --light-gold:#e7d6a5;
  --paper:#fffefa;
  --gray:#77766f;
  --line:#ded8c7;
}
*{box-sizing:border-box}
body{
  margin:0;
  background:#e9e8e3;
  color:var(--black);
  font-family:'Vazirmatn',Tahoma,sans-serif;
}
button,input,textarea,select{font:inherit}
.toolbar{
  max-width:1100px;
  margin:24px auto;
  padding:18px;
  background:#fff;
  border-radius:14px;
  display:flex;
  justify-content:center;
  gap:12px;
  flex-wrap:wrap;
  box-shadow:0 5px 24px #0000000d;
}
.toolbar button{
  border:0;
  padding:12px 22px;
  border-radius:8px;
  background:var(--black);
  color:white;
  cursor:pointer;
  font-weight:600;
}
.toolbar button.gold{background:var(--gold);color:#111}
.toolbar button:hover{opacity:.86}
.hint{
  width:100%;
  text-align:center;
  color:#777;
  font-size:12px;
}
.document{
  position:relative;
  margin:24px auto;
  background:var(--paper);
  box-shadow:0 12px 40px #00000012;
  overflow:hidden;
}
.a4{width:210mm;min-height:297mm;padding:12mm}
.a5{width:210mm;min-height:148mm;padding:8mm}
.frame{
  position:relative;
  min-height:100%;
  border:1.5px solid var(--gold);
  padding:7mm;
}
.a4 .frame{min-height:272mm}
.a5 .frame{min-height:130mm}
.frame:before{
  content:"";
  position:absolute;
  inset:2mm;
  border:1px solid #b697543d;
  pointer-events:none;
}
.header{
  position:relative;
  text-align:center;
  border-bottom:2px solid var(--gold);
  padding:2mm 0 5mm;
}
.brand{
  font-family:Georgia,serif;
  font-size:27px;
  font-weight:bold;
  letter-spacing:5px;
  color:var(--black);
}
.brand span{color:var(--gold)}
.subtitle{
  font-size:10px;
  letter-spacing:2px;
  color:#777;
  margin-top:2px;
}
.doc-title{
  display:inline-block;
  margin-top:12px;
  border:1px solid var(--gold);
  padding:5px 25px;
  font-size:17px;
  font-weight:800;
  letter-spacing:.2px;
}
.doc-subtitle{font-size:10px;color:var(--gray);margin-top:5px}
.top-meta{
  display:flex;
  justify-content:space-between;
  gap:12px;
  font-size:10px;
  margin:12px 0;
}
.field{
  display:flex;
  align-items:center;
  gap:5px;
  min-width:0;
  font-size:11px;
}
.field label{white-space:nowrap;color:#555}
.field input,.field textarea,.field select{
  min-width:0;
  width:100%;
  background:transparent;
  border:0;
  border-bottom:1px dotted #aaa;
  outline:none;
  padding:4px 3px;
  border-radius:0;
  color:#111;
}
.section-title{
  display:flex;
  align-items:center;
  gap:8px;
  margin:12px 0 7px;
  font-size:11px;
  font-weight:800;
}
.section-title:before{
  content:"";
  width:4px;height:15px;
  background:var(--gold);
}
.section-title:after{
  content:"";
  height:1px;
  flex:1;
  background:var(--line);
}
.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:8px 15px;
}
.grid.three{grid-template-columns:repeat(3,1fr)}
.panel{
  border:1px solid var(--line);
  padding:8px;
  background:#fffefa;
}
.id-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:12px;
}
.id-box{
  height:39mm;
  border:1px dashed #b9a36d;
  background:#faf8f0;
  position:relative;
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;
  text-align:center;
  gap:4px;
  overflow:hidden;
}
.id-box strong{font-size:11px}
.id-box small{font-size:9px;color:#777}
.id-box input[type=file]{
  max-width:90%;
  font-size:9px;
}
.id-box img{
  max-width:100%;
  max-height:29mm;
  object-fit:contain;
  display:none;
}
.data-table{
  width:100%;
  border-collapse:collapse;
  font-size:10px;
  margin-top:7px;
}
.data-table th{
  background:#191a16;
  color:#e8d8ac;
  font-weight:500;
}
.data-table th,.data-table td{
  border:1px solid var(--line);
  padding:7px 5px;
  text-align:center;
}
.data-table td input{
  width:100%;
  border:0;
  outline:0;
  background:transparent;
  text-align:center;
}
.description{
  width:100%;
  min-height:42px;
  resize:vertical;
  border:1px solid var(--line);
  background:#fffefa;
  padding:7px;
  outline:none;
  font-size:10px;
}
.declaration{
  font-size:10px;
  line-height:2.1;
  text-align:justify;
  padding:8px 10px;
  border-right:3px solid var(--gold);
  background:#f7f5ee;
  margin-top:10px;
}
.signatures{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:12px;
  margin-top:12px;
}
.signature-box{
  height:27mm;
  border:1px solid var(--line);
  padding:8px;
  text-align:center;
  position:relative;
}
.signature-box strong{font-size:10px}
.signature-box small{display:block;font-size:9px;color:#777;margin-top:3px}
.signature-box input{
  width:100%;
  border:0;
  border-bottom:1px dotted #aaa;
  outline:none;
  text-align:center;
  margin-top:8px;
  background:transparent;
  font-size:10px;
}
.footer{
  border-top:1px solid var(--gold);
  padding-top:6px;
  margin-top:10px;
  text-align:center;
  font-size:9px;
  color:#777;
}
.stamp{
  width:24mm;
  height:24mm;
  border:2px double #9d8146;
  color:#8e7137;
  border-radius:50%;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
  transform:rotate(-9deg);
  margin:auto;
  font-weight:800;
  background:#fffdf5;
  outline:1px solid #c3ad78;
  outline-offset:-5px;
}
.stamp span:first-child{font-size:10px;letter-spacing:1px}
.stamp span:last-child{font-size:8px;margin-top:3px}
.receipt-head{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:10px;
}
.receipt-head .brand{font-size:25px}
.receipt-number{
  border:1px solid var(--gold);
  padding:6px 10px;
  min-width:35mm;
  font-size:10px;
  text-align:center;
}
.receipt-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:8px 16px;
}
.amount-box{
  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:10px;
  background:#171813;
  color:#fff;
  border-right:4px solid var(--gold);
  padding:12px;
  margin-top:10px;
}
.amount-box strong{color:var(--light-gold);font-size:12px}
.amount-box input{
  background:transparent;
  color:white;
  border:0;
  border-bottom:1px dotted var(--light-gold);
  width:43%;
  outline:none;
  text-align:center;
  font-weight:800;
}
.receipt-bottom{
  display:grid;
  grid-template-columns:1fr 1fr 1fr;
  gap:10px;
  margin-top:12px;
  align-items:center;
}
.receipt-bottom .signature-box{height:24mm}
.receipt-bottom .stamp{width:22mm;height:22mm}
.contact{
  text-align:center;
  margin-top:9px;
  font-size:9px;
  line-height:2;
}
.gold-text{color:#9b7a39}
.no-print{}
@media(max-width:800px){
  .document{transform-origin:top center}
  .a4,.a5{width:100%;min-height:0;padding:12px}
  .frame{padding:12px}
}
@media print{
  @page{margin:0}
  body{background:white}
  body *{visibility:hidden}
  .document.printing,.document.printing *{visibility:visible}
  .document.printing{
    position:absolute;
    left:0;top:0;
    margin:0;
    box-shadow:none;
    transform:none;
    overflow:hidden;
  }
  .document.printing.a4{
    width:210mm;height:297mm;min-height:297mm;
    padding:10mm;
  }
  .document.printing.a5{
    width:210mm;height:148mm;min-height:148mm;
    padding:6mm;
  }
  .document.printing .frame{height:100%;min-height:0}
  .no-print,.id-box input[type=file]{display:none!important}
  input,textarea,select{
    -webkit-appearance:none;
    appearance:none;
  }
  input::placeholder,textarea::placeholder{color:transparent}
  .id-box img{display:block}
}
</style>
</head>
<body>

<div class="toolbar no-print">
  <button class="gold" onclick="printDocument('certificate')">چاپ گواهی شرکت A4</button>
  <button onclick="printDocument('receipt')">چاپ رسید مشتری A5</button>
  <button onclick="clearForm()">پاک کردن فرم‌ها</button>
  <div class="hint">اطلاعات را وارد کن؛ سپس برگه موردنظر را جداگانه چاپ بگیر.</div>
</div>

<!-- گواهی شرکت A4 -->
<main class="document a4" id="certificate">
<div class="frame">

<header class="header">
  <div class="brand">BANK<span>ET</span></div>
  <div class="subtitle">PRECIOUS METALS • OFFICIAL DOCUMENTS</div>
  <div class="doc-title">گواهی رسمی تحویل و دریافت</div>
  <div class="doc-subtitle">گواهی ثبت مشخصات طرفین و جزئیات تحویل کالا</div>
</header>

<div class="top-meta">
  <div class="field"><label>شماره گواهی:</label><input placeholder="شماره سند"></div>
  <div class="field"><label>تاریخ:</label><input placeholder="روز / ماه / سال"></div>
  <div class="field"><label>ساعت:</label><input placeholder="۰۰:۰۰"></div>
</div>

<div class="section-title">مشخصات تحویل‌دهنده اول</div>
<div class="panel">
  <div class="grid">
    <div class="field"><label>نام و نام خانوادگی:</label><input></div>
    <div class="field"><label>کد ملی:</label><input maxlength="10" inputmode="numeric"></div>
    <div class="field"><label>شماره تماس:</label><input inputmode="tel"></div>
    <div class="field"><label>شماره سند / مدرک:</label><input></div>
  </div>
</div>

<div class="section-title">اسکن کارت ملی تحویل‌دهنده اول</div>
<div class="id-grid">
  <div class="id-box">
    <strong>تصویر روی کارت ملی</strong>
    <small>تصویر روی کارت را انتخاب کنید</small>
    <input class="no-print" type="file" accept="image/*" onchange="previewImage(this,'id1front')">
    <img id="id1front" alt="روی کارت ملی تحویل‌دهنده اول">
  </div>
  <div class="id-box">
    <strong>تصویر پشت کارت ملی</strong>
    <small>تصویر پشت کارت را انتخاب کنید</small>
    <input class="no-print" type="file" accept="image/*" onchange="previewImage(this,'id1back')">
    <img id="id1back" alt="پشت کارت ملی تحویل‌دهنده اول">
  </div>
</div>

<div class="section-title">مشخصات تحویل‌دهنده دوم</div>
<div class="panel">
  <div class="grid">
    <div class="field"><label>نام و نام خانوادگی:</label><input></div>
    <div class="field"><label>کد ملی:</label><input maxlength="10" inputmode="numeric"></div>
    <div class="field"><label>شماره تماس:</label><input inputmode="tel"></div>
    <div class="field"><label>شماره سند / مدرک:</label><input></div>
  </div>
</div>

<div class="section-title">اسکن کارت ملی تحویل‌دهنده دوم</div>
<div class="id-grid">
  <div class="id-box">
    <strong>تصویر روی کارت ملی</strong>
    <small>تصویر روی کارت را انتخاب کنید</small>
    <input class="no-print" type="file" accept="image/*" onchange="previewImage(this,'id2front')">
    <img id="id2front" alt="روی کارت ملی تحویل‌دهنده دوم">
  </div>
  <div class="id-box">
    <strong>تصویر پشت کارت ملی</strong>
    <small>تصویر پشت کارت را انتخاب کنید</small>
    <input class="no-print" type="file" accept="image/*" onchange="previewImage(this,'id2back')">
    <img id="id2back" alt="پشت کارت ملی تحویل‌دهنده دوم">
  </div>
</div>

<div class="section-title">جزئیات کالا / موضوع تحویل</div>
<table class="data-table">
  <thead>
    <tr>
      <th>ردیف</th><th>شرح کالا</th><th>عیار / مشخصات</th>
      <th>تعداد</th><th>وزن</th><th>توضیحات</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>۱</td>
      <td><input placeholder="نام کالا"></td>
      <td><input placeholder="مشخصات"></td>
      <td><input placeholder="تعداد"></td>
      <td><input placeholder="گرم"></td>
      <td><input placeholder="توضیحات"></td>
    </tr>
    <tr>
      <td>۲</td>
      <td><input></td><td><input></td><td><input></td><td><input></td><td><input></td>
    </tr>
  </tbody>
</table>

<div class="grid" style="margin-top:10px">
  <div class="field"><label>مبلغ / ارزش اظهارشده (تومان):</label><input></div>
  <div class="field"><label>محل تحویل:</label><input placeholder="محل دقیق تحویل"></div>
</div>

<div class="section-title">شرح و شرایط تحویل</div>
<textarea class="description" placeholder="شرح کامل موضوع، وضعیت کالا، شرایط و توضیحات تکمیلی..."></textarea>

<div class="declaration">
  این سند جهت ثبت مشخصات اشخاص، شرح اقلام و جزئیات تحویل تنظیم شده است.
  طرفین با امضای این برگه، صحت اطلاعات درج‌شده و مفاد توافق ثبت‌شده را تأیید می‌کنند.
  اعتبار هرگونه تعهد مالی یا حقوقی، تابع توافق واقعی طرفین و قوانین مربوط خواهد بود.
</div>

<div class="signatures">
  <div class="signature-box">
    <strong>امضا و اثر انگشت تحویل‌دهنده اول</strong>
    <small>نام و نام خانوادگی</small>
    <input placeholder="نام کامل">
  </div>
  <div class="signature-box">
    <strong>امضا و اثر انگشت تحویل‌دهنده دوم</strong>
    <small>نام و نام خانوادگی</small>
    <input placeholder="نام کامل">
  </div>
</div>

<div class="signatures">
  <div class="signature-box">
    <strong>تأیید و امضای نماینده شرکت</strong>
    <small>نام، سمت و امضا</small>
    <input placeholder="نام و سمت">
  </div>
  <div class="signature-box" style="display:flex;align-items:center;justify-content:center;gap:12px">
    <div class="stamp"><span>BANKET</span><span>مهر شرکت</span></div>
    <div style="font-size:10px;color:#777">محل مهر رسمی شرکت</div>
  </div>
</div>

<div class="footer">
  BANKET | تلفن: 02146852366 | کوروش مال، طبقه منفی ۱، پلاک ۱۱
  <br>این برگه پس از تکمیل اطلاعات و امضای طرفین، به‌عنوان سابقه تحویل نگهداری شود.
</div>

</div>
</main>

<!-- رسید مشتری A5 -->
<section class="document a5" id="receipt">
<div class="frame">

<header class="header">
  <div class="receipt-head">
    <div style="text-align:right">
      <div class="brand">BANK<span>ET</span></div>
      <div class="subtitle" style="text-align:right">PRECIOUS METALS</div>
    </div>
    <div style="text-align:center">
      <div style="font-size:16px;font-weight:800">رسید مشتری</div>
      <div class="doc-subtitle">رسید خرید و فروش</div>
    </div>
    <div class="receipt-number">
      شماره رسید<br>
      <input style="width:100%;border:0;border-bottom:1px dotted #aaa;text-align:center;background:transparent;outline:0" placeholder="................">
    </div>
  </div>
</header>

<div class="top-meta">
  <div class="field"><label>تاریخ:</label><input placeholder="روز / ماه / سال"></div>
  <div class="field"><label>ساعت:</label><input placeholder="۰۰:۰۰"></div>
</div>

<div class="section-title">مشخصات مشتری</div>
<div class="receipt-grid">
  <div class="field"><label>نام مشتری:</label><input></div>
  <div class="field"><label>شماره تماس:</label><input inputmode="tel"></div>
</div>

<div class="section-title">مشخصات معامله</div>
<div class="receipt-grid">
  <div class="field"><label>نوع معامله:</label>
    <select>
      <option>خرید از مشتری</option>
      <option>فروش به مشتری</option>
      <option>سایر</option>
    </select>
  </div>
  <div class="field"><label>نوع فلز / کالا:</label><input></div>
  <div class="field"><label>عیار / مشخصات:</label><input></div>
  <div class="field"><label>وزن:</label><input placeholder="گرم"></div>
  <div class="field"><label>قیمت واحد (تومان):</label><input></div>
  <div class="field"><label>اجرت / کارمزد (تومان):</label><input></div>
  <div class="field"><label>سایر هزینه‌ها (تومان):</label><input></div>
  <div class="field"><label>روش پرداخت:</label>
    <select>
      <option>کارت‌خوان</option>
      <option>انتقال بانکی</option>
      <option>نقدی</option>
      <option>سایر</option>
    </select>
  </div>
</div>

<div class="amount-box">
  <strong>مبلغ نهایی معامله (تومان)</strong>
  <input placeholder="۰">
</div>

<div class="field" style="margin-top:8px">
  <label>مبلغ به حروف:</label><input>
</div>

<div class="field" style="margin-top:8px">
  <label>توضیحات:</label><input placeholder="توضیحات و شرایط معامله">
</div>

<div class="receipt-bottom">
  <div class="signature-box">
    <strong>امضای مشتری</strong>
    <small>تأیید دریافت رسید</small>
  </div>
  <div style="text-align:center">
    <div class="stamp"><span>BANKET</span><span>مهر فروشگاه</span></div>
  </div>
  <div class="signature-box">
    <strong>امضا و تأیید فروشنده</strong>
    <small>نماینده مجموعه</small>
  </div>
</div>

<div class="contact">
  <strong class="gold-text">BANKET | بانکِت</strong>
  <br>تلفن: 02146852366
  <br>آدرس: کوروش مال، طبقه منفی ۱، پلاک ۱۱
</div>

</div>
</section>

<script>
function printDocument(id){
  document.querySelectorAll('.document').forEach(el=>{
    el.classList.remove('printing');
  });
  const doc=document.getElementById(id);
  doc.classList.add('printing');
  window.print();
}
window.addEventListener('afterprint',()=>{
  document.querySelectorAll('.document').forEach(el=>{
    el.classList.remove('printing');
  });
});

function previewImage(input,id){
  const img=document.getElementById(id);
  const file=input.files && input.files[0];
  if(!file)return;
  if(!file.type.startsWith('image/')){
    alert('لطفاً فایل تصویری انتخاب کن.');
    input.value='';
    return;
  }
  const reader=new FileReader();
  reader.onload=e=>{
    img.src=e.target.result;
    img.style.display='block';
    const box=img.closest('.id-box');
    const labels=box.querySelectorAll('strong,small');
    labels.forEach(label=>label.style.display='none');
  };
  reader.readAsDataURL(file);
}

function clearForm(){
  if(!confirm('تمام اطلاعات واردشده و تصاویر انتخابی پاک شوند؟'))return;
  document.querySelectorAll('input:not([type=file]),textarea').forEach(el=>{
    el.value='';
  });
  document.querySelectorAll('select').forEach(el=>el.selectedIndex=0);
  document.querySelectorAll('input[type=file]').forEach(el=>el.value='');
  document.querySelectorAll('.id-box img').forEach(img=>{
    img.removeAttribute('src');
    img.style.display='none';
  });
  document.querySelectorAll('.id-box strong,.id-box small').forEach(el=>{
    el.style.display='';
  });
}
</script>
</body>
</html>
