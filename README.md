[tire_inventory_download-12.html](https://github.com/user-attachments/files/30432011/tire_inventory_download-12.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>الزيني للإطارات والبطاريات</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Cairo',sans-serif;background:#eef3fb;color:#111;direction:rtl}
/* SPLASH */
.splash{position:fixed;inset:0;background:linear-gradient(160deg,#1a56db,#1e3a8a 60%,#0f2460);z-index:999;display:flex;flex-direction:column;align-items:center;justify-content:center;overflow-y:auto}
.splash-logo{width:100px;height:100px;background:#fff;border-radius:50%;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 32px rgba(0,0,0,0.2);margin-bottom:20px}
.splash h2{color:#fff;font-size:22px;font-weight:900;margin-bottom:6px;text-align:center}
.splash p{color:rgba(255,255,255,0.75);font-size:13px;margin-bottom:20px}
.splash-search{width:90%;max-width:400px;padding:12px 16px;border:none;border-radius:10px;font-size:14px;font-family:inherit;outline:none;direction:rtl;background:rgba(255,255,255,0.15);color:#fff;border:1.5px solid rgba(255,255,255,0.3);margin-bottom:6px}
.splash-search::placeholder{color:rgba(255,255,255,0.6)}
.splash-results{width:90%;max-width:400px;max-height:250px;overflow-y:auto;border-radius:10px;margin-bottom:10px;display:none}
.splash-results.show{display:block}
.res-item{background:#fff;padding:10px 14px;border-bottom:1px solid #eee;cursor:pointer}
.res-item:hover{background:#dbeafe}
.res-item:first-child{border-radius:10px 10px 0 0}
.res-item:last-child{border-bottom:none;border-radius:0 0 10px 10px}
.res-size{font-size:13px;font-weight:900;color:#1a56db}
.res-type{font-size:11px;color:#555;margin-top:2px}
.res-cat{font-size:10px;color:#888}
.grid-btns{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;width:90%;max-width:400px;margin-bottom:10px}
.hbtn{background:rgba(255,255,255,0.15);color:#fff;border:1.5px solid rgba(255,255,255,0.3);padding:12px 6px;border-radius:10px;font-size:13px;font-family:inherit;font-weight:800;cursor:pointer;text-align:center;transition:all 0.2s}
.hbtn:hover{background:rgba(255,255,255,0.28);transform:translateY(-2px)}
.hbtn-wide{grid-column:span 2;padding:13px}
.enter-btn{margin-top:10px;background:#fff;color:#1a56db;border:none;padding:12px 40px;border-radius:25px;font-size:15px;font-family:inherit;font-weight:900;cursor:pointer;box-shadow:0 4px 16px rgba(0,0,0,0.2)}
/* HEADER */
.header{background:linear-gradient(135deg,#1a56db,#1e3a8a);color:#fff;padding:12px 16px;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:100;box-shadow:0 2px 10px rgba(26,86,219,0.3)}
.hlogo{display:flex;align-items:center;gap:10px}
.hicon{width:36px;height:36px;background:#fff;border-radius:50%;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.htxt h1{font-size:14px;font-weight:900;line-height:1.2}
.htxt p{font-size:10px;opacity:0.75}
.hbtns{display:flex;gap:6px}
.hbtn2{background:rgba(255,255,255,0.15);color:#fff;border:1px solid rgba(255,255,255,0.3);padding:6px 10px;border-radius:5px;cursor:pointer;font-size:11px;font-family:inherit;font-weight:700}
/* TABS */
.tabs{display:flex;background:#fff;border-bottom:2px solid #dbeafe;overflow-x:auto;padding:0 8px}
.tab{padding:10px 12px;cursor:pointer;font-size:12px;font-weight:700;color:#888;white-space:nowrap;border-bottom:3px solid transparent;margin-bottom:-2px;transition:all 0.2s}
.tab.active{color:#1a56db;border-bottom-color:#1a56db}
/* SEARCH */
.search-area{background:#fff;padding:10px;border-bottom:1px solid #dbeafe}
.sinput{width:100%;padding:10px 14px;border:1.5px solid #ddd;border-radius:6px;font-size:14px;font-family:inherit;outline:none;direction:rtl}
.sinput:focus{border-color:#1a56db}
/* STATS */
.stats{display:flex;gap:8px;padding:8px 10px;overflow-x:auto}
.stat{background:#fff;border:1.5px solid #dbeafe;border-radius:6px;padding:8px 12px;min-width:100px;text-align:center;flex-shrink:0}
.stat-n{font-size:18px;font-weight:900}
.stat-l{font-size:10px;color:#888;margin-top:2px}
/* CONTENT */
.content{padding:10px}
.section{background:#fff;border-radius:8px;border:1.5px solid #dbeafe;margin-bottom:10px;overflow:hidden;box-shadow:0 1px 4px rgba(26,86,219,0.06)}
.sec-head{background:linear-gradient(135deg,#1a56db,#1e3a8a);color:#fff;padding:10px 14px;display:flex;align-items:center;justify-content:space-between;cursor:pointer}
.sec-head h3{font-size:13px;font-weight:900}
.sec-info{font-size:11px;opacity:0.7;margin-right:6px}
.tw{overflow-x:auto}
table{width:100%;border-collapse:collapse;min-width:480px}
th{background:#f0f4ff;padding:7px 10px;font-size:11px;font-weight:800;text-align:center;border-bottom:1.5px solid #dbeafe;color:#555;white-space:nowrap}
th.thr{text-align:right}
td{padding:7px 10px;font-size:12px;text-align:center;border-bottom:1px solid #eee;vertical-align:middle}
td.tdr{text-align:right;font-weight:700}
tr:hover td{background:#f8faff}
.editable{border:1px solid transparent;border-radius:4px;padding:2px 6px;cursor:pointer;min-width:40px;display:inline-block;transition:all 0.15s}
.editable:hover{border-color:#ddd;background:#f5f5f5}
.editable:focus{outline:none;border-color:#1a56db;background:#fff}
.c-low{color:#e74c3c;font-weight:900}
.c-ok{color:#27ae60;font-weight:700}
.c-zero{color:#aaa}
.c-year{color:#2980b9;font-weight:900}
.add-btn{width:100%;padding:8px;background:#f8f8f8;border:none;border-top:1px dashed #ddd;color:#888;font-size:12px;font-family:inherit;cursor:pointer;font-weight:700}
.add-btn:hover{background:#eee;color:#1a56db}
.del-btn{background:none;border:none;color:#ccc;cursor:pointer;font-size:13px;padding:2px 4px;border-radius:3px}
.del-btn:hover{color:#e74c3c}
.no-res{text-align:center;padding:40px;color:#aaa;font-size:14px}
/* MODAL */
.overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,0.5);z-index:200;align-items:center;justify-content:center}
.overlay.show{display:flex}
.modal{background:#fff;border-radius:10px;padding:20px;width:92%;max-width:380px}
.modal h3{font-size:15px;font-weight:900;margin-bottom:14px}
.modal input,.modal select{width:100%;padding:9px 12px;border:1.5px solid #ddd;border-radius:5px;font-size:13px;font-family:inherit;margin-bottom:8px;direction:rtl;outline:none}
.modal input:focus,.modal select:focus{border-color:#1a56db}
.mbtn-p{flex:1;padding:9px;background:linear-gradient(135deg,#1a56db,#1e3a8a);color:#fff;border:none;border-radius:5px;font-size:13px;font-family:inherit;font-weight:700;cursor:pointer}
.mbtn-s{flex:1;padding:9px;background:#eee;color:#111;border:none;border-radius:5px;font-size:13px;font-family:inherit;font-weight:700;cursor:pointer}
.mbtns{display:flex;gap:8px;margin-top:6px}
/* LOADING */
.loading{text-align:center;padding:40px;color:#1a56db;font-size:14px;font-weight:700}
.spinner{width:40px;height:40px;border:4px solid #dbeafe;border-top:4px solid #1a56db;border-radius:50%;animation:spin 0.8s linear infinite;margin:0 auto 12px}
@keyframes spin{to{transform:rotate(360deg)}}
/* TOAST */
.toast{position:fixed;bottom:20px;left:50%;transform:translateX(-50%) translateY(100px);background:#1a56db;color:#fff;padding:9px 22px;border-radius:20px;font-size:13px;font-weight:700;z-index:300;transition:transform 0.3s;white-space:nowrap}
.toast.show{transform:translateX(-50%) translateY(0)}
/* SALES */
.sum-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:10px}
.sum-card{background:#fff;border:1.5px solid #dbeafe;border-radius:8px;padding:10px;text-align:center}
.sum-n{font-size:20px;font-weight:900}
.sum-l{font-size:10px;color:#888;margin-top:2px}
.log-item{padding:10px 12px;border-bottom:1px solid #eee;font-size:12px}
.log-sell{border-right:3px solid #e74c3c}
.log-buy{border-right:3px solid #27ae60}
/* OPS */
.ops-tabs{display:flex;gap:8px;margin-bottom:12px}
.ops-tab{flex:1;padding:9px;border:2px solid #dbeafe;border-radius:8px;background:#fff;font-family:inherit;font-size:13px;font-weight:800;cursor:pointer;color:#1a56db;text-align:center}
.ops-tab.active{background:#1a56db;color:#fff;border-color:#1a56db}
.op-select{padding:9px 12px;border:1.5px solid #ddd;border-radius:6px;font-size:13px;font-family:inherit;direction:rtl;outline:none;background:#fff;width:100%;margin-bottom:8px}
.op-btn-sell{background:#e74c3c;color:#fff;width:100%;padding:10px;border:none;border-radius:6px;font-family:inherit;font-size:13px;font-weight:900;cursor:pointer;margin-top:4px}
.op-btn-buy{background:#27ae60;color:#fff;width:100%;padding:10px;border:none;border-radius:6px;font-family:inherit;font-size:13px;font-weight:900;cursor:pointer;margin-top:4px}
@media(max-width:500px){.htxt h1{font-size:12px}.tab{padding:8px 10px;font-size:11px}}
</style>
</head>
<body>

<!-- SPLASH -->
<div class="splash" id="splash">
  <div class="splash-logo">
    <svg width="60" height="60" viewBox="0 0 100 100" fill="none">
      <circle cx="50" cy="50" r="45" stroke="#1a56db" stroke-width="8"/>
      <circle cx="50" cy="50" r="20" fill="#1a56db"/>
      <circle cx="50" cy="50" r="8" fill="#fff"/>
      <line x1="50" y1="5" x2="50" y2="25" stroke="#1a56db" stroke-width="6" stroke-linecap="round"/>
      <line x1="50" y1="75" x2="50" y2="95" stroke="#1a56db" stroke-width="6" stroke-linecap="round"/>
      <line x1="5" y1="50" x2="25" y2="50" stroke="#1a56db" stroke-width="6" stroke-linecap="round"/>
      <line x1="75" y1="50" x2="95" y2="50" stroke="#1a56db" stroke-width="6" stroke-linecap="round"/>
    </svg>
  </div>
  <h2>الزيني للإطارات والبطاريات</h2>
  <p>نظام إدارة المخزون</p>

  <input class="splash-search" id="splashQ" placeholder="🔍 ابحث عن مقاس أو ماركة..." oninput="splashSearch(this.value)">
  <div class="splash-results" id="splashRes"></div>

  <div style="color:rgba(255,255,255,0.8);font-size:12px;font-weight:700;margin-bottom:8px;width:90%;max-width:400px">🛞 الإطارات</div>
  <div class="grid-btns">
    <button class="hbtn" onclick="goTo('جنط 13')">جنط 13</button>
    <button class="hbtn" onclick="goTo('جنط 14')">جنط 14</button>
    <button class="hbtn" onclick="goTo('جنط 15')">جنط 15</button>
    <button class="hbtn" onclick="goTo('جنط 16')">جنط 16</button>
    <button class="hbtn" onclick="goTo('جنط 17')">جنط 17</button>
    <button class="hbtn" onclick="goTo('جنط 18')">جنط 18</button>
    <button class="hbtn" onclick="goTo('جنط 19')">جنط 19</button>
    <button class="hbtn" onclick="goTo('جنط 20')">جنط 20</button>
    <button class="hbtn hbtn-wide" onclick="goTo('كاوتش النقل')">🚛 كاوتش النقل</button>
    <button class="hbtn hbtn-wide" onclick="goTo('رانفلات')">🔵 رانفلات</button>
  </div>
  <div style="color:rgba(255,255,255,0.8);font-size:12px;font-weight:700;margin:6px 0 8px;width:90%;max-width:400px">🔋 البطاريات</div>
  <div style="width:90%;max-width:400px;margin-bottom:16px">
    <button class="hbtn" style="width:100%;padding:13px" onclick="goTo('البطاريات')">🔋 البطاريات</button>
  </div>
  <button class="enter-btn" onclick="hideSplash()">دخول للتطبيق ←</button>
</div>

<!-- HEADER -->
<div class="header">
  <div class="hlogo">
    <div class="hicon">
      <svg width="22" height="22" viewBox="0 0 100 100" fill="none">
        <circle cx="50" cy="50" r="45" stroke="#1a56db" stroke-width="10"/>
        <circle cx="50" cy="50" r="18" fill="#1a56db"/>
        <circle cx="50" cy="50" r="7" fill="#fff"/>
        <line x1="50" y1="5" x2="50" y2="28" stroke="#1a56db" stroke-width="7" stroke-linecap="round"/>
        <line x1="50" y1="72" x2="50" y2="95" stroke="#1a56db" stroke-width="7" stroke-linecap="round"/>
        <line x1="5" y1="50" x2="28" y2="50" stroke="#1a56db" stroke-width="7" stroke-linecap="round"/>
        <line x1="72" y1="50" x2="95" y2="50" stroke="#1a56db" stroke-width="7" stroke-linecap="round"/>
      </svg>
    </div>
    <div class="htxt">
      <h1>الزيني للإطارات والبطاريات</h1>
      <p>نظام إدارة المخزون</p>
    </div>
  </div>
  <div class="hbtns">
    <button class="hbtn2" onclick="openOp()" style="background:rgba(231,76,60,0.4)">🛒 بيع/وارد</button>
    <button class="hbtn2" onclick="showSplash()">🏠</button>
  </div>
</div>

<div class="tabs" id="tabs"></div>
<div class="search-area">
  <input class="sinput" id="mainQ" placeholder="🔍 ابحث بالمقاس أو الماركة..." oninput="filterContent()">
</div>
<div class="stats" id="stats"></div>
<div class="content" id="content">
  <div class="loading"><div class="spinner"></div>جاري تحميل البيانات...</div>
</div>

<!-- Modal: إضافة نوع -->
<div class="overlay" id="modalType">
  <div class="modal">
    <h3>➕ إضافة نوع جديد</h3>
    <input type="text" id="inName" placeholder="اسم الماركة">
    <input type="text" id="inOrigin" placeholder="البلد">
    <input type="number" id="inPrice" placeholder="السعر">
    <input type="number" id="inShop" placeholder="عدد المحل">
    <input type="number" id="inStore" placeholder="عدد المخزن">
    <input type="number" id="inYear" placeholder="سنة الإنتاج">
    <div class="mbtns">
      <button class="mbtn-p" onclick="confirmAddType()">إضافة</button>
      <button class="mbtn-s" onclick="closeM('modalType')">إلغاء</button>
    </div>
  </div>
</div>

<!-- Modal: بيع/وارد -->
<div class="overlay" id="modalOp">
  <div class="modal">
    <h3>🛒 تسجيل عملية</h3>
    <div class="ops-tabs">
      <button class="ops-tab active" id="tabSell" onclick="switchOp('sell')">🔴 بيع</button>
      <button class="ops-tab" id="tabBuy" onclick="switchOp('buy')">🟢 وارد</button>
    </div>
    <select class="op-select" id="opSheet" onchange="loadOpSizes()">
      <option value="">اختر القسم...</option>
    </select>
    <select class="op-select" id="opSize" onchange="loadOpTypes()">
      <option value="">اختر المقاس...</option>
    </select>
    <select class="op-select" id="opType">
      <option value="">اختر النوع...</option>
    </select>
    <input type="number" id="opQty" placeholder="الكمية" min="1" value="1" style="width:100%;padding:9px 12px;border:1.5px solid #ddd;border-radius:6px;font-size:13px;font-family:inherit;direction:rtl;outline:none;margin-bottom:8px">
    <select class="op-select" id="opFrom">
      <option value="shop">من المحل</option>
      <option value="store">من المخزن</option>
      <option value="both">من الاتنين</option>
    </select>
    <button class="op-btn-sell" id="opSubmit" onclick="submitOp()">✅ تأكيد البيع</button>
    <button class="mbtn-s" onclick="closeM('modalOp')" style="width:100%;margin-top:8px">إلغاء</button>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
var DB = {};
var TABS = [];
var currentTab = '';
var currentOp = 'sell';
var addTypeSizeTarget = '';

// تحميل البيانات من Google Sheets
function loadData() {
  // البيانات محملة في window.onload
}

function toast(msg) {
  var t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(function(){ t.classList.remove('show'); }, 2500);
}

function esc(s) {
  if (!s) return '';
  return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;');
}

function cls(v) {
  var n = parseInt(v);
  if (!v || isNaN(n)) return 'c-zero';
  if (n <= 2) return 'c-low';
  return 'c-ok';
}

// SPLASH
function splashSearch(q) {
  var el = document.getElementById('splashRes');
  q = q.trim().toLowerCase();
  if (!q) { el.classList.remove('show'); el.innerHTML=''; return; }
  var qc = q.replace(/[\/\-\. ]/g,'');
  var results = [];
  Object.keys(DB).forEach(function(cat) {
    (DB[cat]||[]).forEach(function(s) {
      var sc = s.size.toLowerCase().replace(/[\/\-\. ]/g,'');
      var ms = s.size.toLowerCase().includes(q) || sc.includes(qc);
      var mt = s.types.some(function(t){ return (t.name+' '+t.origin).toLowerCase().includes(q); });
      if (ms || mt) results.push({cat:cat, s:s});
    });
  });
  if (!results.length) { el.innerHTML='<div class="res-item" style="color:#aaa">لا توجد نتائج</div>'; el.classList.add('show'); return; }
  el.innerHTML = results.slice(0,10).map(function(r) {
    var types = r.s.types.filter(function(t){return t.name;}).map(function(t){return t.name;}).join(' | ');
    var st = r.s.types.reduce(function(a,t){return a+(parseInt(t.shop)||0)+(parseInt(t.store)||0);},0);
    return '<div class="res-item" onclick="goTo(\''+esc(r.cat)+'\',\''+encodeURIComponent(r.s.size)+'\')">'
      +'<div class="res-size">📐 '+esc(r.s.size)+'</div>'
      +(types?'<div class="res-type">'+esc(types)+'</div>':'')
      +'<div class="res-cat">'+esc(r.cat)+' | إجمالي: '+st+' قطعة</div>'
      +'</div>';
  }).join('');
  el.classList.add('show');
}

function goTo(cat, sizeEnc) {
  hideSplash();
  currentTab = cat;
  document.getElementById('mainQ').value = '';
  renderTabs();
  renderStats();
  renderContent();
  if (sizeEnc) {
    var size = decodeURIComponent(sizeEnc);
    setTimeout(function() {
      var secs = document.querySelectorAll('[data-size]');
      secs.forEach(function(sec) {
        if (sec.getAttribute('data-size') === size) {
          sec.scrollIntoView({behavior:'smooth', block:'center'});
          sec.style.boxShadow = '0 0 0 3px #1a56db';
          setTimeout(function(){ sec.style.boxShadow=''; }, 2000);
        }
      });
    }, 400);
  }
}

function hideSplash() {
  var s = document.getElementById('splash');
  s.style.opacity = '0';
  s.style.transition = 'opacity 0.5s';
  setTimeout(function(){ s.style.display='none'; }, 500);
}

function showSplash() {
  var s = document.getElementById('splash');
  s.style.display = 'flex';
  s.style.opacity = '1';
}

// TABS
function renderTabs() {
  var el = document.getElementById('tabs');
  el.innerHTML = TABS.map(function(t) {
    return '<div class="tab'+(t===currentTab?' active':'')+'" onclick="switchTab(\''+esc(t)+'\')">'
      + (t==='البطاريات'?'🔋 ':t==='رانفلات'?'🔵 ':'') + t + '</div>';
  }).join('') + '<div class="tab" onclick="addNewTab()" style="color:#2980b9">＋ جديد</div>';
}

function switchTab(t) {
  currentTab = t;
  document.getElementById('mainQ').value = '';
  renderTabs();
  renderStats();
  renderContent();
}

// STATS
function renderStats() {
  var sizes = DB[currentTab] || [];
  var types=0, shop=0, store=0;
  sizes.forEach(function(s){ s.types.forEach(function(t){ if(t.name)types++; shop+=parseInt(t.shop)||0; store+=parseInt(t.store)||0; }); });
  document.getElementById('stats').innerHTML =
    '<div class="stat"><div class="stat-n">'+sizes.length+'</div><div class="stat-l">مقاسات</div></div>'
    +'<div class="stat"><div class="stat-n">'+types+'</div><div class="stat-l">أنواع</div></div>'
    +'<div class="stat"><div class="stat-n" style="color:#27ae60">'+shop+'</div><div class="stat-l">المحل</div></div>'
    +'<div class="stat"><div class="stat-n" style="color:#2980b9">'+store+'</div><div class="stat-l">المخزن</div></div>';
}

// CONTENT
function renderContent() {
  var q = document.getElementById('mainQ').value.trim().toLowerCase();
  var qc = q.replace(/[\/\-\. ]/g,'');
  var sizes = DB[currentTab] || [];
  var el = document.getElementById('content');

  var filtered = sizes.filter(function(s) {
    if (!q) return true;
    var sc = s.size.toLowerCase().replace(/[\/\-\. ]/g,'');
    if (s.size.toLowerCase().includes(q) || sc.includes(qc)) return true;
    return s.types.some(function(t){ return (t.name+' '+t.origin).toLowerCase().includes(q); });
  });

  if (!filtered.length) {
    el.innerHTML = '<div class="no-res">🔍 لا توجد نتائج</div>'
      +'<div style="text-align:center;padding:10px"><button onclick="openAddSize()" style="padding:9px 20px;background:#1a56db;color:#fff;border:none;border-radius:6px;font-family:inherit;font-weight:700;cursor:pointer">+ إضافة مقاس</button></div>';
    return;
  }

  el.innerHTML = filtered.map(function(s) {
    var shopT = s.types.reduce(function(a,t){return a+(parseInt(t.shop)||0);},0);
    var storeT = s.types.reduce(function(a,t){return a+(parseInt(t.store)||0);},0);
    var rows = s.types.map(function(t, ti) {
      return '<tr>'
        +'<td class="tdr"><span class="editable" contenteditable="true" onblur="upd(\''+esc(s.size)+'\','+ti+',\'name\',this.textContent.trim())">'+esc(t.name)+'</span></td>'
        +'<td><span class="editable" contenteditable="true" onblur="upd(\''+esc(s.size)+'\','+ti+',\'origin\',this.textContent.trim())">'+esc(t.origin)+'</span></td>'
        +'<td><span class="editable" contenteditable="true" onblur="upd(\''+esc(s.size)+'\','+ti+',\'price\',this.textContent.trim())">'+esc(t.price)+'</span></td>'
        +'<td><span class="editable '+cls(t.shop)+'" contenteditable="true" onblur="upd(\''+esc(s.size)+'\','+ti+',\'shop\',this.textContent.trim())">'+esc(t.shop)+'</span></td>'
        +'<td><span class="editable '+cls(t.store)+'" contenteditable="true" onblur="upd(\''+esc(s.size)+'\','+ti+',\'store\',this.textContent.trim())">'+esc(t.store)+'</span></td>'
        +'<td><span class="editable c-year" contenteditable="true" onblur="upd(\''+esc(s.size)+'\','+ti+',\'year\',this.textContent.trim())">'+esc(t.year)+'</span></td>'
        +'<td><button class="del-btn" onclick="delType(\''+esc(s.size)+'\','+ti+')">✕</button></td>'
        +'</tr>';
    }).join('');
    return '<div class="section" data-size="'+esc(s.size)+'">'
      +'<div class="sec-head" onclick="toggleSec(this)">'
      +'<h3>📐 '+esc(s.size)+'<span class="sec-info">محل:'+shopT+' مخزن:'+storeT+'</span></h3>'
      +'<div style="display:flex;gap:6px;align-items:center">'
      +'<button style="background:rgba(255,255,255,0.15);color:#fff;border:none;padding:4px 10px;border-radius:4px;font-size:11px;font-family:inherit;font-weight:700;cursor:pointer" onclick="event.stopPropagation();openAddType(\''+esc(s.size)+'\')">+ نوع</button>'
      +'<span style="font-size:12px">▲</span></div></div>'
      +'<div class="tw"><table><thead><tr>'
      +'<th class="thr">النوع / الماركة</th><th>البلد</th><th>السعر (ج)</th><th>المحل</th><th>المخزن</th><th>سنة الإنتاج</th><th style="width:28px"></th>'
      +'</tr></thead><tbody>'+rows+'</tbody></table>'
      +'<button class="add-btn" onclick="openAddType(\''+esc(s.size)+'\')">+ إضافة نوع</button>'
      +'</div></div>';
  }).join('')
  +'<div style="text-align:center;padding:14px 0"><button onclick="openAddSize()" style="padding:9px 24px;background:#1a56db;color:#fff;border:none;border-radius:6px;font-size:13px;font-family:inherit;font-weight:700;cursor:pointer">+ إضافة مقاس جديد</button></div>';
}

function filterContent() { renderContent(); }

function toggleSec(h) {
  var w = h.nextElementSibling;
  var a = h.querySelector('span:last-child');
  w.style.display = w.style.display==='none' ? '' : 'none';
  if(a) a.textContent = w.style.display==='none' ? '▼' : '▲';
}

// UPDATE
function upd(size, ti, field, val) {
  var sizeObj = (DB[currentTab]||[]).find(function(s){return s.size===size;});
  if (!sizeObj || !sizeObj.types[ti]) return;
  var typeName = sizeObj.types[ti].name;
  sizeObj.types[ti][field] = val;
  // حفظ في localStorage
  localStorage.setItem('tireDB', JSON.stringify(DB));
  renderStats();
}

// ADD SIZE
function openAddSize() {
  var name = prompt('اسم المقاس الجديد (مثال: 205/55/16):');
  if (!name || !name.trim()) return;
  if (!DB[currentTab]) DB[currentTab] = [];
  DB[currentTab].push({size:name.trim(), types:[{name:'',origin:'',price:'',shop:'',store:'',year:''}]});
  renderContent();
  toast('✅ تم إضافة المقاس');
}

// ADD TYPE
var addTypeSize = '';
function openAddType(size) {
  addTypeSize = size;
  ['inName','inOrigin','inPrice','inShop','inStore','inYear'].forEach(function(id){document.getElementById(id).value='';});
  document.getElementById('modalType').classList.add('show');
}

function confirmAddType() {
  var name = document.getElementById('inName').value.trim();
  if (!name) { alert('أدخل اسم الماركة'); return; }
  var t = {
    name: name,
    origin: document.getElementById('inOrigin').value.trim(),
    price: document.getElementById('inPrice').value.trim(),
    shop: document.getElementById('inShop').value.trim(),
    store: document.getElementById('inStore').value.trim(),
    year: document.getElementById('inYear').value.trim(),
  };
  var sizeObj = (DB[currentTab]||[]).find(function(s){return s.size===addTypeSize;});
  if (sizeObj) sizeObj.types.push(t);
  localStorage.setItem('tireDB', JSON.stringify(DB));
  toast('✅ تم إضافة '+name);
  renderContent();
  renderStats();
  closeM('modalType');
}

function delType(size, ti) {
  if (!confirm('حذف هذا النوع؟')) return;
  var sizeObj = (DB[currentTab]||[]).find(function(s){return s.size===size;});
  if (sizeObj) sizeObj.types.splice(ti, 1);
  renderContent(); renderStats();
  toast('🗑 تم الحذف');
}

function addNewTab() {
  var name = prompt('اسم القسم الجديد:');
  if (!name||!name.trim()) return;
  TABS.push(name.trim());
  DB[name.trim()] = [];
  currentTab = name.trim();
  renderTabs(); renderStats(); renderContent();
  toast('✅ تم إضافة '+name.trim());
}

// OPS
function openOp() {
  var sel = document.getElementById('opSheet');
  sel.innerHTML = '<option value="">اختر القسم...</option>';
  TABS.forEach(function(t){ sel.innerHTML += '<option value="'+esc(t)+'">'+esc(t)+'</option>'; });
  document.getElementById('opSize').innerHTML = '<option value="">اختر المقاس...</option>';
  document.getElementById('opType').innerHTML = '<option value="">اختر النوع...</option>';
  document.getElementById('opQty').value = 1;
  switchOp('sell');
  document.getElementById('modalOp').classList.add('show');
}

function switchOp(op) {
  currentOp = op;
  document.getElementById('tabSell').classList.toggle('active', op==='sell');
  document.getElementById('tabBuy').classList.toggle('active', op==='buy');
  var btn = document.getElementById('opSubmit');
  btn.textContent = op==='sell' ? '✅ تأكيد البيع' : '✅ تأكيد الوارد';
  btn.className = op==='sell' ? 'op-btn-sell' : 'op-btn-buy';
}

function loadOpSizes() {
  var cat = document.getElementById('opSheet').value;
  var sel = document.getElementById('opSize');
  sel.innerHTML = '<option value="">اختر المقاس...</option>';
  document.getElementById('opType').innerHTML = '<option value="">اختر النوع...</option>';
  if (!cat) return;
  (DB[cat]||[]).forEach(function(s,i){ sel.innerHTML += '<option value="'+i+'">'+esc(s.size)+'</option>'; });
}

function loadOpTypes() {
  var cat = document.getElementById('opSheet').value;
  var si = parseInt(document.getElementById('opSize').value);
  var sel = document.getElementById('opType');
  sel.innerHTML = '<option value="">اختر النوع...</option>';
  if (!cat || isNaN(si)) return;
  var sizeObj = (DB[cat]||[])[si];
  if (!sizeObj) return;
  sizeObj.types.forEach(function(t,i){
    if (!t.name) return;
    sel.innerHTML += '<option value="'+i+'">'+esc(t.name)+(t.origin?' ('+esc(t.origin)+')':'')
      +' | محل:'+(t.shop||0)+' مخزن:'+(t.store||0)+'</option>';
  });
}

function submitOp() {
  var cat = document.getElementById('opSheet').value;
  var si = parseInt(document.getElementById('opSize').value);
  var ti = parseInt(document.getElementById('opType').value);
  var qty = parseInt(document.getElementById('opQty').value)||0;
  var from = document.getElementById('opFrom').value;
  if (!cat||isNaN(si)||isNaN(ti)||qty<=0) { alert('اختر القسم والمقاس والنوع والكمية!'); return; }
  var sizeObj = (DB[cat]||[])[si];
  var typeObj = sizeObj.types[ti];
  var price = parseFloat(typeObj.price)||0;
  if (currentOp==='sell') {
    var curShop = parseInt(typeObj.shop)||0;
    var curStore = parseInt(typeObj.store)||0;
    if (from==='shop'&&qty>curShop) { alert('المحل فيه '+curShop+' فقط!'); return; }
    if (from==='store'&&qty>curStore) { alert('المخزن فيه '+curStore+' فقط!'); return; }
    if (from==='shop') typeObj.shop = String(curShop-qty);
    else if (from==='store') typeObj.store = String(curStore-qty);
    else { typeObj.shop = String(Math.max(0,curShop-Math.ceil(qty/2))); typeObj.store = String(Math.max(0,curStore-Math.floor(qty/2))); }
    localStorage.setItem('tireDB', JSON.stringify(DB));
    toast('✅ تم تسجيل البيع - ' + qty + ' قطعة');
    renderContent(); renderStats();
  } else {
    typeObj.store = String((parseInt(typeObj.store)||0)+qty);
    localStorage.setItem('tireDB', JSON.stringify(DB));
    toast('✅ تم إضافة الوارد - ' + qty + ' قطعة');
    renderContent(); renderStats();
  }
  closeM('modalOp');
}

function closeM(id) { document.getElementById(id).classList.remove('show'); }
document.querySelectorAll('.overlay').forEach(function(el){
  el.addEventListener('click', function(e){ if(e.target===el) el.classList.remove('show'); });
});

// INIT - البيانات محملة محلياً
var INITIAL_DATA = {"r13": [{"size": "175/70/13", "types": [{"name": "جي تي", "origin": "اندونيسي", "price": "2200", "shop": "1", "store": "", "year": ""}, {"name": "هي كوبا", "origin": "صيني", "price": "1700", "shop": "2", "store": "1", "year": ""}, {"name": "سينوفيل", "origin": "صيني", "price": "", "shop": "0", "store": "", "year": ""}, {"name": "ميراج", "origin": "صيني", "price": "1500", "shop": "2", "store": "2", "year": ""}, {"name": "مرشال", "origin": "كوري", "price": "1950", "shop": "2", "store": "", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "1900", "shop": "2", "store": "2", "year": ""}, {"name": "داينمو صيني", "origin": "صيني", "price": "1600", "shop": "2", "store": "9", "year": ""}, {"name": "لاسا", "origin": "تركي", "price": "1950", "shop": "2", "store": "6", "year": ""}]}, {"size": "165/65/13", "types": [{"name": "بتلس تركي", "origin": "تركي", "price": "2150", "shop": "2", "store": "4", "year": ""}, {"name": "ستار ماكس", "origin": "تركي", "price": "2150", "shop": "3", "store": "", "year": ""}, {"name": "امريكان", "origin": "تايلاندي", "price": "2150", "shop": "2", "store": "2", "year": ""}, {"name": "بتلس تركي 26", "origin": "تركي", "price": "2350", "shop": "", "store": "", "year": ""}]}, {"size": "155/65/13", "types": [{"name": "بتلس", "origin": "تركي", "price": "2100", "shop": "", "store": "", "year": ""}, {"name": "هدواي", "origin": "صيني", "price": "1650", "shop": "2", "store": "", "year": ""}]}, {"size": "155/70/13", "types": [{"name": "جي تي", "origin": "اندونيسي", "price": "2200", "shop": "2", "store": "2", "year": ""}, {"name": "بطلس", "origin": "تركي", "price": "2100", "shop": "2", "store": "8", "year": ""}, {"name": "ستار ماكس", "origin": "تركي", "price": "2000", "shop": "2", "store": "2", "year": ""}, {"name": "كروس وند", "origin": "صربي", "price": "1850", "shop": "2", "store": "6", "year": ""}]}, {"size": "185/60/13", "types": [{"name": "اكس ليرا", "origin": "تايلاندي", "price": "2200", "shop": "2", "store": "4", "year": ""}]}, {"size": "165/70/13", "types": [{"name": "داينمو", "origin": "صيني", "price": "1650", "shop": "2", "store": "", "year": ""}, {"name": "بتلس", "origin": "تركي", "price": "2100", "shop": "2", "store": "2", "year": ""}]}, {"size": "185/70/13", "types": [{"name": "", "origin": "", "price": "", "shop": "", "store": "", "year": ""}, {"name": "داينمو", "origin": "صيني", "price": "1800", "shop": "4", "store": "", "year": "2026"}]}], "r14": [{"size": "165/60/14", "types": [{"name": "مرشال", "origin": "كوري", "price": "2800", "shop": "1", "store": "", "year": ""}, {"name": "هي كوبا", "origin": "صيني", "price": "1900", "shop": "2", "store": "8", "year": ""}, {"name": "اتلندر", "origin": "تايلاندي", "price": "2200", "shop": "2", "store": "3", "year": ""}, {"name": "كومهو", "origin": "كوري", "price": "2800", "shop": "2", "store": "1", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "2400", "shop": "2", "store": "2", "year": ""}, {"name": "لاسا", "origin": "تركي", "price": "2600", "shop": "2", "store": "2", "year": ""}]}, {"size": "185/60/14", "types": [{"name": "هي كوبا", "origin": "صيني", "price": "1850", "shop": "2", "store": "", "year": ""}, {"name": "لوفن", "origin": "كوري", "price": "2600", "shop": "2", "store": "", "year": ""}, {"name": "هانكوك", "origin": "مجري", "price": "2900", "shop": "2", "store": "", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "2400", "shop": "2", "store": "2", "year": ""}, {"name": "اتلاندر تالاندي", "origin": "تايلاند", "price": "2200", "shop": "2", "store": "2", "year": "2026"}]}, {"size": "165/65/14", "types": [{"name": "اتلندر", "origin": "تايلاندي", "price": "2250", "shop": "1", "store": "1", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "3200", "shop": "2", "store": "", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "2400", "shop": "2", "store": "2", "year": ""}]}, {"size": "165/70/14", "types": [{"name": "", "origin": "", "price": "", "shop": "", "store": "", "year": ""}]}, {"size": "175/65/14", "types": [{"name": "هيدواي", "origin": "صيني", "price": "1850", "shop": "2", "store": "2", "year": ""}]}, {"size": "185/65/14", "types": [{"name": "لوفن", "origin": "كوري", "price": "2600", "shop": "2", "store": "", "year": ""}, {"name": "ديليام", "origin": "اندونيسيا", "price": "2400", "shop": "", "store": "", "year": ""}, {"name": "هي كوبا", "origin": "صيني", "price": "1850", "shop": "", "store": "", "year": ""}, {"name": "امريكان", "origin": "تايلاندي", "price": "2200", "shop": "2", "store": "4", "year": ""}, {"name": "كروس وند", "origin": "صربيا 🇷🇸", "price": "2400", "shop": "2", "store": "2", "year": ""}]}, {"size": "185/70/14", "types": [{"name": "هانكوك", "origin": "كوري", "price": "2900", "shop": "2", "store": "", "year": ""}, {"name": "شوينج", "origin": "تايلاندي", "price": "2200", "shop": "3", "store": "", "year": ""}, {"name": "اتلاندر", "origin": "تايلاندي", "price": "2200", "shop": "2", "store": "", "year": ""}, {"name": "لوفين كوري", "origin": "كوريا 🇰🇷", "price": "2650", "shop": "2", "store": "4", "year": ""}]}, {"size": "175/70/14", "types": [{"name": "", "origin": "", "price": "", "shop": "", "store": "", "year": ""}]}, {"size": "175/60/14", "types": [{"name": "", "origin": "", "price": "", "shop": "", "store": "", "year": ""}, {"name": "كروس وند", "origin": "صربيا 🇷🇸", "price": "2400", "shop": "2", "store": "", "year": "2026"}]}], "r15": [{"size": "185/65/15", "types": [{"name": "هانكوك", "origin": "كوري", "price": "3200", "shop": "2", "store": "1", "year": ""}, {"name": "اتلندر", "origin": "تايلاندي", "price": "2500", "shop": "2", "store": "5", "year": ""}, {"name": "هيدواي", "origin": "صيني", "price": "2150", "shop": "1", "store": "", "year": ""}, {"name": "هاكوبا", "origin": "صيني", "price": "2150", "shop": "4", "store": "", "year": ""}, {"name": "لوفن", "origin": "كوري", "price": "2800", "shop": "2", "store": "6", "year": ""}, {"name": "كروس وند", "origin": "صربيا", "price": "2650", "shop": "2", "store": "4", "year": "2026"}, {"name": "شاوينج", "origin": "تايلاند 🇹🇭", "price": "2500", "shop": "2", "store": "4", "year": "2026"}]}, {"size": "195/65/15", "types": [{"name": "ليو", "origin": "صيني", "price": "2150", "shop": "2", "store": "3", "year": ""}, {"name": "هانكوك", "origin": "مجري", "price": "3500", "shop": "", "store": "", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "3850", "shop": "", "store": "", "year": ""}, {"name": "لاسا", "origin": "تركي", "price": "2900", "shop": "", "store": "", "year": ""}, {"name": "شاويانج", "origin": "تايلاندي", "price": "2600", "shop": "", "store": "", "year": ""}, {"name": "لوفين", "origin": "كوريا 🇰🇷", "price": "3000", "shop": "2", "store": "3", "year": ""}]}, {"size": "195/60/15", "types": [{"name": "كمهو", "origin": "فتنامي", "price": "2700", "shop": "1", "store": "", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "", "shop": "", "store": "", "year": ""}, {"name": "هيكوبا", "origin": "صيني", "price": "2200", "shop": "", "store": "", "year": ""}, {"name": "صنفل", "origin": "صيني", "price": "2000", "shop": "", "store": "", "year": ""}, {"name": "اتلندر", "origin": "تايلاندي", "price": "2650", "shop": "2", "store": "1", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "3300", "shop": "2", "store": "2", "year": ""}, {"name": "لوفن", "origin": "كوري", "price": "3000", "shop": "2", "store": "", "year": ""}, {"name": "كروس وند", "origin": "صربيا", "price": "2650", "shop": "2", "store": "2", "year": ""}]}, {"size": "195/50/15", "types": [{"name": "دينامو", "origin": "صيني", "price": "2100", "shop": "2", "store": "", "year": ""}, {"name": "اتلندر", "origin": "تايلاندي", "price": "2500", "shop": "2", "store": "2", "year": ""}, {"name": "ليو", "origin": "صيني", "price": "", "shop": "", "store": "", "year": ""}]}, {"size": "185/55/15", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "2700", "shop": "2", "store": "2", "year": ""}, {"name": "مرشال", "origin": "كوري", "price": "3200", "shop": "2", "store": "", "year": ""}, {"name": "اتلندر", "origin": "تايلاندي", "price": "2500", "shop": "2", "store": "1", "year": ""}]}, {"size": "175/50/15", "types": [{"name": "اتلندر", "origin": "تايلاندي", "price": "2500", "shop": "", "store": "", "year": ""}]}, {"size": "195/55/15", "types": [{"name": "شارينج", "origin": "تايلاندي", "price": "2400", "shop": "1", "store": "", "year": ""}]}, {"size": "205/65/15", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "2900", "shop": "2", "store": "2", "year": ""}, {"name": "هيكوبا", "origin": "صيني", "price": "2300", "shop": "2", "store": "", "year": ""}]}], "r16": [{"size": "205/55/16", "types": [{"name": "ميشلان", "origin": "ألماني", "price": "5500", "shop": "2", "store": "10", "year": "2026"}, {"name": "كونتيننتال", "origin": "فرنساوي", "price": "4500", "shop": "0", "store": "", "year": ""}, {"name": "برجستون", "origin": "تركي", "price": "4350", "shop": "2", "store": "2", "year": ""}, {"name": "يوكوهاما", "origin": "ياباني", "price": "4000", "shop": "2", "store": "2", "year": ""}, {"name": "جدير", "origin": "ألماني", "price": "3900", "shop": "2", "store": "8", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "3850", "shop": "0", "store": "", "year": ""}, {"name": "هانكوك", "origin": "مجري", "price": "2900", "shop": "2", "store": "0", "year": "2024"}, {"name": "لوفن", "origin": "كوري", "price": "3300", "shop": "2", "store": "", "year": ""}, {"name": "لاسيا", "origin": "تركي", "price": "3250", "shop": "2", "store": "", "year": ""}, {"name": "بتلس", "origin": "تركي", "price": "3000", "shop": "0", "store": "", "year": ""}, {"name": "تا", "origin": "تايلاندي", "price": "2700", "shop": "2", "store": "2", "year": ""}, {"name": "رود ستار", "origin": "تايلاندي", "price": "2700", "shop": "2", "store": "4", "year": ""}, {"name": "هيدواي", "origin": "صيني", "price": "2150", "shop": "4", "store": "9", "year": ""}, {"name": "كمهو", "origin": "كوري", "price": "3400", "shop": "2", "store": "5", "year": ""}, {"name": "شاوينج", "origin": "تايلاندي", "price": "2700", "shop": "2", "store": "3", "year": ""}]}, {"size": "205/60/16", "types": [{"name": "ميشلان", "origin": "ألماني", "price": "5500", "shop": "0", "store": "0", "year": ""}, {"name": "دتنلوب", "origin": "ياباني", "price": "4500", "shop": "2", "store": "8", "year": "2025"}, {"name": "برجستون", "origin": "بولندي", "price": "4500", "shop": "1/1", "store": "3", "year": "2025/2024"}, {"name": "هانكوك", "origin": "كوري", "price": "4250", "shop": "2", "store": "", "year": "2025"}, {"name": "هانكوك", "origin": "مجري", "price": "4000", "shop": "2", "store": "1", "year": "2025"}, {"name": "كومهو", "origin": "كوري", "price": "4100", "shop": "2", "store": "3", "year": "2025"}, {"name": "اتلاندر", "origin": "تايلاندي", "price": "2850", "shop": "2", "store": "8", "year": "2026"}, {"name": "هدواي", "origin": "صيني", "price": "2350", "shop": "2", "store": "1", "year": "2025"}]}, {"size": "195/50/16", "types": [{"name": "اطلس", "origin": "تركي", "price": "2300", "shop": "2", "store": "", "year": ""}]}, {"size": "195/55/16", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "2850", "shop": "2", "store": "2", "year": ""}, {"name": "كومكو", "origin": "كوري", "price": "4400", "shop": "2", "store": "", "year": ""}, {"name": "ترانس ميت", "origin": "صيني", "price": "2200", "shop": "1", "store": "", "year": ""}]}, {"size": "195/60/16", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "3500", "shop": "2", "store": "2", "year": ""}]}, {"size": "185/55/16", "types": [{"name": "ترانس ميت", "origin": "صيني", "price": "2400", "shop": "2", "store": "2", "year": "2024"}]}, {"size": "205/65/16", "types": [{"name": "اتلندر", "origin": "تايلاندي", "price": "3250", "shop": "2", "store": "2", "year": ""}]}, {"size": "225/55/16", "types": [{"name": "كروسنت", "origin": "صربي", "price": "2600", "shop": "2", "store": "2", "year": ""}]}, {"size": "215/70/16", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "3800", "shop": "2", "store": "2", "year": ""}]}, {"size": "215/65/16", "types": [{"name": "اتلاندر تايلاندي", "origin": "تايلاندي", "price": "3700", "shop": "2", "store": "2", "year": ""}, {"name": "كروس وند صربي", "origin": "صربي", "price": "4000", "shop": "2", "store": "0", "year": ""}]}, {"size": "215/60/16", "types": [{"name": "كروسنت", "origin": "صربي", "price": "", "shop": "", "store": "", "year": ""}]}, {"size": "215/55/16", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "3600", "shop": "2", "store": "2", "year": ""}]}, {"size": "215/45/16", "types": [{"name": "بطلس", "origin": "تركي", "price": "3800", "shop": "1", "store": "", "year": "2026"}]}], "r17": [{"size": "225/45/17", "types": [{"name": "هانكوك", "origin": "كوري", "price": "4500", "shop": "1", "store": "3", "year": ""}, {"name": "لانجستر", "origin": "تايلاندي", "price": "3650", "shop": "1", "store": "2", "year": ""}, {"name": "ميشلان", "origin": "اسباني", "price": "6200", "shop": "1", "store": "3", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "3700", "shop": "1", "store": "3", "year": ""}, {"name": "كودير", "origin": "فرنسي", "price": "5000", "shop": "1", "store": "3", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "3800", "shop": "1", "store": "3", "year": ""}, {"name": "لوفن", "origin": "كوري", "price": "3500", "shop": "1", "store": "1", "year": ""}, {"name": "دينامو", "origin": "صيني", "price": "3200", "shop": "1", "store": "3", "year": ""}, {"name": "برجستون", "origin": "بولندي", "price": "5000", "shop": "1", "store": "2", "year": ""}, {"name": "كمهو", "origin": "كوري", "price": "4000", "shop": "1", "store": "3", "year": ""}, {"name": "اتلاندر", "origin": "تيلاندي", "price": "", "shop": "", "store": "4", "year": ""}]}, {"size": "225/60/17", "types": [{"name": "هيكوبا", "origin": "صيني", "price": "3300", "shop": "1", "store": "3", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "4250", "shop": "1", "store": "1", "year": ""}, {"name": "هانكوك", "origin": "مجري", "price": "5800", "shop": "1", "store": "12", "year": "25_26"}, {"name": "لانجستر", "origin": "تايلاندي", "price": "3900", "shop": "0", "store": "0", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "4900", "shop": "1", "store": "1", "year": "24"}]}, {"size": "225/50/17", "types": [{"name": "هيكوبا", "origin": "صيني", "price": "3300", "shop": "1", "store": "1", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "6000", "shop": "1", "store": "7", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "3900", "shop": "1", "store": "0", "year": "24"}, {"name": "لوفن", "origin": "كوري", "price": "4800", "shop": "1", "store": "5", "year": ""}, {"name": "دينامو", "origin": "صيني", "price": "3500", "shop": "1", "store": "3", "year": ""}, {"name": "زيتا", "origin": "تيلاندي", "price": "3800", "shop": "1", "store": "0", "year": ""}, {"name": "اتلاندر", "origin": "تيلاندي", "price": "3800", "shop": "1", "store": "3", "year": ""}, {"name": "يوكوهاما", "origin": "يباني", "price": "5000", "shop": "1", "store": "3", "year": ""}]}, {"size": "225/55/17", "types": [{"name": "كومهو", "origin": "كوري", "price": "2800", "shop": "1", "store": "0", "year": "2022"}, {"name": "كروس ويند", "origin": "صربي", "price": "4200", "shop": "1", "store": "3", "year": ""}]}, {"size": "215/45/17", "types": [{"name": "زيتا", "origin": "تايلاندي", "price": "3500", "shop": "1", "store": "1", "year": ""}, {"name": "دينامو", "origin": "صيني", "price": "2950", "shop": "1", "store": "2", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "4000", "shop": "1", "store": "0", "year": ""}]}, {"size": "215/50/17", "types": [{"name": "كومهو", "origin": "كوري", "price": "4300", "shop": "1", "store": "1", "year": "24"}, {"name": "هانكوك", "origin": "مجري", "price": "5300", "shop": "1", "store": "1", "year": ""}, {"name": "يوكوهاما", "origin": "ياباني", "price": "5000", "shop": "1", "store": "3", "year": ""}, {"name": "شاويانج", "origin": "تيلاندي", "price": "3400", "shop": "1", "store": "3", "year": ""}, {"name": "كروس وايند", "origin": "صربي", "price": "4000", "shop": "1", "store": "3", "year": ""}]}, {"size": "215/55/17", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "4000", "shop": "1", "store": "1", "year": ""}, {"name": "اتلندر", "origin": "تايلاندي", "price": "3800", "shop": "1", "store": "5", "year": ""}]}, {"size": "215/60/17", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "4200", "shop": "1", "store": "0", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "5600", "shop": "1", "store": "5", "year": ""}]}, {"size": "205/45/17", "types": [{"name": "مارشال", "origin": "كوري", "price": "3500", "shop": "1", "store": "0", "year": "24"}, {"name": "بلاك هوك", "origin": "صيني", "price": "2500", "shop": "1", "store": "0", "year": "24"}]}, {"size": "205/55/17", "types": [{"name": "كومهو", "origin": "كوري", "price": "5200", "shop": "1", "store": "3", "year": ""}, {"name": "كروس وايند", "origin": "صيربي", "price": "3800", "shop": "1", "store": "3", "year": ""}, {"name": "بلاك هوك", "origin": "صيني", "price": "2600", "shop": "1", "store": "0", "year": "24"}, {"name": "لوفين", "origin": "مجري", "price": "4000", "shop": "1", "store": "1", "year": ""}]}, {"size": "225/65/17", "types": [{"name": "لانكستر", "origin": "تايلاندي", "price": "4250", "shop": "1", "store": "1", "year": ""}, {"name": "لوفن", "origin": "كوري", "price": "2800", "shop": "1", "store": "0", "year": ""}]}, {"size": "215/65/17", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "4000", "shop": "1", "store": "3", "year": ""}]}], "r18": [{"size": "225/40/18", "types": [{"name": "زيتا", "origin": "تايلاندي", "price": "4500", "shop": "1", "store": "1", "year": ""}, {"name": "بطلس", "origin": "تركي", "price": "0", "shop": "0", "store": "0", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "5800", "shop": "1", "store": "0", "year": "24"}, {"name": "كروس ويند", "origin": "صربي", "price": "4900", "shop": "1", "store": "3", "year": "26"}, {"name": "اكس ليرا", "origin": "اندونيسي", "price": "3900", "shop": "1", "store": "3", "year": "24"}, {"name": "مارشال", "origin": "كوري", "price": "4800", "shop": "1", "store": "0", "year": "24"}, {"name": "دينامو", "origin": "صيني", "price": "3700", "shop": "1", "store": "1", "year": ""}]}, {"size": "225/45/18", "types": [{"name": "بطلس", "origin": "تركي", "price": "4250", "shop": "0", "store": "0", "year": ""}, {"name": "اتلندر", "origin": "تايلاندي", "price": "4200", "shop": "1", "store": "0", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "4500", "shop": "1", "store": "3", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "5800", "shop": "1", "store": "0", "year": ""}, {"name": "دينامو", "origin": "صيني", "price": "3250", "shop": "1", "store": "2", "year": ""}]}, {"size": "235/45/18", "types": [{"name": "ميشلان", "origin": "اسباني", "price": "6900", "shop": "1", "store": "3", "year": "24"}, {"name": "مارشال", "origin": "كوري", "price": "5800", "shop": "1", "store": "3", "year": "26"}, {"name": "كروس ويند", "origin": "صربي", "price": "4800", "shop": "1", "store": "3", "year": ""}, {"name": "دينامو", "origin": "صيني", "price": "3250", "shop": "1", "store": "5", "year": ""}, {"name": "امريكان", "origin": "تايلاندي", "price": "4200", "shop": "1", "store": "2", "year": ""}]}, {"size": "215/40/18", "types": [{"name": "زيتا", "origin": "تايلاندي", "price": "4000", "shop": "1", "store": "1", "year": "25"}, {"name": "بطلس", "origin": "تركي", "price": "5000", "shop": "1", "store": "0", "year": "25"}, {"name": "اتلاندر", "origin": "تيلاندي", "price": "4000", "shop": "1", "store": "1", "year": "26"}]}, {"size": "215/45/18", "types": [{"name": "بطلس", "origin": "تركي", "price": "4250", "shop": "1", "store": "0", "year": "24"}, {"name": "زيتا", "origin": "تايلاندي", "price": "4000", "shop": "1", "store": "0", "year": "25"}]}, {"size": "215/50/18", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "4500", "shop": "1", "store": "1", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "6000", "shop": "0", "store": "0", "year": ""}, {"name": "جوديير", "origin": "الماني", "price": "", "shop": "1", "store": "0", "year": "25"}]}, {"size": "215/55/18", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "4500", "shop": "1", "store": "3", "year": ""}, {"name": "بطلس", "origin": "تركي", "price": "5000", "shop": "1", "store": "0", "year": "25"}]}, {"size": "225/50/18", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "4800", "shop": "1", "store": "6", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "0", "shop": "", "store": "", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "0", "shop": "", "store": "", "year": ""}]}, {"size": "225/55/18", "types": [{"name": "ميشلان", "origin": "ألماني", "price": "8500", "shop": "1", "store": "2", "year": ""}, {"name": "كروس ويند", "origin": "صربي", "price": "4800", "shop": "1", "store": "3", "year": ""}, {"name": "دينامو", "origin": "صيني", "price": "4000", "shop": "1", "store": "3", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "7500", "shop": "1", "store": "1", "year": ""}]}, {"size": "225/60/18", "types": [{"name": "اطلس", "origin": "تايلاندي", "price": "3750", "shop": "1", "store": "3", "year": "24"}]}, {"size": "235/50/18", "types": [{"name": "اتلندر", "origin": "تايلاندي", "price": "4500", "shop": "1", "store": "3", "year": "26"}, {"name": "كروس ويند", "origin": "صربي", "price": "4800", "shop": "", "store": "", "year": ""}, {"name": "بطلس", "origin": "تركي", "price": "5000", "shop": "", "store": "", "year": ""}]}, {"size": "235/55/18", "types": [{"name": "كروس وايند", "origin": "صيربي", "price": "4800", "shop": "1", "store": "3", "year": "2026"}, {"name": "مارشال", "origin": "كوري", "price": "6000", "shop": "1", "store": "3", "year": "2026"}, {"name": "بتلس", "origin": "تركي", "price": "4800", "shop": "1", "store": "1", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "7000", "shop": "1", "store": "1", "year": "2026"}]}, {"size": "245/45/18", "types": [{"name": "لوفن", "origin": "كوري", "price": "5000", "shop": "1", "store": "3", "year": ""}]}], "r19": [{"size": "235/50/19", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "5000", "shop": "1", "store": "2", "year": ""}, {"name": "دينامو", "origin": "صيني", "price": "4300", "shop": "1", "store": "2", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "8000", "shop": "1", "store": "4", "year": ""}, {"name": "بيرلي", "origin": "روماني", "price": "10500", "shop": "1", "store": "3", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "6300", "shop": "1", "store": "0", "year": "24"}, {"name": "بتلس", "origin": "تركي", "price": "5250", "shop": "1", "store": "3", "year": "26"}]}, {"size": "245/45/19", "types": [{"name": "لوفين", "origin": "كوري", "price": "6350", "shop": "1", "store": "0", "year": ""}, {"name": "هانكوك", "origin": "كوري", "price": "9500", "shop": "1", "store": "1", "year": ""}, {"name": "بلس", "origin": "تركي", "price": "5800", "shop": "1", "store": "4", "year": "26"}, {"name": "لانكستر", "origin": "تايلاندي", "price": "", "shop": "", "store": "", "year": ""}, {"name": "", "origin": "", "price": "", "shop": "", "store": "", "year": ""}, {"name": "مارشال", "origin": "كوري", "price": "", "shop": "", "store": "", "year": ""}]}, {"size": "255/45/19", "types": [{"name": "ليو", "origin": "تايلاندي", "price": "6500", "shop": "1", "store": "6", "year": "26"}, {"name": "كونتيننتال", "origin": "برتغال", "price": "18500", "shop": "2", "store": "", "year": "26"}, {"name": "ميشلان", "origin": "بولندي", "price": "16000", "shop": "1", "store": "2", "year": "26"}, {"name": "بيرلي  لحام داخلي", "origin": "روماني", "price": "17200", "shop": "1", "store": "3", "year": "26"}, {"name": "ميشلان  100W", "origin": "مجري", "price": "16500", "shop": "1", "store": "0", "year": "52-25"}, {"name": "بريلي", "origin": "روماني", "price": "15500", "shop": "1", "store": "1", "year": "25"}]}, {"size": "235/45/19", "types": [{"name": "اكس ليرا", "origin": "اندونيسي", "price": "5500", "shop": "1", "store": "1", "year": "24"}, {"name": "اكس ليرا", "origin": "اندونيسي", "price": "6500", "shop": "2", "store": "0", "year": "26"}]}, {"size": "235/40/19", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "7000", "shop": "1", "store": "4", "year": ""}, {"name": "رودستون", "origin": "كوري", "price": "8000", "shop": "1", "store": "1", "year": ""}]}, {"size": "235/55/19", "types": [{"name": "بتلس", "origin": "تركي", "price": "6000", "shop": "1", "store": "1", "year": ""}]}, {"size": "245/40/19", "types": [{"name": "بيرلي", "origin": "روماني", "price": "12500", "shop": "1", "store": "2", "year": "26"}, {"name": "اتلاندر", "origin": "تيلاندي", "price": "4800", "shop": "1", "store": "3", "year": ""}]}, {"size": "225/45/19", "types": [{"name": "هاكوبا صيني", "origin": "صيني", "price": "3500", "shop": "1", "store": "2", "year": "2026"}, {"name": "امريكان", "origin": "تايلاندي", "price": "4300", "shop": "1", "store": "", "year": "2026"}, {"name": "بتلس تركي", "origin": "تركي", "price": "5500", "shop": "1", "store": "3", "year": ""}]}, {"size": "225/55/19", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "5500", "shop": "1", "store": "3", "year": ""}]}], "r20": [{"size": "235/50/20", "types": [{"name": "بيرلي", "origin": "روماني", "price": "16500", "shop": "2", "store": "", "year": ""}, {"name": "بيرلي", "origin": "ألماني", "price": "14500", "shop": "1", "store": "0", "year": "2024"}]}, {"size": "235/45/20", "types": [{"name": "هانكوك", "origin": "مجري", "price": "13500", "shop": "1", "store": "4", "year": "2026/11"}, {"name": "ميشلان", "origin": "اسباني", "price": "", "shop": "", "store": "", "year": ""}]}, {"size": "255/40/20", "types": [{"name": "بتلس تركي", "origin": "تركي", "price": "7500", "shop": "1", "store": "2", "year": "6/2026"}]}, {"size": "255/45/20", "types": [{"name": "كروس ويند", "origin": "صربي", "price": "7700", "shop": "1", "store": "3", "year": "2026"}, {"name": "ويست ليك", "origin": "تايلاندي", "price": "6000", "shop": "1", "store": "0", "year": "2024"}, {"name": "بتلس تركي", "origin": "تركي", "price": "6500", "shop": "1", "store": "3", "year": "2026"}]}, {"size": "265/45/20", "types": [{"name": "كونتيننتال", "origin": "SL", "price": "18000", "shop": "2", "store": "0", "year": "2025"}]}, {"size": "265/50/20", "types": [{"name": "كومهو", "origin": "كوري", "price": "9000", "shop": "2", "store": "2", "year": "11/2025"}]}], "tr": [{"size": "225/70/15 — 8 تيلا", "types": [{"name": "هاكوبا", "origin": "صيني", "price": "3300", "shop": "4", "store": "0", "year": "2026"}]}, {"size": "215/70/15 — 8 تيلا", "types": [{"name": "ميشلان", "origin": "تايلاندي", "price": "5900", "shop": "5", "store": "0", "year": "2026"}, {"name": "اتلندر", "origin": "تايلاندي", "price": "3800", "shop": "4", "store": "1", "year": "2026"}, {"name": "Pace", "origin": "صيني", "price": "2500", "shop": "1", "store": "0", "year": "2025"}]}, {"size": "195/R14 — 8 تيلا", "types": [{"name": "Thunderer", "origin": "تايلاندي", "price": "3800", "shop": "2", "store": "0", "year": "2025"}, {"name": "اوفيشن", "origin": "صيني", "price": "2700", "shop": "3", "store": "0", "year": "2026"}, {"name": "شاوينج", "origin": "تايلاندي", "price": "3500", "shop": "4", "store": "2", "year": "2026"}]}, {"size": "155/12 — 8 تيلا", "types": [{"name": "هاكوبا", "origin": "صيني", "price": "2000", "shop": "4", "store": "0", "year": "2026"}, {"name": "جيرني", "origin": "صني", "price": "1600", "shop": "1", "store": "0", "year": "2024"}]}, {"size": "175/70/12 — 8 تيلا", "types": [{"name": "لاسا", "origin": "تركي", "price": "2300", "shop": "2", "store": "0", "year": "2026"}]}, {"size": "750/16 — 16 تيلا", "types": [{"name": "دبل كوين", "origin": "صيني", "price": "6500", "shop": "2", "store": "0", "year": "2026"}]}], "custom_1783197391838": [], "custom_1783253062798": [], "runflat": [{"size": "225/50/17", "types": [{"name": "ميشلان", "origin": "الماني", "price": "0", "shop": "4", "store": "0", "year": "2026"}]}, {"size": "245/45/18", "types": [{"name": "ميشلان", "origin": "ميشلان", "price": "", "shop": "4", "store": "0", "year": "2026"}]}, {"size": "245/45/20", "types": [{"name": "بريلي", "origin": "روماني", "price": "16000", "shop": "1", "store": "0", "year": "2024"}]}, {"size": "275/40/20", "types": [{"name": "بريلي", "origin": "روماني", "price": "16500", "shop": "2", "store": "0", "year": "2025"}]}], "bat": [{"size": "NS 40", "types": [{"name": "فارتا", "origin": "", "price": "3000", "shop": "3", "store": "", "year": ""}, {"name": "توبلا", "origin": "", "price": "2200", "shop": "0", "store": "", "year": ""}, {"name": "ستارتر", "origin": "كوري", "price": "2400", "shop": "3", "store": "", "year": ""}, {"name": "بوش", "origin": "", "price": "", "shop": "0", "store": "", "year": ""}, {"name": "دايمون", "origin": "كوري", "price": "2400", "shop": "", "store": "", "year": ""}, {"name": "أشر", "origin": "تركي", "price": "2000", "shop": "0", "store": "", "year": ""}, {"name": "رويل", "origin": "تركي", "price": "2000", "shop": "4", "store": "", "year": ""}]}, {"size": "TD 70 عدل", "types": [{"name": "فارتا", "origin": "", "price": "", "shop": "", "store": "", "year": ""}, {"name": "رويل", "origin": "تركي", "price": "2800", "shop": "2", "store": "", "year": ""}]}, {"size": "TD 70 معكوس", "types": [{"name": "رويال", "origin": "تركي", "price": "2800", "shop": "2", "store": "", "year": ""}, {"name": "فارتا", "origin": "اسباني", "price": "3500", "shop": "2", "store": "", "year": ""}, {"name": "اياس", "origin": "تركي", "price": "3000", "shop": "1", "store": "", "year": ""}, {"name": "اكوا تركي", "origin": "تركي", "price": "2800", "shop": "3", "store": "", "year": ""}]}, {"size": "N 60 عالي", "types": [{"name": "ستارتر", "origin": "كوري", "price": "3400", "shop": "1", "store": "", "year": ""}]}, {"size": "DN 74", "types": [{"name": "ستارتر", "origin": "كوري", "price": "4000", "shop": "1", "store": "0", "year": ""}, {"name": "رويال", "origin": "تركي", "price": "", "shop": "", "store": "", "year": ""}, {"name": "فارتا", "origin": "", "price": "5500", "shop": "1", "store": "0", "year": ""}, {"name": "اكوا", "origin": "تركي", "price": "3700", "shop": "1", "store": "0", "year": ""}, {"name": "اكوا75", "origin": "", "price": "3800", "shop": "1", "store": "0", "year": ""}]}, {"size": "NS 60", "types": [{"name": "إنديكو", "origin": "كوري", "price": "", "shop": "", "store": "", "year": ""}, {"name": "سولايت", "origin": "كوري", "price": "2800", "shop": "", "store": "", "year": ""}]}, {"size": "DN 44", "types": [{"name": "فارتا50", "origin": "", "price": "3500", "shop": "1", "store": "", "year": ""}, {"name": "بوش", "origin": "", "price": "3200", "shop": "", "store": "", "year": ""}, {"name": "ستارتر", "origin": "كوري", "price": "2800", "shop": "", "store": "", "year": ""}, {"name": "دايموند", "origin": "تركي", "price": "2400", "shop": "", "store": "", "year": ""}]}, {"size": "DN 50", "types": [{"name": "", "origin": "", "price": "", "shop": "", "store": "", "year": ""}]}, {"size": "N 90", "types": [{"name": "ستارتر", "origin": "كوري", "price": "4500", "shop": "0", "store": "", "year": ""}, {"name": "رويال", "origin": "تركي", "price": "4000", "shop": "2", "store": "", "year": ""}, {"name": "سوليت", "origin": "كوري", "price": "4500", "shop": "4", "store": "", "year": ""}]}]};

window.onload = function() {
  // تحميل البيانات المحلية
  var catNames = {
    r13:'جنط 13', r14:'جنط 14', r15:'جنط 15', r16:'جنط 16',
    r17:'جنط 17', r18:'جنط 18', r19:'جنط 19', r20:'جنط 20',
    tr:'كاوتش النقل', runflat:'رانفلات', bat:'البطاريات'
  };
  var result = {};
  Object.keys(INITIAL_DATA).forEach(function(key) {
    if (key.startsWith('custom_') && (!INITIAL_DATA[key] || INITIAL_DATA[key].length===0)) return;
    var name = catNames[key] || key;
    result[name] = INITIAL_DATA[key] || [];
  });
  DB = result;
  TABS = Object.keys(DB);
  if (TABS.length > 0) currentTab = TABS[0];
  renderTabs();
  renderStats();
  renderContent();
  // إخفاء الـ splash بعد ثانيتين
  setTimeout(function(){ hideSplash(); }, 100);
};
</script>
</body>
</html>
