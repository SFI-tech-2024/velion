<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Velion — Enterprise Intelligence Platform</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Arabic:wght@300;400;500;600;700&family=Sora:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<style>
:root{
  --navy-900:#06101F;--navy-800:#0A1A2F;--navy-700:#102540;--navy-600:#16304F;--navy-500:#1E3D63;
  --gold:#D4AF37;--gold-soft:#E8C766;--gold-deep:#B8901C;
  --surface:#F5F7FB;--surface-2:#FFFFFF;--surface-3:#EEF2F8;--line:#E1E8F2;--line-dark:#1C3252;
  --ink:#15233B;--ink-2:#3C4E68;--muted:#7A8AA3;
  --success:#2E9E6B;--warn:#E0A93B;--danger:#D9534F;--info:#3D7FC4;
  --r-sm:8px;--r-md:14px;--r-lg:20px;--r-xl:28px;
  --shadow-sm:0 1px 2px rgba(13,30,56,.06),0 1px 3px rgba(13,30,56,.05);
  --shadow-md:0 8px 24px rgba(13,30,56,.10);--shadow-lg:0 20px 50px rgba(6,16,31,.28);
  --t:.22s cubic-bezier(.4,0,.2,1);
}
*{margin:0;padding:0;box-sizing:border-box}
html,body{height:100%}
body{font-family:'IBM Plex Sans Arabic',system-ui,sans-serif;background:var(--surface);color:var(--ink);-webkit-font-smoothing:antialiased;line-height:1.55}
.display,.lat{font-family:'Sora','IBM Plex Sans Arabic',sans-serif}
button,input,select,textarea{font-family:inherit;font-size:inherit}
button{cursor:pointer;border:none;background:none}
a{color:inherit;text-decoration:none}
::selection{background:var(--gold);color:var(--navy-900)}
:focus-visible{outline:2px solid var(--gold);outline-offset:2px}
img{max-width:100%}
.hidden{display:none!important}
.row{display:flex;align-items:center}
.gap-s{gap:8px}.gap-m{gap:16px}.gap-l{gap:24px}
.grow{flex:1}

#landing{min-height:100vh;display:flex;flex-direction:column;
  background:radial-gradient(1200px 600px at 80% -10%,rgba(212,175,55,.14),transparent 60%),
             radial-gradient(900px 500px at 10% 110%,rgba(61,127,196,.16),transparent 55%),
             linear-gradient(160deg,var(--navy-900),var(--navy-800) 55%,var(--navy-700));
  color:#fff;position:relative;overflow:hidden}
#landing::before{content:"";position:absolute;inset:0;
  background-image:linear-gradient(rgba(255,255,255,.04) 1px,transparent 1px),linear-gradient(90deg,rgba(255,255,255,.04) 1px,transparent 1px);
  background-size:54px 54px;mask-image:radial-gradient(circle at 50% 30%,#000 0%,transparent 75%);opacity:.5;pointer-events:none}
.land-nav{display:flex;align-items:center;justify-content:space-between;padding:22px clamp(20px,5vw,64px);position:relative;z-index:3}
.brand{display:flex;align-items:center;gap:12px;font-weight:700}
.brand-mark{width:40px;height:40px;border-radius:11px;display:grid;place-items:center;background:linear-gradient(145deg,var(--gold),var(--gold-deep));color:var(--navy-900);font-family:'Sora';font-weight:800;font-size:20px;box-shadow:0 6px 18px rgba(212,175,55,.35)}
.brand-name{font-family:'Sora';font-size:21px;letter-spacing:.5px}
.brand-name span{color:var(--gold)}
.land-nav .links{display:flex;align-items:center;gap:28px;font-size:14.5px;color:#C9D4E6}
.land-nav .links a:hover{color:#fff}
.lang-pill{display:flex;background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.14);border-radius:999px;padding:3px;font-size:13px}
.lang-pill button{padding:6px 14px;border-radius:999px;color:#C9D4E6;font-weight:600;transition:var(--t)}
.lang-pill button.active{background:var(--gold);color:var(--navy-900)}
.land-main{flex:1;display:grid;grid-template-columns:1.05fr .95fr;gap:40px;align-items:center;padding:clamp(20px,3vw,40px) clamp(20px,5vw,64px) 60px;position:relative;z-index:2;max-width:1340px;margin:0 auto;width:100%}
.hero-eyebrow{display:inline-flex;align-items:center;gap:9px;font-size:13px;letter-spacing:.12em;text-transform:uppercase;color:var(--gold-soft);background:rgba(212,175,55,.1);border:1px solid rgba(212,175,55,.25);padding:7px 15px;border-radius:999px;font-weight:600}
.hero-eyebrow .dot{width:7px;height:7px;border-radius:50%;background:var(--gold);box-shadow:0 0 0 4px rgba(212,175,55,.25)}
.hero h1{font-family:'Sora';font-size:clamp(34px,4.6vw,58px);line-height:1.08;font-weight:800;margin:22px 0 18px;letter-spacing:-.5px}
.hero h1 .hl{background:linear-gradient(120deg,var(--gold),var(--gold-soft));-webkit-background-clip:text;background-clip:text;color:transparent}
.hero p.lead{font-size:clamp(15px,1.5vw,18px);color:#C2D0E4;max-width:560px;margin-bottom:30px}
.hero-stats{display:flex;gap:34px;flex-wrap:wrap;margin-top:8px}
.hstat .n{font-family:'Sora';font-size:30px;font-weight:700;color:#fff}
.hstat .n b{color:var(--gold)}
.hstat .l{font-size:12.5px;color:#92A2BC;letter-spacing:.04em}
.hero-modules{display:flex;flex-wrap:wrap;gap:9px;margin-top:34px;max-width:560px}
.hero-modules span{font-size:12.5px;padding:6px 12px;border-radius:8px;background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.1);color:#B9C7DC}
.auth-card{background:rgba(255,255,255,.97);color:var(--ink);border-radius:var(--r-xl);padding:34px 32px;box-shadow:var(--shadow-lg);border:1px solid rgba(255,255,255,.5);backdrop-filter:blur(6px);max-width:440px;width:100%;justify-self:end}
.auth-tabs{display:flex;background:var(--surface-3);border-radius:12px;padding:4px;margin-bottom:24px}
.auth-tabs button{flex:1;padding:10px;border-radius:9px;font-weight:600;font-size:14px;color:var(--ink-2);transition:var(--t)}
.auth-tabs button.active{background:#fff;color:var(--navy-800);box-shadow:var(--shadow-sm)}
.auth-card h2{font-family:'Sora';font-size:23px;margin-bottom:5px;color:var(--navy-800)}
.auth-card .sub{font-size:13.5px;color:var(--muted);margin-bottom:22px}
.field{margin-bottom:15px}
.field label{display:block;font-size:13px;font-weight:600;color:var(--ink-2);margin-bottom:7px}
.field input,.field select,.field textarea{width:100%;padding:12px 14px;border:1.5px solid var(--line);border-radius:11px;background:#fff;color:var(--ink);transition:var(--t);font-size:14.5px}
.field textarea{resize:vertical;min-height:78px}
.field input:focus,.field select:focus,.field textarea:focus{border-color:var(--gold);outline:none;box-shadow:0 0 0 4px rgba(212,175,55,.13)}
.field .hint{font-size:11.5px;color:var(--muted);margin-top:5px}
.field.req label::after{content:" *";color:var(--danger)}
.form-grid{display:grid;grid-template-columns:1fr 1fr;gap:0 14px}
.form-grid .full{grid-column:1/-1}
.btn-primary{width:100%;padding:13px;border-radius:12px;font-weight:700;font-size:15px;background:linear-gradient(135deg,var(--navy-700),var(--navy-600));color:#fff;box-shadow:0 8px 22px rgba(16,37,64,.3);transition:var(--t);position:relative;overflow:hidden}
.btn-primary:hover{transform:translateY(-1px);box-shadow:0 12px 28px rgba(16,37,64,.4)}
.btn-primary::after{content:"";position:absolute;inset:0;background:linear-gradient(135deg,var(--gold),transparent);opacity:0;transition:var(--t)}
.btn-primary:hover::after{opacity:.16}
.demo-note{margin-top:16px;padding:11px 13px;background:rgba(61,127,196,.08);border:1px solid rgba(61,127,196,.2);border-radius:10px;font-size:12px;color:var(--info);line-height:1.5}
.demo-note b{color:var(--navy-700)}
.auth-err{background:rgba(217,83,79,.1);border:1px solid rgba(217,83,79,.3);color:var(--danger);padding:10px 13px;border-radius:10px;font-size:13px;margin-bottom:14px;display:none}
.auth-err.show{display:block}
.land-foot{padding:18px 64px;border-top:1px solid rgba(255,255,255,.08);font-size:12.5px;color:#7C8CA6;display:flex;justify-content:space-between;flex-wrap:wrap;gap:10px;position:relative;z-index:2}

#app{display:none;height:100vh;overflow:hidden}
.shell{display:flex;height:100vh}
.sidebar{width:268px;flex-shrink:0;background:linear-gradient(180deg,var(--navy-800),var(--navy-900));color:#C5D1E4;display:flex;flex-direction:column;border-inline-end:1px solid var(--line-dark);transition:var(--t);z-index:60}
.sb-head{padding:20px 20px 16px;display:flex;align-items:center;gap:11px;border-bottom:1px solid rgba(255,255,255,.07)}
.sb-head .brand-name{font-size:18px}
.sb-roleband{margin:14px 16px 6px;padding:11px 14px;border-radius:12px;background:linear-gradient(135deg,rgba(212,175,55,.16),rgba(212,175,55,.05));border:1px solid rgba(212,175,55,.22)}
.sb-roleband .who{font-size:13.5px;font-weight:600;color:#fff}
.sb-roleband .role{font-size:11.5px;color:var(--gold-soft);margin-top:2px}
.sb-nav{flex:1;overflow-y:auto;padding:10px 12px 16px}
.sb-nav::-webkit-scrollbar{width:5px}.sb-nav::-webkit-scrollbar-thumb{background:rgba(255,255,255,.12);border-radius:4px}
.nav-group-label{font-size:10.5px;letter-spacing:.12em;text-transform:uppercase;color:#5E708C;padding:14px 12px 6px;font-weight:600}
.nav-item{display:flex;align-items:center;gap:12px;padding:11px 13px;border-radius:11px;font-size:14px;color:#B5C2D8;cursor:pointer;transition:var(--t);position:relative;margin-bottom:2px}
.nav-item:hover{background:rgba(255,255,255,.06);color:#fff}
.nav-item.active{background:linear-gradient(135deg,rgba(212,175,55,.18),rgba(212,175,55,.06));color:#fff}
.nav-item.active::before{content:"";position:absolute;inset-inline-start:-12px;top:50%;transform:translateY(-50%);width:4px;height:22px;border-radius:0 4px 4px 0;background:var(--gold)}
html[dir="rtl"] .nav-item.active::before{border-radius:4px 0 0 4px}
.nav-item .ic{width:20px;text-align:center;flex-shrink:0;font-size:16px}
.nav-item .badge{margin-inline-start:auto;background:var(--gold);color:var(--navy-900);font-size:11px;font-weight:700;border-radius:999px;padding:1px 8px;min-width:20px;text-align:center}
.sb-foot{padding:14px 16px;border-top:1px solid rgba(255,255,255,.07)}
.sb-lang{display:flex;background:rgba(255,255,255,.06);border-radius:10px;padding:3px;margin-bottom:10px}
.sb-lang button{flex:1;padding:7px;border-radius:8px;font-size:12.5px;font-weight:600;color:#9FB0C8;transition:var(--t)}
.sb-lang button.active{background:var(--gold);color:var(--navy-900)}
.sb-logout{display:flex;align-items:center;gap:10px;width:100%;padding:10px 12px;border-radius:10px;color:#C5D1E4;font-size:13.5px;transition:var(--t)}
.sb-logout:hover{background:rgba(217,83,79,.16);color:#FF9C98}
.main{flex:1;display:flex;flex-direction:column;min-width:0}
.topbar{height:64px;flex-shrink:0;background:var(--surface-2);border-bottom:1px solid var(--line);display:flex;align-items:center;gap:16px;padding:0 clamp(16px,3vw,30px)}
.menu-btn{display:none;font-size:22px;color:var(--ink-2)}
.page-title{font-family:'Sora';font-size:18px;font-weight:600;color:var(--navy-800)}
.page-title small{display:block;font-family:'IBM Plex Sans Arabic';font-size:12px;color:var(--muted);font-weight:400;margin-top:1px}
.topbar-search{margin-inline-start:auto;display:flex;align-items:center;gap:8px;background:var(--surface-3);border:1px solid var(--line);border-radius:11px;padding:8px 13px;width:min(280px,30vw)}
.topbar-search input{border:none;background:none;outline:none;width:100%;font-size:13.5px;color:var(--ink)}
.topbar-search input::placeholder{color:var(--muted)}
.icon-btn{width:40px;height:40px;border-radius:11px;display:grid;place-items:center;color:var(--ink-2);background:var(--surface-3);border:1px solid var(--line);font-size:17px;transition:var(--t);position:relative}
.icon-btn:hover{background:#fff;color:var(--navy-700);box-shadow:var(--shadow-sm)}
.icon-btn .dot{position:absolute;top:8px;inset-inline-end:9px;width:8px;height:8px;border-radius:50%;background:var(--danger);border:2px solid var(--surface-2)}
.avatar{width:40px;height:40px;border-radius:12px;display:grid;place-items:center;font-weight:700;font-size:14px;background:linear-gradient(145deg,var(--navy-600),var(--navy-700));color:var(--gold-soft);cursor:pointer}
.content{flex:1;overflow-y:auto;padding:clamp(18px,3vw,30px);scroll-behavior:smooth}
.content::-webkit-scrollbar{width:9px}.content::-webkit-scrollbar-thumb{background:#C9D4E4;border-radius:6px;border:2px solid var(--surface)}
.page-head{display:flex;align-items:flex-end;justify-content:space-between;flex-wrap:wrap;gap:14px;margin-bottom:22px}
.page-head h1{font-family:'Sora';font-size:24px;color:var(--navy-800);font-weight:700}
.page-head p{color:var(--muted);font-size:13.5px;margin-top:3px}
.btn{display:inline-flex;align-items:center;gap:8px;padding:10px 18px;border-radius:11px;font-weight:600;font-size:14px;transition:var(--t)}
.btn.gold{background:linear-gradient(135deg,var(--gold),var(--gold-deep));color:var(--navy-900);box-shadow:0 6px 16px rgba(212,175,55,.3)}
.btn.gold:hover{transform:translateY(-1px);box-shadow:0 10px 22px rgba(212,175,55,.4)}
.btn.ghost{background:var(--surface-2);border:1.5px solid var(--line);color:var(--ink-2)}
.btn.ghost:hover{border-color:var(--gold);color:var(--navy-700)}
.btn.dark{background:var(--navy-700);color:#fff}.btn.dark:hover{background:var(--navy-600)}
.grid{display:grid;gap:18px}
.cols-4{grid-template-columns:repeat(4,1fr)}
.cols-3{grid-template-columns:repeat(3,1fr)}
.cols-2{grid-template-columns:repeat(2,1fr)}
.card{background:var(--surface-2);border:1px solid var(--line);border-radius:var(--r-lg);padding:22px;box-shadow:var(--shadow-sm)}
.card-h{display:flex;align-items:center;justify-content:space-between;margin-bottom:16px}
.card-h h3{font-family:'Sora';font-size:15.5px;color:var(--navy-800);font-weight:600}
.card-h .more{font-size:12.5px;color:var(--info);font-weight:600;cursor:pointer}
.kpi{position:relative;overflow:hidden}
.kpi .top{display:flex;align-items:flex-start;justify-content:space-between}
.kpi .ic{width:46px;height:46px;border-radius:13px;display:grid;place-items:center;font-size:21px}
.kpi .val{font-family:'Sora';font-size:28px;font-weight:700;color:var(--navy-800);margin-top:14px;line-height:1}
.kpi .lbl{font-size:13px;color:var(--muted);margin-top:6px}
.ic.b1{background:rgba(212,175,55,.14);color:var(--gold-deep)}
.ic.b2{background:rgba(61,127,196,.14);color:var(--info)}
.ic.b3{background:rgba(46,158,107,.14);color:var(--success)}
.ic.b4{background:rgba(155,89,182,.14);color:#8E44AD}
.ic.b5{background:rgba(224,169,59,.16);color:var(--warn)}
.badge2{display:inline-flex;align-items:center;gap:5px;font-size:11.5px;font-weight:600;padding:4px 10px;border-radius:999px}
.bg-success{background:rgba(46,158,107,.13);color:var(--success)}
.bg-warn{background:rgba(224,169,59,.16);color:#B5821C}
.bg-danger{background:rgba(217,83,79,.13);color:var(--danger)}
.bg-info{background:rgba(61,127,196,.13);color:var(--info)}
.bg-gold{background:rgba(212,175,55,.16);color:var(--gold-deep)}
.bg-mute{background:var(--surface-3);color:var(--ink-2)}
table{width:100%;border-collapse:collapse;font-size:13.5px}
th{text-align:start;font-size:11.5px;letter-spacing:.04em;text-transform:uppercase;color:var(--muted);font-weight:600;padding:0 14px 12px;border-bottom:1px solid var(--line)}
td{padding:14px;border-bottom:1px solid var(--surface-3);color:var(--ink-2)}
tr:last-child td{border-bottom:none}
tbody tr{transition:var(--t)}
tbody tr:hover{background:var(--surface)}
td .pname{font-weight:600;color:var(--ink)}
.del-btn{width:32px;height:32px;border-radius:9px;display:inline-grid;place-items:center;color:var(--muted);background:var(--surface-3);border:1px solid var(--line);transition:var(--t);font-size:13px}
.del-btn:hover{background:rgba(217,83,79,.12);color:var(--danger);border-color:rgba(217,83,79,.35)}
.kcard{position:relative}
.kcard .kdel{position:absolute;top:7px;inset-inline-end:7px;width:22px;height:22px;border-radius:6px;display:grid;place-items:center;font-size:15px;line-height:1;color:var(--muted);background:var(--surface-3);opacity:0;transition:var(--t)}
.kcard:hover .kdel{opacity:1}
.kcard .kdel:hover{background:rgba(217,83,79,.16);color:var(--danger)}
.kcard{cursor:grab}
.kcard.dragging{opacity:.45;cursor:grabbing}
.kcol{transition:var(--t)}
.kcol.drag-over{background:rgba(212,175,55,.16);outline:2px dashed var(--gold);outline-offset:-4px}
.kacts{display:flex;gap:6px;margin-top:9px}
.kact{flex:1;font-size:11.5px;padding:5px 6px;border-radius:7px;background:var(--surface-3);color:var(--ink-2);transition:var(--t)}
.kact:hover{background:var(--navy-700);color:#fff}
.kact.adv{background:rgba(212,175,55,.16);color:var(--gold-deep)}
.kact.adv:hover{background:var(--gold);color:var(--navy-900)}
.kbadge{margin-top:8px;font-size:11px;color:var(--success);background:rgba(46,158,107,.1);border-radius:6px;padding:3px 8px;display:inline-block}
.edit-btn:hover{background:rgba(61,127,196,.12)!important;color:var(--info)!important;border-color:rgba(61,127,196,.32)!important}
.attach-list{display:flex;flex-wrap:wrap;gap:7px;margin-top:8px}
.attach-chip{display:inline-flex;align-items:center;gap:4px;font-size:12px;padding:5px 11px;border-radius:999px;background:var(--surface-3);border:1px solid var(--line);color:var(--ink-2);transition:var(--t);cursor:pointer}
.attach-chip:hover{border-color:var(--gold);color:var(--navy-700)}
.dnd-hint{font-size:12px;color:var(--muted);display:inline-flex;align-items:center;gap:6px}
.pm-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:10px}
.pm-cell{border:1px solid var(--line);border-radius:12px;padding:10px;min-height:80px;background:var(--surface-2)}
.pm-cell.clickable{cursor:pointer;transition:var(--t)}
.pm-cell.clickable:hover{border-color:var(--gold);box-shadow:var(--shadow-sm);transform:translateY(-2px)}
.pm-cell.filled{background:var(--surface)}
.pm-mn{font-size:11.5px;font-weight:700;color:var(--navy-800);margin-bottom:6px}
.pm-prog{height:5px;background:var(--surface-3);border-radius:999px;overflow:hidden}
.pm-prog span{display:block;height:100%;border-radius:999px}
.pm-val{font-size:12px;font-weight:700;color:var(--ink);margin-top:4px}
.pm-note{font-size:11px;color:var(--muted);margin-top:4px;overflow:hidden;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical}
.pm-by{font-size:10.5px;color:var(--gold-deep);margin-top:4px}
.pm-files{font-size:10.5px;color:var(--info);margin-top:3px}
.pm-empty{display:grid;place-items:center;height:44px;color:var(--muted);font-size:22px}
@media(max-width:560px){.pm-grid{grid-template-columns:repeat(2,1fr)}}
.progress{height:7px;background:var(--surface-3);border-radius:999px;overflow:hidden;min-width:90px}
.progress span{display:block;height:100%;border-radius:999px;background:linear-gradient(90deg,var(--gold),var(--gold-soft))}
.progress.green span{background:linear-gradient(90deg,var(--success),#5CC78F)}
.kanban{display:grid;grid-template-columns:repeat(6,minmax(190px,1fr));gap:14px;overflow-x:auto;padding-bottom:8px}
.kcol{background:var(--surface-3);border-radius:var(--r-md);padding:12px;min-height:160px}
.kcol-h{display:flex;align-items:center;justify-content:space-between;margin-bottom:12px;padding:0 4px}
.kcol-h .t{font-size:13px;font-weight:700;color:var(--navy-800)}
.kcol-h .c{font-size:11px;font-weight:700;color:var(--muted);background:#fff;border-radius:999px;padding:1px 8px}
.kcard{background:#fff;border:1px solid var(--line);border-radius:12px;padding:13px;margin-bottom:10px;box-shadow:var(--shadow-sm);cursor:pointer;transition:var(--t)}
.kcard:hover{box-shadow:var(--shadow-md);transform:translateY(-2px);border-color:var(--gold)}
.kcard .cn{font-weight:600;font-size:13.5px;color:var(--ink)}
.kcard .cv{font-family:'Sora';font-weight:700;color:var(--gold-deep);font-size:14px;margin:6px 0}
.kcard .cm{font-size:11.5px;color:var(--muted);display:flex;justify-content:space-between;margin-top:8px}
.kempty{text-align:center;color:var(--muted);font-size:12px;padding:14px}
.timeline{position:relative;padding-inline-start:24px}
.timeline::before{content:"";position:absolute;inset-inline-start:7px;top:6px;bottom:6px;width:2px;background:var(--line)}
.tl-item{position:relative;padding-bottom:20px}
.tl-item::before{content:"";position:absolute;inset-inline-start:-22px;top:4px;width:14px;height:14px;border-radius:50%;background:#fff;border:3px solid var(--gold);box-shadow:0 0 0 3px rgba(212,175,55,.18)}
.tl-item.done::before{background:var(--success);border-color:var(--success)}
.tl-item .tt{font-weight:600;font-size:13.5px;color:var(--ink)}
.tl-item .td{font-size:12px;color:var(--muted);margin-top:2px}
.ai-card{background:linear-gradient(135deg,var(--navy-800),var(--navy-700));color:#fff;border:1px solid var(--line-dark)}
.ai-card .card-h h3{color:#fff}
.ai-insight{display:flex;gap:13px;padding:14px;border-radius:13px;background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.08);margin-bottom:11px}
.ai-insight .ai-ic{width:38px;height:38px;border-radius:11px;display:grid;place-items:center;flex-shrink:0;font-size:18px}
.ai-insight .h{font-weight:600;font-size:13.5px}
.ai-insight .b{font-size:12.5px;color:#AFC0D8;margin-top:3px}
.list-row{display:flex;align-items:center;gap:13px;padding:13px 0;border-bottom:1px solid var(--surface-3)}
.list-row:last-child{border-bottom:none}
.list-row .l-ic{width:38px;height:38px;border-radius:11px;display:grid;place-items:center;flex-shrink:0;font-size:16px}
.list-row .l-t{font-weight:600;font-size:13.5px;color:var(--ink)}
.list-row .l-s{font-size:12px;color:var(--muted);margin-top:1px}
.list-row .l-time{margin-inline-start:auto;font-size:11.5px;color:var(--muted);white-space:nowrap}
.chip-row{display:flex;gap:8px;flex-wrap:wrap}
.chip{padding:6px 13px;border-radius:999px;font-size:12.5px;border:1.5px solid var(--line);color:var(--ink-2);transition:var(--t)}
.chip.active{background:var(--navy-700);color:#fff;border-color:var(--navy-700)}
.modal-wrap{position:fixed;inset:0;background:rgba(6,16,31,.55);backdrop-filter:blur(3px);display:none;align-items:center;justify-content:center;z-index:200;padding:20px}
.modal-wrap.show{display:flex}
.modal{background:#fff;border-radius:var(--r-xl);padding:30px;width:min(560px,100%);max-height:90vh;overflow-y:auto;box-shadow:var(--shadow-lg);animation:pop .25s ease}
@keyframes pop{from{transform:translateY(14px) scale(.98);opacity:0}to{transform:none;opacity:1}}
.modal h2{font-family:'Sora';font-size:20px;color:var(--navy-800);margin-bottom:4px}
.modal .msub{color:var(--muted);font-size:13px;margin-bottom:20px}
#toast{position:fixed;bottom:24px;inset-inline-end:24px;z-index:300;display:flex;flex-direction:column;gap:10px}
.toast{background:var(--navy-800);color:#fff;padding:13px 18px;border-radius:13px;box-shadow:var(--shadow-lg);display:flex;align-items:center;gap:11px;font-size:13.5px;animation:slideIn .3s ease;border-inline-start:4px solid var(--gold);max-width:340px}
@keyframes slideIn{from{transform:translateY(20px);opacity:0}to{transform:none;opacity:1}}
.empty{text-align:center;padding:46px 20px;color:var(--muted)}
.empty .e-ic{font-size:44px;margin-bottom:12px;opacity:.7}
.empty .e-t{font-weight:600;color:var(--ink-2);font-size:15px;margin-bottom:4px}
.empty .e-b{font-size:13px;margin-bottom:18px;max-width:360px;margin-inline:auto}
.locked{display:grid;place-items:center;height:100%;min-height:50vh;text-align:center;color:var(--muted)}
.locked .l-ic{font-size:46px;color:var(--gold);margin-bottom:14px}
.seg{display:inline-flex;background:var(--surface-3);border-radius:11px;padding:4px}
.seg button{padding:8px 16px;border-radius:8px;font-size:13px;font-weight:600;color:var(--ink-2);transition:var(--t)}
.seg button.active{background:#fff;color:var(--navy-800);box-shadow:var(--shadow-sm)}
.mobile-overlay{display:none;position:fixed;inset:0;background:rgba(6,16,31,.5);z-index:55}
.chart-empty{height:100%;display:grid;place-items:center;text-align:center;color:var(--muted);font-size:13px}
@media(max-width:1100px){.cols-4{grid-template-columns:repeat(2,1fr)}.land-main{grid-template-columns:1fr;gap:30px}.auth-card{justify-self:stretch;max-width:560px;margin:0 auto}.hero{text-align:center}.hero-eyebrow,.hero-modules,.hero-stats{justify-content:center}}
@media(max-width:860px){.sidebar{position:fixed;inset-block:0;inset-inline-start:0;transform:translateX(-110%);box-shadow:var(--shadow-lg)}html[dir="rtl"] .sidebar{transform:translateX(110%)}.sidebar.open{transform:none}.mobile-overlay.show{display:block}.menu-btn{display:grid;place-items:center}.cols-3,.cols-2{grid-template-columns:1fr}.topbar-search{display:none}.land-nav .links a{display:none}.form-grid{grid-template-columns:1fr}}
@media(max-width:560px){.cols-4{grid-template-columns:1fr}.land-nav{padding:18px 20px}.auth-card{padding:26px 20px}.page-head{align-items:flex-start}.content{padding:16px}}
</style>
</head>
<body data-lang="ar">

<section id="landing">
  <nav class="land-nav">
    <div class="brand"><div class="brand-mark lat">V</div><div class="brand-name lat">Velion<span>.</span></div></div>
    <div class="links">
      <a data-i="nav_features">المنصة</a><a data-i="nav_modules">الوحدات</a><a data-i="nav_security">الأمان</a>
      <div class="lang-pill"><button data-setlang="ar" class="active">عربي</button><button data-setlang="en">EN</button></div>
    </div>
  </nav>
  <div class="land-main">
    <div class="hero">
      <span class="hero-eyebrow"><span class="dot"></span><span data-i="hero_eyebrow">منصة الذكاء المؤسسي المتكاملة</span></span>
      <h1 data-i="hero_title">قرارٌ واحد. <span class="hl">رؤيةٌ شاملة.</span><br>منصة Velion.</h1>
      <p class="lead" data-i="hero_lead">منصة مؤسسية موحّدة تجمع إدارة العملاء والمشاريع والعمليات والذكاء المالي في نظام واحد. ابدأ بإدخال بياناتك لتُبنى لوحاتك وتقاريرك لحظيًا.</p>
      <div class="hero-stats">
        <div class="hstat"><div class="n"><b>9</b></div><div class="l" data-i="hs_modules">وحدات أساسية</div></div>
        <div class="hstat"><div class="n"><b>8</b></div><div class="l" data-i="hs_roles">أدوار مستخدمين</div></div>
        <div class="hstat"><div class="n">99.9<b>%</b></div><div class="l" data-i="hs_uptime">جاهزية النظام</div></div>
        <div class="hstat"><div class="n"><b>AR</b>/EN</div><div class="l" data-i="hs_lang">دعم ثنائي اللغة</div></div>
      </div>
      <div class="hero-modules">
        <span data-i="m_crm">إدارة العملاء (CRM)</span><span data-i="m_proj">إدارة المشاريع</span><span data-i="m_ops">العمليات</span>
        <span data-i="m_fin">الذكاء المالي</span><span data-i="m_ai">تحليلات AI</span><span data-i="m_rep">التقارير</span>
      </div>
    </div>
    <div class="auth-card">
      <div class="auth-err" id="authErr"></div>
      <form id="loginForm">
        <h2 data-i="login_h">تسجيل الدخول</h2>
        <p class="sub" data-i="login_sub">نظام وصول مغلق — الدخول بحساب أنشأه مدير النظام فقط.</p>
        <div class="field req"><label data-i="f_userid">البريد الإلكتروني / اسم المستخدم</label><input type="text" id="li_email" placeholder="name@company.com" required></div>
        <div class="field req"><label data-i="f_pass">كلمة المرور</label><input type="password" id="li_pass" placeholder="••••••••" required></div>
        <button type="submit" class="btn-primary" data-i="btn_login">الدخول إلى المنصة</button>
        <div class="demo-note"><b data-i="closed_t">نظام مغلق:</b> <span data-i="closed_b">لا يوجد تسجيل ذاتي. يتولى مدير النظام إنشاء الحسابات وتوزيع الصلاحيات.</span></div>
      </form>
      <form id="setupForm" class="hidden">
        <h2 data-i="setup_h">تهيئة مدير النظام</h2>
        <p class="sub" data-i="setup_sub">لا توجد حسابات بعد. أنشئ حساب مدير النظام الأول لتفعيل المنصة.</p>
        <div class="field req"><label data-i="f_name">الاسم الكامل</label><input type="text" id="su_name" required></div>
        <div class="field req"><label data-i="f_userid">البريد الإلكتروني / اسم المستخدم</label><input type="text" id="su_email" required></div>
        <div class="field req"><label data-i="f_pass">كلمة المرور</label><input type="password" id="su_pass" required></div>
        <div class="field req"><label data-i="f_pass2">تأكيد كلمة المرور</label><input type="password" id="su_pass2" required></div>
        <button type="submit" class="btn-primary" data-i="btn_setup">إنشاء حساب مدير النظام والدخول</button>
        <div class="demo-note" style="background:rgba(224,169,59,.1);border-color:rgba(224,169,59,.3);color:#9a6f12"><b>⚠</b> <span data-i="sec_note">تنبيه: هذا الملف يعمل بلا خادم، لذا تُحفظ كلمات المرور محليًا كنص — للعرض والنماذج فقط، لا تُدخل كلمات مرور حقيقية.</span></div>
      </form>
    </div>
  </div>
  <footer class="land-foot">
    <div>© 2026 Velion Enterprise Platform · <span data-i="foot_by">تطوير SFI — AI Data Makers</span></div>
    <div>info@sfi-tech.sa · www.sfi-tech.sa</div>
  </footer>
</section>

<div id="app">
  <div class="mobile-overlay" id="mOverlay"></div>
  <div class="shell">
    <aside class="sidebar" id="sidebar">
      <div class="sb-head"><div class="brand-mark lat">V</div><div class="brand-name lat">Velion<span style="color:var(--gold)">.</span></div></div>
      <div class="sb-roleband"><div class="who" id="sbWho">—</div><div class="role" id="sbRole">—</div></div>
      <nav class="sb-nav" id="sbNav"></nav>
      <div class="sb-foot">
        <div class="sb-lang"><button data-setlang="ar">عربي</button><button data-setlang="en">English</button></div>
        <button class="sb-logout" id="btnLogout"><span>⎋</span><span data-i="logout">تسجيل الخروج</span></button>
      </div>
    </aside>
    <div class="main">
      <header class="topbar">
        <button class="menu-btn" id="menuBtn">☰</button>
        <div class="page-title" id="pageTitle">—</div>
        <div class="topbar-search"><span>🔍</span><input type="text" id="globalSearch" data-iph="ph_search" placeholder="بحث في المنصة…"></div>
        <button class="icon-btn" id="topNotif" title="Notifications">🔔<span class="dot hidden" id="notifDot"></span></button>
        <button class="icon-btn" id="topLang" title="Language">🌐</button>
        <div class="avatar" id="topAvatar">—</div>
      </header>
      <main class="content" id="view"></main>
    </div>
  </div>
</div>

<div class="modal-wrap" id="modalWrap"><div class="modal" id="modalBox"></div></div>
<div id="toast"></div>

<script>
/* ===== i18n ===== */
const I18N={
 ar:{nav_features:"المنصة",nav_modules:"الوحدات",nav_security:"الأمان",hero_eyebrow:"منصة الذكاء المؤسسي المتكاملة",
 hs_modules:"وحدات أساسية",hs_roles:"أدوار مستخدمين",hs_uptime:"جاهزية النظام",hs_lang:"دعم ثنائي اللغة",
 m_crm:"إدارة العملاء (CRM)",m_proj:"إدارة المشاريع",m_ops:"العمليات",m_fin:"الذكاء المالي",m_ai:"تحليلات AI",m_rep:"التقارير",
 tab_login:"تسجيل الدخول",tab_reg:"إنشاء حساب",login_h:"مرحباً بعودتك",login_sub:"سجّل الدخول للوصول إلى لوحة التحكم الخاصة بدورك.",
 f_email:"البريد الإلكتروني",f_pass:"كلمة المرور",f_role_login:"الدخول بدور (وضع العرض)",hint_role:"اختر الدور لمعاينة الصلاحيات والوحدات المتاحة له.",
 btn_login:"الدخول إلى المنصة",demo_t:"ابدأ فورًا:",demo_b:"سجّل بأي بريد وكلمة مرور، واختر دورك. المنصة تبدأ فارغة لإدخال بياناتك الحقيقية.",
 reg_h:"أنشئ حسابك",reg_sub:"سجّل حسب نوع المستخدم لتُخصَّص لك الوحدات والصلاحيات.",f_name:"الاسم الكامل",f_org:"المؤسسة / الشركة",
 f_role:"نوع المستخدم (الدور)",hint_reg_role:"يحدد الدور لوحة التحكم والوحدات والصلاحيات الممنوحة لك.",btn_reg:"إنشاء الحساب والدخول",
 foot_by:"تطوير SFI — AI Data Makers",logout:"تسجيل الخروج",ph_search:"بحث في المنصة…",
 g_main:"الرئيسية",g_commercial:"المسار التجاري",g_delivery:"التنفيذ والعمليات",g_intel:"الذكاء والتقارير",g_admin:"الإدارة",
 nav_dashboard:"لوحة التحكم",nav_crm:"العملاء والمبيعات",nav_projects:"المشاريع",nav_operations:"العمليات",nav_financial:"النظام المالي",
 nav_reports:"التقارير",nav_ai:"الذكاء والتحليلات",nav_notifications:"التنبيهات",nav_notes:"الملاحظات والموافقات",nav_archive:"الأرشيف",
 nav_users:"المستخدمون والصلاحيات",nav_settings:"الإعدادات",
 dash_sub:"نظرة لحظية على أداء المؤسسة",crm_sub:"دورة العميل من المحتمل إلى المشروع",proj_sub:"متابعة المشاريع والمهام والإنجاز",
 ops_sub:"التقارير الميدانية والأداء",fin_sub:"الفواتير والتدفق النقدي والتحصيل",rep_sub:"تقارير قابلة للتصدير والجدولة",
 ai_sub:"تنبؤات ومخاطر وتوصيات مبنية على بياناتك",notif_sub:"تنبيهات مبنية على بياناتك الفعلية",notes_sub:"ملاحظات وتصنيفات وإجراءات الموافقة",
 arch_sub:"مستندات ومرفقات وسجل تاريخي",users_sub:"إدارة الأدوار والصلاحيات والوصول",set_sub:"تفضيلات الحساب والمنصة",
 kpi_revenue:"قيمة المشاريع",kpi_collected:"المحصّل",kpi_pending:"مستحقات معلّقة",kpi_projects:"مشاريع نشطة",kpi_clients:"عملاء",
 kpi_pipeline:"قيمة الفرص",kpi_risk:"مشاريع بمخاطر",kpi_tasks:"الفواتير",kpi_invoices:"الفواتير",
 ch_revenue:"الإيراد والتحصيل عبر الأشهر",ch_pipeline:"توزيع خط الأنابيب",ch_ops:"أداء الفِرق",
 active_projects:"المشاريع النشطة",recent_activity:"النشاط الأخير",ai_insights:"رؤى الذكاء الاصطناعي",
 st_lead:"عميل محتمل",st_opp:"فرصة",st_prop:"عرض",st_neg:"تفاوض",st_contract:"عقد",st_active:"مفعّل",crm_clients:"قاعدة العملاء",
 col_project:"المشروع",col_client:"العميل",col_pm:"مدير المشروع",col_progress:"الإنجاز",col_status:"الحالة",col_value:"القيمة",col_due:"الاستحقاق",
 ops_daily:"يومي",ops_monthly:"شهري",ops_annual:"سنوي",ops_field:"التقارير الميدانية",ops_kpi:"مؤشرات الأداء",team_perf:"أداء الفِرق",
 fin_issued:"صادرة",fin_collected:"محصّلة",fin_pending:"معلّقة",fin_invoices:"الفواتير",col_invoice:"رقم الفاتورة",col_amount:"المبلغ",col_date:"التاريخ",cashflow:"التدفق النقدي",
 rep_fin:"تقرير مالي",rep_ops:"تقرير تشغيلي",rep_exec:"تقرير تنفيذي",rep_perf:"تقرير أداء",rep_gen:"إنشاء تلقائي · تصدير PDF / Excel · جدولة",
 export_pdf:"تصدير PDF",export_xls:"تصدير Excel",schedule:"جدولة",ai_delay:"تنبؤ التأخير",ai_risk:"كشف المخاطر",ai_score:"تقييم الأداء",ai_reco:"محرك التوصيات",
 mark_read:"تعليم الكل كمقروء",add_note:"إضافة ملاحظة",note_ph:"اكتب ملاحظتك هنا…",cat_risk:"مخاطرة",cat_issue:"مشكلة",cat_sug:"اقتراح",
 approve:"اعتماد",reject:"رفض",col_doc:"المستند",col_type:"النوع",col_project2:"المشروع",col_user:"المستخدم",col_role:"الدور",col_access:"الوصول",
 set_lang:"لغة الواجهة",set_profile:"الملف الشخصي",save:"حفظ",view_all:"عرض الكل",locked_t:"لا تملك صلاحية الوصول",
 locked_b:"هذه الوحدة غير متاحة لدورك الحالي. تواصل مع مدير النظام لرفع الصلاحيات.",created:"تمت الإضافة بنجاح",saved:"تم الحفظ بنجاح",
 welcome:"تم تسجيل الدخول — أهلاً",approved:"تم الاعتماد",rejected:"تم الرفض",all_read:"تم تعليم التنبيهات كمقروءة",
 report_gen:"جارٍ إنشاء التقرير…",probability:"الاحتمالية",owner_label:"المسؤول",this_month:"هذا الشهر",readonly_badge:"عرض فقط",
 cancel:"إلغاء",required_err:"يرجى تعبئة الحقول المطلوبة.",now:"الآن",download:"تنزيل",downloading:"جارٍ التنزيل…",
 add_client:"إضافة عميل",add_opp:"إضافة فرصة / عميل محتمل",add_project:"إضافة مشروع",add_invoice:"إضافة فاتورة",add_report:"إضافة تقرير ميداني",
 add_doc:"رفع مستند",add_user:"إضافة مستخدم",add_team:"إضافة فريق",
 f_contact:"الشخص المسؤول",f_phone:"الهاتف",f_source:"مصدر العميل",f_industry:"القطاع",f_desc:"الوصف",f_start:"تاريخ البدء",
 f_period:"الفترة",f_dept:"الإدارة / القسم",f_decision:"صنّاع القرار",f_expclose:"تاريخ الإغلاق المتوقع",f_competitors:"المنافسون",
 f_stage:"المرحلة",f_amount:"المبلغ",f_score:"درجة الأداء (%)",f_team:"اسم الفريق",f_report_txt:"نص التقرير",f_invoice_no:"رقم الفاتورة",
 f_status:"الحالة",f_filetype:"نوع الملف",f_progress:"نسبة الإنجاز (%)",select_opt:"— اختر —",
 empty_dash_t:"لوحتك جاهزة لاستقبال بياناتك",empty_dash_b:"ابدأ بإضافة عميل أو مشروع أو فاتورة، وستُبنى المؤشرات والرسوم هنا تلقائيًا.",
 empty_clients_t:"لا يوجد عملاء بعد",empty_clients_b:"أضف أول عميل لبدء بناء قاعدة عملائك وخط الأنابيب.",
 empty_pipe_t:"خط الأنابيب فارغ",empty_pipe_b:"أضف فرصة أو عميلاً محتملاً لتظهر هنا حسب مرحلتها.",
 empty_proj_t:"لا توجد مشاريع بعد",empty_proj_b:"أضف أول مشروع لمتابعة الإنجاز والمهام والقيمة.",
 empty_inv_t:"لا توجد فواتير بعد",empty_inv_b:"أضف فاتورة لبناء التدفق النقدي ومؤشرات التحصيل.",
 empty_rep_t:"لا توجد تقارير ميدانية",empty_rep_b:"أضف تقريرًا يوميًا أو شهريًا أو سنويًا للفِرق.",
 empty_notes_t:"لا توجد ملاحظات",empty_notes_b:"أضف ملاحظة مصنّفة لإرسالها لمسار الموافقة.",
 empty_arch_t:"الأرشيف فارغ",empty_arch_b:"أضف مستندًا لحفظ مرفقات المشاريع والعقود.",
 empty_ai_t:"لا توجد رؤى بعد",empty_ai_b:"تُولَّد الرؤى تلقائيًا من مشاريعك وفواتيرك بمجرد إدخالها.",
 empty_notif_t:"لا توجد تنبيهات",empty_notif_b:"تظهر التنبيهات تلقائيًا عند وجود مشاريع متأخرة أو مستحقات معلّقة.",
 empty_act_t:"لا يوجد نشاط بعد",empty_act_b:"تُسجَّل أنشطتك هنا فور إضافة البيانات.",
 empty_team_t:"لا توجد فِرق",empty_team_b:"أضف فريقًا ودرجة أدائه لعرض الرسم البياني.",
 alert_delay:"مشروع متأخر عن الجدول",alert_risk:"مخاطرة على مشروع",alert_pending:"فاتورة مستحقة بانتظار التحصيل",alert_note:"ملاحظة بانتظار الاعتماد",
 ins_delay_h:"مشاريع متأخرة",ins_risk_h:"مشاريع بمخاطر",ins_coll_h:"توصية تحصيل",ins_top_h:"أعلى الفِرق أداءً",
 st_ontrack:"على المسار",st_risk:"مخاطرة",st_delay:"متأخر",active_w:"نشط",new_w:"جديد",pending_w:"بانتظار",modules_w:"وحدة",delete:"حذف",deleted:"تم الحذف بنجاح",confirm_del_t:"تأكيد الحذف",confirm_del_b:"هل أنت متأكد من حذف هذا العنصر؟ لا يمكن التراجع عن العملية.",yes_delete:"نعم، احذف"},
 en:{nav_features:"Platform",nav_modules:"Modules",nav_security:"Security",hero_eyebrow:"Integrated Enterprise Intelligence Platform",
 hs_modules:"Core Modules",hs_roles:"User Roles",hs_uptime:"System Uptime",hs_lang:"Bilingual Support",
 m_crm:"CRM & Sales",m_proj:"Projects",m_ops:"Operations",m_fin:"Financial Intelligence",m_ai:"AI Analytics",m_rep:"Reporting",
 tab_login:"Sign In",tab_reg:"Create Account",login_h:"Welcome back",login_sub:"Sign in to reach the dashboard built for your role.",
 f_email:"Email address",f_pass:"Password",f_role_login:"Enter as role (demo mode)",hint_role:"Pick a role to preview its permissions and modules.",
 btn_login:"Enter platform",demo_t:"Start now:",demo_b:"Sign in with any email and password, pick your role. The platform starts empty for your real data.",
 reg_h:"Create your account",reg_sub:"Register by user type to get modules and permissions tailored to you.",f_name:"Full name",f_org:"Organization / Company",
 f_role:"User type (role)",hint_reg_role:"Your role defines your dashboard, modules and permissions.",btn_reg:"Create account & enter",
 foot_by:"Built by SFI — AI Data Makers",logout:"Sign out",ph_search:"Search the platform…",
 g_main:"Overview",g_commercial:"Commercial",g_delivery:"Delivery & Ops",g_intel:"Intelligence",g_admin:"Administration",
 nav_dashboard:"Dashboard",nav_crm:"CRM & Sales",nav_projects:"Projects",nav_operations:"Operations",nav_financial:"Financial",
 nav_reports:"Reports",nav_ai:"AI & Analytics",nav_notifications:"Notifications",nav_notes:"Notes & Approvals",nav_archive:"Archive",
 nav_users:"Users & Permissions",nav_settings:"Settings",
 dash_sub:"Real-time view of organizational performance",crm_sub:"Client lifecycle from lead to project",proj_sub:"Track projects, tasks and delivery",
 ops_sub:"Field reports and performance",fin_sub:"Invoices, cash flow and collections",rep_sub:"Exportable, schedulable reports",
 ai_sub:"Predictions, risks and recommendations from your data",notif_sub:"Alerts generated from your actual data",notes_sub:"Notes, categories and approvals",
 arch_sub:"Documents, attachments and history",users_sub:"Manage roles, permissions and access",set_sub:"Account and platform preferences",
 kpi_revenue:"Project value",kpi_collected:"Collected",kpi_pending:"Pending receivables",kpi_projects:"Active projects",kpi_clients:"Clients",
 kpi_pipeline:"Pipeline value",kpi_risk:"At-risk projects",kpi_tasks:"Invoices",kpi_invoices:"Invoices",
 ch_revenue:"Revenue vs collections by month",ch_pipeline:"Pipeline distribution",ch_ops:"Team performance",
 active_projects:"Active projects",recent_activity:"Recent activity",ai_insights:"AI insights",
 st_lead:"Lead",st_opp:"Opportunity",st_prop:"Proposal",st_neg:"Negotiation",st_contract:"Contract",st_active:"Activated",crm_clients:"Client base",
 col_project:"Project",col_client:"Client",col_pm:"Project manager",col_progress:"Progress",col_status:"Status",col_value:"Value",col_due:"Due",
 ops_daily:"Daily",ops_monthly:"Monthly",ops_annual:"Annual",ops_field:"Field reports",ops_kpi:"KPI monitoring",team_perf:"Team performance",
 fin_issued:"Issued",fin_collected:"Collected",fin_pending:"Pending",fin_invoices:"Invoices",col_invoice:"Invoice no.",col_amount:"Amount",col_date:"Date",cashflow:"Cash flow",
 rep_fin:"Financial report",rep_ops:"Operational report",rep_exec:"Executive report",rep_perf:"Performance report",rep_gen:"Auto-generated · Export PDF / Excel · Scheduled",
 export_pdf:"Export PDF",export_xls:"Export Excel",schedule:"Schedule",ai_delay:"Delay prediction",ai_risk:"Risk detection",ai_score:"Performance scoring",ai_reco:"Recommendation engine",
 mark_read:"Mark all read",add_note:"Add note",note_ph:"Write your note here…",cat_risk:"Risk",cat_issue:"Issue",cat_sug:"Suggestion",
 approve:"Approve",reject:"Reject",col_doc:"Document",col_type:"Type",col_project2:"Project",col_user:"User",col_role:"Role",col_access:"Access",
 set_lang:"Interface language",set_profile:"Profile",save:"Save",view_all:"View all",locked_t:"Access not permitted",
 locked_b:"This module is not available for your current role. Contact the administrator for elevated access.",created:"Added successfully",saved:"Saved successfully",
 welcome:"Signed in — welcome",approved:"Approved",rejected:"Rejected",all_read:"Notifications marked as read",
 report_gen:"Generating report…",probability:"Probability",owner_label:"Owner",this_month:"This month",readonly_badge:"Read-only",
 cancel:"Cancel",required_err:"Please fill in the required fields.",now:"Just now",download:"Download",downloading:"Downloading…",
 add_client:"Add client",add_opp:"Add opportunity / lead",add_project:"Add project",add_invoice:"Add invoice",add_report:"Add field report",
 add_doc:"Upload document",add_user:"Add user",add_team:"Add team",
 f_contact:"Contact person",f_phone:"Phone",f_source:"Lead source",f_industry:"Industry",f_desc:"Description",f_start:"Start date",
 f_period:"Period",f_dept:"Department",f_decision:"Decision makers",f_expclose:"Expected close",f_competitors:"Competitors",
 f_stage:"Stage",f_amount:"Amount",f_score:"Performance score (%)",f_team:"Team name",f_report_txt:"Report text",f_invoice_no:"Invoice number",
 f_status:"Status",f_filetype:"File type",f_progress:"Progress (%)",select_opt:"— Select —",
 empty_dash_t:"Your dashboard is ready for your data",empty_dash_b:"Add a client, project or invoice and the KPIs and charts will build here automatically.",
 empty_clients_t:"No clients yet",empty_clients_b:"Add your first client to start building your base and pipeline.",
 empty_pipe_t:"Pipeline is empty",empty_pipe_b:"Add an opportunity or lead to see it here by stage.",
 empty_proj_t:"No projects yet",empty_proj_b:"Add your first project to track progress, tasks and value.",
 empty_inv_t:"No invoices yet",empty_inv_b:"Add an invoice to build cash flow and collection KPIs.",
 empty_rep_t:"No field reports",empty_rep_b:"Add a daily, monthly or annual report for your teams.",
 empty_notes_t:"No notes",empty_notes_b:"Add a categorized note to send it through approvals.",
 empty_arch_t:"Archive is empty",empty_arch_b:"Add a document to store project and contract attachments.",
 empty_ai_t:"No insights yet",empty_ai_b:"Insights are generated automatically from your projects and invoices.",
 empty_notif_t:"No notifications",empty_notif_b:"Alerts appear automatically when projects are delayed or receivables are pending.",
 empty_act_t:"No activity yet",empty_act_b:"Your actions will be logged here as you add data.",
 empty_team_t:"No teams",empty_team_b:"Add a team and its performance score to render the chart.",
 alert_delay:"Project behind schedule",alert_risk:"Risk on project",alert_pending:"Invoice pending collection",alert_note:"Note awaiting approval",
 ins_delay_h:"Delayed projects",ins_risk_h:"At-risk projects",ins_coll_h:"Collections recommendation",ins_top_h:"Top performing team",
 st_ontrack:"On track",st_risk:"At risk",st_delay:"Delayed",active_w:"Active",new_w:"New",pending_w:"Pending",modules_w:"modules",delete:"Delete",deleted:"Deleted successfully",confirm_del_t:"Confirm deletion",confirm_del_b:"Are you sure you want to delete this item? This action cannot be undone.",yes_delete:"Yes, delete"}
};

/* ===== roles & perms ===== */
const ROLES={system_admin:{ar:"مدير النظام",en:"System Administrator"},ceo:{ar:"الرئيس التنفيذي",en:"CEO"},board:{ar:"عضو مجلس الإدارة",en:"Board Member"},pm:{ar:"مدير مشروع",en:"Project Manager"},team_lead:{ar:"قائد فريق",en:"Team Lead"},member:{ar:"عضو فريق",en:"Team Member"},reviewer:{ar:"مراجع / مدقق",en:"Reviewer / Auditor"}};
const PERMS={
 system_admin:["dashboard","crm","projects","operations","financial","reports","ai","notifications","notes","archive","users","audit","settings"],
 ceo:["dashboard","crm","projects","operations","financial","reports","ai","notifications","notes","archive","users","audit","settings"],
 board:["dashboard","projects","financial","reports","ai","notifications","notes","archive","settings"],
 pm:["dashboard","crm","projects","operations","reports","ai","notifications","notes","archive","settings"],
 team_lead:["dashboard","projects","operations","notifications","notes","settings"],
 member:["dashboard","projects","operations","notifications","notes","settings"],
 reviewer:["dashboard","projects","reports","notifications","notes","archive","settings"]
};
// modules a role may only view (no create/edit/delete)
const READONLY={board:["dashboard","projects","financial","reports","ai","archive"],reviewer:["dashboard","projects","reports","archive"],member:["dashboard"],team_lead:["dashboard"]};
const NAV=[{group:"g_main",items:["dashboard"]},{group:"g_commercial",items:["crm"]},{group:"g_delivery",items:["projects","operations"]},{group:"g_intel",items:["financial","reports","ai"]},{group:"g_admin",items:["notifications","notes","archive","users","audit","settings"]}];
const NAV_ICONS_AUDIT="🛡";
const NAV_ICONS={dashboard:"◧",crm:"◎",projects:"▤",operations:"⚙",financial:"₪",reports:"▦",ai:"✦",notifications:"🔔",notes:"✎",archive:"🗂",users:"☷",audit:"🛡",settings:"⚙"};

/* ===== safe storage ===== */
const Store=(()=>{let ok=false;try{localStorage.setItem("__v","1");localStorage.removeItem("__v");ok=true;}catch(e){ok=false;}let mem={};
 return{available:ok,get(k,d){try{if(ok){const v=localStorage.getItem(k);return v?JSON.parse(v):d;}}catch(e){}return(k in mem)?mem[k]:d;},set(k,v){try{if(ok){localStorage.setItem(k,JSON.stringify(v));return;}}catch(e){}mem[k]=v;}};})();
const DKEY="velion_data_v3";
const blank={clients:[],pipeline:[],projects:[],invoices:[],reports:[],notes:[],archive:[],users:[],team:[],activity:[],audit:[]};
let DATA=Object.assign({},blank,Store.get(DKEY,{}));
for(const k in blank){if(!Array.isArray(DATA[k]))DATA[k]=[];}
let __id=Date.now();function uid(){return "id"+(++__id).toString(36)+Math.floor(Math.random()*1e4).toString(36);}
["clients","pipeline","projects","invoices","reports","notes","archive","users","team"].forEach(k=>DATA[k].forEach(r=>{if(r&&!r.id)r.id=uid();}));
// normalise user accounts: ensure status + role validity
DATA.users.forEach(u=>{if(u&&!u.status)u.status="active";if(u&&!ROLES[u.role])u.role="member";});
function save(){Store.set(DKEY,DATA);}
function logAudit(action,target){DATA.audit.unshift({id:uid(),ts:Date.now(),actor:state.user?state.user.name:"—",role:state.user?state.user.role:"—",action,target:target||""});DATA.audit=DATA.audit.slice(0,300);save();}

const state={lang:Store.get("velion_lang","ar"),user:null,view:"dashboard"};
let charts={};

/* ===== helpers ===== */
const $=(s,r=document)=>r.querySelector(s);
const $$=(s,r=document)=>[...r.querySelectorAll(s)];
const t=k=>(I18N[state.lang][k]!==undefined?I18N[state.lang][k]:k);
const L=o=>(o&&typeof o==="object")?(o[state.lang]||o.ar||o.en||""):(o||"");
const esc=s=>String(s==null?"":s).replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]));
const money=n=>{n=+n||0;const s=state.lang==="ar"?"ر.س":"SAR";const v=n>=1000000?(n/1000000).toFixed(2)+(state.lang==="ar"?"م":"M"):n>=1000?(n/1000).toFixed(0)+(state.lang==="ar"?"ك":"K"):Math.round(n);return state.lang==="ar"?v+" "+s:s+" "+v;};
const can=m=>state.user&&PERMS[state.user.role].includes(m);
const isRO=m=>state.user&&READONLY[state.user.role]&&READONLY[state.user.role].includes(m);
const today=()=>new Date().toISOString().slice(0,10);
function toast(msg){const el=document.createElement("div");el.className="toast";el.innerHTML='<span style="color:var(--gold)">✦</span><span>'+esc(msg)+'</span>';$("#toast").appendChild(el);setTimeout(()=>{el.style.opacity="0";el.style.transition="opacity .3s";setTimeout(()=>el.remove(),300);},2400);}
function openModal(h){$("#modalBox").innerHTML=h;$("#modalWrap").classList.add("show");}
function closeModal(){$("#modalWrap").classList.remove("show");}
window.closeModal=closeModal;window.velionToast=toast;
$("#modalWrap").addEventListener("click",e=>{if(e.target.id==="modalWrap")closeModal();});
function logAct(ic,cls,text){DATA.activity.unshift({ic,cls,text,date:Date.now()});DATA.activity=DATA.activity.slice(0,20);save();}
function timeAgo(ts){const d=Math.floor((Date.now()-ts)/60000);if(d<1)return t("now");if(d<60)return d+(state.lang==="ar"?" د":"m");const h=Math.floor(d/60);if(h<24)return h+(state.lang==="ar"?" س":"h");return Math.floor(h/24)+(state.lang==="ar"?" ي":"d");}
function delBtn(arr,id,label){return '<button class="del-btn" data-del="'+arr+'|'+id+'" data-label="'+esc(label)+'" title="'+t("delete")+'">🗑</button>';}
function editBtn(kind,id){return '<button class="del-btn edit-btn" data-edit="'+kind+'|'+id+'" title="'+t("edit")+'">✎</button>';}
const STAGES=["lead","opp","prop","neg","contract","active"];
const STAGE_PROB={lead:15,opp:40,prop:60,neg:75,contract:90,active:100};
function activateOpp(opp){if(opp.projectId&&DATA.projects.find(p=>p.id===opp.projectId))return;const pid=uid();DATA.projects.unshift({id:pid,name:opp.name,client:opp.name,pm:(opp.owner&&opp.owner!=="—")?opp.owner:"",val:+opp.val||0,prog:0,start:today(),due:opp.expclose||"",status:"ontrack",desc:(state.lang==="ar"?"أُنشئ تلقائيًا عند تفعيل الفرصة":"Auto-created on opportunity activation"),fromOpp:opp.id});opp.projectId=pid;}
function moveOpp(id,stage){const p=DATA.pipeline.find(x=>x.id===id);if(!p||p.stage===stage)return;p.stage=stage;if(!p.prob||p.prob<STAGE_PROB[stage])p.prob=STAGE_PROB[stage];let msg=t("moved")+": "+L(p.name)+" → "+t("st_"+stage);if(stage==="active"){activateOpp(p);msg=t("activated_proj");}save();logAct("◎","b1",msg);renderShell();renderView();toast(msg);}
function advanceOpp(id){const p=DATA.pipeline.find(x=>x.id===id);if(!p)return;const i=STAGES.indexOf(p.stage);if(i>-1&&i<STAGES.length-1)moveOpp(id,STAGES[i+1]);}
function convertClient(id){const c=DATA.clients.find(x=>x.id===id);if(!c)return;DATA.pipeline.unshift({id:uid(),stage:"lead",name:L(c.name),val:+c.val||0,prob:STAGE_PROB.lead,owner:c.owner||c.contact||"—",clientId:c.id,competitors:"",decision:""});save();logAct("◎","b1",t("converted")+": "+L(c.name));renderShell();renderView();toast(t("converted"));}
let __drag=null;
function bindKanban(){$$(".kcard[draggable='true']").forEach(c=>{c.addEventListener("dragstart",()=>{__drag=c.dataset.id;c.classList.add("dragging");});c.addEventListener("dragend",()=>{__drag=null;c.classList.remove("dragging");});});
 $$(".kcol[data-stage]").forEach(col=>{col.addEventListener("dragover",e=>{e.preventDefault();col.classList.add("drag-over");});col.addEventListener("dragleave",()=>col.classList.remove("drag-over"));col.addEventListener("drop",e=>{e.preventDefault();col.classList.remove("drag-over");if(__drag)moveOpp(__drag,col.dataset.stage);});});}
function confirmDelete(label,onYes){openModal('<h2>'+t("confirm_del_t")+'</h2><p class="msub">'+t("confirm_del_b")+'</p><div class="card" style="padding:14px;margin-bottom:18px;border-inline-start:4px solid var(--danger)"><b style="color:var(--ink)">'+esc(label)+'</b></div><div class="row gap-s"><button class="btn grow" style="background:var(--danger);color:#fff" id="del_yes">🗑 '+t("yes_delete")+'</button><button class="btn ghost" onclick="closeModal()">'+t("cancel")+'</button></div>');$("#del_yes").addEventListener("click",()=>{closeModal();onYes();});}
function delById(arr,id,label){confirmDelete(label,()=>{const i=DATA[arr].findIndex(r=>r.id===id);if(i>-1){DATA[arr].splice(i,1);save();logAct("🗑","b5",t("deleted")+(label?": "+label:""));renderShell();renderView();toast(t("deleted"));}});}
function bindDeletes(){
 $$("[data-del]").forEach(b=>b.addEventListener("click",e=>{e.stopPropagation();const i=b.dataset.del.indexOf("|");delById(b.dataset.del.slice(0,i),b.dataset.del.slice(i+1),b.dataset.label||"");}));
 $$("[data-edit]").forEach(b=>b.addEventListener("click",e=>{e.stopPropagation();const i=b.dataset.edit.indexOf("|");const kind=b.dataset.edit.slice(0,i),id=b.dataset.edit.slice(i+1);if(EDITORS[kind])EDITORS[kind](id);}));
 $$("[data-conv]").forEach(b=>b.addEventListener("click",e=>{e.stopPropagation();convertClient(b.dataset.conv);}));
 $$("[data-adv]").forEach(b=>b.addEventListener("click",e=>{e.stopPropagation();advanceOpp(b.dataset.adv);}));
 $$("[data-plan]").forEach(b=>b.addEventListener("click",e=>{e.stopPropagation();projectModal(b.dataset.plan);}));
 bindKanban();
}

/* ===== language ===== */
function applyLang(){document.documentElement.lang=state.lang;document.documentElement.dir=state.lang==="ar"?"rtl":"ltr";document.body.dataset.lang=state.lang;
 $$("[data-i]").forEach(el=>el.textContent=t(el.dataset.i));$$("[data-iph]").forEach(el=>el.placeholder=t(el.dataset.iph));
 $$("[data-setlang]").forEach(b=>b.classList.toggle("active",b.dataset.setlang===state.lang));Store.set("velion_lang",state.lang);}
function setLang(l){state.lang=l;applyLang();if($("#app").style.display==="block"){renderShell();renderView();}}
$$("[data-setlang]").forEach(b=>b.addEventListener("click",()=>setLang(b.dataset.setlang)));

/* ===== auth (closed access) ===== */
function authMode(){const hasAdmin=DATA.users.some(u=>u.role==="system_admin");$("#loginForm").classList.toggle("hidden",!hasAdmin);$("#setupForm").classList.toggle("hidden",hasAdmin);$("#authErr").classList.remove("show");}
$("#loginForm").addEventListener("submit",e=>{e.preventDefault();const id=$("#li_email").value.trim().toLowerCase(),pass=$("#li_pass").value;
 const u=DATA.users.find(x=>(x.email||"").toLowerCase()===id||(x.username||"").toLowerCase()===id);
 if(!u){return showErr(t("err_nouser"));}
 if(u.status==="suspended"){return showErr(t("err_suspended"));}
 if((u.pass||"")!==pass){return showErr(t("err_wrongpass"));}
 login(u);});
$("#setupForm").addEventListener("submit",e=>{e.preventDefault();const name=$("#su_name").value.trim(),email=$("#su_email").value.trim(),p1=$("#su_pass").value,p2=$("#su_pass2").value;
 if(!name||!email||!p1)return showErr(t("required_err"));if(p1!==p2)return showErr(t("err_passmatch"));
 const admin={id:uid(),name,email,username:email,pass:p1,role:"system_admin",status:"active",dept:"",projects:[],created:today()};
 DATA.users.unshift(admin);save();login(admin);});
function showErr(msg){const e=$("#authErr");e.textContent=msg||t("required_err");e.classList.add("show");}
function login(u){state.user=u;state.view="dashboard";u.lastLogin=Date.now();save();$("#landing").style.display="none";$("#app").style.display="block";logAudit("login","");renderShell();renderView();toast(t("welcome")+" "+u.name.split(" ")[0]+" 👋");}
$("#btnLogout").addEventListener("click",()=>{logAudit("logout","");state.user=null;destroyCharts();$("#app").style.display="none";$("#landing").style.display="flex";$("#li_email").value="";$("#li_pass").value="";authMode();});

/* ===== shell ===== */
function computeAlerts(){const a=[];DATA.projects.forEach(p=>{if(p.status==="delay")a.push({ic:"⚠",cls:"b5",text:t("alert_delay")+": "+L(p.name)});else if(p.status==="risk")a.push({ic:"⚠",cls:"b4",text:t("alert_risk")+": "+L(p.name)});});DATA.invoices.forEach(i=>{if(i.status!=="collected")a.push({ic:"₪",cls:"b3",text:t("alert_pending")+": "+i.no+" — "+money(i.amt)});});DATA.notes.forEach(n=>{if(n.status==="pending")a.push({ic:"✎",cls:"b2",text:t("alert_note")});});return a;}
function renderShell(){$("#sbWho").textContent=state.user.name;$("#sbRole").textContent=ROLES[state.user.role][state.lang];$("#topAvatar").textContent=state.user.name.trim().charAt(0).toUpperCase();
 const alerts=computeAlerts();$("#notifDot").classList.toggle("hidden",alerts.length===0);
 const nav=$("#sbNav");nav.innerHTML="";
 NAV.forEach(grp=>{const allowed=grp.items.filter(m=>can(m));if(!allowed.length)return;const gl=document.createElement("div");gl.className="nav-group-label";gl.textContent=t(grp.group);nav.appendChild(gl);
  allowed.forEach(m=>{const it=document.createElement("div");it.className="nav-item"+(state.view===m?" active":"");const badge=(m==="notifications"&&alerts.length)?'<span class="badge">'+alerts.length+'</span>':"";it.innerHTML='<span class="ic">'+NAV_ICONS[m]+'</span><span>'+t("nav_"+m)+'</span>'+badge;it.addEventListener("click",()=>{state.view=m;closeSidebar();renderShell();renderView();});nav.appendChild(it);});});}
$("#topLang").addEventListener("click",()=>setLang(state.lang==="ar"?"en":"ar"));
$("#topNotif").addEventListener("click",()=>{if(can("notifications")){state.view="notifications";renderShell();renderView();}});
$("#menuBtn").addEventListener("click",()=>{$("#sidebar").classList.add("open");$("#mOverlay").classList.add("show");});
$("#mOverlay").addEventListener("click",closeSidebar);
function closeSidebar(){$("#sidebar").classList.remove("open");$("#mOverlay").classList.remove("show");}
$("#globalSearch").addEventListener("keydown",e=>{if(e.key==="Enter"&&e.target.value)toast((state.lang==="ar"?"بحث عن: ":"Searching: ")+e.target.value);});

/* ===== generic form modal ===== */
function readFiles(input){return Promise.all([...input.files].map(file=>new Promise(res=>{const r=new FileReader();r.onload=()=>res({name:file.name,type:(file.name.split(".").pop()||"FILE").toUpperCase(),size:file.size,data:r.result});r.onerror=()=>res({name:file.name,type:"FILE",size:file.size,data:null});r.readAsDataURL(file);})));}
function fileLabel(f){const kb=f.size?(f.size>1048576?(f.size/1048576).toFixed(1)+"MB":Math.max(1,Math.round(f.size/1024))+"KB"):"";return esc(f.name)+(kb?' <span style="color:var(--muted)">· '+kb+'</span>':"");}
function attachChips(files){if(!files||!files.length)return"";return '<div class="attach-list">'+files.map(f=>'<a class="attach-chip" '+(f.data?'href="'+f.data+'" download="'+esc(f.name)+'"':'')+'>📎 '+fileLabel(f)+'</a>').join("")+'</div>';}
function formModal(title,sub,fields,onSave,initial){
 initial=initial||{};
 const body=fields.map(f=>{const req=f.required?" req":"";let ctl="";
  const v=(initial[f.id]!=null&&typeof initial[f.id]!=="object")?String(initial[f.id]):(f.value!=null?String(f.value):"");
  if(f.type==="textarea")ctl='<textarea id="ff_'+f.id+'" placeholder="'+(f.ph||"")+'">'+esc(v)+'</textarea>';
  else if(f.type==="select")ctl='<select id="ff_'+f.id+'"><option value="">'+t("select_opt")+'</option>'+f.options.map(o=>'<option value="'+esc(o.v)+'"'+(String(o.v)===v?' selected':'')+'>'+esc(o.label)+'</option>').join("")+'</select>';
  else if(f.type==="datalist"){const dl="dl_"+f.id;ctl='<input id="ff_'+f.id+'" list="'+dl+'" value="'+esc(v)+'" placeholder="'+(f.ph||"")+'"><datalist id="'+dl+'">'+(f.list||[]).map(o=>'<option value="'+esc(o)+'">').join("")+'</datalist>';}
  else if(f.type==="file"){const ex=(initial[f.id]&&initial[f.id].length)?attachChips(initial[f.id]):"";ctl='<input id="ff_'+f.id+'" type="file" multiple style="padding:9px 12px;background:var(--surface-3)">'+(ex?'<div class="hint" style="margin-top:6px">'+t("current_files")+':</div>'+ex:"")+'<div class="hint">'+t("upload_hint")+'</div>';}
  else ctl='<input id="ff_'+f.id+'" type="'+(f.type||"text")+'" value="'+esc(v)+'" placeholder="'+(f.ph||"")+'">';
  return '<div class="field'+req+(f.full?' full':'')+'"><label>'+esc(f.label)+'</label>'+ctl+'</div>';}).join("");
 openModal('<h2>'+esc(title)+'</h2><p class="msub">'+esc(sub)+'</p><div class="form-grid">'+body+'</div><div class="row gap-s" style="margin-top:10px"><button class="btn gold grow" id="ff_save">'+t("save")+'</button><button class="btn ghost" onclick="closeModal()">'+t("cancel")+'</button></div>');
 $("#ff_save").addEventListener("click",async()=>{const btn=$("#ff_save");const out={};let okFlag=true;
  for(const f of fields){if(f.type==="file"){const inp=$("#ff_"+f.id);let nf=[];if(inp.files&&inp.files.length){btn.disabled=true;btn.textContent="…";nf=await readFiles(inp);}out[f.id]=(initial[f.id]||[]).concat(nf);}else{const v=$("#ff_"+f.id).value.trim();out[f.id]=v;if(f.required&&!v)okFlag=false;}}
  if(!okFlag){toast(t("required_err"));btn.disabled=false;btn.textContent=t("save");return;}
  try{onSave(out);}catch(e){console.error(e);}closeModal();});
}
const clientNames=()=>DATA.clients.map(c=>L(c.name));
const projectNames=()=>DATA.projects.map(p=>L(p.name));

/* ===== view router ===== */
function destroyCharts(){Object.values(charts).forEach(c=>{try{c.destroy();}catch(e){}});charts={};}
function renderView(){destroyCharts();const v=state.view;
 $("#pageTitle").innerHTML=t("nav_"+v)+'<small>'+t((v==="dashboard"?"dash":v==="crm"?"crm":v==="projects"?"proj":v==="operations"?"ops":v==="financial"?"fin":v==="reports"?"rep":v==="ai"?"ai":v==="notifications"?"notif":v==="notes"?"notes":v==="archive"?"arch":v==="users"?"users":v==="audit"?"audit":"set")+"_sub")+'</small>';
 if(!can(v)){$("#view").innerHTML=lockedView();return;}
 ({dashboard:viewDashboard,crm:viewCRM,projects:viewProjects,operations:viewOperations,financial:viewFinancial,reports:viewReports,ai:viewAI,notifications:viewNotifications,notes:viewNotes,archive:viewArchive,users:viewUsers,audit:viewAudit,settings:viewSettings}[v]||viewDashboard)();}
function lockedView(){return '<div class="locked"><div class="l-ic">🔒</div><h2 style="color:var(--navy-800);font-family:Sora;margin-bottom:8px">'+t("locked_t")+'</h2><p style="max-width:380px">'+t("locked_b")+'</p></div>';}
function headHTML(title,sub,actions){return '<div class="page-head"><div><h1>'+title+'</h1><p>'+sub+'</p></div><div class="row gap-s">'+(actions||"")+'</div></div>';}
function roBadge(m){return isRO(m)?'<span class="badge2 bg-mute" style="margin-inline-start:8px">'+t("readonly_badge")+'</span>':"";}
function emptyState(icon,tk,bk,btnLabel,btnId){return '<div class="empty"><div class="e-ic">'+icon+'</div><div class="e-t">'+t(tk)+'</div><div class="e-b">'+t(bk)+'</div>'+(btnLabel?'<button class="btn gold" id="'+btnId+'">+ '+btnLabel+'</button>':'')+'</div>';}
function statusBadge(s){const m={ontrack:["bg-success","st_ontrack"],risk:["bg-warn","st_risk"],delay:["bg-danger","st_delay"]};const x=m[s]||m.ontrack;return '<span class="badge2 '+x[0]+'">'+t(x[1])+'</span>';}
function bindGo(){$$("[data-go]").forEach(e=>e.addEventListener("click",()=>{const m=e.dataset.go;if(can(m)){state.view=m;renderShell();renderView();}}));}

/* ===== DASHBOARD ===== */
function viewDashboard(){
 const hasData=DATA.projects.length||DATA.invoices.length||DATA.clients.length||DATA.pipeline.length;
 const totalVal=DATA.projects.reduce((a,p)=>a+(+p.val||0),0);
 const collected=DATA.invoices.filter(i=>i.status==="collected").reduce((a,i)=>a+(+i.amt||0),0);
 const pending=DATA.invoices.filter(i=>i.status!=="collected").reduce((a,i)=>a+(+i.amt||0),0);
 const pipeline=DATA.pipeline.filter(p=>p.stage!=="active").reduce((a,p)=>a+(+p.val||0),0);
 let kpis=[{ic:"₪",b:"b1",val:money(totalVal),lbl:t("kpi_revenue")},{ic:"✓",b:"b3",val:money(collected),lbl:t("kpi_collected")},{ic:"◷",b:"b5",val:money(pending),lbl:t("kpi_pending")},{ic:"▤",b:"b2",val:DATA.projects.length,lbl:t("kpi_projects")}];
 if(state.user.role==="board")kpis=[{ic:"✓",b:"b3",val:money(collected),lbl:t("kpi_collected")},{ic:"◷",b:"b5",val:money(pending),lbl:t("kpi_pending")},{ic:"₪",b:"b1",val:money(totalVal),lbl:t("kpi_revenue")},{ic:"▤",b:"b2",val:DATA.projects.length,lbl:t("kpi_projects")}];
 if(["team_lead","member","reviewer"].includes(state.user.role))kpis=[{ic:"▤",b:"b2",val:DATA.projects.length,lbl:t("kpi_projects")},{ic:"⚠",b:"b5",val:DATA.projects.filter(p=>p.status!=="ontrack").length,lbl:t("kpi_risk")},{ic:"▦",b:"b3",val:DATA.reports.length,lbl:t("ops_field")},{ic:"◎",b:"b1",val:DATA.clients.length,lbl:t("kpi_clients")}];
 const kpiHTML=kpis.map(k=>'<div class="card kpi"><div class="top"><div><div class="val">'+k.val+'</div><div class="lbl">'+k.lbl+'</div></div><div class="ic '+k.b+'">'+k.ic+'</div></div></div>').join("");
 if(!hasData){$("#view").innerHTML=headHTML((state.lang==="ar"?"أهلاً، ":"Hello, ")+state.user.name.split(" ")[0],t("dash_sub"))+'<div class="grid cols-4" style="margin-bottom:18px">'+kpiHTML+'</div><div class="card">'+emptyState("◧","empty_dash_t","empty_dash_b",can("projects")?t("add_project"):can("crm")?t("add_client"):"",can("projects")?"goAddProj":"goAddClient")+'</div>';
  const gp=$("#goAddProj");if(gp)gp.addEventListener("click",()=>{state.view="projects";renderShell();renderView();});const gc=$("#goAddClient");if(gc)gc.addEventListener("click",()=>{state.view="crm";renderShell();renderView();});return;}
 const projRows=DATA.projects.slice(0,5).map(p=>'<tr><td><div class="pname">'+esc(L(p.name))+'</div><div style="font-size:11.5px;color:var(--muted)">'+esc(L(p.client))+'</div></td><td>'+statusBadge(p.status)+'</td><td><div class="row gap-s"><div class="progress green"><span style="width:'+(+p.prog||0)+'%"></span></div><b style="font-size:12px">'+(+p.prog||0)+'%</b></div></td><td style="font-weight:600;color:var(--gold-deep)">'+money(p.val)+'</td></tr>').join("");
 const projTable=DATA.projects.length?'<table><thead><tr><th>'+t("col_project")+'</th><th>'+t("col_status")+'</th><th>'+t("col_progress")+'</th><th>'+t("col_value")+'</th></tr></thead><tbody>'+projRows+'</tbody></table>':emptyState("▤","empty_proj_t","empty_proj_b");
 const ins=buildInsights().slice(0,2);
 const aiHTML=ins.length?ins.map(a=>'<div class="ai-insight"><div class="ai-ic ic '+a.ic+'">'+a.glyph+'</div><div><div class="h">'+esc(a.h)+'</div><div class="b">'+esc(a.b)+'</div></div></div>').join(""):'<div style="color:#AFC0D8;font-size:13px;padding:8px">'+t("empty_ai_b")+'</div>';
 const acts=DATA.activity.slice(0,6);
 const actHTML=acts.length?acts.map(a=>'<div class="list-row"><div class="l-ic ic '+a.cls+'">'+a.ic+'</div><div class="grow"><div class="l-t">'+esc(a.text)+'</div></div><div class="l-time">'+timeAgo(a.date)+'</div></div>').join(""):emptyState("◷","empty_act_t","empty_act_b");
 $("#view").innerHTML=headHTML((state.lang==="ar"?"أهلاً، ":"Hello, ")+state.user.name.split(" ")[0],t("dash_sub"))+
  '<div class="grid cols-4" style="margin-bottom:18px">'+kpiHTML+'</div>'+
  '<div class="grid cols-3" style="margin-bottom:18px"><div class="card" style="grid-column:span 2"><div class="card-h"><h3>'+t("ch_revenue")+'</h3></div><div style="height:280px"><canvas id="cRev"></canvas></div></div><div class="card"><div class="card-h"><h3>'+t("ch_pipeline")+'</h3></div><div style="height:280px"><canvas id="cPipe"></canvas></div></div></div>'+
  '<div class="grid cols-3"><div class="card" style="grid-column:span 2"><div class="card-h"><h3>'+t("active_projects")+'</h3>'+(DATA.projects.length?'<span class="more" data-go="projects">'+t("view_all")+' →</span>':'')+'</div>'+projTable+'</div><div class="card ai-card"><div class="card-h"><h3>✦ '+t("ai_insights")+'</h3>'+(can("ai")?'<span class="more" data-go="ai" style="color:var(--gold-soft)">'+t("view_all")+' →</span>':'')+'</div>'+aiHTML+'</div></div>'+
  '<div class="grid cols-2" style="margin-top:18px"><div class="card"><div class="card-h"><h3>'+t("recent_activity")+'</h3></div>'+actHTML+'</div><div class="card"><div class="card-h"><h3>'+t("ch_ops")+'</h3></div><div style="height:240px"><canvas id="cTeam"></canvas></div></div></div>'+planCardHTML();
 bindGo();drawRevenue();drawPipe();drawTeam();
}
function planUpdates(){const out=[];DATA.projects.forEach(p=>{if(p.plan)Object.keys(p.plan).forEach(m=>{const e=p.plan[m];out.push({proj:L(p.name),m:+m,prog:e.prog,status:e.status,note:e.note,by:e.by,date:e.date||"",files:e.files});});});return out.sort((a,b)=>(b.date||"").localeCompare(a.date||"")||b.m-a.m);}
function planCardHTML(){const pu=planUpdates();if(!pu.length)return"";const mn=monthsList();return '<div class="card" style="margin-top:18px"><div class="card-h"><h3>📅 '+t("monthly_updates")+'</h3></div>'+pu.slice(0,6).map(u=>'<div class="list-row"><div class="l-ic ic b1" style="font-weight:700;font-size:13px">'+mn[u.m].slice(0,3)+'</div><div class="grow"><div class="l-t">'+esc(u.proj)+' · '+mn[u.m]+'</div><div class="l-s">'+esc(u.note||"—")+(u.by?' — '+esc(u.by):'')+((u.files&&u.files.length)?' · 📎 '+u.files.length:'')+'</div></div><div class="row gap-s">'+statusBadge(u.status||"ontrack")+'<b style="font-size:13px;color:var(--gold-deep)">'+(u.prog||0)+'%</b></div></div>').join("")+'</div>';}
function buildInsights(){const out=[];const del=DATA.projects.filter(p=>p.status==="delay");const rsk=DATA.projects.filter(p=>p.status==="risk");const pend=DATA.invoices.filter(i=>i.status!=="collected");
 if(del.length)out.push({cat:"ai_delay",ic:"b5",glyph:"◷",h:t("ins_delay_h"),b:del.map(p=>L(p.name)).join("، ")});
 if(rsk.length)out.push({cat:"ai_risk",ic:"b4",glyph:"⚠",h:t("ins_risk_h"),b:rsk.map(p=>L(p.name)).join("، ")});
 if(pend.length)out.push({cat:"ai_reco",ic:"b1",glyph:"✦",h:t("ins_coll_h"),b:(state.lang==="ar"?"مستحقات معلّقة بقيمة ":"Pending receivables of ")+money(pend.reduce((a,i)=>a+(+i.amt||0),0))});
 if(DATA.team.length){const top=[...DATA.team].sort((a,b)=>b.score-a.score)[0];out.push({cat:"ai_score",ic:"b3",glyph:"★",h:t("ins_top_h"),b:L(top.name)+" — "+top.score+"%"});}
 return out;}
const cFont=()=>({family:state.lang==="ar"?"IBM Plex Sans Arabic":"Sora"});
function gridOpts(){return{plugins:{legend:{labels:{font:cFont(),color:"#3C4E68",usePointStyle:true,padding:16}}},scales:{x:{ticks:{font:cFont(),color:"#7A8AA3"},grid:{display:false}},y:{ticks:{font:cFont(),color:"#7A8AA3"},grid:{color:"#EEF2F8"}}},maintainAspectRatio:false,responsive:true};}
function chartEmpty(id,tk){const c=document.getElementById(id);if(c){c.outerHTML='<div class="chart-empty">'+t(tk)+'</div>';}return true;}
function drawRevenue(){const inv=DATA.invoices;if(!inv.length)return chartEmpty("cRev","empty_inv_b");const map={};inv.forEach(i=>{const m=(i.date||today()).slice(0,7);if(!map[m])map[m]={iss:0,col:0};map[m].iss+=+i.amt||0;if(i.status==="collected")map[m].col+=+i.amt||0;});const labels=Object.keys(map).sort();const ctx=$("#cRev");charts.rev=new Chart(ctx,{type:"bar",data:{labels,datasets:[{label:state.lang==="ar"?"صادرة":"Issued",data:labels.map(l=>map[l].iss/1000),backgroundColor:"#1E3D63",borderRadius:6,maxBarThickness:26},{label:t("fin_collected"),data:labels.map(l=>map[l].col/1000),backgroundColor:"#D4AF37",borderRadius:6,maxBarThickness:26}]},options:gridOpts()});}
function drawPipe(){const stages=["lead","opp","prop","neg","contract"];const data=stages.map(s=>DATA.pipeline.filter(p=>p.stage===s).reduce((a,p)=>a+(+p.val||0)/1000,0));if(data.every(d=>d===0))return chartEmpty("cPipe","empty_pipe_b");const ctx=$("#cPipe");charts.pipe=new Chart(ctx,{type:"doughnut",data:{labels:stages.map(s=>t("st_"+s)),datasets:[{data,backgroundColor:["#3D7FC4","#5CC78F","#D4AF37","#E0A93B","#16304F"],borderWidth:0}]},options:{cutout:"62%",maintainAspectRatio:false,responsive:true,plugins:{legend:{position:state.lang==="ar"?"right":"left",labels:{font:cFont(),color:"#3C4E68",usePointStyle:true,padding:11,boxWidth:8}}}}});}
function drawTeam(){if(!DATA.team.length)return chartEmpty("cTeam","empty_team_b");const ctx=$("#cTeam");charts.team=new Chart(ctx,{type:"bar",data:{labels:DATA.team.map(x=>L(x.name)),datasets:[{label:t("team_perf"),data:DATA.team.map(x=>+x.score||0),backgroundColor:DATA.team.map(x=>x.score>=85?"#2E9E6B":x.score>=70?"#D4AF37":"#D9534F"),borderRadius:6,maxBarThickness:34}]},options:Object.assign({indexAxis:"y"},gridOpts(),{plugins:{legend:{display:false}}})});}

/* ===== CRM ===== */
function viewCRM(){
 const ro=isRO("crm");
 const stages=[["lead","st_lead"],["opp","st_opp"],["prop","st_prop"],["neg","st_neg"],["contract","st_contract"],["active","st_active"]];
 const hasPipe=DATA.pipeline.length;
 const cols=stages.map(([s,k])=>{const items=DATA.pipeline.filter(p=>p.stage===s);const cards=items.map(p=>'<div class="kcard" draggable="'+(ro?'false':'true')+'" data-id="'+p.id+'">'+(ro?'':'<button class="kdel" data-del="pipeline|'+p.id+'" data-label="'+esc(L(p.name))+'" title="'+t("delete")+'">×</button>')+'<div class="cn">'+esc(L(p.name))+'</div><div class="cv">'+money(p.val)+'</div><div class="cm"><span>'+t("probability")+': '+(p.prob||0)+'%</span><span>'+esc(p.owner||"—")+'</span></div>'+(p.projectId?'<div class="kbadge">✓ '+t("linked_proj")+'</div>':'')+(ro?'':'<div class="kacts"><button class="kact" data-edit="opp|'+p.id+'" title="'+t("edit")+'">✎</button>'+(p.stage!=="active"?'<button class="kact adv" data-adv="'+p.id+'">'+(state.lang==="ar"?"التالي ←":"Next →")+'</button>':'')+'</div>')+'</div>').join("")||'<div class="kempty">—</div>';return '<div class="kcol" data-stage="'+s+'"><div class="kcol-h"><span class="t">'+t(k)+'</span><span class="c">'+items.length+'</span></div>'+cards+'</div>';}).join("");
 const clientsBlock=DATA.clients.length?'<table><thead><tr><th>'+t("col_client")+'</th><th>'+t("col_responsible")+'</th><th>'+t("col_phone")+'</th><th>'+t("f_account_owner")+'</th><th>'+t("col_value")+'</th>'+(ro?'':'<th></th>')+'</tr></thead><tbody>'+DATA.clients.map(c=>'<tr><td class="pname">'+esc(L(c.name))+(c.industry?'<div style="font-size:11px;color:var(--muted);font-weight:400">'+esc(c.industry)+'</div>':'')+'</td><td>'+esc(c.contact||"—")+(c.contactTitle?'<div style="font-size:11px;color:var(--muted)">'+esc(c.contactTitle)+'</div>':'')+'</td><td dir="ltr" style="text-align:start">'+esc(c.phone||"—")+(c.phone2?'<div style="font-size:11px;color:var(--muted)">'+esc(c.phone2)+'</div>':'')+'</td><td>'+esc(c.owner||"—")+'</td><td style="font-weight:600;color:var(--gold-deep)">'+money(c.val)+'</td>'+(ro?'':'<td><div class="row gap-s"><button class="btn ghost" style="padding:6px 11px;font-size:12px" data-conv="'+c.id+'" title="'+t("to_opp")+'">→ '+t("to_opp")+'</button>'+editBtn("client",c.id)+delBtn("clients",c.id,L(c.name))+'</div></td>')+'</tr>').join("")+'</tbody></table>':emptyState("◎","empty_clients_t","empty_clients_b",ro?"":t("add_client"),"emClient");
 const actions=ro?"":'<button class="btn ghost" id="addClient">+ '+t("add_client")+'</button><button class="btn gold" id="addOpp">+ '+t("add_opp")+'</button>';
 $("#view").innerHTML=headHTML(t("nav_crm")+roBadge("crm"),t("crm_sub"),actions)+
  '<div class="card" style="margin-bottom:18px"><div class="card-h"><h3>'+(state.lang==="ar"?"خط أنابيب المبيعات":"Sales pipeline")+'</h3>'+(hasPipe&&!ro?'<span class="dnd-hint">↔ '+t("drag_hint")+'</span>':'')+'</div>'+(hasPipe?'<div class="kanban">'+cols+'</div>':emptyState("◎","empty_pipe_t","empty_pipe_b",ro?"":t("add_opp"),"emOpp"))+'</div>'+
  '<div class="card"><div class="card-h"><h3>'+t("crm_clients")+'</h3></div>'+clientsBlock+'</div>';
 [["addClient",addClient],["emClient",addClient],["addOpp",addOpp],["emOpp",addOpp]].forEach(([id,fn])=>{const el=$("#"+id);if(el)el.addEventListener("click",fn);});
 bindDeletes();
}
function clientFields(){return [
 {id:"name",label:t("col_client"),required:true,full:true},
 {id:"industry",label:t("f_industry")},{id:"source",label:t("f_source")},
 {id:"contact",label:t("f_responsible")},{id:"contactTitle",label:t("f_resp_title")},
 {id:"phone",label:t("f_resp_phone"),type:"tel"},{id:"phone2",label:t("f_resp_phone2"),type:"tel"},
 {id:"email",label:t("f_resp_email"),type:"email"},{id:"owner",label:t("f_account_owner")},
 {id:"val",label:t("kpi_pipeline"),type:"number",full:true},
];}
function addClient(){formModal(t("add_client"),t("crm_sub"),clientFields(),o=>{DATA.clients.unshift({id:uid(),name:o.name,industry:o.industry,source:o.source,contact:o.contact,contactTitle:o.contactTitle,phone:o.phone,phone2:o.phone2,email:o.email,owner:o.owner,val:+o.val||0});save();logAct("◎","b1",t("add_client")+": "+o.name);renderShell();renderView();toast(t("created"));});}
function editClient(id){const c=DATA.clients.find(x=>x.id===id);if(!c)return;formModal(t("edit_client"),t("change_resp_hint"),clientFields(),o=>{const oldOwner=c.owner;Object.assign(c,{name:o.name,industry:o.industry,source:o.source,contact:o.contact,contactTitle:o.contactTitle,phone:o.phone,phone2:o.phone2,email:o.email,owner:o.owner,val:+o.val||0});if(oldOwner!==o.owner){DATA.pipeline.forEach(p=>{if(p.clientId===c.id)p.owner=o.owner||p.owner;});}save();logAct("✎","b2",t("saved")+": "+o.name);renderShell();renderView();toast(t("saved"));},c);}
function oppFields(){return [
 {id:"name",label:t("col_client"),required:true,full:true,type:"datalist",list:clientNames()},
 {id:"stage",label:t("f_stage"),type:"select",required:true,options:STAGES.map(s=>({v:s,label:t("st_"+s)}))},
 {id:"val",label:t("kpi_pipeline"),type:"number"},{id:"prob",label:t("probability")+" %",type:"number"},
 {id:"owner",label:t("owner_label")},{id:"expclose",label:t("f_expclose"),type:"date"},
 {id:"competitors",label:t("f_competitors"),full:true},{id:"decision",label:t("f_decision"),full:true},
];}
function addOpp(){formModal(t("add_opp"),t("crm_sub"),oppFields(),o=>{const opp={id:uid(),stage:o.stage,name:o.name,val:+o.val||0,prob:+o.prob||STAGE_PROB[o.stage]||0,owner:o.owner||"—",expclose:o.expclose,competitors:o.competitors,decision:o.decision};DATA.pipeline.unshift(opp);if(o.stage==="active")activateOpp(opp);save();logAct("◎","b1",t("add_opp")+": "+o.name);renderShell();renderView();toast(t("created"));});}
function editOpp(id){const p=DATA.pipeline.find(x=>x.id===id);if(!p)return;formModal(t("edit_opp"),t("crm_sub"),oppFields(),o=>{Object.assign(p,{stage:o.stage,name:o.name,val:+o.val||0,prob:+o.prob||0,owner:o.owner||"—",expclose:o.expclose,competitors:o.competitors,decision:o.decision});if(o.stage==="active")activateOpp(p);save();logAct("✎","b2",t("saved")+": "+o.name);renderShell();renderView();toast(t("saved"));},p);}

/* ===== PROJECTS ===== */
function viewProjects(){const ro=isRO("projects");const canManage=["system_admin","ceo"].includes(state.user.role);
 const showArch=state.showArchived;const list=DATA.projects.filter(p=>showArch?p.archived:!p.archived);
 const archCount=DATA.projects.filter(p=>p.archived).length;
 const toggleArch=archCount?'<button class="btn ghost" id="toggleArch">🗂 '+t("show_archived")+(showArch?' ✓':'')+' ('+archCount+')</button>':'';
 const actions=(ro?"":'<button class="btn gold" id="addProj">+ '+t("add_project")+'</button>')+toggleArch;
 if(!list.length){$("#view").innerHTML=headHTML(t("nav_projects")+roBadge("projects"),t("proj_sub"),actions)+'<div class="card">'+emptyState("▤","empty_proj_t","empty_proj_b",ro?"":t("add_project"),"emProj")+'</div>';[["addProj"],["emProj"]].forEach(([id])=>{const e=$("#"+id);if(e)e.addEventListener("click",addProject);});const ta=$("#toggleArch");if(ta)ta.addEventListener("click",()=>{state.showArchived=!state.showArchived;renderView();});return;}
 const rows=list.map(p=>{const mgmt=canManage?(p.archived?'<button class="del-btn" data-restore="'+p.id+'" title="'+t("restore_action")+'">↩</button>':'<button class="del-btn" data-archive="'+p.id+'" title="'+t("archive_action")+'">🗂</button><button class="del-btn" data-transfer="'+p.id+'" title="'+t("transfer_action")+'">⇄</button>'):'';
  return '<tr style="cursor:pointer'+(p.archived?';opacity:.65':'')+'" data-proj="'+p.id+'"><td><div class="pname">'+esc(L(p.name))+(p.archived?' <span class="badge2 bg-mute">'+t("archived_w")+'</span>':'')+'</div>'+(p.fromOpp?'<div style="font-size:11px;color:var(--success)">✓ '+t("linked_proj")+'</div>':'')+'</td><td>'+esc(L(p.client))+'</td><td>'+esc(p.pm||"—")+'</td><td><div class="row gap-s"><div class="progress green"><span style="width:'+(+p.prog||0)+'%"></span></div><b style="font-size:12px">'+(+p.prog||0)+'%</b></div></td><td>'+statusBadge(p.status)+'</td><td style="font-weight:600;color:var(--gold-deep)">'+money(p.val)+'</td><td>'+esc(p.due||"—")+'</td>'+(ro?'':'<td><div class="row gap-s"><button class="del-btn" data-plan="'+p.id+'" title="'+t("year_plan")+'">📅</button>'+editBtn("project",p.id)+mgmt+delBtn("projects",p.id,L(p.name))+'</div></td>')+'</tr>';}).join("");
 $("#view").innerHTML=headHTML(t("nav_projects")+roBadge("projects"),t("proj_sub"),actions)+'<div class="card"><table><thead><tr><th>'+t("col_project")+'</th><th>'+t("col_client")+'</th><th>'+t("col_pm")+'</th><th>'+t("col_progress")+'</th><th>'+t("col_status")+'</th><th>'+t("col_value")+'</th><th>'+t("col_due")+'</th>'+(ro?'':'<th></th>')+'</tr></thead><tbody>'+rows+'</tbody></table></div>';
 const e=$("#addProj");if(e)e.addEventListener("click",addProject);
 const ta=$("#toggleArch");if(ta)ta.addEventListener("click",()=>{state.showArchived=!state.showArchived;renderView();});
 $$("[data-proj]").forEach(r=>r.addEventListener("click",()=>projectModal(r.dataset.proj)));
 $$("[data-archive]").forEach(b=>b.addEventListener("click",e=>{e.stopPropagation();const p=DATA.projects.find(x=>x.id===b.dataset.archive);if(p){p.archived=true;save();logAudit("archive_project",L(p.name));renderShell();renderView();toast(t("project_archived"));}}));
 $$("[data-restore]").forEach(b=>b.addEventListener("click",e=>{e.stopPropagation();const p=DATA.projects.find(x=>x.id===b.dataset.restore);if(p){p.archived=false;save();logAudit("restore_project",L(p.name));renderShell();renderView();toast(t("project_restored"));}}));
 $$("[data-transfer]").forEach(b=>b.addEventListener("click",e=>{e.stopPropagation();transferProject(b.dataset.transfer);}));
 bindDeletes();
}
function transferProject(id){const p=DATA.projects.find(x=>x.id===id);if(!p)return;formModal(t("transfer_action"),L(p.name),[{id:"pm",label:t("f_new_owner"),required:true,full:true,type:"datalist",list:DATA.users.map(u=>u.name)}],o=>{const old=p.pm;p.pm=o.pm;save();logAudit("transfer_project",L(p.name)+": "+(old||"—")+" → "+o.pm);renderShell();renderView();toast(t("transferred"));});}
function projectFields(){return [
 {id:"name",label:t("col_project"),required:true,full:true},
 {id:"client",label:t("col_client"),type:"datalist",list:clientNames()},{id:"pm",label:t("col_pm")},
 {id:"val",label:t("col_value"),type:"number"},{id:"prog",label:t("f_progress"),type:"number"},
 {id:"start",label:t("f_start"),type:"date"},{id:"due",label:t("col_due"),type:"date"},
 {id:"status",label:t("col_status"),type:"select",options:[["ontrack","st_ontrack"],["risk","st_risk"],["delay","st_delay"]].map(([v,k])=>({v,label:t(k)}))},
 {id:"desc",label:t("f_desc"),type:"textarea",full:true},
];}
function addProject(){formModal(t("add_project"),t("proj_sub"),projectFields(),o=>{DATA.projects.unshift({id:uid(),name:o.name,client:o.client,pm:o.pm,val:+o.val||0,prog:+o.prog||0,start:o.start,due:o.due,status:o.status||"ontrack",desc:o.desc,plan:{}});save();logAct("▤","b2",t("add_project")+": "+o.name);renderShell();renderView();toast(t("created"));});}
function editProject(id){const p=DATA.projects.find(x=>x.id===id);if(!p)return;formModal(t("edit_project"),t("proj_sub"),projectFields(),o=>{Object.assign(p,{name:o.name,client:o.client,pm:o.pm,val:+o.val||0,prog:+o.prog||0,start:o.start,due:o.due,status:o.status||"ontrack",desc:o.desc});save();logAct("✎","b2",t("saved")+": "+o.name);renderShell();renderView();toast(t("saved"));},p);}
function monthsList(){return state.lang==="ar"?["يناير","فبراير","مارس","أبريل","مايو","يونيو","يوليو","أغسطس","سبتمبر","أكتوبر","نوفمبر","ديسمبر"]:["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];}
function projectModal(id){const p=DATA.projects.find(x=>x.id===id);if(!p)return;const canPlan=!isRO("projects");const mn=monthsList();p.plan=p.plan||{};
 const grid=mn.map((nm,m)=>{const e=p.plan[m];const col=e?(e.status==="delay"?"var(--danger)":e.status==="risk"?"var(--warn)":"var(--success)"):"var(--line)";return '<div class="pm-cell'+(e?' filled':'')+(canPlan?' clickable':'')+'" '+(canPlan?'data-month="'+m+'"':'')+'><div class="pm-mn">'+nm+'</div>'+(e?'<div class="pm-prog"><span style="width:'+(e.prog||0)+'%;background:'+col+'"></span></div><div class="pm-val">'+(e.prog||0)+'%</div>'+(e.note?'<div class="pm-note">'+esc(e.note)+'</div>':'')+((e.files&&e.files.length)?'<div class="pm-files">📎 '+e.files.length+'</div>':'')+(e.by?'<div class="pm-by">'+esc(e.by)+'</div>':''):'<div class="pm-empty">'+(canPlan?'+':'—')+'</div>')+'</div>';}).join("");
 openModal('<h2>'+esc(L(p.name))+'</h2><p class="msub">'+esc(L(p.client)||"—")+' · '+esc(p.pm||"—")+'</p>'+(p.desc?'<p style="font-size:13.5px;color:var(--ink-2);margin-bottom:16px">'+esc(p.desc)+'</p>':'')+'<div class="grid cols-2" style="gap:12px;margin-bottom:18px"><div class="card" style="padding:14px"><div style="font-size:12px;color:var(--muted)">'+t("col_value")+'</div><div style="font-family:Sora;font-weight:700;color:var(--gold-deep);font-size:18px">'+money(p.val)+'</div></div><div class="card" style="padding:14px"><div style="font-size:12px;color:var(--muted)">'+t("col_progress")+'</div><div style="font-family:Sora;font-weight:700;font-size:18px">'+(+p.prog||0)+'%</div></div></div><div class="row" style="justify-content:space-between;margin-bottom:12px"><h3 style="font-family:Sora;font-size:14px;color:var(--navy-800)">📅 '+t("year_plan")+'</h3>'+(canPlan?'<span class="dnd-hint">'+t("plan_hint")+'</span>':'')+'</div><div class="pm-grid">'+grid+'</div><button class="btn ghost" style="width:100%;margin-top:18px" onclick="closeModal()">'+t("cancel")+'</button>');
 if(canPlan)$$("[data-month]").forEach(c=>c.addEventListener("click",()=>monthEntryForm(p.id,+c.dataset.month)));
}
function monthEntryForm(id,m){const p=DATA.projects.find(x=>x.id===id);if(!p)return;const mn=monthsList();const ex=(p.plan&&p.plan[m])||null;formModal(mn[m]+" — "+L(p.name),t("month_entry_sub"),[
 {id:"progress",label:t("f_progress"),type:"number"},
 {id:"status",label:t("col_status"),type:"select",options:[["ontrack","st_ontrack"],["risk","st_risk"],["delay","st_delay"]].map(([v,k])=>({v,label:t(k)}))},
 {id:"note",label:t("f_month_note"),type:"textarea",full:true},
 {id:"files",label:t("f_support_docs"),type:"file",full:true},
],o=>{p.plan=p.plan||{};p.plan[m]={prog:+o.progress||0,status:o.status||"ontrack",note:o.note,files:o.files||[],by:state.user.name.split(" ")[0],date:today()};const filled=Object.keys(p.plan).map(Number).sort((a,b)=>a-b);const last=filled[filled.length-1];if(last!=null){p.prog=p.plan[last].prog;p.status=p.plan[last].status;}save();logAct("📅","b2",t("month_saved")+": "+L(p.name)+" — "+mn[m]);renderShell();renderView();toast(t("month_saved"));projectModal(id);},ex?{progress:ex.prog,status:ex.status,note:ex.note,files:ex.files}:null);}

/* ===== OPERATIONS ===== */
let opsMode="daily";
function viewOperations(){const ro=isRO("operations");
 $("#view").innerHTML=headHTML(t("nav_operations")+roBadge("operations"),t("ops_sub"),'<div class="seg" id="opsSeg"><button class="active" data-ops="daily">'+t("ops_daily")+'</button><button data-ops="monthly">'+t("ops_monthly")+'</button><button data-ops="annual">'+t("ops_annual")+'</button></div>'+(ro?"":'<button class="btn gold" id="addRep">+ '+t("add_report")+'</button>'))+'<div id="opsBody"></div>';
 $$("[data-ops]").forEach(b=>b.addEventListener("click",()=>{$$("[data-ops]").forEach(x=>x.classList.remove("active"));b.classList.add("active");opsMode=b.dataset.ops;opsBody();}));
 const e=$("#addRep");if(e)e.addEventListener("click",addReport);opsBody();}
function opsBody(){const ro=isRO("operations");const reps=DATA.reports.filter(r=>r.period===opsMode);
 const kpis='<div class="grid cols-4" style="margin-bottom:18px"><div class="card kpi"><div class="val">'+DATA.reports.length+'</div><div class="lbl">'+t("ops_field")+'</div></div><div class="card kpi"><div class="val">'+DATA.projects.filter(p=>p.status==="ontrack").length+'</div><div class="lbl">'+t("st_ontrack")+'</div></div><div class="card kpi"><div class="val" style="color:var(--danger)">'+DATA.projects.filter(p=>p.status!=="ontrack").length+'</div><div class="lbl">'+t("kpi_risk")+'</div></div><div class="card kpi"><div class="val">'+DATA.team.length+'</div><div class="lbl">'+t("team_perf")+'</div></div></div>';
 const list=reps.length?reps.map(r=>'<div class="list-row"><div class="l-ic ic b2">▦</div><div class="grow"><div class="l-t">'+esc(r.team||"—")+(r.project?' · '+esc(r.project):'')+'</div><div class="l-s">'+esc(r.text||"")+'</div>'+attachChips(r.files)+'</div>'+statusBadge(r.status||"ontrack")+(ro?'':' '+editBtn("report",r.id)+delBtn("reports",r.id,r.team||""))+'</div>').join(""):emptyState("⚙","empty_rep_t","empty_rep_b",ro?"":t("add_report"),"emRep");
 $("#opsBody").innerHTML=kpis+'<div class="grid cols-2"><div class="card"><div class="card-h"><h3>'+t("ops_field")+' — '+t("ops_"+opsMode)+'</h3></div>'+list+'</div><div class="card"><div class="card-h"><h3>'+t("team_perf")+'</h3></div><div style="height:260px"><canvas id="cOps"></canvas></div></div></div>';
 const er=$("#emRep");if(er)er.addEventListener("click",addReport);
 bindDeletes();
 if(charts.ops){try{charts.ops.destroy();}catch(e){}}
 if(!DATA.team.length){chartEmpty("cOps","empty_team_b");}else{const ctx=$("#cOps");charts.ops=new Chart(ctx,{type:"radar",data:{labels:DATA.team.map(x=>L(x.name)),datasets:[{label:t("team_perf"),data:DATA.team.map(x=>+x.score||0),backgroundColor:"rgba(212,175,55,.18)",borderColor:"#D4AF37",pointBackgroundColor:"#16304F",borderWidth:2}]},options:{maintainAspectRatio:false,responsive:true,plugins:{legend:{display:false}},scales:{r:{beginAtZero:true,max:100,ticks:{display:false},grid:{color:"#EEF2F8"},pointLabels:{font:cFont(),color:"#3C4E68"}}}}});}
}
function reportFields(){return [
 {id:"team",label:t("f_team"),required:true},
 {id:"project",label:t("col_project"),type:"datalist",list:projectNames()},
 {id:"period",label:t("f_period"),type:"select",required:true,options:[["daily","ops_daily"],["monthly","ops_monthly"],["annual","ops_annual"]].map(([v,k])=>({v,label:t(k)}))},
 {id:"status",label:t("col_status"),type:"select",options:[["ontrack","st_ontrack"],["risk","st_risk"],["delay","st_delay"]].map(([v,k])=>({v,label:t(k)}))},
 {id:"text",label:t("f_report_txt"),type:"textarea",full:true,required:true},
 {id:"files",label:t("f_support_docs"),type:"file",full:true},
];}
function addReport(){formModal(t("add_report"),t("ops_sub"),reportFields(),o=>{DATA.reports.unshift({id:uid(),team:o.team,project:o.project,period:o.period,status:o.status||"ontrack",text:o.text,files:o.files||[],date:today()});save();logAct("⚙","b2",t("add_report")+": "+o.team);opsMode=o.period;$$("[data-ops]").forEach(x=>x.classList.toggle("active",x.dataset.ops===o.period));opsBody();toast(t("created"));});}
function editReport(id){const r=DATA.reports.find(x=>x.id===id);if(!r)return;formModal(t("edit_report"),t("ops_sub"),reportFields(),o=>{Object.assign(r,{team:o.team,project:o.project,period:o.period,status:o.status||"ontrack",text:o.text,files:o.files||[]});save();logAct("✎","b2",t("saved")+": "+o.team);opsMode=o.period;$$("[data-ops]").forEach(x=>x.classList.toggle("active",x.dataset.ops===o.period));opsBody();toast(t("saved"));},r);}

/* ===== FINANCIAL ===== */
function viewFinancial(){const ro=isRO("financial");
 const actions=ro?"":'<button class="btn gold" id="addInv">+ '+t("add_invoice")+'</button>';
 if(!DATA.invoices.length){$("#view").innerHTML=headHTML(t("nav_financial")+roBadge("financial"),t("fin_sub"),actions)+'<div class="card">'+emptyState("₪","empty_inv_t","empty_inv_b",ro?"":t("add_invoice"),"emInv")+'</div>';[["addInv"],["emInv"]].forEach(([id])=>{const e=$("#"+id);if(e)e.addEventListener("click",addInvoice);});return;}
 const issued=DATA.invoices.reduce((a,i)=>a+(+i.amt||0),0);const collected=DATA.invoices.filter(i=>i.status==="collected").reduce((a,i)=>a+(+i.amt||0),0);const pending=issued-collected;
 const rows=DATA.invoices.map(i=>{const m={collected:["bg-success","fin_collected"],pending:["bg-warn","fin_pending"],issued:["bg-info","fin_issued"]};const x=m[i.status]||m.issued;return '<tr><td class="pname">'+esc(i.no)+'</td><td>'+esc(L(i.client)||"—")+'</td><td style="font-weight:600;color:var(--gold-deep)">'+money(i.amt)+'</td><td>'+esc(i.date||"—")+'</td><td><span class="badge2 '+x[0]+'">'+t(x[1])+'</span></td>'+(ro?'':'<td><div class="row gap-s">'+editBtn("invoice",i.id)+delBtn("invoices",i.id,i.no)+'</div></td>')+'</tr>';}).join("");
 $("#view").innerHTML=headHTML(t("nav_financial")+roBadge("financial"),t("fin_sub"),actions)+
  '<div class="grid cols-3" style="margin-bottom:18px"><div class="card kpi"><div class="top"><div><div class="val">'+money(issued)+'</div><div class="lbl">'+t("fin_issued")+'</div></div><div class="ic b2">▦</div></div></div><div class="card kpi"><div class="top"><div><div class="val" style="color:var(--success)">'+money(collected)+'</div><div class="lbl">'+t("fin_collected")+'</div></div><div class="ic b3">✓</div></div></div><div class="card kpi"><div class="top"><div><div class="val" style="color:var(--warn)">'+money(pending)+'</div><div class="lbl">'+t("fin_pending")+'</div></div><div class="ic b5">◷</div></div></div></div>'+
  '<div class="grid cols-3"><div class="card" style="grid-column:span 2"><div class="card-h"><h3>'+t("fin_invoices")+'</h3></div><table><thead><tr><th>'+t("col_invoice")+'</th><th>'+t("col_client")+'</th><th>'+t("col_amount")+'</th><th>'+t("col_date")+'</th><th>'+t("col_status")+'</th>'+(ro?'':'<th></th>')+'</tr></thead><tbody>'+rows+'</tbody></table></div><div class="card"><div class="card-h"><h3>'+t("cashflow")+'</h3></div><div style="height:300px"><canvas id="cFlow"></canvas></div></div></div>';
 const e=$("#addInv");if(e)e.addEventListener("click",addInvoice);
 bindDeletes();
 const map={};DATA.invoices.filter(i=>i.status==="collected").forEach(i=>{const m=(i.date||today()).slice(0,7);map[m]=(map[m]||0)+(+i.amt||0);});const labels=Object.keys(map).sort();if(labels.length){const ctx=$("#cFlow");charts.flow=new Chart(ctx,{type:"line",data:{labels,datasets:[{label:t("cashflow"),data:labels.map(l=>map[l]/1000),fill:true,backgroundColor:"rgba(46,158,107,.12)",borderColor:"#2E9E6B",tension:.4,pointBackgroundColor:"#2E9E6B",borderWidth:2.5}]},options:gridOpts()});}else chartEmpty("cFlow","empty_inv_b");
}
function invoiceFields(def){def=def||{};return [
 {id:"no",label:t("f_invoice_no"),required:true,value:def.no},
 {id:"client",label:t("col_client"),type:"datalist",list:clientNames()},
 {id:"project",label:t("col_project"),type:"datalist",list:projectNames()},
 {id:"amt",label:t("f_amount"),type:"number",required:true},
 {id:"date",label:t("col_date"),type:"date",value:def.date},
 {id:"status",label:t("col_status"),type:"select",required:true,options:[["issued","fin_issued"],["pending","fin_pending"],["collected","fin_collected"]].map(([v,k])=>({v,label:t(k)}))},
];}
function addInvoice(){const n="INV-"+String(2000+DATA.invoices.length+1);formModal(t("add_invoice"),t("fin_sub"),invoiceFields({no:n,date:today()}),o=>{DATA.invoices.unshift({id:uid(),no:o.no,client:o.client,project:o.project,amt:+o.amt||0,date:o.date||today(),status:o.status||"issued"});save();logAct("₪","b3",t("add_invoice")+": "+o.no);renderShell();renderView();toast(t("created"));});}
function editInvoice(id){const r=DATA.invoices.find(x=>x.id===id);if(!r)return;formModal(t("edit_invoice"),t("fin_sub"),invoiceFields(),o=>{Object.assign(r,{no:o.no,client:o.client,project:o.project,amt:+o.amt||0,date:o.date||today(),status:o.status||"issued"});save();logAct("✎","b2",t("saved")+": "+o.no);renderShell();renderView();toast(t("saved"));},r);}

/* ===== REPORTS ===== */
function viewReports(){const reps=[["rep_fin","b1","▦"],["rep_ops","b2","⚙"],["rep_exec","b4","★"],["rep_perf","b3","◎"]];const cards=reps.map(([k,b,ic])=>'<div class="card"><div class="row gap-m" style="margin-bottom:14px"><div class="ic '+b+'" style="width:48px;height:48px;border-radius:14px;font-size:22px">'+ic+'</div><div><h3 style="font-family:Sora;font-size:15px;color:var(--navy-800)">'+t(k)+'</h3><p style="font-size:12px;color:var(--muted);margin-top:2px">'+t("rep_gen")+'</p></div></div><div class="row gap-s"><button class="btn ghost grow" data-rep="'+t(k)+'|PDF">📄 '+t("export_pdf")+'</button><button class="btn ghost grow" data-rep="'+t(k)+'|XLS">📊 '+t("export_xls")+'</button><button class="btn dark" data-rep="'+t(k)+'|SCH">⏱ '+t("schedule")+'</button></div></div>').join("");$("#view").innerHTML=headHTML(t("nav_reports")+roBadge("reports"),t("rep_sub"))+'<div class="grid cols-2">'+cards+'</div>';$$("[data-rep]").forEach(b=>b.addEventListener("click",()=>{const[n,mode]=b.dataset.rep.split("|");toast(t("report_gen")+" — "+n+" ("+mode+")");}));}

/* ===== AI ===== */
function viewAI(){const engines=[["ai_delay","b5"],["ai_risk","b4"],["ai_score","b3"],["ai_reco","b1"]].map(([k,b])=>'<div class="card kpi"><div class="ic '+b+'" style="width:42px;height:42px;border-radius:12px;font-size:19px;margin-bottom:12px">✦</div><div style="font-weight:600;color:var(--navy-800)">'+t(k)+'</div><div style="font-size:11.5px;color:var(--success);margin-top:6px">● '+(state.lang==="ar"?"مفعّل":"Active")+'</div></div>').join("");
 const ins=buildInsights();const cards=ins.length?ins.map(a=>'<div class="card" style="border-inline-start:4px solid var(--gold)"><div class="row gap-m" style="margin-bottom:10px"><div class="ic '+a.ic+'" style="width:46px;height:46px;border-radius:13px;font-size:20px">'+a.glyph+'</div><div><div style="font-size:11.5px;letter-spacing:.04em;color:var(--muted);text-transform:uppercase">'+t(a.cat)+'</div><h3 style="font-family:Sora;font-size:15px;color:var(--navy-800)">'+esc(a.h)+'</h3></div></div><p style="font-size:13.5px;color:var(--ink-2);line-height:1.6">'+esc(a.b)+'</p></div>').join(""):'<div class="card" style="grid-column:1/-1">'+emptyState("✦","empty_ai_t","empty_ai_b")+'</div>';
 $("#view").innerHTML=headHTML(t("nav_ai"),t("ai_sub"))+'<div class="grid cols-4" style="margin-bottom:18px">'+engines+'</div><div class="grid cols-2">'+cards+'</div>';}

/* ===== NOTIFICATIONS ===== */
function viewNotifications(){const alerts=computeAlerts();const list=alerts.length?alerts.map(n=>'<div class="list-row"><div class="l-ic ic '+n.cls+'">'+n.ic+'</div><div class="grow"><div class="l-t">'+esc(n.text)+'</div></div><span class="badge2 bg-mute">'+t("new_w")+'</span></div>').join(""):emptyState("🔔","empty_notif_t","empty_notif_b");$("#view").innerHTML=headHTML(t("nav_notifications"),t("notif_sub"))+'<div class="card">'+list+'</div>';}

/* ===== NOTES ===== */
let noteCat="risk";
function viewNotes(){const ro=isRO("notes");const canApprove=["system_admin","ceo","board","pm","reviewer"].includes(state.user.role);
 const composer=ro?"":'<div class="card" style="margin-bottom:18px"><div class="card-h"><h3>'+t("add_note")+'</h3></div><div style="display:flex;flex-direction:column;gap:10px"><textarea id="noteTxt" placeholder="'+t("note_ph")+'" style="width:100%;border:1.5px solid var(--line);border-radius:12px;padding:13px;resize:vertical;min-height:80px;font-size:14px"></textarea><input id="noteProj" list="dlNoteProj" placeholder="'+t("col_project")+' ('+t("f_link_project")+')" style="border:1.5px solid var(--line);border-radius:11px;padding:11px 13px"><datalist id="dlNoteProj">'+projectNames().map(p=>'<option value="'+esc(p)+'">').join("")+'</datalist><label style="font-size:12.5px;color:var(--ink-2);font-weight:600">'+t("f_support_docs")+'</label><input type="file" multiple id="noteFiles" style="border:1.5px solid var(--line);border-radius:11px;padding:9px 12px;background:var(--surface-3)"><div class="chip-row" id="catRow"><button class="chip active" data-cat="risk">⚠ '+t("cat_risk")+'</button><button class="chip" data-cat="issue">● '+t("cat_issue")+'</button><button class="chip" data-cat="sug">✦ '+t("cat_sug")+'</button></div><button class="btn gold" id="saveNote" style="align-self:flex-start">'+t("add_note")+'</button></div></div>';
 const cats={risk:["bg-danger","cat_risk"],issue:["bg-warn","cat_issue"],sug:["bg-info","cat_sug"]};
 const notesHTML=DATA.notes.length?DATA.notes.map((n,i)=>{const stMap={pending:["bg-mute","pending_w"],approved:["bg-success","approved"],rejected:["bg-danger","rejected"]};const x=cats[n.cat]||cats.risk;const st=stMap[n.status]||stMap.pending;const appr=(canApprove&&n.status==="pending")?'<button class="btn gold" style="padding:7px 14px;font-size:12.5px" data-note="'+i+'|approve">'+t("approve")+'</button><button class="btn ghost" style="padding:7px 14px;font-size:12.5px" data-note="'+i+'|reject">'+t("reject")+'</button>':"";const acts=ro?'':editBtn("note",n.id)+delBtn("notes",n.id,L(n.txt).slice(0,30));const footer=(appr||acts)?'<div class="row gap-s" style="margin-top:10px;justify-content:space-between"><div class="row gap-s">'+appr+'</div><div class="row gap-s">'+acts+'</div></div>':'';return '<div class="card" style="margin-bottom:12px"><div class="row gap-s" style="justify-content:space-between"><span class="badge2 '+x[0]+'">'+t(x[1])+'</span><span class="badge2 '+st[0]+'">'+t(st[1])+'</span></div><p style="margin:12px 0 4px;color:var(--ink)">'+esc(L(n.txt))+'</p>'+attachChips(n.files)+'<div style="font-size:12px;color:var(--muted);margin-top:6px">'+t("owner_label")+': '+esc(n.by)+(n.project?' · '+esc(n.project):'')+'</div>'+footer+'</div>';}).join(""):'<div class="card">'+emptyState("✎","empty_notes_t","empty_notes_b")+'</div>';
 $("#view").innerHTML=headHTML(t("nav_notes"),t("notes_sub"))+composer+'<div>'+notesHTML+'</div>';
 if(!ro){$$("#catRow .chip").forEach(c=>c.addEventListener("click",()=>{$$("#catRow .chip").forEach(x=>x.classList.remove("active"));c.classList.add("active");noteCat=c.dataset.cat;}));$("#saveNote").addEventListener("click",async()=>{const v=$("#noteTxt").value.trim();if(!v){toast(t("required_err"));return;}const inp=$("#noteFiles");let files=[];if(inp.files&&inp.files.length)files=await readFiles(inp);DATA.notes.unshift({id:uid(),cat:noteCat,txt:{ar:v,en:v},project:$("#noteProj").value.trim(),files,by:state.user.name.split(" ")[0],status:"pending"});save();logAct("✎","b2",t("add_note"));renderShell();renderView();toast(t("created"));});}
 $$("[data-note]").forEach(b=>b.addEventListener("click",()=>{const[i,act]=b.dataset.note.split("|");DATA.notes[+i].status=act==="approve"?"approved":"rejected";save();renderShell();renderView();toast(act==="approve"?t("approved"):t("rejected"));}));
 bindDeletes();
}
function editNote(id){const n=DATA.notes.find(x=>x.id===id);if(!n)return;formModal(t("edit_note"),t("notes_sub"),[
 {id:"txt",label:t("add_note"),type:"textarea",full:true,required:true},
 {id:"cat",label:t("cat_risk")+"/"+t("cat_issue")+"/"+t("cat_sug"),type:"select",options:[["risk","cat_risk"],["issue","cat_issue"],["sug","cat_sug"]].map(([v,k])=>({v,label:t(k)}))},
 {id:"project",label:t("col_project"),type:"datalist",list:projectNames()},
 {id:"files",label:t("f_support_docs"),type:"file",full:true},
],o=>{Object.assign(n,{txt:{ar:o.txt,en:o.txt},cat:o.cat||n.cat,project:o.project,files:o.files||[]});save();logAct("✎","b2",t("saved"));renderShell();renderView();toast(t("saved"));},{txt:L(n.txt),cat:n.cat,project:n.project,files:n.files});}

/* ===== ARCHIVE ===== */
function viewArchive(){const actions='<button class="btn gold" id="addDoc">+ '+t("add_doc")+'</button>';
 if(!DATA.archive.length){$("#view").innerHTML=headHTML(t("nav_archive"),t("arch_sub"),actions)+'<div class="card">'+emptyState("🗂","empty_arch_t","empty_arch_b",t("add_doc"),"emDoc")+'</div>';[["addDoc"],["emDoc"]].forEach(([id])=>{const e=$("#"+id);if(e)e.addEventListener("click",addDoc);});return;}
 const rows=DATA.archive.map(d=>{const f0=(d.files&&d.files[0])||null;const dl=(f0&&f0.data)?'<a class="btn ghost" style="padding:6px 12px;font-size:12px" href="'+f0.data+'" download="'+esc(f0.name)+'">↓ '+t("download")+'</a>':'<button class="btn ghost" style="padding:6px 12px;font-size:12px" onclick="window.velionToast(\''+t("downloading")+'\')">↓ '+t("download")+'</button>';return '<tr><td><div class="row gap-s"><span class="ic '+(d.type==="PDF"?"b5":"b2")+'" style="width:34px;height:34px;border-radius:9px;font-size:12px;font-weight:700">'+esc(d.type||"DOC")+'</span><span class="pname">'+esc(d.doc)+'</span></div></td><td>'+esc(d.type||"—")+'</td><td>'+esc(d.project||"—")+'</td><td>'+esc(d.date||"—")+'</td><td><div class="row gap-s">'+dl+editBtn("doc",d.id)+delBtn("archive",d.id,d.doc)+'</div></td></tr>';}).join("");
 $("#view").innerHTML=headHTML(t("nav_archive"),t("arch_sub"),actions)+'<div class="card"><table><thead><tr><th>'+t("col_doc")+'</th><th>'+t("col_type")+'</th><th>'+t("col_project2")+'</th><th>'+t("col_date")+'</th><th></th></tr></thead><tbody>'+rows+'</tbody></table></div>';
 const e=$("#addDoc");if(e)e.addEventListener("click",addDoc);bindDeletes();}
function docFields(){return [
 {id:"doc",label:t("col_doc"),required:true,full:true},
 {id:"project",label:t("col_project"),type:"datalist",list:projectNames()},
 {id:"type",label:t("f_filetype"),type:"select",options:["PDF","DOCX","XLSX","PNG","JPG","ZIP"].map(v=>({v,label:v}))},
 {id:"files",label:t("f_support_docs"),type:"file",full:true},
];}
function addDoc(){formModal(t("add_doc"),t("arch_sub"),docFields(),o=>{const f0=(o.files&&o.files[0])||null;DATA.archive.unshift({id:uid(),doc:o.doc,type:o.type||(f0?f0.type:"DOC"),project:o.project,files:o.files||[],date:today()});save();logAct("🗂","b2",t("add_doc")+": "+o.doc);renderView();toast(t("created"));});}
function editDoc(id){const d=DATA.archive.find(x=>x.id===id);if(!d)return;formModal(t("edit_doc"),t("arch_sub"),docFields(),o=>{const f0=(o.files&&o.files[0])||null;Object.assign(d,{doc:o.doc,type:o.type||(f0?f0.type:d.type),project:o.project,files:o.files||[]});save();logAct("✎","b2",t("saved")+": "+o.doc);renderView();toast(t("saved"));},d);}

/* ===== USERS ===== */
function viewUsers(){
 const rows=DATA.users.map(u=>{const self=u.email.toLowerCase()===state.user.email.toLowerCase();const susp=u.status==="suspended";
  const stBadge=susp?'<span class="badge2 bg-danger">'+t("st_suspended")+'</span>':'<span class="badge2 bg-success">'+t("st_active_acc")+'</span>';
  const acts='<div class="row gap-s">'+editBtn("user",u.id)
   +'<button class="del-btn" data-pwd="'+u.id+'" title="'+t("reset_pwd")+'">🔑</button>'
   +(self?'':'<button class="del-btn" data-toggle="'+u.id+'" title="'+(susp?t("activate"):t("suspend"))+'">'+(susp?'▶':'⏸')+'</button>')
   +(self?'<span class="badge2 bg-mute">'+(state.lang==="ar"?"أنت":"You")+'</span>':delBtn("users",u.id,u.name))+'</div>';
  const projs=(u.projects&&u.projects.length)?u.projects.length+' '+t("proj_w"):'—';
  return '<tr'+(susp?' style="opacity:.6"':'')+'><td><div class="row gap-s"><div class="avatar" style="width:34px;height:34px;border-radius:10px;font-size:13px">'+esc(u.name.charAt(0))+'</div><div><div class="pname">'+esc(u.name)+'</div><div style="font-size:11.5px;color:var(--muted)">'+esc(u.email||u.username||"—")+(u.dept?' · '+esc(u.dept):'')+'</div></div></div></td><td><span class="badge2 bg-gold">'+ROLES[u.role][state.lang]+'</span></td><td>'+stBadge+'</td><td><span style="font-size:12px;color:var(--muted)">'+projs+' · '+PERMS[u.role].length+' '+t("modules_w")+'</span></td><td>'+acts+'</td></tr>';}).join("");
 $("#view").innerHTML=headHTML(t("nav_users"),t("users_sub"),'<button class="btn gold" id="addUser">+ '+t("add_user")+'</button>')+
  '<div class="card" style="margin-bottom:16px;border-inline-start:4px solid var(--warn);background:rgba(224,169,59,.06)"><div style="font-size:12.5px;color:#8a6a1e">⚠ '+t("sec_note")+'</div></div>'+
  '<div class="card"><table><thead><tr><th>'+t("col_user")+'</th><th>'+t("col_role")+'</th><th>'+t("col_status")+'</th><th>'+t("col_access")+'</th><th></th></tr></thead><tbody>'+rows+'</tbody></table></div>';
 $("#addUser").addEventListener("click",()=>userForm());
 $$("[data-pwd]").forEach(b=>b.addEventListener("click",()=>resetPwd(b.dataset.pwd)));
 $$("[data-toggle]").forEach(b=>b.addEventListener("click",()=>toggleUser(b.dataset.toggle)));
 bindDeletes();
}
function userFields(edit){return [
 {id:"name",label:t("f_name"),required:true,full:true},
 {id:"email",label:t("f_userid"),type:"text",required:true},{id:"dept",label:t("f_dept")},
 {id:"role",label:t("f_role"),type:"select",required:true,options:Object.keys(ROLES).map(k=>({v:k,label:ROLES[k][state.lang]}))},
 {id:"projects",label:t("f_linked_projects"),type:"datalist",list:projectNames(),full:true,ph:t("comma_sep")},
 {id:"pass",label:edit?t("f_pass_optional"):t("f_pass"),type:"password",required:!edit},
 {id:"pass2",label:t("f_pass2"),type:"password",required:!edit},
];}
function userForm(){formModal(t("add_user"),t("user_form_sub"),userFields(false),o=>{
 if(o.pass!==o.pass2){toast(t("err_passmatch"));return;}
 if(DATA.users.some(x=>(x.email||"").toLowerCase()===o.email.toLowerCase())){toast(t("err_dupuser"));return;}
 DATA.users.unshift({id:uid(),name:o.name,email:o.email,username:o.email,dept:o.dept,role:o.role,pass:o.pass,status:"active",projects:o.projects?o.projects.split(",").map(s=>s.trim()).filter(Boolean):[],created:today()});
 save();logAudit("create_user",o.name);renderView();toast(t("created"));});}
function editUser(id){const u=DATA.users.find(x=>x.id===id);if(!u)return;formModal(t("edit_user"),t("user_form_sub"),userFields(true),o=>{
 if(o.pass&&o.pass!==o.pass2){toast(t("err_passmatch"));return;}
 const oldRole=u.role;Object.assign(u,{name:o.name,email:o.email,username:o.email,dept:o.dept,role:o.role,projects:o.projects?o.projects.split(",").map(s=>s.trim()).filter(Boolean):[]});if(o.pass)u.pass=o.pass;
 if(u.email.toLowerCase()===state.user.email.toLowerCase()){state.user.name=o.name;state.user.role=o.role;}
 save();logAudit("edit_user",o.name+(oldRole!==o.role?" ("+t("col_role")+": "+ROLES[o.role][state.lang]+")":""));renderShell();renderView();toast(t("saved"));},{name:u.name,email:u.email,dept:u.dept,role:u.role,projects:(u.projects||[]).join(", ")});}
function resetPwd(id){const u=DATA.users.find(x=>x.id===id);if(!u)return;formModal(t("reset_pwd"),u.name,[{id:"pass",label:t("f_pass"),type:"password",required:true,full:true},{id:"pass2",label:t("f_pass2"),type:"password",required:true,full:true}],o=>{if(o.pass!==o.pass2){toast(t("err_passmatch"));return;}u.pass=o.pass;save();logAudit("reset_password",u.name);toast(t("pwd_reset_done"));});}
function toggleUser(id){const u=DATA.users.find(x=>x.id===id);if(!u)return;u.status=u.status==="suspended"?"active":"suspended";save();logAudit(u.status==="suspended"?"suspend_user":"activate_user",u.name);renderView();toast(u.status==="suspended"?t("user_suspended"):t("user_activated"));}

/* ===== AUDIT TRAIL ===== */
function viewAudit(){
 const rows=DATA.audit.length?DATA.audit.map(a=>'<tr><td style="white-space:nowrap;font-size:12px;color:var(--muted)">'+new Date(a.ts).toLocaleString(state.lang==="ar"?"ar":"en")+'</td><td class="pname">'+esc(a.actor)+'</td><td><span class="badge2 bg-mute">'+(ROLES[a.role]?ROLES[a.role][state.lang]:esc(a.role))+'</span></td><td>'+esc(t("audit_"+a.action)||a.action)+'</td><td>'+esc(a.target||"—")+'</td></tr>').join(""):'';
 const clear=DATA.audit.length?'<button class="btn ghost" id="clrAudit">🗑 '+t("clear_audit")+'</button>':'';
 $("#view").innerHTML=headHTML(t("nav_audit"),t("audit_sub"),clear)+(DATA.audit.length?'<div class="card"><table><thead><tr><th>'+t("col_time")+'</th><th>'+t("col_actor")+'</th><th>'+t("col_role")+'</th><th>'+t("col_action")+'</th><th>'+t("col_target")+'</th></tr></thead><tbody>'+rows+'</tbody></table></div>':'<div class="card">'+emptyState("🛡","empty_audit_t","empty_audit_b")+'</div>');
 const c=$("#clrAudit");if(c)c.addEventListener("click",()=>{DATA.audit=[];save();renderView();toast(t("done"));});
}

/* ===== SETTINGS ===== */
function viewSettings(){const canTeam=can("operations")||can("dashboard");
 $("#view").innerHTML=headHTML(t("nav_settings"),t("set_sub"))+
 '<div class="grid cols-2"><div class="card"><div class="card-h"><h3>'+t("set_profile")+'</h3></div><div class="field"><label>'+t("f_name")+'</label><input value="'+esc(state.user.name)+'" id="s_name"></div><div class="field"><label>'+t("f_email")+'</label><input value="'+esc(state.user.email)+'" id="s_email"></div><div class="field"><label>'+t("f_role")+'</label><input value="'+ROLES[state.user.role][state.lang]+'" disabled style="background:var(--surface-3)"></div><button class="btn gold" id="saveProfile">'+t("save")+'</button></div>'+
 '<div class="card"><div class="card-h"><h3>'+t("set_lang")+'</h3></div><div class="seg" style="margin-bottom:22px"><button class="'+(state.lang==="ar"?"active":"")+'" data-setlang="ar">عربي</button><button class="'+(state.lang==="en"?"active":"")+'" data-setlang="en">English</button></div>'+
 '<div class="card-h"><h3>'+t("team_perf")+'</h3>'+(canTeam?'<span class="more" id="addTeam">+ '+t("add_team")+'</span>':'')+'</div>'+(DATA.team.length?DATA.team.map(x=>'<div class="list-row"><div class="l-ic ic b1">◎</div><div class="grow"><div class="l-t">'+esc(L(x.name))+'</div></div><b style="color:var(--gold-deep)">'+x.score+'%</b>'+editBtn("team",x.id)+delBtn("team",x.id,L(x.name))+'</div>').join(""):'<p style="font-size:13px;color:var(--muted);padding:8px 0">'+t("empty_team_b")+'</p>')+
 '<div class="card-h" style="margin-top:18px"><h3>'+(state.lang==="ar"?"الأمان":"Security")+'</h3></div><div class="list-row"><div class="l-ic ic b3">🔐</div><div class="grow"><div class="l-t">'+(state.lang==="ar"?"التحكم بالوصول حسب الدور":"Role-based access control")+'</div><div class="l-s">'+(state.lang==="ar"?"مفعّل":"Enabled")+'</div></div><span class="badge2 bg-success">●</span></div><div class="list-row"><div class="l-ic ic b2">🗄</div><div class="grow"><div class="l-t">'+(state.lang==="ar"?"حفظ تلقائي للبيانات":"Auto data persistence")+'</div><div class="l-s">'+(Store.available?(state.lang==="ar"?"مفعّل على هذا الجهاز":"Enabled on this device"):(state.lang==="ar"?"في الجلسة فقط":"Session only"))+'</div></div><span class="badge2 '+(Store.available?"bg-success":"bg-warn")+'">●</span></div></div></div>';
 $("#saveProfile").addEventListener("click",()=>{state.user.name=$("#s_name").value;state.user.email=$("#s_email").value;renderShell();toast(t("saved"));});
 $$("#view [data-setlang]").forEach(b=>b.addEventListener("click",()=>setLang(b.dataset.setlang)));
 const at=$("#addTeam");if(at)at.addEventListener("click",()=>formModal(t("add_team"),t("team_perf"),[{id:"name",label:t("f_team"),required:true},{id:"score",label:t("f_score"),type:"number",required:true,attr:'min="0" max="100"'}],o=>{DATA.team.unshift({id:uid(),name:o.name,score:Math.min(100,+o.score||0)});save();renderView();toast(t("created"));}));bindDeletes();}
function editTeam(id){const x=DATA.team.find(r=>r.id===id);if(!x)return;formModal(t("edit_team"),t("team_perf"),[{id:"name",label:t("f_team"),required:true},{id:"score",label:t("f_score"),type:"number",required:true}],o=>{Object.assign(x,{name:o.name,score:Math.min(100,+o.score||0)});save();renderView();toast(t("saved"));},{name:L(x.name),score:x.score});}
const EDITORS={client:editClient,opp:editOpp,project:editProject,invoice:editInvoice,report:editReport,doc:editDoc,user:editUser,team:editTeam,note:editNote};

/* ===== init ===== */
I18N.ar.f_link_project="ربط بمشروع";I18N.en.f_link_project="link to project";
Object.assign(I18N.ar,{edit:"تعديل",edit_client:"تعديل بيانات العميل",edit_opp:"تعديل الفرصة",edit_project:"تعديل المشروع",edit_invoice:"تعديل الفاتورة",edit_report:"تعديل التقرير",edit_doc:"تعديل المستند",edit_user:"تعديل المستخدم",edit_team:"تعديل الفريق",edit_note:"تعديل الملاحظة",to_opp:"تحويل لفرصة",converted:"تم تحويل العميل إلى فرصة في خط الأنابيب",moved:"تم نقل الفرصة",next_stage:"المرحلة التالية",activated_proj:"تم التفعيل وإنشاء مشروع مرتبط تلقائيًا",linked_proj:"مرتبط بمشروع",change_resp_hint:"يمكنك تحديث بيانات المسؤول أو تغييره بالكامل هنا.",f_responsible:"اسم المسؤول",f_resp_title:"المسمى الوظيفي",f_resp_phone:"هاتف المسؤول",f_resp_phone2:"هاتف بديل",f_resp_email:"بريد المسؤول",f_account_owner:"مدير الحساب",upload_hint:"يمكن اختيار أكثر من ملف (PDF، صورة، Word…). تُحفظ المرفقات الصغيرة على جهازك.",current_files:"المرفقات الحالية",f_support_docs:"رفع التقارير الورقية / المؤيدات",col_phone:"الهاتف",col_responsible:"المسؤول",drag_hint:"اسحب البطاقة بين المراحل لتحويلها، أو استخدم زر «التالي»."});
Object.assign(I18N.en,{edit:"Edit",edit_client:"Edit client",edit_opp:"Edit opportunity",edit_project:"Edit project",edit_invoice:"Edit invoice",edit_report:"Edit report",edit_doc:"Edit document",edit_user:"Edit user",edit_team:"Edit team",edit_note:"Edit note",to_opp:"To opportunity",converted:"Client converted to a pipeline opportunity",moved:"Opportunity moved",next_stage:"Next stage",activated_proj:"Activated — a linked project was auto-created",linked_proj:"Linked to project",change_resp_hint:"Update the contact's details or change the responsible person here.",f_responsible:"Responsible name",f_resp_title:"Job title",f_resp_phone:"Responsible phone",f_resp_phone2:"Alternate phone",f_resp_email:"Responsible email",f_account_owner:"Account owner",upload_hint:"You can pick multiple files (PDF, image, Word…). Small attachments are stored on your device.",current_files:"Current attachments",f_support_docs:"Upload paper reports / supporting docs",col_phone:"Phone",col_responsible:"Responsible",drag_hint:"Drag a card between stages to convert it, or use the “Next” button."});
Object.assign(I18N.ar,{year_plan:"المخطط الشهري للسنة",plan_hint:"اضغط على أي شهر لإضافة/تعديل التقدم والملاحظات والمؤيدات",month_entry_sub:"أدخل التقدم والملاحظات والمؤيدات لهذا الشهر",f_month_note:"ملاحظات الشهر",month_saved:"تم حفظ تحديث الشهر",monthly_updates:"آخر التحديثات الشهرية للمشاريع",no_plan:"لا توجد تحديثات شهرية بعد"});
Object.assign(I18N.en,{year_plan:"Monthly year plan",plan_hint:"Click any month to add/edit progress, notes and supporting docs",month_entry_sub:"Enter progress, notes and supporting docs for this month",f_month_note:"Month notes",month_saved:"Month update saved",monthly_updates:"Latest monthly project updates",no_plan:"No monthly updates yet"});
Object.assign(I18N.ar,{f_userid:"البريد الإلكتروني / اسم المستخدم",f_pass2:"تأكيد كلمة المرور",f_pass_optional:"كلمة المرور (اتركها فارغة للإبقاء)",closed_t:"نظام مغلق:",closed_b:"لا يوجد تسجيل ذاتي. يتولى مدير النظام إنشاء الحسابات وتوزيع الصلاحيات.",setup_h:"تهيئة مدير النظام",setup_sub:"لا توجد حسابات بعد. أنشئ حساب مدير النظام الأول لتفعيل المنصة.",btn_setup:"إنشاء حساب مدير النظام والدخول",sec_note:"تنبيه أمني: هذا الملف يعمل بلا خادم، لذا تُحفظ كلمات المرور محليًا كنص — للعرض والنماذج فقط، لا تُدخل كلمات مرور حقيقية.",err_nouser:"لا يوجد حساب بهذا المعرّف. يقوم مدير النظام بإنشاء الحسابات.",err_suspended:"هذا الحساب موقوف. تواصل مع مدير النظام.",err_wrongpass:"كلمة المرور غير صحيحة.",err_passmatch:"كلمتا المرور غير متطابقتين.",err_dupuser:"يوجد حساب بهذا البريد مسبقًا.",nav_audit:"سجل التدقيق",audit_sub:"تتبّع كامل لجميع العمليات داخل النظام",user_form_sub:"يُنشئ مدير النظام الحساب ويوزّع الدور والصلاحيات والمشاريع",f_linked_projects:"المشاريع المرتبطة",comma_sep:"افصل بفاصلة بين المشاريع",reset_pwd:"إعادة تعيين كلمة المرور",suspend:"إيقاف الحساب",activate:"تفعيل الحساب",st_active_acc:"مفعّل",st_suspended:"موقوف",proj_w:"مشروع",pwd_reset_done:"تمت إعادة تعيين كلمة المرور",user_suspended:"تم إيقاف الحساب",user_activated:"تم تفعيل الحساب",col_time:"الوقت",col_actor:"المستخدم",col_action:"العملية",col_target:"التفاصيل",clear_audit:"تفريغ السجل",done:"تم",empty_audit_t:"لا توجد عمليات بعد",empty_audit_b:"تُسجَّل كل العمليات (إنشاء/تعديل/حذف/دخول…) هنا تلقائيًا.",audit_login:"تسجيل دخول",audit_logout:"تسجيل خروج",audit_create_user:"إنشاء مستخدم",audit_edit_user:"تعديل مستخدم",audit_reset_password:"إعادة تعيين كلمة مرور",audit_suspend_user:"إيقاف مستخدم",audit_activate_user:"تفعيل مستخدم",audit_delete:"حذف",audit_archive_project:"أرشفة مشروع",audit_restore_project:"استعادة مشروع",audit_transfer_project:"تحويل ملكية مشروع",archive_action:"أرشفة",restore_action:"استعادة",transfer_action:"تحويل ملكية",archived_w:"مؤرشف",f_new_owner:"المالك الجديد (مدير/فريق)",project_archived:"تمت أرشفة المشروع",project_restored:"تمت استعادة المشروع",transferred:"تم تحويل ملكية المشروع",show_archived:"عرض المؤرشفة"});
Object.assign(I18N.en,{f_userid:"Email / Username",f_pass2:"Confirm password",f_pass_optional:"Password (leave blank to keep)",closed_t:"Closed system:",closed_b:"No self sign-up. The administrator creates accounts and assigns permissions.",setup_h:"Set up administrator",setup_sub:"No accounts yet. Create the first System Administrator to activate the platform.",btn_setup:"Create admin account & enter",sec_note:"Security note: this file runs without a server, so passwords are stored locally as plain text — for demo/prototyping only, do not enter real passwords.",err_nouser:"No account with this identifier. The administrator creates accounts.",err_suspended:"This account is suspended. Contact the administrator.",err_wrongpass:"Incorrect password.",err_passmatch:"Passwords do not match.",err_dupuser:"An account with this email already exists.",nav_audit:"Audit trail",audit_sub:"Full trace of all operations in the system",user_form_sub:"The admin creates the account and assigns role, permissions and projects",f_linked_projects:"Linked projects",comma_sep:"Separate projects with commas",reset_pwd:"Reset password",suspend:"Suspend account",activate:"Activate account",st_active_acc:"Active",st_suspended:"Suspended",proj_w:"projects",pwd_reset_done:"Password reset done",user_suspended:"Account suspended",user_activated:"Account activated",col_time:"Time",col_actor:"User",col_action:"Action",col_target:"Details",clear_audit:"Clear log",done:"Done",empty_audit_t:"No operations yet",empty_audit_b:"Every operation (create/edit/delete/login…) is logged here automatically.",audit_login:"Login",audit_logout:"Logout",audit_create_user:"Create user",audit_edit_user:"Edit user",audit_reset_password:"Reset password",audit_suspend_user:"Suspend user",audit_activate_user:"Activate user",audit_delete:"Delete",audit_archive_project:"Archive project",audit_restore_project:"Restore project",audit_transfer_project:"Transfer project",archive_action:"Archive",restore_action:"Restore",transfer_action:"Transfer ownership",archived_w:"Archived",f_new_owner:"New owner (manager/team)",project_archived:"Project archived",project_restored:"Project restored",transferred:"Project ownership transferred",show_archived:"Show archived"});
applyLang();authMode();
</script>
</body>
</html>
