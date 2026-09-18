# Ksu-edugate
النظام الأكاديمي - جامعة الملك سعود
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Blackboard Learn - جامعة الملك سعود</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;500;600;700;800&display=swap');
*{margin:0;padding:0;box-sizing:border-box;}
:root{
  --blue:#1a4f8a;--blue-dark:#0f3460;--blue-mid:#2563b0;--blue-light:#3a7bd5;
  --blue-pale:#e8f0fb;--blue-border:#c5d8f5;--white:#fff;--bg:#f0f4f9;
  --border:#dde6f0;--text:#1a1a2e;--text-mid:#4a5568;--text-light:#8898aa;
  --radius:5px;--shadow:0 1px 4px rgba(26,79,138,.10);
  --green:#1a7a4a;--green-pale:#e6f5ec;--green-border:#a8dbbe;
}
body{font-family:'Cairo',sans-serif;background:var(--bg);color:var(--text);font-size:14px;min-height:100vh;display:flex;flex-direction:column;}

/* ── TOP BAR ── */
.topbar{background:var(--blue-dark);height:48px;display:flex;align-items:center;justify-content:space-between;padding:0 24px;position:sticky;top:0;z-index:200;box-shadow:0 2px 8px rgba(0,0,0,.25);}
.topbar-brand{display:flex;align-items:center;gap:12px;}
.brand-logo{width:34px;height:34px;background:#fff;border-radius:50%;display:flex;align-items:center;justify-content:center;}
.brand-text{color:#fff;font-weight:700;font-size:15px;line-height:1.2;}
.brand-text small{display:block;font-weight:400;font-size:10px;opacity:.7;direction:ltr;text-align:right;}
.tb-actions{display:flex;align-items:center;gap:8px;}
.tb-btn{background:rgba(255,255,255,.12);border:none;color:#fff;height:32px;padding:0 12px;border-radius:4px;cursor:pointer;font-family:'Cairo',sans-serif;font-size:12px;font-weight:600;transition:background .15s;display:flex;align-items:center;gap:6px;}
.tb-btn:hover{background:rgba(255,255,255,.22);}
.user-chip{display:flex;align-items:center;gap:8px;background:rgba(255,255,255,.12);border-radius:20px;padding:3px 12px 3px 6px;color:#fff;cursor:pointer;border:none;font-family:'Cairo',sans-serif;font-size:13px;font-weight:600;transition:background .15s;}
.user-chip:hover{background:rgba(255,255,255,.22);}
.user-av{width:26px;height:26px;background:var(--blue-light);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;font-weight:800;color:#fff;}

/* ── SUB NAV ── */
.subnav{background:var(--blue);display:flex;padding:0 24px;border-bottom:1px solid rgba(255,255,255,.1);}
.snl{color:rgba(255,255,255,.75);text-decoration:none;font-size:13px;font-weight:600;padding:0 14px;height:40px;display:flex;align-items:center;border-bottom:3px solid transparent;transition:all .15s;cursor:pointer;background:none;border-top:none;border-left:none;border-right:none;font-family:'Cairo',sans-serif;white-space:nowrap;}
.snl:hover{color:#fff;background:rgba(255,255,255,.08);}
.snl.active{color:#fff;border-bottom-color:#7eb8f7;font-weight:700;}

/* ── LAYOUT ── */
.wrap{display:flex;flex:1;min-height:0;}
.sidebar{width:220px;background:#fff;border-left:1px solid var(--border);flex-shrink:0;overflow-y:auto;}
.sb-sec{border-bottom:1px solid var(--border);}
.sb-hd{padding:10px 14px 6px;font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:1px;color:var(--text-light);}
.sbi{display:flex;align-items:center;gap:8px;padding:9px 14px;font-size:13px;color:var(--text-mid);cursor:pointer;border:none;background:none;width:100%;text-align:right;font-family:'Cairo',sans-serif;font-weight:500;transition:background .12s,color .12s;border-right:3px solid transparent;}
.sbi:hover{background:var(--blue-pale);color:var(--blue);}
.sbi.active{background:var(--blue-pale);color:var(--blue);font-weight:700;border-right-color:var(--blue);}
.sb-dot{width:6px;height:6px;border-radius:50%;background:var(--blue-light);flex-shrink:0;}
.sb-badge{margin-right:auto;background:var(--blue);color:#fff;font-size:10px;border-radius:10px;padding:1px 7px;font-weight:700;}

/* ── MAIN ── */
.main{flex:1;padding:20px;overflow-y:auto;}
.page{display:none;}.page.active{display:block;}
.pg-title{font-size:17px;font-weight:800;color:var(--blue-dark);margin-bottom:16px;padding-bottom:10px;border-bottom:2px solid var(--blue-pale);}

/* ── CARD ── */
.card{background:#fff;border:1px solid var(--border);border-radius:var(--radius);box-shadow:var(--shadow);overflow:hidden;margin-bottom:16px;}
.ch{background:var(--blue-dark);color:#fff;padding:10px 16px;font-size:13px;font-weight:700;display:flex;align-items:center;justify-content:space-between;}
.ch .cnt{background:var(--blue-light);color:#fff;font-size:11px;border-radius:10px;padding:1px 9px;font-weight:700;}

/* ── STUDENT BANNER ── */
.stu-banner{background:#fff;border:1px solid var(--border);border-radius:var(--radius);box-shadow:var(--shadow);margin-bottom:16px;display:flex;align-items:stretch;}
.stu-aside{background:var(--blue-dark);color:#fff;padding:20px 18px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:8px;border-radius:var(--radius) 0 0 var(--radius);min-width:120px;}
.stu-av{width:64px;height:64px;border-radius:50%;background:var(--blue-light);display:flex;align-items:center;justify-content:center;font-size:24px;font-weight:800;color:#fff;border:2px solid rgba(255,255,255,.3);}
.stu-stag{background:rgba(255,255,255,.15);border:1px solid rgba(255,255,255,.25);border-radius:10px;font-size:10px;font-weight:700;padding:2px 10px;}
.stu-body{padding:16px 20px;flex:1;}
.stu-name{font-size:18px;font-weight:800;color:var(--blue-dark);margin-bottom:12px;}
.stu-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px 20px;}
.sf .lbl{font-size:10px;color:var(--text-light);text-transform:uppercase;letter-spacing:.5px;margin-bottom:2px;}
.sf .val{font-size:13px;font-weight:700;color:var(--text);}
.sf .val.gpa{font-size:18px;color:var(--blue);font-weight:900;}

/* ── STATS ── */
.stats-row{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-bottom:16px;}
.sc{background:#fff;border:1px solid var(--border);border-radius:var(--radius);border-top:3px solid var(--blue-light);padding:14px 16px;box-shadow:var(--shadow);}
.sc .sv{font-size:24px;font-weight:900;color:var(--blue-dark);line-height:1;}
.sc .sl{font-size:11px;color:var(--text-light);margin-top:4px;}

/* ── TABLE ── */
.tbl{width:100%;border-collapse:collapse;}
.tbl th{background:#f0f4f9;border-bottom:2px solid var(--blue-border);padding:9px 14px;font-size:11px;font-weight:700;color:var(--blue-dark);text-align:right;}
.tbl td{padding:9px 14px;border-bottom:1px solid var(--border);font-size:13px;vertical-align:middle;}
.tbl tr:last-child td{border-bottom:none;}
.tbl tbody tr:hover td{background:#fafcff;}
.code{font-size:11px;color:var(--text-light);font-family:monospace;direction:ltr;text-align:right;display:block;margin-top:2px;}
.cn{font-weight:600;color:var(--blue-dark);}

/* ── BADGES ── */
.bh{background:var(--blue-pale);color:var(--blue);font-size:11px;font-weight:700;border-radius:10px;padding:2px 9px;}
.bt{font-size:10px;font-weight:700;border-radius:10px;padding:2px 9px;}
.bt.eng{background:#e8f0fb;color:#1a4f8a;}
.bt.stat{background:#e8f5fb;color:#1a6b8a;}
.bt.elec{background:#f0ebfb;color:#5a3a8a;}

/* ── GRADES ── */
.gr{font-size:12px;font-weight:800;border-radius:4px;padding:3px 10px;display:inline-block;}
.gr-ap{background:#dff0d8;color:#2d6a4f;}
.gr-a{background:#e5f5e0;color:#3d8b5e;}
.gr-bp{background:#dbeafe;color:#1e40af;}
.gr-b{background:#e0edfb;color:#2563ae;}
.gr-p{background:#eff6ff;color:#3b82f6;}

/* ── RANK ── */
.rank-tag{background:var(--blue-dark);color:#fff;font-size:11px;font-weight:800;border-radius:10px;padding:3px 14px;display:inline-block;}

/* ── GPA WIDGET ── */
.gpa-widget{padding:16px;display:flex;gap:20px;align-items:center;}
.gpa-circle{width:100px;height:100px;border-radius:50%;background:conic-gradient(var(--blue) 0% 97.8%,#dde6f0 97.8% 100%);display:flex;align-items:center;justify-content:center;flex-shrink:0;box-shadow:0 3px 10px rgba(26,79,138,.2);}
.gpa-inner{width:76px;height:76px;background:#fff;border-radius:50%;display:flex;flex-direction:column;align-items:center;justify-content:center;}
.gpa-inner .num{font-size:22px;font-weight:900;color:var(--blue-dark);line-height:1;}
.gpa-inner .denom{font-size:9px;color:var(--text-light);margin-top:2px;}
.gpa-meta{flex:1;}
.gpa-grid{display:grid;grid-template-columns:1fr 1fr;gap:6px;margin-top:8px;}
.gi{background:var(--blue-pale);border-radius:4px;padding:6px 10px;}
.gi .lbl{font-size:10px;color:var(--text-light);}
.gi .val{font-size:13px;font-weight:700;color:var(--blue-dark);}
.prog-wrap{padding:12px 16px 14px;border-top:1px solid var(--border);}
.prog-lbl{font-size:11px;color:var(--text-mid);font-weight:600;margin-bottom:5px;display:flex;justify-content:space-between;}
.prog-track{background:#dde6f0;border-radius:10px;height:8px;overflow:hidden;}
.prog-fill{background:linear-gradient(to left,var(--blue-light),var(--blue-dark));height:100%;border-radius:10px;}

/* ── SEM BAR ── */
.sem-bar{background:var(--blue-pale);border-bottom:1px solid var(--blue-border);padding:8px 14px;font-size:12px;font-weight:700;color:var(--blue-dark);display:flex;justify-content:space-between;align-items:center;}
.sem-tag{background:var(--blue);color:#fff;font-size:10px;border-radius:4px;padding:2px 8px;font-weight:700;}
.sem-tag.done{background:#888;}
.tbl-foot{background:#f0f4f9;border-top:1px solid var(--blue-border);padding:8px 14px;display:flex;justify-content:flex-end;gap:24px;font-size:12px;font-weight:700;color:var(--blue-dark);}

/* ── TABS ── */
.tab-bar{display:flex;border-bottom:2px solid var(--border);padding:0 16px;background:#fafcff;}
.tab{padding:10px 16px;font-size:13px;font-weight:600;color:var(--text-mid);cursor:pointer;border:none;background:none;font-family:'Cairo',sans-serif;border-bottom:2px solid transparent;margin-bottom:-2px;transition:all .15s;}
.tab:hover{color:var(--blue);}
.tab.active{color:var(--blue);border-bottom-color:var(--blue);}

/* ── TRANSCRIPT ── */
.trans-sem{margin-bottom:18px;}
.trans-head{background:var(--blue-dark);color:#fff;padding:8px 14px;font-size:12px;font-weight:700;border-radius:5px 5px 0 0;display:flex;justify-content:space-between;align-items:center;}
.ytag{font-size:10px;background:rgba(255,255,255,.18);border-radius:8px;padding:1px 8px;}
.trans-foot{background:var(--blue-pale);padding:7px 14px;border-top:1px solid var(--blue-border);border-radius:0 0 5px 5px;display:flex;justify-content:flex-end;gap:24px;font-size:12px;font-weight:700;color:var(--blue-dark);}
.cum-bar{background:var(--blue-dark);color:#fff;padding:14px 20px;border-radius:5px;display:flex;justify-content:space-between;align-items:center;margin-top:4px;}
.cum-bar .lbl{font-size:13px;font-weight:700;}
.cum-bar .sub{font-size:11px;opacity:.7;margin-top:2px;}
.cum-bar .big{font-size:34px;font-weight:900;line-height:1;}
.cum-bar .tag{font-size:11px;font-weight:700;opacity:.85;text-align:center;}

/* ── SCHEDULE ── */
.sched-body{padding:12px 16px;}
.sched-day{margin-bottom:14px;}
.sched-dt{font-size:12px;font-weight:700;color:#fff;background:var(--blue);padding:4px 10px;border-radius:4px;display:inline-block;margin-bottom:6px;}
.sched-slot{display:grid;grid-template-columns:120px 1fr auto;align-items:center;gap:10px;padding:7px 10px;border-bottom:1px dashed var(--border);border-right:3px solid var(--blue-light);background:var(--blue-pale);border-radius:0 4px 4px 0;margin-bottom:4px;}
.sched-time{font-size:11px;color:var(--text-mid);font-family:monospace;direction:ltr;}
.sched-course{font-size:12px;font-weight:700;color:var(--blue-dark);}
.sched-loc{font-size:11px;color:var(--text-light);text-align:left;}
.sched-break{display:flex;align-items:center;justify-content:center;gap:8px;padding:4px 10px;margin:2px 0 6px;font-size:11px;color:var(--text-light);font-weight:600;}
.sched-break::before,.sched-break::after{content:"";flex:1;height:1px;background:var(--border);}
.sched-off{padding:14px;text-align:center;color:var(--text-light);font-size:12px;font-weight:600;background:#fafcff;border-radius:4px;}

/* ── REWARDS ── */
.rewards-header{background:var(--blue-dark);color:#fff;border-radius:var(--radius) var(--radius) 0 0;padding:14px 18px;display:flex;justify-content:space-between;align-items:center;}
.rewards-header .rh-title{font-size:15px;font-weight:800;}
.rewards-header .rh-sub{font-size:11px;opacity:.75;margin-top:2px;}
.rewards-header .rh-total{text-align:left;}
.rewards-header .rh-total .rnum{font-size:26px;font-weight:900;line-height:1;}
.rewards-header .rh-total .rlbl{font-size:11px;opacity:.75;}
.rewards-body{padding:0;}
.rewards-table{width:100%;border-collapse:collapse;}
.rewards-table th{background:#f0f4f9;border-bottom:2px solid var(--blue-border);padding:9px 14px;font-size:11px;font-weight:700;color:var(--blue-dark);text-align:right;}
.rewards-table td{padding:10px 14px;border-bottom:1px solid var(--border);font-size:13px;vertical-align:middle;}
.rewards-table tr:last-child td{border-bottom:none;}
.rewards-table tr:hover td{background:#fafcff;}
.r-status{font-size:11px;font-weight:700;border-radius:10px;padding:3px 10px;display:inline-block;}
.r-paid{background:#dff0d8;color:#2d6a4f;}
.r-pending{background:#fff3cd;color:#856404;}
.r-zero{background:#f1f1f4;color:#6b7280;}
.r-month{font-weight:700;color:var(--blue-dark);}
.r-amount{font-size:14px;font-weight:800;color:var(--blue-dark);}
.r-note{font-size:11px;color:var(--text-light);}
.reward-summary{display:grid;grid-template-columns:repeat(3,1fr);gap:0;border-top:2px solid var(--blue-border);}
.rs-item{padding:12px 16px;text-align:center;border-left:1px solid var(--border);}
.rs-item:last-child{border-left:none;}
.rs-item .rv{font-size:18px;font-weight:900;color:var(--blue-dark);}
.rs-item .rl{font-size:11px;color:var(--text-light);margin-top:2px;}
.reward-note-bar{background:#fff8e1;border-top:1px solid #ffe082;padding:9px 14px;font-size:12px;color:#7a5c00;display:flex;align-items:center;gap:8px;}

/* ── COURSES GRID ── */
.courses-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;}
.ccard{background:#fff;border:1px solid var(--border);border-radius:var(--radius);border-right:4px solid var(--blue);padding:14px 16px;box-shadow:var(--shadow);display:flex;justify-content:space-between;align-items:flex-start;}
.ccard.stat{border-right-color:#1a6b8a;}
.ccard.elec{border-right-color:#5a3a8a;}
.cc-name{font-size:13px;font-weight:700;color:var(--blue-dark);margin-bottom:4px;}
.cc-code{font-size:11px;color:var(--text-light);font-family:monospace;direction:ltr;display:block;margin-bottom:6px;}
.cc-right{text-align:left;display:flex;flex-direction:column;gap:4px;align-items:flex-end;}

/* ── TOOLS ── */
.tools-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;}
.tool-card{background:#fff;border:1px solid var(--border);border-radius:var(--radius);padding:18px 16px;text-align:center;cursor:pointer;transition:box-shadow .15s,border-color .15s;box-shadow:var(--shadow);}
.tool-card:hover{box-shadow:0 4px 14px rgba(26,79,138,.15);border-color:var(--blue-border);}
.tool-icon{width:44px;height:44px;background:var(--blue-pale);border-radius:8px;display:flex;align-items:center;justify-content:center;margin:0 auto 10px;}
.tool-name{font-size:13px;font-weight:700;color:var(--blue-dark);margin-bottom:3px;}
.tool-desc{font-size:11px;color:var(--text-light);}

/* ── GRADE SCALE ── */
.gs-row{display:flex;flex-wrap:wrap;gap:8px;padding:14px 16px;}
.gs-item{background:var(--blue-pale);border:1px solid var(--blue-border);border-radius:5px;padding:8px 14px;text-align:center;min-width:90px;}
.gs-item .pts{font-size:13px;font-weight:800;color:var(--blue-dark);display:block;}
.gs-item .rng{font-size:10px;color:var(--text-light);display:block;}
.gs-item .desc{font-size:10px;color:var(--text-mid);font-weight:600;display:block;margin-top:2px;}

/* ── FOOTER ── */
.footer{background:var(--blue-dark);color:rgba(255,255,255,.5);text-align:center;padding:11px;font-size:11px;}
</style>
</head>
<body>

<!-- TOP BAR -->
<header class="topbar">
  <div class="topbar-brand">
    <div class="brand-logo">
      <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg>
    </div>
    <div class="brand-text">نظام بلاك بورد – جامعة الملك سعود<small>King Saud University · Blackboard Learn</small></div>
  </div>
  <div class="tb-actions">
    <button class="tb-btn">
      <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 8A6 6 0 006 8c0 7-3 9-3 9h18s-3-2-3-9"/><path d="M13.73 21a2 2 0 01-3.46 0"/></svg>الإشعارات
    </button>
    <div class="user-chip"><div class="user-av">وم</div>وليد العنزي</div>
  </div>
</header>

<!-- SUBNAV -->
<nav class="subnav">
  <button class="snl active" onclick="showPage('home',this)">الرئيسية</button>
  <button class="snl" onclick="showPage('courses',this)">مقرراتي</button>
  <button class="snl" onclick="showPage('grades',this)">الدرجات والمعدل</button>
  <button class="snl" onclick="showPage('schedule',this)">الجدول الدراسي</button>
  <button class="snl" onclick="showPage('transcript',this)">السجل الأكاديمي</button>
  <button class="snl" onclick="showPage('rewards',this)">المكافآت المالية</button>
  <button class="snl" onclick="showPage('tools',this)">الأدوات</button>
</nav>

<div class="wrap">
<!-- SIDEBAR -->
<aside class="sidebar">
  <div class="sb-sec">
    <div class="sb-hd">القائمة الرئيسية</div>
    <button class="sbi active" onclick="showPage('home',null)"><div class="sb-dot"></div>الصفحة الرئيسية</button>
    <button class="sbi" onclick="showPage('courses',null)"><div class="sb-dot"></div>مقرراتي<span class="sb-badge">12</span></button>
    <button class="sbi" onclick="showPage('grades',null)"><div class="sb-dot"></div>الدرجات والمعدل</button>
    <button class="sbi" onclick="showPage('schedule',null)"><div class="sb-dot"></div>الجدول الدراسي</button>
    <button class="sbi" onclick="showPage('transcript',null)"><div class="sb-dot"></div>السجل الأكاديمي</button>
    <button class="sbi" onclick="showPage('rewards',null)"><div class="sb-dot"></div>المكافآت المالية</button>
  </div>
  <div class="sb-sec">
    <div class="sb-hd">الأدوات</div>
    <button class="sbi" onclick="showPage('tools',null)"><div class="sb-dot"></div>الأدوات والخدمات</button>
    <button class="sbi"><div class="sb-dot"></div>الواجبات<span class="sb-badge">2</span></button>
    <button class="sbi"><div class="sb-dot"></div>المحتوى الدراسي</button>
    <button class="sbi"><div class="sb-dot"></div>التقويم الأكاديمي</button>
  </div>
  <div class="sb-sec">
    <div class="sb-hd">الدعم</div>
    <button class="sbi"><div class="sb-dot"></div>الدعم الفني</button>
    <button class="sbi"><div class="sb-dot"></div>الإرشاد الأكاديمي</button>
  </div>
</aside>

<!-- MAIN -->
<main class="main">

<!-- ══════════════════════ HOME ══════════════════════ -->
<div class="page active" id="page-home">
  <div class="pg-title">الصفحة الرئيسية</div>

  <div class="stu-banner">
    <div class="stu-aside">
      <div class="stu-av">وم</div>
      <div class="stu-stag">مسجّل ونشط</div>
    </div>
    <div class="stu-body">
      <div class="stu-name">وليد مخلف العنزي</div>
      <div class="stu-grid">
        <div class="sf"><div class="lbl">الرقم الجامعي</div><div class="val" style="font-family:monospace;direction:ltr;text-align:right;">446101289</div></div>
        <div class="sf"><div class="lbl">رقم الجوال</div><div class="val" style="font-family:monospace;direction:ltr;text-align:right;">0537441043</div></div>
        <div class="sf"><div class="lbl">الكلية</div><div class="val">كلية الهندسة</div></div>
        <div class="sf"><div class="lbl">التخصص</div><div class="val">هندسة صناعية</div></div>
        <div class="sf"><div class="lbl">المستوى الدراسي</div><div class="val">الفصل الأول – هندسة صناعية</div></div>
        <div class="sf"><div class="lbl">الفصل الحالي</div><div class="val">الأول – 1448 هـ</div></div>
        <div class="sf"><div class="lbl">المعدل التراكمي</div><div class="val gpa">4.89 / 5.00</div></div>
        <div class="sf"><div class="lbl">التصنيف الأكاديمي</div><div class="val"><span class="rank-tag">متفوق</span></div></div>
      </div>
    </div>
  </div>

  <div class="stats-row">
    <div class="sc"><div class="sv">12</div><div class="sl">مقررات الترم الحالي</div></div>
    <div class="sc"><div class="sv">0</div><div class="sl">المعدل الحالي</div></div>
    <div class="sc"><div class="sv">0</div><div class="sl">إجمالي الساعات المكتسبة</div></div>
    <div class="sc"><div class="sv">0</div><div class="sl">فصول دراسية مكتملة</div></div>
  </div>

  <div style="display:grid;grid-template-columns:1fr 320px;gap:16px;">
    <!-- current courses summary -->
    <div class="card">
      <div class="ch">مقررات الفصل الأول – هندسة صناعية<span class="cnt">12 مادة</span></div>
      <div class="sem-bar">الفصل الدراسي الأول – 1448 هـ<span class="sem-tag">جارٍ</span></div>
      <table class="tbl">
        <thead><tr><th>المقرر</th><th>النوع</th><th>الساعات</th><th>الدرجة</th></tr></thead>
        <tbody>
          <tr><td><span class="cn">حساب التفاضل والتكامل 1</span><span class="code">MATH 101</span></td><td><span class="bt eng">هندسة صناعية</span></td><td><span class="bh">4 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
          <tr><td><span class="cn">الفيزياء العامة 1</span><span class="code">PHYS 101</span></td><td><span class="bt eng">هندسة صناعية</span></td><td><span class="bh">3 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
          <tr><td><span class="cn">الكيمياء العامة</span><span class="code">CHEM 101</span></td><td><span class="bt eng">هندسة صناعية</span></td><td><span class="bh">3 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
          <tr><td><span class="cn">مقدمة في الهندسة</span><span class="code">ENGD 100</span></td><td><span class="bt eng">هندسة صناعية</span></td><td><span class="bh">2 س</span></td><td><span class="gr gr-a">A</span></td></tr>
          <tr><td><span class="cn">الرسم الهندسي</span><span class="code">ENGD 102</span></td><td><span class="bt eng">هندسة صناعية</span></td><td><span class="bh">2 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
          <tr><td><span class="cn">برمجة الحاسب</span><span class="code">CS 101</span></td><td><span class="bt eng">هندسة صناعية</span></td><td><span class="bh">3 س</span></td><td><span class="gr gr-a">A</span></td></tr>
          <tr><td><span class="cn">اللغة الإنجليزية التقني</span><span class="code">ENG 101</span></td><td><span class="bt eng">هندسة صناعية</span></td><td><span class="bh">3 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
          <tr><td><span class="cn">الميكانيكا الهندسية</span><span class="code">ENGD 110</span></td><td><span class="bt eng">هندسة صناعية</span></td><td><span class="bh">3 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
          <tr><td><span class="cn">مبادئ الاحتمالات والإحصاء</span><span class="code">STAT 101</span></td><td><span class="bt stat">إحصاء</span></td><td><span class="bh">3 س</span></td><td><span class="gr gr-a">A</span></td></tr>
          <tr><td><span class="cn">الإحصاء الهندسي</span><span class="code">STAT 201</span></td><td><span class="bt stat">إحصاء</span></td><td><span class="bh">3 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
          <tr><td><span class="cn">مهارات الاتصال والتقديم</span><span class="code">GE 110</span></td><td><span class="bt elec">اختياري</span></td><td><span class="bh">2 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
          <tr><td><span class="cn">التفكير الإبداعي</span><span class="code">GE 120</span></td><td><span class="bt elec">اختياري</span></td><td><span class="bh">3 س</span></td><td><span class="gr gr-ap">A+</span></td></tr>
        </tbody>
      </table>
      <div class="tbl-foot"><span>مجموع الساعات: 34</span><span>المعدل الفصلي: 4.89</span></div>
    </div>

    <!-- GPA -->
    <div>
      <div class="card">
        <div class="ch">المعدل التراكمي والتصنيف</div>
        <div class="gpa-widget">
          <div class="gpa-circle"><div class="gpa-inner"><span class="num">4.89</span><span class="denom">من 5.00</span></div></div>
          <div class="gpa-meta">
            <span class="rank-tag">متفوق</span>
            <div class="gpa-grid">
              <div class="gi"><div class="lbl">الساعات الكلية</div><div class="val">68 ساعة</div></div>
              <div class="gi"><div class="lbl">المقررات</div><div class="val">36 مقرر</div></div>
              <div class="gi"><div class="lbl">السنة الدراسية</div><div class="val">هندسة صناعية</div></div>
              <div class="gi"><div class="lbl">الرتبة</div><div class="val">الأول</div></div>
            </div>
          </div>
        </div>
        <div class="prog-wrap">
          <div class="prog-lbl"><span>مستوى المعدل التراكمي</span><span style="color:var(--blue);font-weight:800;">4.89 / 5.00</span></div>
          <div class="prog-track"><div class="prog-fill" style="width:97.8%;"></div></div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════════════ COURSES ══════════════════════ -->
<div class="page" id="page-courses">
  <div class="pg-title">مقرراتي المسجّلة</div>

  <!-- Semester tabs -->
  <div class="card" style="margin-bottom:16px;">
    <div class="tab-bar">
      <button class="tab active" onclick="switchSem(this,'sem1')">الفصل الأول 1448 – الحالي</button>
      <button class="tab" onclick="switchSem(this,'sem2')">الفصل الثاني 1448</button>
    </div>

    <!-- SEM 1 -->
    <div id="sem1">
      <div class="sem-bar">الفصل الدراسي الأول – هندسة صناعية – 1448 هـ<span class="sem-tag">جارٍ</span></div>
      <div class="courses-grid" style="padding:14px;">
        <div class="ccard"><div class="cc-left"><div class="cc-name">حساب التفاضل والتكامل 1</div><span class="cc-code">MATH 101 – 4 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span style="font-size:11px;color:var(--text-light);">قيد الدراسة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">الفيزياء العامة 1</div><span class="cc-code">PHYS 101 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span style="font-size:11px;color:var(--text-light);">قيد الدراسة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">الكيمياء العامة</div><span class="cc-code">CHEM 101 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span style="font-size:11px;color:var(--text-light);">قيد الدراسة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">مقدمة في الهندسة</div><span class="cc-code">ENGD 100 – 2 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span style="font-size:11px;color:var(--text-light);">قيد الدراسة</span></div></div>
      </div>
    </div>

    <!-- SEM 2 -->
    <div id="sem2" style="display:none;">
      <div class="sem-bar">الفصل الدراسي الثاني – هندسة صناعية – 1448 هـ<span class="sem-tag done">مكتمل</span></div>
      <div class="courses-grid" style="padding:14px;">
        <div class="ccard"><div class="cc-left"><div class="cc-name">حساب التفاضل والتكامل 2</div><span class="cc-code">MATH 102 – 4 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">الفيزياء العامة 2</div><span class="cc-code">PHYS 102 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">المعادلات التفاضلية</div><span class="cc-code">MATH 201 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span class="gr gr-a">A</span><span style="font-size:11px;color:var(--text-light);">4.75 نقطة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">الجبر الخطي</div><span class="cc-code">MATH 203 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">الكيمياء العضوية</div><span class="cc-code">CHEM 102 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">الديناميكا الحرارية</div><span class="cc-code">ENGD 201 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span class="gr gr-a">A</span><span style="font-size:11px;color:var(--text-light);">4.75 نقطة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">الدوائر الكهربائية</div><span class="cc-code">EE 201 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
        <div class="ccard"><div class="cc-left"><div class="cc-name">علم المواد الهندسية</div><span class="cc-code">ENGD 210 – 3 ساعات</span><span class="bt eng">هندسة صناعية</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
        <div class="ccard stat"><div class="cc-left"><div class="cc-name">الإحصاء التطبيقي</div><span class="cc-code">STAT 301 – 3 ساعات</span><span class="bt stat">إحصاء</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
        <div class="ccard stat"><div class="cc-left"><div class="cc-name">نماذج الاحتمالات</div><span class="cc-code">STAT 302 – 3 ساعات</span><span class="bt stat">إحصاء</span></div><div class="cc-right"><span class="gr gr-a">A</span><span style="font-size:11px;color:var(--text-light);">4.75 نقطة</span></div></div>
        <div class="ccard elec"><div class="cc-left"><div class="cc-name">الكتابة التقنية</div><span class="cc-code">GE 210 – 2 ساعات</span><span class="bt elec">اختياري</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
        <div class="ccard elec"><div class="cc-left"><div class="cc-name">ريادة الأعمال الهندسية</div><span class="cc-code">GE 220 – 2 ساعات</span><span class="bt elec">اختياري</span></div><div class="cc-right"><span class="gr gr-ap">A+</span><span style="font-size:11px;color:var(--text-light);">5.00 نقطة</span></div></div>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════════════ GRADES ══════════════════════ -->
<div class="page" id="page-grades">
  <div class="pg-title">الدرجات والمعدل التراكمي</div>

  <div class="card" style="margin-bottom:0;">
    <div class="tab-bar">
      <button class="tab" onclick="switchGradeSem(this,'g-sem1')">الفصل الأول</button>
      <button class="tab active" onclick="switchGradeSem(this,'g-sem2')">الفصل الثاني – الحالي</button>
    </div>

    <!-- grades sem 1 -->
    <div id="g-sem1" style="display:none;">
      <div class="sem-bar">الفصل الدراسي الأول – هندسة صناعية – 1448 هـ<span class="sem-tag done">مكتمل</span></div>
      <table class="tbl">
        <thead><tr><th>الرمز</th><th>المادة</th><th>النوع</th><th>الساعات</th><th>الدرجة</th><th>النقاط</th><th>الحالة</th></tr></thead>
        <tbody>
          <tr><td style="font-family:monospace;direction:ltr;">MATH 101</td><td>حساب التفاضل والتكامل 1</td><td><span class="bt eng">هندسة صناعية</span></td><td>4</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">PHYS 101</td><td>الفيزياء العامة 1</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">CHEM 101</td><td>الكيمياء العامة</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">ENGD 100</td><td>مقدمة في الهندسة</td><td><span class="bt eng">هندسة صناعية</span></td><td>2</td><td><span class="gr gr-a">A</span></td><td>4.75</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">ENGD 102</td><td>الرسم الهندسي</td><td><span class="bt eng">هندسة صناعية</span></td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">CS 101</td><td>برمجة الحاسب</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">ENG 101</td><td>اللغة الإنجليزية التقني</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">ENGD 110</td><td>الميكانيكا الهندسية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">STAT 101</td><td>مبادئ الاحتمالات والإحصاء</td><td><span class="bt stat">إحصاء</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">STAT 201</td><td>الإحصاء الهندسي</td><td><span class="bt stat">إحصاء</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">GE 110</td><td>مهارات الاتصال والتقديم</td><td><span class="bt elec">اختياري</span></td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">GE 120</td><td>التفكير الإبداعي</td><td><span class="bt elec">اختياري</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
        </tbody>
      </table>
      <div class="tbl-foot"><span>مجموع الساعات: 34</span><span>المعدل الفصلي: 4.89</span><span class="rank-tag">متفوق</span></div>
    </div>

    <!-- grades sem 2 -->
    <div id="g-sem2" style="display:none;">
      <div class="sem-bar">الفصل الدراسي الثاني – هندسة صناعية – 1448 هـ<span class="sem-tag done">مكتمل</span></div>
      <table class="tbl">
        <thead><tr><th>الرمز</th><th>المادة</th><th>النوع</th><th>الساعات</th><th>الدرجة</th><th>النقاط</th><th>الحالة</th></tr></thead>
        <tbody>
          <tr><td style="font-family:monospace;direction:ltr;">MATH 102</td><td>حساب التفاضل والتكامل 2</td><td><span class="bt eng">هندسة صناعية</span></td><td>4</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">PHYS 102</td><td>الفيزياء العامة 2</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">MATH 201</td><td>المعادلات التفاضلية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">MATH 203</td><td>الجبر الخطي</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">CHEM 102</td><td>الكيمياء العضوية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">ENGD 201</td><td>الديناميكا الحرارية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">EE 201</td><td>الدوائر الكهربائية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">ENGD 210</td><td>علم المواد الهندسية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">STAT 301</td><td>الإحصاء التطبيقي</td><td><span class="bt stat">إحصاء</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">STAT 302</td><td>نماذج الاحتمالات</td><td><span class="bt stat">إحصاء</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">GE 210</td><td>الكتابة التقنية</td><td><span class="bt elec">اختياري</span></td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
          <tr><td style="font-family:monospace;direction:ltr;">GE 220</td><td>ريادة الأعمال الهندسية</td><td><span class="bt elec">اختياري</span></td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td><td style="color:#2d6a4f;font-weight:700;">ناجح</td></tr>
        </tbody>
      </table>
      <div class="tbl-foot"><span>مجموع الساعات: 35</span><span>المعدل الفصلي: 4.89</span><span class="rank-tag">متفوق</span></div>
    </div>
  </div>

  <div class="card" style="margin-top:16px;">
    <div class="ch">مقياس الدرجات المعتمد</div>
    <div class="gs-row">
      <div class="gs-item"><span class="gr gr-ap">A+</span><span class="pts">5.00</span><span class="rng">95–100</span><span class="desc">ممتاز +</span></div>
      <div class="gs-item"><span class="gr gr-a">A</span><span class="pts">4.75</span><span class="rng">90–94</span><span class="desc">ممتاز</span></div>
      <div class="gs-item"><span class="gr gr-bp">B+</span><span class="pts">4.50</span><span class="rng">85–89</span><span class="desc">جيد جداً +</span></div>
      <div class="gs-item"><span class="gr gr-b">B</span><span class="pts">4.00</span><span class="rng">80–84</span><span class="desc">جيد جداً</span></div>
      <div class="gs-item"><span class="gr gr-p">C+</span><span class="pts">3.50</span><span class="rng">75–79</span><span class="desc">جيد +</span></div>
      <div class="gs-item"><span class="gr gr-p">C</span><span class="pts">3.00</span><span class="rng">70–74</span><span class="desc">جيد</span></div>
      <div class="gs-item"><span class="gr gr-p">D+</span><span class="pts">2.50</span><span class="rng">65–69</span><span class="desc">مقبول +</span></div>
      <div class="gs-item"><span class="gr gr-p">D</span><span class="pts">2.00</span><span class="rng">60–64</span><span class="desc">مقبول</span></div>
    </div>
  </div>
</div>

<!-- ══════════════════════ SCHEDULE ══════════════════════ -->
<div class="page" id="page-schedule">
  <div class="pg-title">الجدول الدراسي – الفصل الأول 1448 هـ</div>

  <div class="card" style="margin-bottom:0;">
    <div class="tab-bar">
      <button class="tab active" onclick="switchSchedSem(this,'sc1')">الفصل الأول</button>
      <button class="tab" onclick="switchSchedSem(this,'sc2')">الفصل الثاني</button>
    </div>

    <div id="sc1">
      <div class="ch" style="border-radius:0;">الجدول الأسبوعي – الفصل الأول – هندسة صناعية</div>
      <div class="sched-body">
        <div class="sched-day"><div class="sched-dt">الأحد</div>
          <div class="sched-slot"><span class="sched-time">12:30 – 15:00</span><span class="sched-course">محاضرة</span><span class="sched-loc">حضوري</span></div>
        </div>
        <div class="sched-day"><div class="sched-dt">الاثنين</div>
          <div class="sched-slot"><span class="sched-time">12:00 – 13:50</span><span class="sched-course">المحاضرة الأولى</span><span class="sched-loc">حضوري</span></div>
          <div class="sched-slot"><span class="sched-time">14:00 – 15:30</span><span class="sched-course">المحاضرة الثانية</span><span class="sched-loc">حضوري</span></div>
        </div>
        <div class="sched-day"><div class="sched-dt">الثلاثاء</div>
          <div class="sched-slot"><span class="sched-time">13:00 – 15:25</span><span class="sched-course">محاضرة عن بُعد (الجزء الأول)</span><span class="sched-loc">عن بُعد</span></div>
          <div class="sched-break">استراحة 10 دقائق</div>
          <div class="sched-slot"><span class="sched-time">15:35 – 18:00</span><span class="sched-course">محاضرة عن بُعد (الجزء الثاني)</span><span class="sched-loc">عن بُعد</span></div>
        </div>
        <div class="sched-day"><div class="sched-dt">الأربعاء</div>
          <div class="sched-slot"><span class="sched-time">13:00 – 15:00</span><span class="sched-course">محاضرة</span><span class="sched-loc">حضوري</span></div>
        </div>
        <div class="sched-day"><div class="sched-dt">الخميس</div>
          <div class="sched-off">لا توجد محاضرات (يوم راحة)</div>
        </div>
      </div>
    </div>

    <div id="sc2" style="display:none;">
      <div class="ch" style="border-radius:0;">الجدول الأسبوعي – الفصل الثاني</div>
      <div class="sched-body">
        <div class="sched-day"><div class="sched-dt">الأحد</div>
          <div class="sched-slot"><span class="sched-time">08:00 – 08:50</span><span class="sched-course">حساب التفاضل والتكامل 2 (MATH 102)</span><span class="sched-loc">مبنى 3 / قاعة 205</span></div>
          <div class="sched-slot"><span class="sched-time">10:00 – 10:50</span><span class="sched-course">الكيمياء العضوية (CHEM 102)</span><span class="sched-loc">مبنى 5 / قاعة 108</span></div>
          <div class="sched-slot"><span class="sched-time">12:00 – 12:50</span><span class="sched-course">الإحصاء التطبيقي (STAT 301)</span><span class="sched-loc">مبنى 7 / قاعة 312</span></div>
        </div>
        <div class="sched-day"><div class="sched-dt">الاثنين</div>
          <div class="sched-slot"><span class="sched-time">08:00 – 08:50</span><span class="sched-course">الفيزياء العامة 2 (PHYS 102)</span><span class="sched-loc">مبنى 2 / قاعة 116</span></div>
          <div class="sched-slot"><span class="sched-time">10:00 – 10:50</span><span class="sched-course">الجبر الخطي (MATH 203)</span><span class="sched-loc">مبنى 3 / قاعة 206</span></div>
          <div class="sched-slot"><span class="sched-time">13:00 – 13:50</span><span class="sched-course">الدوائر الكهربائية (EE 201)</span><span class="sched-loc">مبنى 10 / قاعة 301</span></div>
        </div>
        <div class="sched-day"><div class="sched-dt">الثلاثاء</div>
          <div class="sched-slot"><span class="sched-time">08:00 – 08:50</span><span class="sched-course">المعادلات التفاضلية (MATH 201)</span><span class="sched-loc">مبنى 3 / قاعة 203</span></div>
          <div class="sched-slot"><span class="sched-time">10:00 – 10:50</span><span class="sched-course">الديناميكا الحرارية (ENGD 201)</span><span class="sched-loc">مبنى 4 / قاعة 222</span></div>
          <div class="sched-slot"><span class="sched-time">12:00 – 12:50</span><span class="sched-course">نماذج الاحتمالات (STAT 302)</span><span class="sched-loc">مبنى 7 / قاعة 313</span></div>
        </div>
        <div class="sched-day"><div class="sched-dt">الأربعاء</div>
          <div class="sched-slot"><span class="sched-time">09:00 – 09:50</span><span class="sched-course">علم المواد الهندسية (ENGD 210)</span><span class="sched-loc">مبنى 4 / قاعة 225</span></div>
          <div class="sched-slot"><span class="sched-time">11:00 – 11:50</span><span class="sched-course">الكتابة التقنية (GE 210)</span><span class="sched-loc">مبنى 6 / قاعة 104</span></div>
          <div class="sched-slot"><span class="sched-time">13:00 – 13:50</span><span class="sched-course">ريادة الأعمال الهندسية (GE 220)</span><span class="sched-loc">مبنى 8 / قاعة 206</span></div>
        </div>
        <div class="sched-day"><div class="sched-dt">الخميس</div>
          <div class="sched-slot"><span class="sched-time">08:00 – 08:50</span><span class="sched-course">الفيزياء 2 – مختبر (PHYS 102L)</span><span class="sched-loc">مبنى 2 / مختبر PH-2</span></div>
          <div class="sched-slot"><span class="sched-time">10:00 – 10:50</span><span class="sched-course">حساب التفاضل 2 – تمارين (MATH 102)</span><span class="sched-loc">مبنى 3 / قاعة 207</span></div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════════════ TRANSCRIPT ══════════════════════ -->
<div class="page" id="page-transcript">
  <div class="pg-title">السجل الأكاديمي الرسمي</div>

  <div class="card" style="margin-bottom:14px;">
    <div style="padding:12px 16px;display:grid;grid-template-columns:repeat(4,1fr);gap:12px;text-align:center;border-bottom:1px solid var(--border);">
      <div><div style="font-size:10px;color:var(--text-light);">اسم الطالب</div><div style="font-size:13px;font-weight:700;">وليد مخلف العنزي</div></div>
      <div><div style="font-size:10px;color:var(--text-light);">الرقم الجامعي</div><div style="font-size:13px;font-weight:700;font-family:monospace;direction:ltr;">446101289</div></div>
      <div><div style="font-size:10px;color:var(--text-light);">المعدل التراكمي</div><div style="font-size:20px;font-weight:900;color:var(--blue-dark);">4.89</div></div>
      <div><div style="font-size:10px;color:var(--text-light);">التصنيف</div><div style="margin-top:4px;"><span class="rank-tag">متفوق</span></div></div>
    </div>
    <div style="padding:8px 16px;display:grid;grid-template-columns:repeat(3,1fr);gap:10px;font-size:12px;background:#fafcff;">
      <div><span style="color:var(--text-light);">الكلية: </span><strong>الهندسة</strong></div>
      <div><span style="color:var(--text-light);">التخصص: </span><strong>هندسة صناعية</strong></div>
      <div><span style="color:var(--text-light);">إجمالي الساعات: </span><strong>68 ساعة</strong></div>
    </div>
  </div>

  <!-- Year 1 Sem 1 (Prep) -->
  <div class="trans-sem">
    <div class="trans-head">السنة الأولى المشتركة (التحضيري) – الفصل الأول<span class="ytag">1445/1446 هـ</span></div>
    <table class="tbl"><thead><tr><th>الرمز</th><th>المادة</th><th>الساعات</th><th>الدرجة</th><th>النقاط</th></tr></thead>
    <tbody>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 101</td><td>الرياضيات التحضيرية</td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 102</td><td>الفيزياء التحضيرية</td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 103</td><td>الكيمياء التحضيرية</td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 104</td><td>مهارات الدراسة الجامعية</td><td>2</td><td><span class="gr gr-a">A</span></td><td>4.75</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 105</td><td>اللغة العربية</td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
    </tbody></table>
    <div class="trans-foot"><span>الساعات: 13</span><span>المعدل الفصلي: 4.92</span></div>
  </div>

  <!-- Year 1 Sem 2 (Prep) -->
  <div class="trans-sem">
    <div class="trans-head">السنة الأولى المشتركة (التحضيري) – الفصل الثاني<span class="ytag">1445/1446 هـ</span></div>
    <table class="tbl"><thead><tr><th>الرمز</th><th>المادة</th><th>الساعات</th><th>الدرجة</th><th>النقاط</th></tr></thead>
    <tbody>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 201</td><td>مقدمة في حساب التفاضل</td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 202</td><td>الحاسب ومهاراته</td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 203</td><td>اللغة الإنجليزية</td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 204</td><td>التربية الوطنية</td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PREP 205</td><td>مهارات التواصل</td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
    </tbody></table>
    <div class="trans-foot"><span>الساعات: 12</span><span>المعدل الفصلي: 4.90</span></div>
  </div>

  <div style="background:var(--blue-pale);border:1px solid var(--blue-border);border-radius:5px;padding:10px 16px;margin-bottom:16px;display:flex;justify-content:space-between;align-items:center;font-size:13px;font-weight:700;color:var(--blue-dark);">
    <span>المعدل التراكمي بعد السنة الأولى (التحضيري)</span><span style="font-size:18px;font-weight:900;">4.90 / 5.00</span>
  </div>

  <!-- Prep Eng Sem 1 (current) -->
  <div class="trans-sem">
    <div class="trans-head">هندسة صناعية – الفصل الأول<span class="ytag">1448 هـ</span></div>
    <table class="tbl"><thead><tr><th>الرمز</th><th>المادة</th><th>النوع</th><th>الساعات</th><th>الدرجة</th><th>النقاط</th></tr></thead>
    <tbody>
      <tr><td style="font-family:monospace;direction:ltr;">MATH 101</td><td>حساب التفاضل والتكامل 1</td><td><span class="bt eng">هندسة صناعية</span></td><td>4</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PHYS 101</td><td>الفيزياء العامة 1</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">CHEM 101</td><td>الكيمياء العامة</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">ENGD 100</td><td>مقدمة في الهندسة</td><td><span class="bt eng">هندسة صناعية</span></td><td>2</td><td><span class="gr gr-a">A</span></td><td>4.75</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">ENGD 102</td><td>الرسم الهندسي</td><td><span class="bt eng">هندسة صناعية</span></td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">CS 101</td><td>برمجة الحاسب</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">ENG 101</td><td>اللغة الإنجليزية التقني</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">ENGD 110</td><td>الميكانيكا الهندسية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">STAT 101</td><td>مبادئ الاحتمالات والإحصاء</td><td><span class="bt stat">إحصاء</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">STAT 201</td><td>الإحصاء الهندسي</td><td><span class="bt stat">إحصاء</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">GE 110</td><td>مهارات الاتصال والتقديم</td><td><span class="bt elec">اختياري</span></td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">GE 120</td><td>التفكير الإبداعي</td><td><span class="bt elec">اختياري</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
    </tbody></table>
    <div class="trans-foot"><span>الساعات: 34</span><span>المعدل الفصلي: 4.89</span></div>
  </div>

  <!-- Prep Eng Sem 2 -->
  <div class="trans-sem">
    <div class="trans-head">هندسة صناعية – الفصل الثاني<span class="ytag">1448 هـ</span></div>
    <table class="tbl"><thead><tr><th>الرمز</th><th>المادة</th><th>النوع</th><th>الساعات</th><th>الدرجة</th><th>النقاط</th></tr></thead>
    <tbody>
      <tr><td style="font-family:monospace;direction:ltr;">MATH 102</td><td>حساب التفاضل والتكامل 2</td><td><span class="bt eng">هندسة صناعية</span></td><td>4</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">PHYS 102</td><td>الفيزياء العامة 2</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">MATH 201</td><td>المعادلات التفاضلية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">MATH 203</td><td>الجبر الخطي</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">CHEM 102</td><td>الكيمياء العضوية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">ENGD 201</td><td>الديناميكا الحرارية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">EE 201</td><td>الدوائر الكهربائية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">ENGD 210</td><td>علم المواد الهندسية</td><td><span class="bt eng">هندسة صناعية</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">STAT 301</td><td>الإحصاء التطبيقي</td><td><span class="bt stat">إحصاء</span></td><td>3</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">STAT 302</td><td>نماذج الاحتمالات</td><td><span class="bt stat">إحصاء</span></td><td>3</td><td><span class="gr gr-a">A</span></td><td>4.75</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">GE 210</td><td>الكتابة التقنية</td><td><span class="bt elec">اختياري</span></td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
      <tr><td style="font-family:monospace;direction:ltr;">GE 220</td><td>ريادة الأعمال الهندسية</td><td><span class="bt elec">اختياري</span></td><td>2</td><td><span class="gr gr-ap">A+</span></td><td>5.00</td></tr>
    </tbody></table>
    <div class="trans-foot"><span>الساعات: 35</span><span>المعدل الفصلي: 4.89</span></div>
  </div>

  <div class="cum-bar">
    <div><div class="lbl">المعدل التراكمي الإجمالي</div><div class="sub">إجمالي الساعات المكتسبة: 68 ساعة – 36 مقرر – 4 فصول دراسية</div></div>
    <div><div class="big">4.89</div><div class="tag">متفوق</div></div>
  </div>
</div>

<!-- ══════════════════════ REWARDS ══════════════════════ -->
<div class="page" id="page-rewards">
  <div class="pg-title">المكافآت المالية</div>

  <div class="card">
    <div class="rewards-header">
      <div>
        <div class="rh-title">سجل المكافآت الدراسية</div>
        <div class="rh-sub">وليد مخلف العنزي – 446101289 – كلية الهندسة</div>
      </div>
    </div>
    <div class="rewards-body">
      <table class="rewards-table">
        <thead>
          <tr>
            <th>الفصل الدراسي</th>
            <th>المبلغ</th>
            <th>البيان</th>
            <th>الحالة</th>
          </tr>
        </thead>
        <tbody>
          <tr><td>الفصل الأول – التحضيري</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة بداية الدراسة – شهر 1</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الأول – التحضيري</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 2</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الأول – التحضيري</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 3</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الأول – التحضيري</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 4</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الثاني – التحضيري</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 1</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الثاني – التحضيري</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 2</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الثاني – التحضيري</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 3</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الثاني – التحضيري</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 4</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الأول – إعدادية هندسية</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 1</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الأول – إعدادية هندسية</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 2</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الأول – إعدادية هندسية</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 3</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الأول – إعدادية هندسية</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 4</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الثاني – إعدادية هندسية</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 1</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الثاني – إعدادية هندسية</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 2</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الثاني – إعدادية هندسية</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 3</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
          <tr><td>الفصل الثاني – إعدادية هندسية</td><td><span class="r-amount">990 ر.س</span></td><td><span class="r-note">مكافأة شهرية – شهر 4</span></td><td><span class="r-status r-paid">مُودَعة</span></td></tr>
        </tbody>
      </table>
    </div>
  </div>
</div>

<!-- ══════════════════════ TOOLS ══════════════════════ -->
<div class="page" id="page-tools">
  <div class="pg-title">الأدوات والخدمات الإلكترونية</div>
  <div class="tools-grid">
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg></div><div class="tool-name">البوابة الأكاديمية</div><div class="tool-desc">عرض وتعديل البيانات الأكاديمية</div></div>
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg></div><div class="tool-name">البريد الجامعي</div><div class="tool-desc">البريد الإلكتروني الرسمي</div></div>
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><path d="M2 3h6a4 4 0 014 4v14a3 3 0 00-3-3H2z"/><path d="M22 3h-6a4 4 0 00-4 4v14a3 3 0 013-3h7z"/></svg></div><div class="tool-name">المكتبة الرقمية</div><div class="tool-desc">الوصول للمصادر العلمية</div></div>
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><rect x="1" y="4" width="22" height="16" rx="2"/><line x1="1" y1="10" x2="23" y2="10"/></svg></div><div class="tool-name">الشؤون المالية</div><div class="tool-desc">الرسوم والمكافآت والمدفوعات</div></div>
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/><polyline points="14,2 14,8 20,8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/></svg></div><div class="tool-name">طلب الوثائق</div><div class="tool-desc">شهادات ووثائق رسمية</div></div>
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><rect x="3" y="4" width="18" height="18" rx="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/></svg></div><div class="tool-name">التقويم الأكاديمي</div><div class="tool-desc">جدول الفعاليات والمواعيد</div></div>
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><path d="M21 15a2 2 0 01-2 2H7l-4 4V5a2 2 0 012-2h14a2 2 0 012 2z"/></svg></div><div class="tool-name">الإرشاد الأكاديمي</div><div class="tool-desc">تواصل مع المرشد الأكاديمي</div></div>
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg></div><div class="tool-name">الدعم الفني</div><div class="tool-desc">مساعدة تقنية وحل المشكلات</div></div>
    <div class="tool-card"><div class="tool-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="#1a4f8a" stroke-width="2"><path d="M20.84 4.61a5.5 5.5 0 00-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 00-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 000-7.78z"/></svg></div><div class="tool-name">الخدمات الطبية</div><div class="tool-desc">حجز المواعيد الصحية</div></div>
  </div>
</div>

</main>
</div>

<footer class="footer">
  جامعة الملك سعود &nbsp;·&nbsp; نظام إدارة التعلم Blackboard Learn &nbsp;·&nbsp; &copy; 1446 هـ / 2025 م – جميع الحقوق محفوظة
</footer>

<script>
function showPage(name, el) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  var pg = document.getElementById('page-' + name);
  if (pg) pg.classList.add('active');
  document.querySelectorAll('.snl').forEach(b => b.classList.remove('active'));
  if (el && el.classList && el.classList.contains('snl')) {
    el.classList.add('active');
  } else {
    document.querySelectorAll('.snl').forEach(b => {
      var oc = b.getAttribute('onclick') || '';
      if (oc.includes("'" + name + "'")) b.classList.add('active');
    });
  }
  document.querySelectorAll('.sbi').forEach(b => b.classList.remove('active'));
  document.querySelectorAll('.sbi').forEach(b => {
    var oc = b.getAttribute('onclick') || '';
    if (oc.includes("'" + name + "'")) b.classList.add('active');
  });
}
function switchSem(btn, id) {
  ['sem1','sem2'].forEach(s => { var el = document.getElementById(s); if(el) el.style.display='none'; });
  var t = document.getElementById(id); if(t) t.style.display='block';
  btn.closest('.card').querySelectorAll('.tab').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
}
function switchGradeSem(btn, id) {
  ['g-sem1','g-sem2'].forEach(s => { var el = document.getElementById(s); if(el) el.style.display='none'; });
  var t = document.getElementById(id); if(t) t.style.display='block';
  btn.closest('.card').querySelectorAll('.tab').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
}
function switchSchedSem(btn, id) {
  ['sc1','sc2'].forEach(s => { var el = document.getElementById(s); if(el) el.style.display='none'; });
  var t = document.getElementById(id); if(t) t.style.display='block';
  btn.closest('.card').querySelectorAll('.tab').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
}
</script>
</body>
</html>
