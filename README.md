<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>TaRL Mentor Academy</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
/* Layout: sticky top bar, course outline at left (drawer on phones), one reading column, fixed read-aloud bar at the bottom.
   Colour: the four level colours from the manual's wall chart (Red Beginner, Yellow Letter, Blue Word, Green Story) mark the modules. */
:root{
  --bg:#F2F6F4; --surface:#FFFFFF; --surface2:#E8EFEC; --fg:#14201C; --muted:#52645E; --line:#D3DED9;
  --accent:#0E6B58; --accent-fg:#FFFFFF; --accent-soft:#D6EBE5;
  --c0:#46605A; --c1:#C0432E; --c2:#B9860B; --c3:#2B63B8; --c4:#2E8B4E; --c5:#7A4FA3;
  --ok:#1F7A45; --bad:#B3321F; --hl:#FFF1B8;
  --fd:'Bricolage Grotesque','Inter',system-ui,sans-serif; --fb:'Inter',system-ui,-apple-system,'Segoe UI',sans-serif;
}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){
  --bg:#0D1513; --surface:#151F1C; --surface2:#1C2925; --fg:#E7F0EC; --muted:#9DB0A9; --line:#2A3A35;
  --accent:#4FC3A6; --accent-fg:#06201A; --accent-soft:#16352E;
  --c0:#8FB0A6; --c1:#EE7B66; --c2:#E5B84A; --c3:#6FA1EE; --c4:#5CC27E; --c5:#B28BDA;
  --ok:#5CC27E; --bad:#F08B79; --hl:#4A4220; color-scheme:dark}}
:root[data-theme="dark"]{
  --bg:#0D1513; --surface:#151F1C; --surface2:#1C2925; --fg:#E7F0EC; --muted:#9DB0A9; --line:#2A3A35;
  --accent:#4FC3A6; --accent-fg:#06201A; --accent-soft:#16352E;
  --c0:#8FB0A6; --c1:#EE7B66; --c2:#E5B84A; --c3:#6FA1EE; --c4:#5CC27E; --c5:#B28BDA;
  --ok:#5CC27E; --bad:#F08B79; --hl:#4A4220; color-scheme:dark}
*{box-sizing:border-box}
html,body{height:auto}
body{background:var(--bg);color:var(--fg);font:16px/1.65 var(--fb);margin:0;padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));padding-block:0}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);z-index:40;background:var(--surface)}
a{color:var(--accent)}
button,select,textarea,input{font:inherit;color:inherit}
:focus-visible{outline:3px solid var(--accent);outline-offset:2px}
.top{position:sticky;top:env(safe-area-inset-top,0px);z-index:30;background:var(--surface);border-bottom:1px solid var(--line);margin:0 calc(-1*max(16px,env(safe-area-inset-left,0px)));padding:10px max(16px,env(safe-area-inset-right,0px)) 10px max(16px,env(safe-area-inset-left,0px));display:flex;align-items:center;gap:12px}
.brand{font:700 18px/1.1 var(--fd);letter-spacing:-.01em;display:flex;gap:10px;align-items:center;cursor:pointer;background:none;border:0;padding:0;text-align:left}
.dots{display:grid;grid-template-columns:repeat(2,9px);gap:2px}.dots i{width:9px;height:9px;border-radius:2px;display:block}
.dots i:nth-child(1){background:var(--c1)}.dots i:nth-child(2){background:var(--c2)}.dots i:nth-child(3){background:var(--c3)}.dots i:nth-child(4){background:var(--c4)}
.prog{flex:1;display:flex;align-items:center;gap:10px;min-width:0;justify-content:flex-end}
.bar{height:8px;background:var(--surface2);border-radius:99px;overflow:hidden;flex:0 1 220px;width:100%}
.bar>b{display:block;height:100%;background:var(--accent);width:0;transition:width .3s}
.pct{font-size:13px;color:var(--muted);font-variant-numeric:tabular-nums;white-space:nowrap}
.btn{background:var(--accent);color:var(--accent-fg);border:0;border-radius:8px;padding:9px 16px;font-weight:600;cursor:pointer;min-height:40px}
.btn.ghost{background:transparent;color:var(--accent);border:1px solid var(--accent)}
.btn.sm{padding:5px 12px;min-height:32px;font-size:14px}
.btn:disabled{opacity:.45;cursor:not-allowed}
#menuBtn{display:none}
.shell{display:grid;grid-template-columns:300px minmax(0,1fr);gap:32px;max-width:1240px;margin:0 auto;padding-block:24px 150px}
nav#side{position:sticky;top:calc(64px + env(safe-area-inset-top,0px));align-self:start;max-height:calc(100vh - 150px);overflow:auto;font-size:14px}
nav#side details{border-top:1px solid var(--line);padding:6px 0}
nav#side summary{cursor:pointer;font-weight:600;padding:6px 0;list-style:none;display:flex;gap:8px;align-items:flex-start}
nav#side summary::-webkit-details-marker{display:none}
.sw{width:10px;height:10px;border-radius:3px;margin-top:6px;flex:none}
nav#side a.li{display:flex;gap:8px;padding:6px 8px 6px 18px;text-decoration:none;color:var(--fg);border-radius:6px;line-height:1.35}
nav#side a.li:hover{background:var(--surface2)}
nav#side a.li[aria-current="page"]{background:var(--accent-soft);font-weight:600}
.ck{width:16px;height:16px;border:1.5px solid var(--line);border-radius:50%;flex:none;margin-top:2px;display:grid;place-items:center;font-size:10px}
.ck.on{background:var(--ok);border-color:var(--ok);color:#fff}
main{min-width:0;max-width:760px}
.crumb{font-size:13px;color:var(--muted);text-transform:uppercase;letter-spacing:.08em;display:flex;gap:8px;align-items:center;margin-bottom:6px}
h1{font:700 clamp(28px,5vw,40px)/1.12 var(--fd);letter-spacing:-.02em;margin:0 0 6px;text-wrap:balance}
h3{font:700 21px/1.25 var(--fd);margin:34px 0 8px;text-wrap:balance}
h4{font:700 14px/1.3 var(--fb);text-transform:uppercase;letter-spacing:.07em;margin:0 0 6px}
p{margin:0 0 14px}ul,ol{padding-left:22px;margin:0 0 16px}li{margin-bottom:6px}
.meta{color:var(--muted);font-size:14px;margin-bottom:22px}
.callout{background:var(--accent-soft);border-radius:10px;padding:14px 16px;margin:20px 0}
.callout p:last-child{margin:0}
.callout.warn{background:var(--surface2);border:1px solid var(--line)}
.tw{overflow-x:auto;margin:16px 0;border:1px solid var(--line);border-radius:10px;background:var(--surface)}
table{border-collapse:collapse;width:100%;min-width:560px;font-size:14px;line-height:1.5}
th,td{text-align:left;vertical-align:top;padding:10px 12px;border-bottom:1px solid var(--line)}
th{background:var(--surface2);font-size:12px;text-transform:uppercase;letter-spacing:.06em}
tr:last-child td{border-bottom:0}td.rh{font-weight:600}
.dlg{display:flex;flex-direction:column;gap:8px;margin:16px 0}
.bub{max-width:88%;padding:10px 14px;border-radius:14px;margin:0;font-size:15px}
.bub.m{background:var(--accent-soft);align-self:flex-start;border-bottom-left-radius:4px}
.bub.t{background:var(--surface2);align-self:flex-end;border-bottom-right-radius:4px}
.bub b{display:block;font-size:11px;text-transform:uppercase;letter-spacing:.08em;color:var(--muted);margin-bottom:2px}
.phases{display:flex;border-radius:10px;overflow:hidden;margin:16px 0 6px;min-height:78px}
.phases div{padding:8px 8px;font-size:12px;line-height:1.3;color:#fff;display:flex;flex-direction:column;justify-content:space-between;min-width:0}
.phases b{font-size:16px;font-variant-numeric:tabular-nums}
.widget,.practice{background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:16px;margin:22px 0}
.widget h4,.practice h4{color:var(--accent)}
.pi{border-top:1px solid var(--line);padding-top:12px;margin-top:12px}
.pi:first-of-type{border-top:0;margin-top:0;padding-top:0}
textarea{width:100%;min-height:72px;background:var(--bg);border:1px solid var(--line);border-radius:8px;padding:10px;resize:vertical;margin:6px 0 8px}
.ans{background:var(--accent-soft);border-radius:8px;padding:10px 12px;margin-top:8px}.ans p{margin:0 0 6px}.ans p:last-child{margin:0}
.sl{display:grid;grid-template-columns:minmax(0,1fr) 150px 28px;gap:12px;align-items:center;padding:8px 0;border-top:1px solid var(--line);font-size:14px}
.sl:first-of-type{border-top:0}.sl input{width:100%;accent-color:var(--accent)}.sl output{font-weight:700;text-align:center}
.matrix{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin:10px 0 0}
.matrix button{border:1px solid var(--line);background:var(--bg);border-radius:10px;padding:14px;text-align:left;cursor:pointer;min-height:84px}
.matrix button[aria-pressed="true"]{border-color:var(--accent);background:var(--accent-soft)}
.matrix b{display:block;font-family:var(--fd)}.matrix span{font-size:13px;color:var(--muted)}
.axis{display:flex;justify-content:space-between;font-size:12px;color:var(--muted);text-transform:uppercase;letter-spacing:.06em;margin-top:6px}
.opt{display:flex;gap:10px;align-items:flex-start;padding:8px 10px;border:1px solid var(--line);border-radius:8px;margin:6px 0;cursor:pointer;background:var(--bg)}
.opt input{margin-top:5px;accent-color:var(--accent)}
.opt.right{border-color:var(--ok);background:var(--accent-soft)}.opt.wrong{border-color:var(--bad)}
.qq{border:0;padding:0;margin:0 0 20px}.qq legend{font-weight:600;padding:0;margin-bottom:6px}
.why{font-size:14px;color:var(--muted);margin:6px 0 0}
.score{font:700 28px var(--fd)}
.lvl{display:inline-block;padding:3px 10px;border-radius:99px;color:#fff;font-weight:600;font-size:14px}
.trail{display:flex;gap:6px;flex-wrap:wrap;font-size:13px;color:var(--muted);margin-bottom:10px}
.trail span{background:var(--surface2);padding:2px 8px;border-radius:99px}
.res{margin-top:40px;border-top:2px solid var(--line);padding-top:8px}
.res h3{margin-top:22px}
.rl{display:grid;gap:8px;padding:0;list-style:none;margin:0}
.rl li{margin:0}
.rl a{display:block;padding:10px 12px;border:1px solid var(--line);border-radius:10px;background:var(--surface);text-decoration:none;color:var(--fg)}
.rl a:hover{border-color:var(--accent)}
.rl .t{font-weight:600;display:block}.rl .n{font-size:13px;color:var(--muted)}
.tag{font-size:11px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;padding:1px 7px;border-radius:99px;margin-left:6px;background:var(--surface2);color:var(--muted);vertical-align:middle}
.tag.ok{background:var(--accent-soft);color:var(--accent)}
.foot{display:flex;gap:10px;justify-content:space-between;flex-wrap:wrap;margin-top:34px}
.reflect{margin-top:30px}
.hero{padding:10px 0 4px}
.hero p.lead{font-size:18px;max-width:60ch;color:var(--muted)}
.cards{display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:12px;margin:22px 0}
.card{background:var(--surface);border:1px solid var(--line);border-top:5px solid var(--cc);border-radius:10px;padding:14px;cursor:pointer;text-align:left}
.card:hover{border-color:var(--cc)}
.card b{font:700 17px/1.25 var(--fd);display:block;margin-bottom:4px}.card span{font-size:13px;color:var(--muted)}
.stats{display:flex;gap:26px;flex-wrap:wrap;margin:20px 0}.stats div{min-width:80px}.stats b{font:700 30px var(--fd);display:block;line-height:1}.stats span{font-size:13px;color:var(--muted)}
#audio{position:fixed;left:0;right:0;bottom:0;z-index:35;background:var(--surface);border-top:1px solid var(--line);padding:10px max(16px,env(safe-area-inset-right,0px)) calc(10px + env(safe-area-inset-bottom,0px)) max(16px,env(safe-area-inset-left,0px))}
#audio .in{max-width:1240px;margin:0 auto;display:flex;gap:10px;align-items:center;flex-wrap:wrap}
#audio .in>*{min-width:0}
#audio select{background:var(--bg);border:1px solid var(--line);border-radius:8px;padding:6px;max-width:100%}
#vsel{flex:1 1 140px;max-width:260px}
#astat{font-size:13px;color:var(--muted);flex:1 1 120px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.reading{background:var(--hl);border-radius:4px;box-decoration-break:clone;-webkit-box-decoration-break:clone}
tr.reading td{background:var(--hl)}
.cert{border:3px double var(--accent);border-radius:12px;padding:28px 20px;text-align:center;background:var(--surface);margin:20px 0}
.cert h2{font:700 30px var(--fd);margin:6px 0}.cert .nm{font:700 28px var(--fd);border-bottom:2px solid var(--line);display:inline-block;padding:0 18px 4px;margin:10px 0}
.nameIn{width:100%;max-width:360px;background:var(--bg);border:1px solid var(--line);border-radius:8px;padding:10px}
.sr{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0)}
@media (max-width:900px){
  .shell{grid-template-columns:minmax(0,1fr)}
  #menuBtn{display:inline-block}
  nav#side{display:none;position:fixed;inset:0;top:calc(58px + env(safe-area-inset-top,0px));max-height:none;background:var(--bg);z-index:29;padding:12px max(16px,env(safe-area-inset-right,0px)) 160px max(16px,env(safe-area-inset-left,0px))}
  body.menu nav#side{display:block}
  .pct{display:none}.bar{flex:1}
}
@media (max-width:520px){.sl{grid-template-columns:1fr 28px}.sl input{grid-column:1/2}.bub{max-width:96%}}
@media (prefers-reduced-motion:reduce){*{transition:none!important;scroll-behavior:auto!important}}
</style>

<header class="top">
  <button id="menuBtn" class="btn ghost sm" aria-expanded="false" aria-controls="side">Menu</button>
  <button class="brand" id="brandBtn" aria-label="Course home"><span class="dots" aria-hidden="true"><i></i><i></i><i></i><i></i></span><span>TaRL Mentor Academy</span></button>
  <div class="prog"><span class="pct" id="pct">0%</span><div class="bar" role="progressbar" aria-label="Course progress" id="pbar"><b id="pfill"></b></div></div>
</header>
<div class="shell">
  <nav id="side" aria-label="Course outline"></nav>
  <main id="main" tabindex="-1"></main>
</div>
<div id="audio" hidden>
  <div class="in">
    <button class="btn sm" id="aPrev" aria-label="Previous paragraph">Back</button>
    <button class="btn sm" id="aPlay">Listen</button>
    <button class="btn sm" id="aNext" aria-label="Next paragraph">Skip</button>
    <label class="sr" for="rate">Speed</label>
    <select id="rate"><option value="0.8">0.8x</option><option value="1" selected>1x</option><option value="1.2">1.2x</option><option value="1.5">1.5x</option></select>
    <label class="sr" for="vsel">Voice</label>
    <select id="vsel"></select>
    <span id="astat" aria-live="polite"></span>
  </div>
</div>

<script>
/* ---------- helpers ---------- */
const $=(s,r=document)=>r.querySelector(s), $$=(s,r=document)=>[...r.querySelectorAll(s)];
const esc=s=>String(s).replace(/[&<>"]/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c]));
const T=(h,rows)=>`<div class="tw"><table><thead><tr>${h.map(x=>`<th>${x}</th>`).join('')}</tr></thead><tbody>${rows.map(r=>`<tr>${r.map((c,i)=>`<td${i==0?' class="rh"':''}>${c}</td>`).join('')}</tr>`).join('')}</tbody></table></div>`;
const C=(t,b,w)=>`<aside class="callout${w?' warn':''}"><h4>${t}</h4><p>${b}</p></aside>`;
const UL=a=>`<ul>${a.map(x=>`<li>${x}</li>`).join('')}</ul>`;
const OL=a=>`<ol>${a.map(x=>`<li>${x}</li>`).join('')}</ol>`;
const DLG=a=>`<div class="dlg">${a.map(([r,t])=>`<p class="bub ${r=='M'?'m':'t'}"><b>${r=='M'?'Mentor:':'Teacher:'}</b> ${t}</p>`).join('')}</div>`;
const W=(n,extra='')=>`<div class="${n.startsWith('practice')?'practice':'widget nr'}" data-w="${n}"></div>`;

/* ---------- state ---------- */
const KEY='tarl-mentor-academy-v1';
let S={done:{},notes:{},scores:{},audit:{},name:'',passed:false};
try{const r=localStorage.getItem(KEY);if(r)S=Object.assign(S,JSON.parse(r))}catch(e){}
const save=()=>{try{localStorage.setItem(KEY,JSON.stringify(S))}catch(e){}};

/* ---------- resources ---------- */
const YT=id=>'https://www.youtube.com/watch?v='+id, TS='https://www.teachingattherightlevel.org/', JP='https://www.povertyactionlab.org/';
const RES={
 v_camal:{k:'v',t:'Teaching at the Right Level (TaRL/CAMaL): Pratham\'s teaching-learning methodology',b:'Pratham Education Foundation',u:YT('jqZZ5zz7KDM'),n:'How CAMaL grew out of Pratham\'s work on reading, writing and maths.',ok:1},
 v_pratham:{k:'v',t:'Pratham: Teaching at the Right Level',b:'Pratham USA',u:YT('EDFgH9AsTFI'),n:'Short introduction to TaRL and how it spread from India to other countries.',ok:1},
 v_zambia:{k:'v',t:'Catch Up Programme in Zambia: foundation learning in numeracy and literacy',b:'YouTube',u:YT('Pw3GlVZcGmI'),n:'Government-led scale-up of TaRL in Zambia (Catch Up).'},
 v_chan:{k:'v',t:'Teaching at the Right Level channel',b:'YouTube channel',u:'https://www.youtube.com/channel/UCGj5CH3GNH6_luqnCVYhjDw',n:'Classroom clips and country stories. Browse for videos in your own language context.'},
 v_grow:{k:'v',t:'The GROW Model for Coaching: origins and application',b:'Sir John Whitmore, Performance Consultants International',u:YT('f2M1GuhilR0'),n:'The framework\'s originator explains where GROW came from and how to use it.',ok:1},
 v_grow2:{k:'v',t:'GROW Coaching Model Explained',b:'YouTube',u:YT('Bc5onu-9nsU'),n:'A second, shorter walk-through of Goal, Reality, Options, Wrap-up.'},
 v_growdemo:{k:'v',t:'How to use the GROW Model: coaching demonstration',b:'YouTube',u:YT('7JM1gXkzrnk'),n:'Watch a full coaching conversation, then compare it with the Teacher Sara transcript.'},
 v_listen:{k:'v',t:'Active Listening Skills',b:'Alexander Lyon, Communication Coach',u:YT('Ra6L83XwLko'),n:'Four-part training on listening barriers, core techniques and empathetic listening.',ok:1},
 v_wenger:{k:'v',t:'Interview with Beverly and Etienne Wenger-Trayner',b:'YouTube',u:YT('USbHNY84AR8'),n:'The co-author of the community of practice idea in his own words.'},
 v_cop:{k:'v',t:'Essentials of sustainable online communities of practice',b:'YouTube (plenary)',u:YT('OeKELfOloBw'),n:'Useful when you design and moderate cluster WhatsApp or Telegram groups.'},
 v_ar:{k:'v',t:'How to Conduct Action Research in Education',b:'YouTube',u:YT('oPjgDLjIazA'),n:'Walks through the inquiry cycle teachers use in Unit 5.3.'},
 v_ar2:{k:'v',t:'Action Research 101: Research as Teaching Practice',b:'REL Pacific',u:YT('2kVnlSnCe8k'),n:'Short primer for teachers new to classroom inquiry.'},
 r_site:{k:'r',t:'TaRL Africa and Pratham: official website',b:'teachingattherightlevel.org',u:TS,n:'Start here for the full approach, evidence and community pages.',ok:1},
 r_assess:{k:'r',t:'The TaRL approach: assessment',b:'teachingattherightlevel.org',u:TS+'the-tarl-approach/assessment/',n:'Official guidance on the one-on-one assessment.',ok:1},
 r_class:{k:'r',t:'The TaRL approach: classroom methodology',b:'teachingattherightlevel.org',u:TS+'the-tarl-approach/classroom-methodology/',n:'Official description of grouping, activities and daily routines.',ok:1},
 r_mon:{k:'r',t:'The TaRL approach: measurement and monitoring',b:'teachingattherightlevel.org',u:TS+'the-tarl-approach/monitoring/',n:'How programmes track progress and use data.',ok:1},
 r_teams:{k:'r',t:'The TaRL approach: implementation teams',b:'teachingattherightlevel.org',u:TS+'the-tarl-approach/implementation-teams/',n:'Roles of mentors, supervisors and officials in a TaRL rollout.',ok:1},
 r_evid:{k:'r',t:'TaRL evidence',b:'teachingattherightlevel.org',u:TS+'evidence/',n:'Summary of the trials behind the approach.',ok:1},
 r_action:{k:'r',t:'TaRL in action: country stories',b:'teachingattherightlevel.org',u:TS+'tarl-in-action/',n:'How different countries adapted TaRL.',ok:1},
 r_comm:{k:'r',t:'TaRL community: blog and forum',b:'teachingattherightlevel.org',u:TS+'community/',n:'Practitioner blog and forum for peer learning.',ok:1},
 r_jpal:{k:'r',t:'Teaching at the Right Level to accelerate learning',b:'J-PAL',u:JP+'evidence-effect/teaching-at-the-right-level',n:'Evidence summary from randomised trials.'},
 r_jpal2:{k:'r',t:'Tailoring instruction to students\' learning levels',b:'J-PAL policy insight',u:JP+'policy-insight/tailoring-instruction-students-learning-levels-increase-learning',n:'Policy-level summary of why and how targeted instruction works.'},
 r_jpal3:{k:'r',t:'Teaching at the Right Level to improve learning',b:'J-PAL case study',u:JP+'case-study/teaching-right-level-improve-learning',n:'Case study of how the programme was tested and scaled.'},
 r_zam:{k:'r',t:'Zambia to scale TaRL to 1,800 schools',b:'J-PAL blog',u:JP+'blog/8-8-17/zambia-scale-teaching-right-level-program-1800-schools',n:'Early account of the government-led Zambian scale-up.'},
 r_fln:{k:'r',t:'Inside UNICEF and J-PAL\'s FLN Academy 3.0',b:'J-PAL blog',u:JP+'blog/4-22-25/where-evidence-meets-practice-inside-unicef-and-j-pals-fln-academy-30',n:'How evidence on foundational learning reaches practitioners.'},
 r_olbal:{k:'r',t:'Learning to teach: balancing support and challenge (section 2.2)',b:'OpenLearn, Open University',u:'https://www.open.edu/openlearn/education-development/learning-teach-mentoring-and-tutoring-student-teachers/content-section-2.2',n:'Free reading on the Daloz-style matrix: confirmation, stasis, growth and retreat.',ok:1},
 r_olmind:{k:'r',t:'A mentoring mindset (free course)',b:'OpenLearn, Open University',u:'https://www.open.edu/openlearn/education-development/education-careers/a-mentoring-mindset-meddylfryd-mentora/content-section-overview',n:'Open-access course on mentoring mindsets and reflective practice.'},
 r_hm:{k:'r',t:'Judgementoring and other threats to school-based mentoring',b:'Hobson and Malderez, 2013',u:'https://shura.shu.ac.uk/7224',n:'The paper that named judge mentoring. Repository page with full text options.'},
 r_wt:{k:'r',t:'Communities of practice: a brief introduction',b:'Etienne and Beverly Wenger-Trayner',u:'https://www.wenger-trayner.com/wp-content/uploads/2022/01/07-Brief-introduction-to-communities-of-practice.pdf',n:'Short PDF; covers domain, community and practice and common misconceptions.',ok:1},
 r_infed:{k:'r',t:'Jean Lave, Etienne Wenger and communities of practice',b:'infed.org',u:'https://infed.org/mobi/?p=2651',n:'Plain-language overview of legitimate peripheral participation.'},
 r_schon:{k:'r',t:'Donald Schön: reflective practice',b:'eCampusOntario open textbook',u:'https://ecampusontario.pressbooks.pub/reflectivepracticeinearlyyears/chapter/3-3-donald-schon/',n:'Reflection-in-action and reflection-on-action explained simply.'},
 r_growpdf:{k:'r',t:'The GROW Model user guide (PDF)',b:'Australian Sports Commission',u:'https://ausport.gov.au/__data/assets/pdf_file/0016/1159000/7.-The-GROW-Model_User-Guide.pdf',n:'Question prompts for each GROW stage you can adapt for debriefs.'},
 r_kobo:{k:'r',t:'KoboToolbox',b:'kobotoolbox.org',u:'https://www.kobotoolbox.org/',n:'Free data collection tool named in Unit 4.5 for school aggregation.'},
 r_i1d:{k:'r',t:'Imagine 1day',b:'imagine1day.org',u:'https://imagine1day.org/',n:'Foundational learning work in Ethiopia (listed in Appendix D).'},
 r_ol:{k:'r',t:'OpenLearn: free courses',b:'open.edu/openlearn',u:'https://www.open.edu/openlearn/',n:'Open-access modules on mentoring, coaching and reflective practice (Appendix D).'},
 b_whit:{k:'b',t:'Coaching for Performance',by:'John Whitmore',y:'5th ed., 2017',n:'The standard book on GROW and the coaching mindset.'},
 b_daloz:{k:'b',t:'Mentor: Guiding the Journey of Adult Learners',by:'Laurent A. Daloz',y:'Jossey-Bass',n:'Source of the support and challenge matrix.'},
 b_schon:{k:'b',t:'The Reflective Practitioner',by:'Donald A. Schön',y:'1983',n:'Reflection-in-action and reflection-on-action.'},
 b_lave:{k:'b',t:'Situated Learning: Legitimate Peripheral Participation',by:'Jean Lave and Etienne Wenger',y:'Cambridge University Press, 1991',n:'Original source of the community of practice idea.'},
 b_ccop:{k:'b',t:'Cultivating Communities of Practice',by:'Etienne Wenger, Richard McDermott, William Snyder',y:'Harvard Business Press, 2002',n:'Practical guide to starting and moderating communities.'},
 b_kline:{k:'b',t:'Time to Think: Listening to Ignite the Human Mind',by:'Nancy Kline',y:'1999',n:'Deepens Unit 3.2 on attention, silence and questions.'},
 b_results:{k:'b',t:'Results Coaching: The New Essential for School Leaders',by:'Kee, Anderson, Dearing, Harris and Shuster',y:'Corwin, 2010',n:'The RESULTS model used in Unit 3.5.'},
 b_chel:{k:'b',t:'Coaching Conversations: Transforming Your School One Conversation at a Time',by:'Cheliotes and Reilly',y:'Corwin, 2010',n:'Defining features of a professional coaching conversation (Unit 3.1).'},
 b_knight:{k:'b',t:'Instructional Coaching: A Partnership Approach to Improving Instruction',by:'Jim Knight',y:'Corwin, 2007',n:'Practical coaching cycles for classroom teachers.'},
 b_poor:{k:'b',t:'Poor Economics',by:'Abhijit V. Banerjee and Esther Duflo',y:'PublicAffairs, 2011',n:'The education chapter explains why teaching to the child\'s level matters.'},
 b_mertler:{k:'b',t:'Action Research: Improving Schools and Empowering Educators',by:'Craig A. Mertler',y:'SAGE',n:'Step-by-step guide for teachers running their own inquiries.'}
};
const bookUrl=r=>'https://openlibrary.org/search?q='+encodeURIComponent(r.t+' '+r.by);

/* ---------- practice data ---------- */
const PRACTICE={
 sc11:{t:'Activity 1.1: Calibrate support and challenge',i:'For each classroom scenario, name the Daloz quadrant, then write one Supporting Move and one Challenging Move. Reveal the facilitator\'s model answer afterwards.',items:[
  ['Scenario A. A newly trained Grade 4 teacher is eager to launch TaRL and volunteers to run all three literacy groups at once on Day 1 without peer leaders. The result is chaos.','<b>Supporting move:</b> Affirm her enthusiasm and commitment to learners; co-plan a manageable structure for tomorrow\'s lesson.</p><p><b>Challenging move:</b> Ask: "How can we structure the first 10 minutes as a whole-class warm-up and use two Story-level peer leaders so you can focus deeply on the Beginner group?"'],
  ['Scenario B. An experienced teacher lacks confidence in the one-on-one oral reading assessment and fears she will misclassify children.','<b>Supporting move:</b> Validate that learning a new diagnostic tool takes practice; sit beside her to assess the first 5 learners together.</p><p><b>Challenging move:</b> Invite her to lead the next 5 assessments independently while you observe, then calibrate the scoring afterwards.'],
  ['Scenario C. A teacher publicly scolds an over-age 14-year-old boy in the Beginner group for "not trying hard enough". He shuts down and stops attending.','<b>Supporting move:</b> Speak privately, with empathy, about the stress of managing wide age ranges in one classroom.</p><p><b>Challenging move:</b> Challenge the assumption of laziness: "Older non-readers carry deep shame. How can we give him a dignified leadership role, such as material manager, while discreetly building his phonics?"'],
  ['Scenario D. A veteran teacher is warm and energetic and students love her songs, but midline data shows 0% of her Letter-level learners moved to Word level in 6 weeks.','<b>Supporting move:</b> Celebrate her strong classroom climate and high attendance, which are essential foundations for TaRL.</p><p><b>Challenging move:</b> Show the midline progression chart and ask: "Your learners know their letter sounds well. What is stopping them from blending two-letter syllables, and how can we shift 20 minutes daily to syllable grid practice?"']]},
 rw12:{t:'Activity 1.2: Rewrite judge statements as coaching prompts',i:'Rewrite each deficit-focused statement as an open, non-judgmental question that makes the teacher think.',items:[
  ['"You spent 35 minutes on whole-class talking and left almost no time for level-based group work."','"Looking at our 60-minute lesson clock today, how did the pacing feel across the whole-class and small-group phases? What adjustment might give your Beginner group more hands-on practice tomorrow?"'],
  ['"Why didn\'t you use the Syllable Chart when the Beginner group got stuck?"','"When you noticed the Beginner group struggling to blend sounds today, what options came to mind? How might a visual tool like the Syllable Chart help them tomorrow?"'],
  ['"Three children in your Word group are clearly still at Letter level. Your grouping is wrong."','"Let\'s look closely at those three learners in the Word group today. What did you observe when they tried reading the simple paragraph, and how might we check their placement together?"'],
  ['"You forgot to praise the children when they answered correctly."','"How did learners respond when they took risks reading aloud today? What kinds of encouragement seem to boost confidence most for your quietest students?"'],
  ['"Next week I want to see you using the Basket Game properly."','"Which TaRL phonics game would you like to experiment with next week to energize your Letter group, and would you like us to co-plan or co-teach it first?"']]},
 vig27:{t:'Calibration exercise: score a sample lesson',i:'Read the vignette. Score each of the four rubric domains from 1 to 4, then name the single highest-leverage coaching target.',items:[
  ['Teacher Bekele starts his Grade 4 TaRL session with an energetic 8-minute Picture Reading poster about a local clinic. Quiet students smile and volunteer words, and he helps them form full sentences. He divides the 48 students into three level corners using his updated wall chart. He hands a stack of flashcards to the Beginner group without demonstrating the Basket Game, then spends 28 consecutive minutes with the Story group on comprehension questions. The Beginner group argues over the cards. The Word group finishes in 10 minutes and sits idle until the bell, with no writing.','<b>Model scoring:</b> Domain 1 = Level 3. Domain 2 = Level 2 (unbalanced rotation, missing individual writing). Domain 3 = Level 2 (no "I do" modelling for the Beginner group). Domain 4 = Level 3.</p><p><b>Highest-leverage target:</b> Model the Basket Game for 3 minutes before the group split, and rotate across all three groups in 10-minute intervals.']]},
 q33:{t:'Practice: turn advice into inquiry',i:'Rewrite each flawed question as an open coaching question. Compare with the manual\'s model.',items:[
  ['Leading: "Don\'t you think changing pupil groupings would solve your classroom management issue?"','"What options have you considered for managing grouping dynamics in that class?"'],
  ['Loaded: "Have you thought about giving pupils more thinking time instead of rushing them?"','"How do you feel students responded to the pacing of questions today?"'],
  ['Closed: "Are you aware of the range of Assessment for Learning techniques we use?"','"Which assessment techniques helped you gauge student understanding during the lesson?"'],
  ['Judgmental: "Would you agree that your plenary needs complete redesigning?"','"Looking back at the end of the lesson, how effective was the wrap-up in confirming what learners mastered?"']]},
 rp37:{t:'Role-play card 1: the pacing crisis',i:'Work in threes: Teacher, Coach, Observer. Run about 12 minutes, then swap roles.',items:[
  ['<b>Teacher:</b> You tried to run TaRL for 45 minutes but ran out of time before the writing phase. You feel rushed and frustrated because your principal emphasises syllabus coverage.<br><b>Coach:</b> Use GROW to help the teacher find where time was lost without sounding critical. Prompt the teacher to discover that tightening the whole-class warm-up to 10 minutes solves the pacing problem.','<b>Observer checklist (course-derived from Units 3.2 to 3.4):</b></p><p>Did the coach keep the teacher talking about 70 to 80% of the time? Did the coach hold at least one silence of 5 to 10 seconds? Did the coach mirror the teacher\'s words without judging? Were all questions open? Were Goal, Reality, Options and Wrap-up all covered, ending with who will do what by when?']]}
};

/* ---------- quizzes ---------- */
const Q={
 m0:[
  ['Why do teachers drift back to chalk-and-talk after a good workshop, according to the manual?',['They are lazy','Changing daily classroom habits is hard and uncertain, and without a mentor beside them they retreat to what feels safe','The training content is poor','Textbooks are unavailable'],1,'The manual says it is not laziness and not poor training. Without supportive mentoring the teacher retreats when the class gets noisy.'],
  ['The competency framework has how many competencies, in how many domains?',['10 in 3','12 in 4','8 in 2','12 in 3'],1,'Twelve competencies across four domains: pedagogical mastery, relational trust, coaching dialogue and observation, and data triage and governance.'],
  ['What is the practice class rule for newly trained mentors?',['One 1-hour TaRL class a week for a term','A daily 1-hour TaRL class for 15 to 20 consecutive school days before mentoring teachers','Observe three classes and then start mentoring','Run a class only if the school asks'],1,'Practising the full cycle builds craft knowledge and the moral authority that comes from seeing children progress.'],
  ['When should the Mentor Self-Audit be repeated?',['Never; it is a one-off','Day 5 afternoon and after 60 days of field practice','Only at the end of the year','Every day of the workshop'],1,'It is first used on Day 1 morning, then revisited on Day 5 afternoon and after 60 days of field practice.']],
 m1:[
  ['Which stance fits Weeks 1 to 4 of implementation, or a teacher struggling with basic grouping?',['Coaching','Mentoring, with modelling and structured tips','Administrative inspection','Developmental inspection'],1,'Mentoring is used early; coaching suits Weeks 5 and beyond, once routines are established.'],
  ['In Daloz\'s matrix, which quadrant is high challenge with low support?',['Stasis','Confirmation','Retreat','Growth'],2,'Retreat is typical of judge mentoring: the teacher feels threatened, defensive or burned out.'],
  ['Which of Love\'s four observation types is the core TaRL standard?',['Absent observation','Brutal observation','Collegial observation','Surprise drop-in'],2,'Collegial observation is an agreed full-lesson observation, followed by an ungraded two-way conversation.'],
  ['What does Schön\'s "reflection-in-action" describe?',['Writing a report after the lesson','Adjusting an activity mid-lesson when learners look confused','Reading research before teaching','A school-wide review'],1,'Reflection-on-action is the analysis afterwards; reflection-in-action happens during the lesson.'],
  ['A mentor makes warm visits with lots of praise but never raises weak pedagogy or stagnant data. Which quadrant?',['Stasis','Retreat','Confirmation','Growth'],2,'High support with low challenge. The corrective move is to introduce gentle dissonance with midline data and set one stretch target.']],
 m2:[
  ['Where does the literacy placement test start?',['Letter level','At the Simple Paragraph level','Story level','At the Beginner level'],1,'Starting at the paragraph saves time and respects older learners\' dignity, then branches up or down.'],
  ['A child reads the simple paragraph word by word with 5 mistakes. What next?',['Classify as Story level','Classify as Beginner','Move down to the Word level check (5 familiar words)','Repeat the paragraph until perfect'],2,'More than 3 mistakes or halting reading sends the child down to Step 3, the Word level check.'],
  ['How should the 60-minute lesson be paced?',['30 min warm-up, 30 min group work','10 whole class, 5 modelling and transition, 30 group practice, 10 individual writing, 5 wrap-up','45 min lecture, 15 min writing','Equal time for each of the five phases'],1,'Long warm-ups starve group practice; the blueprint protects 30 minutes for level-specific work and 10 for writing.'],
  ['In numeracy, how is borrowing in 42 - 17 first shown?',['By memorising the vertical algorithm','By untying one bundle of ten into 10 loose sticks','With a calculator','By drawing only numbers'],1,'Concrete, then pictorial, then abstract. Children fail when abstract algorithms come before place value.'],
  ['During a visit, how many learners should a mentor spot-check with the assessment tool?',['1 to 2','5 to 8','All of them','20 to 30'],1,'Spot-checking 5 to 8 learners verifies group placement and that ready learners are promoted.'],
  ['In the Bekele vignette, what is the highest-leverage coaching target?',['Replace the Picture Reading','Model the Basket Game for 3 minutes before the split and rotate across all three groups every 10 minutes','Reduce class size','Give the Story group more time'],1,'It fixes both missing modelling and unbalanced rotation, which also frees time for writing.']],
 m3:[
  ['How much should the teacher speak in a coaching dialogue, versus early directive mentoring?',['Teacher 70 to 80% in coaching; mentor 60 to 70% in directive mentoring','Teacher 20% in both','Equal in both','Mentor 90% in coaching'],0,'The balance of talk shifts as the teacher moves toward autonomy.'],
  ['Which is a leading question?',['What options have you considered for managing grouping?','Don\'t you think changing pupil groupings would solve your classroom management issue?','How did learners respond to the pacing?','What did you notice in the back row?'],1,'It implies the mentor already knows the answer and forces agreement.'],
  ['What does GROW stand for?',['Goal, Reality, Options, Wrap-up','Guide, Review, Observe, Write','Growth, Results, Outcomes, Work','Goal, Reflect, Observe, Watch'],0,'Wrap-up is the Will or Way forward: who will do what by when.'],
  ['A teacher says "My students know those letters; the assessment tool is just unfair." Best response?',['The data does not lie','Depersonalise it and test three children together right now','Cite other teachers\' results','Escalate to the principal'],1,'Sitting together to test three children lets both see exactly where learners get stuck.'],
  ['What is the final S in RESULTS?',['Support','Seize success','Summarise','Share data'],1,'Monitor weekly progress markers and publicly celebrate the milestone.']],
 m4:[
  ['What is the equal-rotation fallacy?',['Visiting every school once a month regardless of need','Rotating teachers between schools','Testing every child monthly','Equal budgets for all districts'],0,'Data-driven monitoring replaces passive equality with active equity.'],
  ['Which is NOT one of the four diagnostic questions?',['Baseline deficit audit','Progression velocity audit','Verification audit','Popularity audit'],3,'The four are baseline deficit, progression velocity, verification and environmental risk.'],
  ['In the triage case, which school is Priority 1 and why?',['Alpha, because the teacher is new','Beta, the largest cohort with only a 5 pp gain and Friday absenteeism','Gamma, strongest community','Delta, requested coaching'],1,'Beta has 280 learners and the slowest progression, leaving about 140 children at the lowest levels.'],
  ['Colour codes on the wall chart?',['Green Story, Blue Word, Yellow Letter, Red Beginner','Red Story, Blue Word, Yellow Letter, Green Beginner','Blue Story, Green Word, Red Letter, Yellow Beginner','Any colours'],0,'When a child is promoted the marker moves up in full view of the class.'],
  ['How often does Tier 2, cluster or zonal level, run its review cycle?',['Daily','Bi-weekly','Monthly','Annually'],1,'Tier 1 is daily and weekly, Tier 2 bi-weekly, Tier 3 monthly and termly.']],
 m5:[
  ['How many administrative tiers must be aligned for institutionalised support?',['Two','Three','Four: school, cluster or zonal, woreda or district, regional or national','Five'],2,'Mentoring is woven into statutory duties rather than relying on NGO project teams.'],
  ['Which is a design rule for cluster WhatsApp or Telegram groups?',['Use them for administrative complaints','Post a weekly challenge prompt every Monday','Only typed messages allowed','Only the mentor may post'],1,'Norms are positive and practice-focused, with weekly prompts and voice notes encouraged.'],
  ['How long is a teacher\'s action research cycle?',['1 week','4 weeks','A full year','2 terms'],1,'Identify the bottleneck, try an intervention, collect evidence, then reflect and share.'],
  ['What does the confidentiality clause of the Coaching Charter say?',['Reports go to the district weekly','Observations and debriefs stay developmental and are never used for punitive appraisal','Teachers may not discuss visits','Debriefs are public'],1,'This protects the psychological safety that mentoring relies on.']]
};

/* ---------- course content ---------- */
const MODS=[
{id:'m0',t:'Orientation',s:'Why mentoring is the decisive lever',c:0,L:[
 {id:'m0-1',t:'Why mentoring is the decisive lever in TaRL',min:8,res:['v_pratham','v_camal','r_site','r_jpal2','b_poor'],ref:'Think of the last reform in your district. What did you actually see in classrooms six weeks later?',html:`
<p>Millions of children sit in Grades 3, 4, 5 and beyond without basic foundational literacy and numeracy. Age-grade curricula march on regardless of whether a learner can recognise letters, decode simple words or do two-digit subtraction.</p>
<p>Teaching at the Right Level (TaRL) breaks that cycle. It groups children by their actual competence rather than age or grade, assesses every child one-on-one, and uses joyful, multi-sensory Combined Activities for Maximized Learning (CAMaL).</p>
<h3>Training alone is never enough</h3>
<p>Evaluations of TaRL across India and Africa show a clear pattern. Teachers return from a 5 or 10 day workshop to crowded classrooms, rigid timetables and administrative pressure, and they drift back to whole-class lecturing. Without sustained, empathetic, data-informed mentoring, classroom practice moves away from the programme design.</p>
<p>The mentor is the bridge between workshop theory and daily classroom fidelity. A good mentor is not a punitive inspector with a fault-finding checklist. The mentor is a trusted teacher-educator and co-inquirer who observes full lessons, models difficult activities live, facilitates reflective dialogue and uses learner progression data to direct support where children need it most.</p>
${C('Core principle of TaRL mentoring','Planning equals execution only when teachers receive continuous, non-judgmental, school-based support. Mentoring turns isolated teachers into confident facilitators and static baseline data into measurable gains in reading and mathematics.')}
<h3>Facilitator prompt: why training alone fails</h3>
<blockquote class="callout warn"><p>"Think back to the last major education reform or new teaching method in your district. Teachers attended a lively workshop, received manuals and clapped at the closing ceremony. Six weeks later, when you walked into their classrooms, what did you actually see?"</p><p>Why does that happen? Not because teachers are lazy, and not because the training was bad. Changing daily classroom habits is hard, uncertain work. When a teacher tries a Syllable Chart for the first time and the class gets noisy, anxiety spikes. Without a mentor beside them to say "Let's try that transition together", the teacher retreats to lecturing. Mentoring is the difference between a workshop that sits on a shelf and a methodology that changes children's lives.</p></blockquote>
<h3>Who this course is for</h3>
${UL(['School-based mentors: senior teachers and school directors','Cluster and zonal supervisors','Woreda and district education officers','NGO programme advisors'])}
<p>The manual draws on the Pratham and TaRL Africa CAMaL methodology, the OpenLearn Mentoring Continuum, Daloz\'s support and challenge matrix, Lofthouse\'s Practice Development Model, and the GROW and RESULTS coaching frameworks. It is adaptable across Sub-Saharan African and South Asian primary systems, including government-led scale-ups in Zambia, Kenya, Ethiopia and Uganda and refugee education settings.</p>
${C('How to use this course','Use the Listen bar at the bottom of any lesson to hear it read aloud, with the current paragraph highlighted. Each lesson ends with a reflection note, and each module ends with a quiz. Resource lists at the bottom of each lesson link to videos, free reading and books. Your progress and notes are saved in this browser.')}`},
 {id:'m0-2',t:'The 12 mentor competencies',min:8,res:['r_teams','r_olmind'],ref:'Which two competencies would most change your practice if you improved them this term?',html:`
<p>TaRL mentors have two jobs: pedagogical supporter and system monitor. To do both they build twelve competencies across four domains.</p>
${T(['Domain','Code','Competency','Observable field indicator'],[
['1. Pedagogical mastery and modelling','C1.1','TaRL methodology and CAMaL fluency','Accurately demonstrates all literacy and numeracy activities across Beginner, Word/Paragraph and Story levels.'],
['1','C1.2','One-on-one assessment integrity','Administers ASER/TaRL placement tools calmly and accurately; verifies teacher grouping accuracy.'],
['1','C1.3','Contextual and multilingual adaptation','Guides teachers in adapting activities for over-age learners, large pupil-teacher ratios and local mother tongues.'],
['2. Relational trust and mentoring stance','C2.1','Psychological safety and acculturation','Builds non-threatening rapport; eliminates punitive "judge mentoring"; fosters willingness to experiment.'],
['2','C2.2','Calibrated support and challenge','Applies Daloz\'s matrix to balance affirmation with stretch challenges based on teacher readiness.'],
['2','C2.3','Continuum navigation','Moves fluidly from directive apprenticeship (modelling) to non-directive coaching (facilitating reflection).'],
['3. Coaching dialogue and observation','C3.1','Collegial full-lesson observation','Observes full 45 to 60 minute sessions, tracking time-on-task and material use rather than superficial compliance.'],
['3','C3.2','Committed active listening','Listens with empathy, tolerates silence, avoids interrupting or imposing premature top-down fixes.'],
['3','C3.3','Structured coaching questioning','Uses GROW and RESULTS to ask open questions that empower teachers to diagnose and solve issues.'],
['4. Data triage and system governance','C4.1','Learner progression analytics','Interprets baseline, midline and endline group-movement tables to spot stagnation early.'],
['4','C4.2','Data-driven school prioritisation','Allocates scarce visit days to schools with the lowest levels or slowest growth.'],
['4','C4.3','Multi-tiered review and peer networks','Leads school and cluster review meetings and moderates WhatsApp or Telegram peer learning communities.']])}
<p>Modules 1 to 5 of this course map onto these domains: Module 1 builds the mentoring stance (Domain 2), Module 2 the pedagogical mastery (Domain 1), Module 3 the coaching dialogue (Domain 3), and Modules 4 and 5 the data and governance work (Domain 4).</p>`},
 {id:'m0-3',t:'Mentor self-audit',min:10,res:['r_olmind'],ref:'Which statement did you rate lowest, and what concrete evidence would show progress in 60 days?',html:`
<p>Rate your current proficiency from 1 (foundational, needs intensive practice) to 5 (exemplary, ready to coach peers). The manual asks you to complete this on Day 1, again on Day 5 afternoon, and after 60 days of field practice. Your ratings are saved here, so you can come back and update them.</p>
${W('audit')}`},
 {id:'m0-4',t:'The 5-day workshop and practice rollout',min:9,res:['r_class','r_assess'],ref:'How would you protect a daily practice class in your school or cluster timetable?',html:`
<p>A rigorous mentor programme combines a 5-day interactive workshop (08:30 to 12:30 and 13:30 to 17:00) with a mandatory 15 to 20 day practice phase. Before mentors ever coach a teacher, they must teach a real TaRL class themselves.</p>
${T(['Day','Morning','Afternoon','Daily deliverable'],[
['Day 1: Mentor mindset and foundations','1.1 Learning crisis and TaRL philosophy<br>1.2 Mentor vs inspector: eliminating judge mentoring<br>1.3 Mentor self-audit','1.4 The mentoring continuum<br>1.5 Daloz matrix and Lofthouse model','Completed self-audit and personal growth charter'],
['Day 2: Assessment integrity and grouping','2.1 One-on-one assessment protocol<br>2.2 Live simulation and inter-rater calibration','2.3 Interpreting data and forming dynamic groups<br>2.4 Managing high PTR and over-age learners','Calibrated assessment scoring sheet and grouping plan'],
['Day 3: TaRL lesson architecture','3.1 CAMaL principles<br>3.2 Whole-class warm-ups (informal talk, picture reading)','3.3 Level-wise literacy activities (Syllable Chart, Basket Game, Mind Map)<br>3.4 Level-wise numeracy (Bundles and Sticks, Number Chart)','Annotated 60-minute lesson observation rubric'],
['Day 4: Live micro-teaching and modelling','4.1 Micro-teaching round 1 (Beginner and Letter)<br>4.2 Peer critique using the collegial observation protocol','4.3 Micro-teaching round 2 (Word, Paragraph and Story)<br>4.4 Co-teaching and respectful in-lesson demonstration','Peer-validated micro-teaching feedback log'],
['Day 5: Coaching dialogue and data triage','5.1 Committed listening and open-question rewrites<br>5.2 Role-playing GROW and RESULTS debriefs','5.3 Data-driven school triage simulation<br>5.4 Multi-tiered governance and 30-day field action plan','30-day prioritised school visit and coaching action plan']])}
${C('Mandatory field immersion: the 15 to 20 day practice class rule','After the workshop, every newly trained mentor, including zonal supervisors and NGO officers, runs a daily 1-hour TaRL practice class for 15 to 20 consecutive school days before mentoring teachers. First, practising the full cycle of testing, grouping, teaching and re-testing builds craft knowledge. Second, seeing children progress under your own instruction builds the conviction and moral authority you need to coach teachers.')}`},
 {id:'m0-q',t:'Orientation quiz',min:5,quiz:'m0'}
]},
{id:'m1',t:'Module 1: Foundations of mentoring and adult learning',s:'Part 1 of the manual',c:1,L:[
 {id:'m1-1',t:'Defining mentoring and coaching',min:10,res:['r_olmind','r_hm','b_daloz','b_knight'],ref:'In your system, where do mentoring, coaching, supervision and monitoring get confused?',html:`
<p>Module purpose: shift your professional identity from administrative inspector to developmental teacher-educator, ground mentoring in adult learning theory, and give you frameworks for calibrating support and challenge. Estimated time in the workshop is 6 hours.</p>
<p>The terms mentoring, coaching, supervision and monitoring are often used interchangeably. That creates role ambiguity for school leaders and teachers, so clarity comes first.</p>
<p><b>Mentoring.</b> Hobson and Malderez (2013) define it as one-to-one support of a novice or less experienced practitioner by a more experienced one, designed to develop the mentee's expertise and induct them into the culture of the profession and the local school. In TaRL it applies whenever an instructor is new to level-based pedagogy, moving into a new facilitation role, or struggling with foundational routines.</p>
<p><b>Coaching.</b> Lofthouse et al. (2010) describe a collaborative, non-judgmental partnership that expands a practitioner's repertoire through structured experimentation and reflective dialogue. Coaches need not be senior; they bring questioning skills and pedagogical curiosity.</p>
${T(['Dimension','Mentoring stance','Coaching stance','Administrative inspection'],[
['Primary objective','Inducting into TaRL methodology, modelling core routines, building foundational confidence.','Refining craft, solving nuanced bottlenecks, fostering teacher agency.','Auditing compliance, checking attendance, grading teacher performance.'],
['Relationship and power','Experienced guide supporting a developing practitioner (high relational trust).','Equal co-inquirers exploring evidence together.','Hierarchical evaluator judging a subordinate.'],
['Dominant communication','Demonstrating ("watch how I do this"), explaining rationale, offering structured tips.','Asking open questions, active listening, prompting self-analysis.','Telling, directing, recording deficits on a scorecard.'],
['When used in TaRL','Weeks 1 to 4, or when a teacher struggles with basic grouping or activities.','Week 5 onward once routines are set, or with experienced facilitators.','Separate formal ministry or district audits; must be decoupled from mentoring.']])}`},
 {id:'m1-2',t:'The mentoring continuum',min:6,res:['r_olmind'],ref:'Think of a teacher you support. Which phase are they in, and how should your stance change?',html:`
<p>Teachers do not master TaRL overnight. Just as learners move from Beginner to Letter, Word, Paragraph and Story, teachers move through three developmental phases.</p>
${UL(['<b>Phase 1, Familiarisation (Weeks 1 to 3).</b> The teacher is learning the vocabulary, assessment tools, grouping rules and basic activity sequences. Cognitive load is high. The mentor gives close, structured support: co-planning, live modelling, and affirming small wins so the teacher feels safe taking risks.','<b>Phase 2, Consolidation (Weeks 4 to 8).</b> The teacher runs standard routines such as Picture Reading, Basket Game and Bundles and Sticks independently but struggles with pacing, multi-level differentiation or promoting fast learners. The mentor moves toward "practical theorising": asking why the teacher chose an activity and how learner data informs the next step.','<b>Phase 3, Autonomy and peer leadership (Week 9 onward).</b> The teacher adapts CAMaL activities fluidly, keeps accurate progression charts and invents local materials. The mentor becomes a critical friend, encourages action research and invites the teacher to host peer observations for colleagues.'])}
${C('Mentoring to coaching','The continuum is the reason the same mentor needs both stances. Directive modelling early, open questioning later. Competency C2.3 in the framework is exactly this movement.')}`},
 {id:'m1-3',t:'Three theoretical pillars of mentor practice',min:9,res:['v_wenger','r_wt','r_infed','r_schon','b_schon','b_lave'],ref:'Describe one moment in your own career that fits each pillar: apprenticeship, reflection, belonging.',html:`
<p>Drawing on teacher-education research (Cain, 2009; Lave and Wenger, 1991; Schön, 1987), effective mentors combine three complementary theories rather than relying on one.</p>
<h3>1. Learning through apprenticeship (Brown and McIntyre, 1993)</h3>
<p>Teaching involves hundreds of micro-decisions every hour. In the apprenticeship model the mentor is a master craftsperson who makes tacit expertise visible. When you step in to read a paragraph with clear voice modulation and finger-pointing, or settle five small groups in under 60 seconds, the teacher sees craft knowledge in action. Guard against creating a "mini-me": every demonstration must be followed by dialogue about the reasoning behind it.</p>
<h3>2. Learning by reflection (Dewey, 1933; Schön, 1987)</h3>
<p>Reflection connects principles such as active learner engagement to the messy reality of the classroom. Schön separates <b>reflection-in-action</b> (adjusting mid-lesson when learners look confused) from <b>reflection-on-action</b> (analysing afterwards why a group struggled). Mentors cultivate it by withholding immediate answers and asking catalytic questions: "What did you notice about the learners in the back row during the letter jump game? Why do you think that happened?"</p>
<h3>3. Professional identity in a community of practice (Lave and Wenger, 1991)</h3>
<p>Teachers develop lasting agency when they belong to a professional community. Newcomers move from "legitimate peripheral participation" to full membership through shared practice, mutual trust and peer collaboration. In TaRL, school teacher circles and cluster WhatsApp or Telegram groups are communities of practice where teachers share homemade flashcards, celebrate promotions and solve attendance problems together.</p>`},
 {id:'m1-4',t:'Balancing support and challenge: Daloz\'s matrix',min:10,res:['r_olbal','b_daloz','r_olmind'],ref:'Which quadrant do you slip into most often when you are busy, and what triggers it?',html:`
<p>Laurent Daloz (1989) showed that transformative adult learning needs a deliberate balance of two forces. <b>Support</b> means affirming the teacher's worth, listening with empathy and providing practical resources. <b>Challenge</b> means questioning habitual assumptions, introducing new techniques and raising expectations for learner progress. When either is out of balance, development stalls in one of four quadrants.</p>
${W('daloz')}
${T(['Quadrant','Support / challenge','Impact on the teacher','Mentor corrective action'],[
['1. Stasis','Low / low','Isolated and ignored; defaults to rote teaching; minimal learner growth.','Start with a warm relational check-in; co-plan one simple TaRL activity together.'],
['2. Retreat','Low support / high challenge','Result of judge mentoring or brutal inspection; teacher feels threatened, defensive or burned out.','Pause evaluative grading at once; validate strengths; co-teach a lesson side by side.'],
['3. Confirmation','High support / low challenge','Warm visits with lots of praise, but weak pedagogy and stagnant data go unaddressed.','Use learner midline data to introduce gentle dissonance; set one concrete stretch target.'],
['4. Growth (target)','High / high','High psychological safety with rigorous curiosity; the teacher experiments, reflects and accelerates.','Sustain collegial dialogue; encourage peer sharing and autonomous innovation.']])}`},
 {id:'m1-5',t:'Eliminating judge mentoring and observation trauma',min:8,res:['r_hm','r_olmind'],ref:'Which of the four observation types has your school experienced most? What would it take to make it collegial?',html:`
<p>Hobson and Malderez (2013) coined the term <b>judge mentoring</b> for mentors who rely too much on evaluating, grading and criticising. It destroys trust and triggers defensive compliance: teachers put on a show lesson when the supervisor arrives and revert to old habits when the supervisor leaves.</p>
<p>Love (2020) identifies four types of classroom observation. Two do active harm and two must be balanced.</p>
${UL(['<b>1. Absent observation (harmful).</b> Unannounced 5 to 15 minute drop-ins; the observer ticks boxes at the back and leaves without speaking to the teacher. It creates paranoia and teaches nothing.','<b>2. Brutal observation (harmful).</b> A one-way monologue listing every mistake with little empathy. It humiliates the teacher, crushes self-efficacy and triggers Daloz\'s Retreat quadrant.','<b>3. Collegial observation (the core TaRL standard).</b> An agreed full-lesson observation on a mutually chosen question, followed by an ungraded two-way conversation where the teacher explains choices and co-designs next steps. It builds trust and genuine skill transfer.','<b>4. Developmental inspection (periodic system check).</b> School-wide quality reviews by district or ministry teams that look at systemic trends and come with constructive recommendations and resources.'])}
${C('Keep inspection separate','Formal audits must be decoupled from mentoring. If teachers think a mentor visit feeds a performance appraisal, honest reflection stops.')}`},
 {id:'m1-6',t:'Lofthouse\'s model and the 12 principles of mentoring',min:10,res:['r_olmind','b_daloz'],ref:'Pick the principle you find hardest to live up to under pressure. What would help?',html:`
<p>Rachel Lofthouse (2018) sees mentoring as a hub of mutual professional learning, not one-way transfer from expert to novice. It runs in iterative cycles of <b>Plan, Do, Enquire and Review</b>. Institutional enablers (leadership support, protected timetable, shared values) and individual attributes (openness, ethical commitment) feed mentoring tools such as scaffolding, evidence collection and reframing. These produce a visible learning culture in which teachers <b>Articulate</b> their thinking, <b>Critique</b> evidence openly and <b>Expand</b> their repertoire.</p>
<p>To anchor daily conduct, mentors follow Dr Matthew Dicken's twelve principles.</p>
${T(['#','Principle','Meaning in TaRL field practice'],[
['1','Accountability and responsibility','Mentor and teacher honour agreed commitments, such as finishing baseline assessments on time and following through on action targets.'],
['2','Commitment and diligence','Mentor shows consistent presence and preparation; teacher prepares low-cost learning materials with diligence.'],
['3','Communication and co-operation','Formal debriefs and informal check-ins settle misunderstandings early and constructively.'],
['4','Understanding and relationship building','Genuine empathy for teachers\' heavy workload and resource limits.'],
['5','Encouragement and feedback','Authentic affirmation of strengths plus clear guidance on 1 to 2 growth areas.'],
['6','Trust and honesty','Teachers can admit an activity failed without fear of punitive reporting.'],
['7','Independence','Mentors resist over-controlling and scaffold teachers to own their decisions.'],
['8','Innovation and willingness to change','Both stay open to testing new local games, stories and grouping strategies.'],
['9','Integrity and excellence','Ethical standards; never falsify assessment scores while striving for every child to read.'],
['10','Motivation and driving force','Keep the moral purpose central: celebrate every child who moves from Beginner to Story.'],
['11','Reflection and evaluation','Protected time after lessons and at midline reviews to evaluate evidence and refine practice.'],
['12','Tolerance and respect','Respect for cultural perspectives, languages and professional dignity at all times.']])}`},
 {id:'m1-7',t:'Practice: calibrating support and rewriting feedback',min:20,res:['v_listen','b_kline'],ref:'Which of your usual feedback phrases sounds most like a judge statement? Rewrite it.',html:`
<p>These two workshop activities come straight from the manual. Try them yourself before you reveal the model answers. Writing your own answer first is what makes the model answer useful.</p>
${W('practice:sc11')}${W('practice:rw12')}
${C('Module 1 summary','Sustainable change cannot be mandated through inspection. It grows from psychological safety, calibrated support and challenge (Daloz, 1989), iterative cycles of inquiry (Lofthouse, 2018), and fluid movement along the mentoring to coaching continuum. Module 2 turns to the pedagogy you need to master in order to coach it.')}`},
 {id:'m1-q',t:'Module 1 quiz',min:6,quiz:'m1'}
]},
{id:'m2',t:'Module 2: Classroom pedagogy, assessment and observation rubrics',s:'Part 2 of the manual',c:2,L:[
 {id:'m2-1',t:'One-on-one assessment integrity',min:14,res:['r_assess','r_site','v_chan'],ref:'Where in your context might placement data be rushed or inflated, and how would you check?',html:`
<p>A mentor cannot coach what they cannot diagnose. Every TaRL intervention begins with sitting beside one child at a time for 3 to 5 minutes with a one-page tool to find out what the child can read and compute today. The placement test is a diagnostic compass, not an exam. If baseline data is rushed, done in groups or inflated to make a school look good, all grouping collapses and children are left on tasks far above their level.</p>
<p>On school visits, spot-check 5 to 8 learners per classroom to verify they are in the right group and that learners who mastered a level have been promoted.</p>
<h3>Literacy placement protocol</h3>
<p>The test is adaptive and starts at the Simple Paragraph, which saves time and respects older learners' dignity.</p>
${T(['Step','Facilitator action','Decision rule'],[
['1. Start at Simple Paragraph','Child reads a 4-sentence paragraph aloud while pointing with a finger.','Reads smoothly with 3 or fewer mistakes: go UP to Step 2. More than 3 mistakes or word-by-word: go DOWN to Step 3.'],
['2. Story level check','Child reads a 70 to 80 word story aloud, then answers 1 to 2 comprehension questions.','3 or fewer mistakes: STORY level. More than 3: PARAGRAPH level.'],
['3. Word level check','Show 5 familiar words (e.g. pot, sand, coat, rope, lock); child reads any 5.','At least 4 of 5 correct: WORD level. Fewer: go DOWN to Step 4.'],
['4. Letter level check','Show a grid of random letters; child names any 5 by sound or name.','At least 4 of 5: LETTER level. Fewer than 4: BEGINNER.']])}
<p>Try the protocol yourself with the simulator below.</p>
${W('place')}
<h3>Numeracy placement protocol</h3>
${T(['Step','Facilitator action','Decision rule'],[
['1. Start at subtraction','Two 2-digit subtraction problems with borrowing (e.g. 42 - 17; 63 - 28); child solves any two.','Both right: go UP to Step 2. Errors or cannot solve: go DOWN to Step 3.'],
['2. Division check','3-digit by 1-digit division (e.g. 432 ÷ 4; 756 ÷ 6); child solves one.','Correct: LEVEL 5 Division (Group 3). Not: LEVEL 4 Subtraction (Group 3).'],
['3. 2-digit recognition','Random grid of 2-digit numbers (19, 34, 57, 82, 96); child reads any 5.','At least 4 of 5: LEVEL 3 2-digit recognition (Group 2). Fewer: go DOWN.'],
['4. 1-digit recognition','Single digits 1 to 9 in random order; child reads any 5.','At least 4 of 5: LEVEL 2 1-digit recognition (Group 1). Fewer: LEVEL 1 Beginner (Group 1).']])}
<h3>Seven non-negotiable rules for auditing oral assessments</h3>
${OL(['Put the child at ease first: greet by name and ask a friendly non-academic question before showing the card.','Fold the sheet so only the section being tested is visible.','Strictly one-on-one: never test within earshot of children waiting in line, because they memorise the words.','Listen patiently without interrupting: allow 5 to 7 seconds when a child hesitates.','Offer a second chance: "Take a breath and try that line again."','Never scold or show disappointment; praise effort whatever the score.','Record immediately on the Classroom Learning Level Chart and check that wall charts match learner notebooks.'])}`},
 {id:'m2-2',t:'Grouping strategies and dynamic promotion',min:8,res:['r_class','v_zambia'],ref:'Which grouping model fits your classes (PTR), and what would a smooth 2-minute transition look like?',html:`
<p>A frequent failure in the field is applying one grouping blueprint to very different class sizes. Mentors help teachers choose between two models according to pupil-teacher ratio (PTR) and staffing.</p>
${T(['Dimension','Model A: heterogeneous (within one classroom)','Model B: homogeneous (across classes or high PTR)'],[
['Best context','Standard classes with 35 to 40 learners per facilitator, or single-stream rural schools.','Very large classes (55 to 60+) or multi-section grades that pool learners across classes.'],
['How learners sit','All levels sit together for the 10-minute warm-up, then split into three level corners.','Learners go straight to level-wise groups or separate rooms (e.g. Teacher 1 takes Beginner and Letter, Teacher 2 Word and Paragraph, Teacher 3 Story).'],
['Peer leaders','Heavy use of Story-level peer readers leading syllable drills and dictation while the teacher rotates.','Teacher gives targeted instruction to a uniform group, rotating between sub-tables of 8 to 10 learners.'],
['Mentor look-for','The teacher does NOT spend 100% of the time with the Story group while Beginners sit idle.','Learners move between rooms or zones in under 2 minutes without losing instructional time.']])}
<h3>The "no holding back" promotion rule</h3>
<p>TaRL is accelerated catch-up, not permanent tracking. Once a Beginner or Letter learner can reliably recognise letters and blend simple syllables, keeping them in Group 1 until the formal midline test wastes weeks. Verify on every visit that teachers do weekly 2-minute informal checks and promote ready learners immediately, celebrating it publicly on the Classroom Learning Level Chart.</p>`},
 {id:'m2-3',t:'CAMaL and the 60-minute lesson',min:10,res:['v_camal','r_class'],ref:'Which of the six CAMaL pathways is weakest in a class you know? What would strengthen it?',html:`
<p>Pratham's CAMaL rests on the idea that children acquire foundational literacy and numeracy fastest when several sensory-motor channels work together. During a 60-minute period you should see all six occurring naturally.</p>
${OL(['<b>Listening carefully.</b> Learners watch the speaker\'s face and lips: active comprehension, not passive hearing.','<b>Observing keenly.</b> They watch finger-tracking, posture, intonation and the step-by-step demonstration before trying.','<b>Speaking expressively.</b> They talk in full sentences in familiar language without fear of mockery.','<b>Doing hands-on.</b> They handle letter cards, jump on floor grids, arrange bundles and sticks, build mind maps.','<b>Reading aloud and silently.</b> They track text with the index finger and practise diction, voice and punctuation pauses.','<b>Writing daily.</b> Every child writes words, sentences or paragraphs, valuing expression and phonetic confidence over red-pen perfection.'])}
<h3>Pacing blueprint</h3>
<div class="phases nr" role="img" aria-label="Lesson timeline: 10, 5, 30, 10 and 5 minutes">
 <div style="flex:10;background:var(--c0)"><span>Warm-up</span><b>10</b></div>
 <div style="flex:5;background:var(--c2)"><span>Model</span><b>5</b></div>
 <div style="flex:30;background:var(--c3)"><span>Level groups</span><b>30</b></div>
 <div style="flex:10;background:var(--c4)"><span>Writing</span><b>10</b></div>
 <div style="flex:5;background:var(--c1)"><span>Wrap</span><b>5</b></div>
</div>
<p class="meta">Minutes per phase, drawn to scale.</p>
${T(['Phase','Time','Grouping','Core activity and teacher behaviour','Common error'],[
['1. Climate and whole-class warm-up','10 min','Whole class, all levels','Greeting, attendance, informal talk, storytelling or picture reading. Teacher models clear speech and invites quiet learners.','Warm-up drags to 25 to 30 minutes and starves group work.'],
['2. Modelling and transition','5 min','Whole class to level groups','Teacher shows the day\'s game or chart ("I do"), checks understanding, moves groups in under 90 seconds.','Vague verbal instructions without demonstration; noisy, confused transition.'],
['3. Level-specific practice (CAMaL)','30 min','Homogeneous small groups (B+L, W+P, Story)','Groups rotate through Syllable Chart, Basket Game, paragraph fluency, story comprehension. Teacher coaches each group in 10-minute cycles.','Teacher lectures from the board while all groups do the same worksheet.'],
['4. Individual application and writing','10 min','Individual','Every child writes in a notebook (copying, dictation, mind-map sentences, story summary). Teacher walks round checking.','Skipping writing, or only checking fast learners in the front row.'],
['5. Wrap-up and promotion check','5 min','Whole class','Two or three learners share writing or read aloud; teacher celebrates effort and updates progress notes.','Bell rings abruptly with no closure or feedback.']])}`},
 {id:'m2-4',t:'Literacy activity mastery and look-fors',min:10,res:['r_class','v_camal','v_chan'],ref:'Choose one activity. What exactly would you say and do in a 5-minute live demonstration?',html:`
<p>When observing level-specific literacy sessions, use this guide to judge quality and, if a teacher struggles, step in for a brief 5-minute live demonstration.</p>
${T(['Level','Activity','Gold-standard look-fors','Live mentor modelling move'],[
['Whole class (all levels)','Picture reading and role-play','Teacher passes a clear, culturally familiar picture; elicits single words first, then full sentences; small groups act out a 2-minute scene.','Model open sensory questions ("What sounds would you hear inside this market scene?") to spark imagination.'],
['Beginner and Letter','Syllable / Barakhadi chart reading','Teacher points while reading horizontally, vertically, diagonally and backwards so children see syllable patterns rather than memorising song order; learners build words from two syllables.','Demonstrate zigzag pointing; invite two shy learners to point with a stick while peers read.'],
['Beginner and Letter','Basket game and letter jump','Children sit in a circle singing a rhyme and passing a basket of lowercase letter cards; when the song stops, the holder picks a card, sounds it and names a word starting with that sound.','Model enthusiastic pacing; show how to gently scaffold a child who forgets the sound rather than letting peers shout the answer.'],
['Word and Paragraph','Mind map and sentence building','Teacher writes a theme word (e.g. Water, Market); learners brainstorm related words, organise them visually and write 2 to 3 original sentences.','Show how to turn brainstormed nouns into action verbs and full sentences on the board.'],
['Word and Paragraph','Ideal reading and peer tracking','Teacher reads a 4-line paragraph expressively while every child tracks with an index finger; children critique the teacher\'s reading before practising.','Read the paragraph twice, once poorly (monotone, too fast) and once expressively, and ask learners to spot the difference.'],
['Story','70 to 80 word story and "What next?"','Learners read longer narratives, infer vocabulary from context, answer why and how questions, and write an alternative ending.','Prompt the teacher to move from literal recall ("What was the boy\'s name?") to inferential questions ("Why did he feel afraid?").']])}`},
 {id:'m2-5',t:'Numeracy: Concrete, Pictorial, Abstract',min:7,res:['r_class','r_site'],ref:'How would you demonstrate borrowing in 63 - 28 using only sticks and string?',html:`
<p>In TaRL numeracy, children fail when forced to memorise abstract vertical algorithms before they understand place value. Mentors check that teachers follow Concrete, then Pictorial, then Abstract.</p>
${UL(['<b>Group 1 (Beginner and 1-digit recognition).</b> Learners count physical stones, bottle caps or sticks (1 to 9), match quantities to number cards, play Number Jump on floor grids and trace digits in sand or notebooks.','<b>Group 2 (2-digit recognition and place value).</b> Learners tie 10 loose sticks into one bundle of ten with a rubber band or string. The teacher dictates a number, e.g. 34, and learners show 3 bundles and 4 loose sticks before writing "34" on the slate.','<b>Group 3 (subtraction with borrowing, and division).</b> Teachers show borrowing physically by untying one bundle of ten into 10 loose sticks when subtracting (e.g. 42 - 17). After concrete mastery, learners draw bundle and stick icons (pictorial) and finally solve standard vertical equations (abstract).'])}`},
 {id:'m2-6',t:'Inclusive and multilingual adaptations',min:8,res:['v_zambia','r_action','r_i1d'],ref:'Which adaptation matters most in your setting, and what low-cost material could you make this week?',html:`
<p>In emergencies, refugee settlements and rural catch-up contexts (for example Uganda's West Nile settlements, Ethiopia's Oromia, Afar and Amhara regions, or rural Zambia), TaRL classrooms often hold adolescents aged 12 to 19 beside 8-year-olds, and children learning in a second language. Mentors coach teachers on four adaptations.</p>
${OL(['<b>Protect adolescent dignity.</b> Older non-readers know they are behind and feel acute shame if treated like toddlers. Use age-respectful themes such as markets, farming, health and community leadership rather than babyish rhymes.','<b>Bridge mother tongue and language of instruction.</b> Where children speak a home language (e.g. Afaan Oromoo, Lugbarati, Kiswahili, Nuer, Dinka) different from the school language, anchor oral warm-ups and phonics comparisons in the familiar language first.','<b>Trauma-informed psychological safety.</b> Displaced learners may show hypervigilance or withdrawal. Cooperative small-group games, predictable routines and zero corporal or verbal punishment make the TaRL hour a safe, healing space.','<b>Low-cost local materials.</b> Where printed kits are scarce, organise school-level TLM workshops where teachers and volunteers craft letter cards from cardboard cartons, bundles from twigs and floor grids with charcoal or chalk.'])}`},
 {id:'m2-7',t:'The 4-point observation rubric',min:18,res:['r_class','r_mon'],ref:'After scoring the vignette, which one coaching goal would you actually choose, and why not two?',html:`
<p>Use the rubric not to grade or penalise teachers but to build a shared, objective picture of classroom practice and to choose 1 to 2 high-leverage coaching goals for the debrief.</p>
${T(['Domain','Level 1: Traditional / absent','Level 2: Emerging TaRL','Level 3: Proficient TaRL','Level 4: Exemplary TaRL'],[
['1. Assessment and grouping fidelity','Learners sit by age or grade; no Learning Level Chart; whole class taught as one unit.','Chart is posted but 25%+ of learners are misgrouped or never promoted.','Learners accurately grouped; chart updated monthly; peer readers assist groups.','Dynamic, accurate grouping; weekly checks promote learners immediately; zero stigma.'],
['2. Lesson structure and pacing','100% teacher lecture; no warm-up or rotation; learners copy passively.','Whole-class warm-up exceeds 20 minutes, leaving rushed group practice and no writing.','Balanced 10-minute warm-up, 30-minute group practice and 10-minute individual writing; smooth transitions.','Seamless transitions under 90 seconds; all six CAMaL pathways active; teacher rotates systematically.'],
['3. Activity execution and TLMs','No TaRL materials; relies on textbook or rote choral chanting.','Charts and cards are held only by the teacher; activities mechanical with no clear modelling.','Teacher models ("I do") clearly; learners handle syllable grids, letter cards or bundles and sticks.','Joyful, multi-sensory mastery; teacher adapts games creatively and scaffolds struggling learners.'],
['4. Climate and inclusion','Harsh tone, public criticism, older or quiet learners ignored.','Polite, but a few confident boys dominate responses and games.','Warm tone; teacher calls on quiet learners and girls equally; familiar language used.','High psychological safety; over-age and vulnerable learners hold leadership roles and take risks.']])}
${W('practice:vig27')}`},
 {id:'m2-q',t:'Module 2 quiz',min:7,quiz:'m2'}
]},
{id:'m3',t:'Module 3: Coaching conversations and active listening',s:'Part 3 of the manual',c:3,L:[
 {id:'m3-1',t:'Anatomy of a coaching conversation',min:7,res:['b_chel','b_knight'],ref:'In your last debrief, who did most of the talking? What would change if the teacher talked 70%?',html:`
<p>Module purpose: move from advice-giving expert to facilitator of reflective dialogue. Estimated time in the workshop is 6 hours.</p>
<p>Even when you observe accurately, a poor debrief can fracture the relationship. Telling a teacher "Here is what you did wrong and what you must do tomorrow" shuts down reflection and breeds compliance rather than agency.</p>
<p>According to Cheliotes and Reilly (2010), a professional coaching dialogue has three defining features: (1) a clear, agreed purpose; (2) a strict focus on the coachee and their strengths and challenges; and (3) the aim of securing genuine professional development and sustainable change.</p>
<p>In Weeks 1 to 3 a beginner teacher needs a directive stance: you explain routines, model phonics games and give concrete tips. As confidence grows you deliberately shift, creating space for the teacher to examine practice, analyse learner evidence and discover solutions independently.</p>
${T(['Dimension','Directive mentoring (early)','Coaching dialogue (consolidation and autonomy)'],[
['Who speaks most','Mentor 60 to 70% of the time (explaining, demonstrating, instructing).','Teacher 70 to 80% (reflecting, analysing, proposing).'],
['Nature of input','Prescriptive: "Here is how you organise the Basket Game step by step."','Inquisitive: "What did you observe when learners tried to form words from the syllable chart?"'],
['Source of solutions','Provided by the mentor from craft knowledge.','Generated by the teacher through structured questioning.'],
['Emotional climate','Supportive instruction; reassurance against overwhelm.','Professional partnership; intellectual stretch and shared problem-solving.']])}`},
 {id:'m3-2',t:'The art of committed active listening',min:8,res:['v_listen','b_kline'],ref:'Try holding a 7-second silence in your next conversation. What happened?',html:`
<p>After you ask a reflective question, the critical skill is complete, uncompromised listening: not interrupting, not finishing the teacher's sentences, not building counter-arguments while they speak (Whitmore, 2010; Edge, 2015). Committed listening shows that the teacher's professional judgement is respected.</p>
${OL(['<b>Empathetic presence and body language.</b> Open posture, leaning slightly forward, nodding, no glances at your watch or phone.','<b>Tolerating productive silence.</b> After a deep question such as "Why do you think the Word group finished 10 minutes early?", teachers often pause 5 to 10 seconds to think. Inexperienced mentors panic and answer their own question. Effective coaches hold the silence.','<b>Non-judgmental mirroring.</b> Reflect back the core of what was said without editorial: "So you felt the transition between warm-up and small groups took longer than expected because learners were confused about where to sit."'])}`},
 {id:'m3-3',t:'Transforming questions into inquiry',min:12,res:['b_chel','r_growpdf'],ref:'Write down three questions you asked in your last debrief. Which type were they?',html:`
<p>The quality of a coaching dialogue depends almost entirely on the quality of the questions. Leading, loaded or closed questions shut down thinking and carry hidden judgements (Fletcher, 2012).</p>
${T(['Type','Flawed question','Why it undermines confidence','Open coaching question'],[
['Leading','"Don\'t you think changing pupil groupings would solve your classroom management issue?"','Implies the mentor already knows the answer and forces agreement.','"What options have you considered for managing grouping dynamics in that class?"'],
['Loaded or biased','"Have you thought about giving pupils more thinking time instead of rushing them?"','A sharp criticism disguised as polite inquiry.','"How do you feel students responded to the pacing of questions today?"'],
['Closed yes/no','"Are you aware of the range of Assessment for Learning techniques we use?"','Invites a defensive one-word answer and stops reflection.','"Which assessment techniques helped you gauge student understanding during the lesson?"'],
['Judgmental','"Would you agree that your plenary needs complete redesigning?"','Harsh evaluation that triggers immediate defensiveness.','"Looking back at the end of the lesson, how effective was the wrap-up in confirming what learners mastered?"']])}
${W('practice:q33')}`},
 {id:'m3-4',t:'Scaffolding dialogue with the GROW model',min:12,res:['v_grow','v_grow2','v_growdemo','r_growpdf','b_whit'],ref:'Plan a GROW debrief for a real lesson. Write one question for each of G, R, O and W.',html:`
<p>GROW comes from executive coaching (Whitmore, 2010) and was adapted for educational leadership (Fletcher, 2012). It is a simple four-step structure for post-lesson debriefs.</p>
${UL(['<b>G, Goal setting.</b> Fix the focus of the conversation. What does the teacher want to achieve or improve?','<b>R, Reality check.</b> Explore what actually happened, using evidence from learners and notebooks.','<b>O, Options.</b> Brainstorm several strategies without filtering or judging too early.','<b>W, Wrap-up (will, way forward).</b> Agree a concrete, achievable plan: who will do what by when.'])}
<h3>Complete verbatim GROW transcript</h3>
<p>Context: a mentor and a teacher sit down 15 minutes after a Grade 3 TaRL session in which the teacher struggled to keep the Beginner group engaged during independent practice.</p>
${DLG([
['M','Good afternoon, Teacher Sara. Thank you for welcoming me into your classroom today. How are you feeling after that session?'],
['T','I\'m a bit exhausted, to be honest. The Beginner group got very restless halfway through the independent work.'],
['M','I noticed that moment. Let\'s make that our focus today. [Goal] When the restlessness started, what was happening in the classroom? [Reality]'],
['T','Well, I had just moved the Word group to their reading task and turned to explain the Syllable Chart to the Beginners. But two children in the back started playing with sticks, and within two minutes the whole table was off-task.'],
['M','Right. You had dual demands at that exact minute. When you reflect on that transition, what options might you have to stop the Beginner group stalling while you set up the Word group? [Options]'],
['T','I suppose I could have prepared a quick matching game on the slate for the Beginners before I turned away, or I could have asked a trusted Story-level peer reader to hand out the cards.'],
['M','Those are both strong pathways. Which of those two feels most realistic for you to test tomorrow? [Options refinement]'],
['T','I will use a peer reader from the Story group to manage card distribution for the Beginners, and I will write the first instruction clearly on the board before dividing the groups.'],
['M','Excellent. Let\'s lock that in as our target for tomorrow. I will drop in for the first 15 minutes to see how smoothly that transition runs. [Wrap-up] Sound good?'],
['T','Yes, that makes me feel much more prepared. Thank you.']])}
${C('Notice','The mentor never says what the teacher should do. The teacher proposes both options, and the mentor\'s only additions are a follow-up commitment and a time to return.')}`},
 {id:'m3-5',t:'The RESULTS model',min:7,res:['b_results'],ref:'Which stagnant result in your area could you tackle with RESULTS?',html:`
<p>For complex or systemic challenges, such as stagnant midline data or chronic absenteeism, use the <b>RESULTS</b> model from Kee et al. (2010).</p>
${UL(['<b>R, Resolve to change results.</b> A mutual decision that current learner outcomes must improve.','<b>E, Establish goal clarity.</b> Pinpoint the exact gap, e.g. "Moving 15 Letter-level learners into Word-level blending."','<b>S, Seek integrity.</b> Build open trust and ethical accountability between mentor and teacher.','<b>U, Unveil multiple pathways.</b> Brainstorm interventions, e.g. daily 15-minute intensive phonics, peer tutoring pairs.','<b>L, Leverage options.</b> Choose the highest-impact, lowest-cost intervention that fits the school calendar.','<b>T, Take action.</b> Carry out the agreed plan with energy and precision.','<b>S, Seize success.</b> Track weekly progress markers and celebrate publicly when the milestone is reached.'])}`},
 {id:'m3-6',t:'Handling resistance and difficult debriefs',min:9,res:['v_listen','b_kline'],ref:'Recall a difficult debrief. Which resistance type was it, and how would you respond now?',html:`
<p>Not every debrief goes smoothly. You will meet resistance rooted in fear, fatigue or professional pride. Effective coaches do not argue or pull rank; they de-escalate.</p>
${T(['Resistance','Underlying root','Flawed response (avoid)','De-escalating response (model)'],[
['Defensiveness: "You don\'t understand how difficult my students are."','Fear of inadequacy, embarrassment, feeling judged.','Arguing back with statistics or rules: "Other teachers manage fine."','Validate the pressure: "You are carrying a massive class size and attendance is unpredictable. Let\'s look at what is within our control to ease that pressure."'],
['Passive compliance: "Yes... okay... whatever you say."','Learned helplessness, burnout or fear of authority.','Accepting empty agreement with no intent to change.','Pause, lower your tone: "I notice you seem hesitant. What part of this suggestion feels unrealistic or difficult to implement in your classroom tomorrow?"'],
['Data denial: "My students know those letters; the assessment tool is just unfair."','Dissonance between perceived effort and poor results.','Insisting: "The data doesn\'t lie; your children failed."','Depersonalise the data: "Assessment tests can be stressful for children. Let\'s test three children right now so we can both see exactly where they get stuck."'],
['Overwhelmed burnout: "I have too much paperwork and marking to do TaRL."','Administrative overload and no planning time.','Dismissing feelings: "We all have paperwork; just get it done."','Pivot to triage: "Let\'s pause all non-essential paperwork this week. What is the single most important TaRL activity we can protect during your 60-minute block?"']])}`},
 {id:'m3-7',t:'Workshop role-play',min:20,res:['v_growdemo','b_whit'],ref:'After the role-play, what was the hardest thing about staying in the coach role?',html:`
<p>In the workshop you spend about 45 minutes on paired role-play with scenario cards. One participant plays the teacher, another plays the coach using GROW, and observers score active listening and open questioning. You will need a timer and an observation sheet.</p>
${W('practice:rp37')}`},
 {id:'m3-q',t:'Module 3 quiz',min:6,quiz:'m3'}
]},
{id:'m4',t:'Module 4: Data-driven monitoring and triage',s:'Part 4 of the manual',c:4,L:[
 {id:'m4-1',t:'The fallacy of fixed inspection schedules',min:7,res:['r_mon','r_teams'],ref:'How are visit days allocated in your zone today? What does the data say about whether that is fair?',html:`
<p>Module purpose: shift from routine-bound visitor to strategic data analyst who directs support to schools with the greatest deficits and slowest progress. Estimated workshop time is 5 hours.</p>
<p>Many systems instruct supervisors to visit every school once every thirty days, in alphabetical or numerical order. This "equal-rotation fallacy" ignores the logic of targeted instruction. School A, where 95% of learners already read stories and teachers run flawless CAMaL, gets the same visits as School B, where novice teachers struggle with grouping and 80% of children remain at Beginner level.</p>
<p>Data-driven monitoring replaces passive equality with active equity. Every time you review monitoring logs, ask four diagnostic questions.</p>
${OL(['<b>Baseline deficit audit.</b> Which schools started with the highest share of non-readers and non-computers?','<b>Progression velocity audit.</b> Between baseline and midline, which schools show the slowest percentage-point movement out of Beginner and Letter?','<b>Verification audit.</b> Which previously coached schools need urgent follow-up to check that agreed action targets were carried out?','<b>Environmental risk audit.</b> Which schools face shocks such as sudden teacher turnover, high absenteeism or overcrowding that need immediate co-teaching?'])}`},
 {id:'m4-2',t:'Learner progression analytics',min:8,res:['r_mon','r_kobo'],ref:'Which of the three KPIs is easiest for you to calculate from your current records?',html:`
<p>TaRL impact is measured by the rate at which children move from lower to higher competence groups, not only by test scores on one day. A progression matrix tracks cohort movement across three windows: <b>Baseline</b> (Month 1), <b>Midline</b> (Month 3) and <b>Endline</b> (Month 5).</p>
<p>Three key performance indicators matter when you read a school's matrix.</p>
${OL(['<b>Beginner reduction rate.</b> What percentage of children classified Beginner at baseline have reached Letter or Word level by midline?','<b>Bottleneck identification.</b> Are children piling up in one tier, for example stuck at Letter level for months without blending syllables? If so, coach on Syllable Chart and Basket Game fidelity.','<b>Equity of progression.</b> Are girls and over-age learners advancing as fast as younger boys, or are vulnerable groups lagging?'])}
${C('Percentage-point gain','Gain in percentage points is the baseline percentage at Beginner/Letter minus the midline percentage. A school that moves from 55% to 50% has gained only 5 pp, however large it is.')}`},
 {id:'m4-3',t:'Triage simulation: allocating scarce mentor time',min:15,res:['r_mon','r_jpal3'],ref:'Which fact in the table changed your mind the most, and what extra data would you ask for?',html:`
<p>You are a zonal education supervisor with 5 cluster schools and only 2 mentor visit days this week because of regional meetings. Examine the midline literacy progression summary below, pick the two schools to visit first and defend your choice with evidence.</p>
${W('triage')}`},
 {id:'m4-4',t:'Multi-tiered governance and review cadence',min:7,res:['r_teams','r_mon'],ref:'Which tier in your system is weakest, and what single change would strengthen it?',html:`
<p>Data-driven monitoring cannot become a top-down police action. It needs a synchronised cadence that links school, cluster and district.</p>
${T(['Tier','Frequency','Key actors','Core monitoring and data actions'],[
['Tier 1: School','Daily and weekly','School director, senior teachers, TaRL instructors','Update Classroom Learning Level Wall Charts weekly; do 2-minute informal checks; review weekly attendance.'],
['Tier 2: Cluster / zonal','Bi-weekly','Cluster supervisors, zonal in-charges, peer mentors','Visit priority schools using data triage; moderate cluster WhatsApp or Telegram groups; share homemade TLMs.'],
['Tier 3: Woreda / district','Monthly and termly','District education officers, NGO programme advisors','Aggregate school midline data into district dashboards; host monthly review meetings; reallocate mobile mentoring teams.']])}`},
 {id:'m4-5',t:'Low-cost digital and paper tracking tools',min:7,res:['r_kobo','r_mon'],ref:'Sketch the wall chart you would put up in a real classroom. How would learners see their own progress?',html:`
<p>Where internet and computers are unreliable, paper dashboards are powerful. Every TaRL classroom keeps a <b>Classroom Learning Level Wall Chart</b>: each student's name beside a colour-coded level marker.</p>
<div class="phases nr" role="img" aria-label="Level colours: Red Beginner, Yellow Letter, Blue Word, Green Story" style="min-height:64px">
 <div style="flex:1;background:var(--c1)"><span>Beginner</span><b>Red</b></div>
 <div style="flex:1;background:var(--c2)"><span>Letter</span><b>Yellow</b></div>
 <div style="flex:1;background:var(--c3)"><span>Word</span><b>Blue</b></div>
 <div style="flex:1;background:var(--c4)"><span>Story</span><b>Green</b></div>
</div>
<p>When a child is promoted, the marker moves up in full view of the class, so progress is public and celebrated.</p>
<p>For district and NGO management, mentors aggregate school data into simplified Excel or KoboToolbox templates that calculate percentage-point gains automatically and rank schools by vulnerability.</p>
${C('Module 4 takeaway','Data does not replace judgement. It tells you where to spend your scarce visit days, and then Modules 1 to 3 tell you what to do when you get there.')}`},
 {id:'m4-q',t:'Module 4 quiz',min:5,quiz:'m4'}
]},
{id:'m5',t:'Module 5: Governance, communities of practice and field toolkit',s:'Part 5 of the manual',c:5,L:[
 {id:'m5-1',t:'Synchronising institutionalised support loops',min:7,res:['r_zam','v_zambia','r_action','r_fln'],ref:'Which statutory duties in your system could carry TaRL mentoring after project funding ends?',html:`
<p>Reform cannot depend forever on external NGO teams or isolated champions. National scale, as in government-led rollouts in Zambia (Catch-Up), Côte d'Ivoire (TREES) and regional districts in Ethiopia, requires mentoring to be woven into the statutory duties of existing education administration. That takes alignment across four tiers.</p>
${OL(['<b>School tier (daily / weekly).</b> Principals and senior teachers protect the 60-minute TaRL timetable, keep learning level charts and hold weekly huddles to review promotion data.','<b>Cluster / zonal tier (bi-weekly).</b> Supervisors and in-charges run data-driven priority visits, moderate peer networks and host bi-weekly reflection meetings.','<b>Woreda / district tier (monthly).</b> Officers aggregate midline progression, review district gains and reassign mobile mentoring teams to lagging schools.','<b>Regional / national tier (termly / annually).</b> Bureaus and ministries review impact evaluations, align curriculum policy with targeted instruction and sustain budgets for mentor transport and training.'])}`},
 {id:'m5-2',t:'Peer learning networks and WhatsApp communities',min:8,res:['v_cop','v_wenger','r_wt','b_ccop'],ref:'Draft your first three Monday challenge prompts for a cluster group.',html:`
<p>Geographic isolation is one of the greatest hazards for rural TaRL teachers. When a teacher meets a stubborn bottleneck, for example engaging 60 children in syllable practice, a local peer network gives immediate psychological and practical relief.</p>
<p>Mentors establish and moderate cluster WhatsApp or Telegram professional learning communities (PLCs). Three design rules make them work.</p>
${OL(['<b>Positive, practice-focused norms.</b> The platform is for photos of homemade TLMs, 30-second clips of successful games and peer problem-solving, never administrative complaints.','<b>Weekly challenge prompts.</b> Post a prompt every Monday, e.g. "Share a photo of how you organised your Word group today!"','<b>Audio-visual storytelling.</b> Encourage short voice notes about a breakthrough with a struggling learner, valuing oral communication over long typing.'])}`},
 {id:'m5-3',t:'Action research for continuous improvement',min:8,res:['v_ar','v_ar2','b_mertler','r_comm'],ref:'Write your own puzzling bottleneck as a question, and one 2-week intervention you could test.',html:`
<p>Action research makes teachers systematic inquirers into their own classrooms. Instead of waiting for outside researchers, they run short 4-week cycles.</p>
${OL(['<b>Identify the puzzling bottleneck.</b> E.g. "Why are my Letter-level learners taking twice as long to reach Word level as last term?"','<b>Formulate an intervention.</b> E.g. a 10-minute daily competitive Syllable Bingo game for two weeks.','<b>Collect evidence.</b> Track weekly formative scores and engagement logs.','<b>Reflect and share.</b> Decide whether the intervention accelerated learning, and share findings at the next cluster meeting.'])}`},
 {id:'m5-4',t:'Field toolkit: observation form, logbook and charter',min:12,res:['r_mon','r_kobo'],ref:'Which parts of these forms would you change for your own context?',html:`
<p>These are the manual's printable templates (Appendices A to C). Use the copy button under each to paste it into a document, a phone note or a messaging app and fill it in there.</p>
<h3>Appendix A: Master classroom observation checklist</h3>
${T(['Field','Record / verification details'],[
['School name and location','______________________'],['Teacher name and grade','______________________'],['Observer / mentor name','______________________'],
['Date and lesson duration','Date: ________ Start: ______ End: ______'],['Total pupils enrolled / present','Enrolled: ____ Present: Boys ____ Girls ____'],
['1. Assessment and grouping','Learning Level Chart visible? [Yes / No]  Accurate groups? [Yes / No]'],
['2. Pacing and time-on-task','Warm-up mins: ___  Group work mins: ___  Writing mins: ___'],
['3. CAMaL activities active','[ ] Listening [ ] Observing [ ] Speaking [ ] Doing [ ] Reading [ ] Writing'],
['4. Material usage (TLMs)','Are low-cost materials actively handled by learners? [Yes / No]'],['5. Agreed coaching target','______________________']])}
<div class="nr"><button class="btn ghost sm" data-copy="A">Copy Appendix A</button></div>
<h3>Appendix B: Mentor visit logbook</h3>
${T(['Visit date','School','Teacher coached','Focus of debrief (GROW)','Agreed action target','Next follow-up date'],[['','','','','',''],['','','','','','']])}
<div class="nr"><button class="btn ghost sm" data-copy="B">Copy Appendix B</button></div>
<h3>Appendix C: Coaching agreement and professional growth charter</h3>
${T(['Clause','Commitment statement'],[
['Mutual purpose','To collaborate as professional partners dedicated to accelerating foundational literacy and numeracy for every child.'],
['Confidentiality','All classroom observations and post-lesson debriefs remain strictly confidential and developmental, never used for punitive appraisal.'],
['Open communication','Both mentor and teacher commit to honest reflection, active listening and respectful feedback.'],
['Action commitment','Both parties honour agreed co-created action targets and maintain consistent follow-through.'],
['Signatures','Mentor: ________________  Teacher: ________________']])}
<div class="nr"><button class="btn ghost sm" data-copy="C">Copy Appendix C</button> <span id="copied" aria-live="polite" class="meta"></span></div>`},
 {id:'m5-5',t:'Global resource compendium and next steps',min:8,res:['r_site','r_evid','r_jpal','r_jpal2','r_ol','r_olmind','r_i1d','r_comm','b_poor','b_whit','b_daloz','b_schon','b_lave'],ref:'Write your 30-day plan: which 3 schools, which 3 coaching targets, which first practice class date?',html:`
<p>Appendix D of the manual points to four global repositories: the TaRL Africa website (toolkits, guides, webinars, case studies), J-PAL and Pratham research (randomised trials of targeted instruction), OpenLearn's open-access mentoring modules, and Imagine 1day's Ethiopia programme portfolios.</p>
<p>This course adds videos, free reading and books to every lesson. The full collection for this lesson is below, including the books the manual's frameworks come from. If you want a place to begin, watch the Pratham CAMaL video, read the TaRL assessment and monitoring pages, then read the Hobson and Malderez paper on judge mentoring.</p>
${C('Your 30-day plan','Start your practice class (15 to 20 days). Rate yourself on the self-audit again after 60 days. Choose your priority schools with the four diagnostic questions, and agree 1 to 2 SMART targets per teacher, never a long list.')}`},
 {id:'m5-q',t:'Module 5 quiz',min:5,quiz:'m5'}
]},
{id:'fin',t:'Final assessment and certificate',s:'Show what you have learned',c:0,L:[
 {id:'fin-1',t:'Final assessment and certificate',min:15,final:1,res:[],html:`
<p>The final assessment draws 12 questions at random from all the module quizzes. You need 70% or higher to pass. When you have also completed every lesson, you can add your name and generate your certificate of completion.</p>
${W('final')}`}
]}
];
const ALL=[];MODS.forEach(m=>m.L.forEach(l=>{l.mod=m;ALL.push(l)}));
const COUNTED=ALL.filter(l=>!l.final);

/* ---------- navigation ---------- */
const main=$('#main'), side=$('#side');
let cur='home';
function pct(){const n=COUNTED.filter(l=>S.done[l.id]).length;return Math.round(100*n/COUNTED.length)}
function updateProg(){const p=pct();$('#pct').textContent=p+'% complete';$('#pfill').style.width=p+'%';$('#pbar').setAttribute('aria-valuenow',p)}
function buildNav(){
  side.innerHTML=MODS.map(m=>`<details ${cur!=='home'&&ALL.find(l=>l.id===cur)?.mod===m||(cur==='home'&&m.id==='m0')?'open':''}><summary><i class="sw" style="background:var(--c${m.c})"></i><span>${m.t}</span></summary>${m.L.map(l=>`<a class="li" href="#${l.id}" data-id="${l.id}" ${l.id===cur?'aria-current="page"':''}><i class="ck ${S.done[l.id]?'on':''}">${S.done[l.id]?'✓':''}</i><span>${l.t}</span></a>`).join('')}</details>`).join('');
}
function go(id,noHash){
  stopAudio();cur=id;
  if(!noHash)location.hash=id==='home'?'':id;
  document.body.classList.remove('menu');$('#menuBtn').setAttribute('aria-expanded','false');
  if(id==='home')renderHome();else renderLesson(ALL.find(l=>l.id===id)||ALL[0]);
  buildNav();updateProg();window.scrollTo(0,0);
  $('#audio').hidden=(id==='home');if(id!=='home')prepAudio();
}
function renderHome(){
  const mins=COUNTED.reduce((a,l)=>a+l.min,0), p=pct();
  const next=COUNTED.find(l=>!S.done[l.id])||ALL[0];
  main.innerHTML=`<div class="hero" id="body"><div class="crumb">Coaching, mentoring and data-driven monitoring</div><h1>TaRL Mentor Academy</h1>
  <p class="lead">An online course for school mentors, supervisors and district officers, built from the five-part Master Facilitator and Mentor Training Manual. Every lesson can be read aloud, and links to videos, free reading and books.</p>
  <div class="stats nr"><div><b>${MODS.length-2}</b><span>modules plus orientation</span></div><div><b>${COUNTED.length}</b><span>lessons and quizzes</span></div><div><b>${Math.round(mins/60*10)/10}</b><span>hours of study</span></div><div><b>${Object.keys(RES).length}</b><span>curated resources</span></div></div>
  <p class="nr"><button class="btn" id="startBtn">${p?'Continue: '+esc(next.t):'Start the course'}</button></p>
  <div class="cards nr">${MODS.map(m=>`<button class="card" style="--cc:var(--c${m.c})" data-go="${m.L[0].id}"><b>${m.t}</b><span>${m.s} &middot; ${m.L.length} items</span></button>`).join('')}</div>
  ${C('Listen anywhere','Open any lesson and press Listen. The course reads each paragraph, table row and dialogue line in turn, highlights it, and lets you change speed and voice. It uses the voices already on your device, so it also works offline once the page has loaded. Most devices include English voices; choose the one you find clearest.')}
  </div>`;
  $('#startBtn').onclick=()=>go(next.id);
}
function resHTML(l){
  if(!l.res||!l.res.length)return'';
  const g={v:[],r:[],b:[]};l.res.forEach(k=>RES[k]&&g[RES[k].k].push(RES[k]));
  const li=(r,book)=>`<li><a href="${book?bookUrl(r):r.u}" target="_blank" rel="noopener"><span class="t">${esc(r.t)}${!book?`<span class="tag ${r.ok?'ok':''}">${r.ok?'Link checked':'Suggested'}</span>`:''}</span><span class="n">${esc(book?r.by+' · '+r.y+'. '+r.n+' Opens an Open Library search.':(r.b+'. '+r.n))}</span></a></li>`;
  return`<section class="res nr" aria-label="Resources"><h3>Go deeper</h3>
  ${g.v.length?`<h4>Videos</h4><ul class="rl">${g.v.map(r=>li(r)).join('')}</ul>`:''}
  ${g.r.length?`<h4 style="margin-top:18px">Free reading and official pages</h4><ul class="rl">${g.r.map(r=>li(r)).join('')}</ul>`:''}
  ${g.b.length?`<h4 style="margin-top:18px">Books</h4><ul class="rl">${g.b.map(r=>li(r,1)).join('')}</ul>`:''}
  <p class="meta" style="margin-top:12px">Links open in a new tab. "Link checked" means the page was opened and matched its description when this course was built; "Suggested" links were found by search and matched by title. Video sites cannot play inside this page. Book links search Open Library so you can borrow or locate a copy.</p></section>`;
}
function renderLesson(l){
  const i=ALL.indexOf(l), prev=ALL[i-1], next=ALL[i+1];
  main.innerHTML=`<article id="body"><div class="crumb nr"><i class="sw" style="background:var(--c${l.mod.c});display:inline-block;margin:0"></i>${l.mod.t}</div>
  <h1>${l.t}</h1><div class="meta nr">About ${l.min} minutes${l.quiz?' &middot; graded quiz':''}</div>
  ${l.quiz?'<div class="widget nr" data-w="quiz:'+l.quiz+'"></div>':l.html}
  ${l.ref?`<section class="reflect nr"><h4>Reflect</h4><p>${esc(l.ref)}</p><label class="sr" for="note">Your private note</label><textarea id="note" placeholder="Write your note here. It is saved in this browser only.">${esc(S.notes[l.id]||'')}</textarea></section>`:''}
  ${resHTML(l)}
  <div class="foot nr"><button class="btn ghost" id="prevB" ${prev?'':'disabled'}>Previous</button>
  ${l.quiz||l.final?'':`<button class="btn ghost" id="doneB">${S.done[l.id]?'Completed ✓ (undo)':'Mark complete'}</button>`}
  <button class="btn" id="nextB" ${next?'':'disabled'}>${next?'Next: '+esc(next.t.length>34?next.t.slice(0,32)+'…':next.t):'End'}</button></div></article>`;
  $('#prevB').onclick=()=>prev&&go(prev.id);
  $('#nextB').onclick=()=>{if(!l.quiz&&!l.final&&!S.done[l.id]){S.done[l.id]=true;save()}next&&go(next.id)};
  const d=$('#doneB');if(d)d.onclick=()=>{S.done[l.id]=!S.done[l.id];save();d.textContent=S.done[l.id]?'Completed ✓ (undo)':'Mark complete';buildNav();updateProg()};
  const n=$('#note');if(n)n.oninput=()=>{S.notes[l.id]=n.value;save()};
  initWidgets();
}

/* ---------- widgets ---------- */
function initWidgets(){$$('[data-w]').forEach(el=>{const[n,a]=el.dataset.w.split(':');({audit,daloz,place,triage,quiz,final:finalExam,practice})[n]?.(el,a)})}
function practice(el,id){
  const p=PRACTICE[id];
  el.innerHTML=`<h4>${p.t}</h4><p>${p.i}</p>`+p.items.map((it,k)=>`<div class="pi"><p>${it[0]}</p><label class="sr" for="${id}-${k}">Your answer</label><textarea id="${id}-${k}" placeholder="Your answer">${esc(S.notes[id+k]||'')}</textarea><button class="btn ghost sm" data-rev="${k}">Show model answer</button><div class="ans" hidden><p>${it[1]}</p></div></div>`).join('');
  el.addEventListener('input',e=>{if(e.target.matches('textarea')){S.notes[e.target.id.replace('-','')]=e.target.value;save()}});
  el.addEventListener('click',e=>{const b=e.target.closest('[data-rev]');if(!b)return;const a=b.nextElementSibling;a.hidden=!a.hidden;b.textContent=a.hidden?'Show model answer':'Hide model answer'});
}
const AUD=['I can act as a positive, enthusiastic pedagogical role model during live classroom demonstrations.','I understand how local school context, language of instruction and class size affect TaRL delivery.','I establish psychological safety before offering critique, avoiding "judge mentoring" behaviours.','I can conduct a full-lesson collegial observation without disrupting the teacher or learners.','I ask open, non-leading coaching questions (GROW) rather than simply telling teachers what to fix.','I practise committed listening: allowing silence and encouraging teachers to analyse their own lessons.','I co-construct 1 to 2 achievable SMART targets with teachers rather than overwhelming them with long lists.','I accurately verify one-on-one learner assessments and spot misgrouped students quickly.','I analyse baseline-to-midline progression tables to prioritise which schools I visit first.','I facilitate peer learning across schools and collaborate with school leaders to solve structural barriers.'];
function audit(el){
  el.innerHTML=`<h4>Mentor self-audit</h4>`+AUD.map((s,i)=>`<div class="sl"><label for="au${i}">${i+1}. ${s}</label><input type="range" id="au${i}" min="1" max="5" step="1" value="${S.audit[i]||3}"><output id="ao${i}">${S.audit[i]||3}</output></div>`).join('')+`<div id="auRes" style="margin-top:12px"></div>`;
  const calc=()=>{const v=AUD.map((_,i)=>+$('#au'+i).value);S.audit=v;save();const avg=(v.reduce((a,b)=>a+b,0)/v.length).toFixed(1);const low=v.map((x,i)=>[x,i]).sort((a,b)=>a[0]-b[0]).slice(0,3);
    $('#auRes').innerHTML=`<p class="score">${avg} <span style="font-size:14px;font-weight:400;color:var(--muted)">average out of 5</span></p><p><b>Your three action targets:</b></p>${UL(low.map(([x,i])=>`Statement ${i+1} (rated ${x}): ${AUD[i]}`))}`};
  el.oninput=e=>{if(e.target.matches('input')){$('#ao'+e.target.id.slice(2)).textContent=e.target.value;calc()}};calc();
}
function daloz(el){
  const Qd={st:['Stasis','Low support, low challenge','Teacher feels isolated and ignored, defaults to rote teaching, learners barely grow. <b>Do this:</b> a warm relational check-in, then co-plan one simple TaRL activity together.'],
  re:['Retreat','Low support, high challenge','Typical of judge mentoring. The teacher feels threatened, defensive or burned out. <b>Do this:</b> pause evaluative grading at once, validate strengths, co-teach a lesson side by side.'],
  co:['Confirmation','High support, low challenge','Friendly visits full of praise, but weak pedagogy and stagnant data are never raised. <b>Do this:</b> use midline data to create gentle dissonance and set one stretch target.'],
  gr:['Growth (target)','High support, high challenge','High psychological safety plus rigorous curiosity. The teacher experiments, reflects and accelerates. <b>Do this:</b> sustain collegial dialogue and encourage peer sharing and innovation.']};
  el.innerHTML=`<h4>Explore the matrix</h4><div class="axis"><span>Higher challenge</span></div><div class="matrix">${[['re','st'],['gr','co']].flat().map(k=>`<button data-k="${k}" aria-pressed="false"><b>${Qd[k][0]}</b><span>${Qd[k][1]}</span></button>`).join('')}</div><div class="axis"><span>Lower support</span><span>Higher support</span></div><p id="dd" style="margin-top:12px" class="meta">Select a quadrant.</p>`;
  el.onclick=e=>{const b=e.target.closest('[data-k]');if(!b)return;$$('[data-k]',el).forEach(x=>x.setAttribute('aria-pressed',x===b));$('#dd',el).className='';$('#dd',el).innerHTML=`<b>${Qd[b.dataset.k][0]}.</b> ${Qd[b.dataset.k][2]}`}
}
function place(el){
  const N={p:{q:'Step 1. The child reads the 4-sentence Simple Paragraph aloud. What happened?',o:[['Reads smoothly with 3 or fewer mistakes','s'],['More than 3 mistakes, or reads word by word','w']]},
   s:{q:'Step 2. The child reads the 70 to 80 word story and answers 1 to 2 questions. What happened?',o:[['3 or fewer mistakes','=STORY'],['More than 3 mistakes','=PARAGRAPH']]},
   w:{q:'Step 3. The child reads any 5 of 5 familiar words. How many were correct?',o:[['4 or 5 correct','=WORD'],['Fewer than 4 correct','l']]},
   l:{q:'Step 4. The child identifies any 5 letters by sound or name. How many were correct?',o:[['4 or 5 correct','=LETTER'],['Fewer than 4 correct','=BEGINNER']]}};
  const col={STORY:'var(--c4)',PARAGRAPH:'var(--c3)',WORD:'var(--c3)',LETTER:'var(--c2)',BEGINNER:'var(--c1)'};
  let trail=[],node='p';
  const draw=()=>{
    const n=N[node];
    el.innerHTML=`<h4>Literacy placement simulator</h4>${trail.length?`<div class="trail">${trail.map(t=>`<span>${t}</span>`).join('')}</div>`:''}`+
    (n?`<p><b>${n.q}</b></p>${n.o.map((o,i)=>`<button class="btn ghost" style="margin:0 8px 8px 0" data-i="${i}">${o[0]}</button>`).join('')}`:
    `<p>Classification: <span class="lvl" style="background:${col[node]}">${node} LEVEL</span></p><p class="meta">That took ${trail.length} step${trail.length>1?'s':''}. The adaptive route is why the test takes only 3 to 5 minutes.</p><button class="btn sm" data-reset>Try another child</button>`);
  };
  el.onclick=e=>{if(e.target.closest('[data-reset]')){trail=[];node='p';draw();return}const b=e.target.closest('[data-i]');if(!b)return;const o=N[node].o[+b.dataset.i];trail.push(o[0]);node=o[1].startsWith('=')?o[1].slice(1):o[1];draw()};
  draw();
}
function triage(el){
  const D=[['School Alpha',120,75,45,'New teacher appointed last month; enthusiastic but struggles with grouping.'],['School Beta',280,55,50,'Largest school in zone; chronic teacher absenteeism on Fridays; class sizes of 60+.'],['School Gamma',90,65,35,'Stable leadership; peer reading circles working well; strong community support.'],['School Delta',110,50,25,'Consistent progress; teacher asked for advanced coaching on Story-level comprehension.'],['School Epsilon',150,40,30,'Moderate progress, but 40 over-age adolescents dropped out during harvest season.']];
  el.innerHTML=`<h4>Triage simulation: pick two schools</h4><div class="tw"><table><thead><tr><th>Visit</th><th>School</th><th>Learners</th><th>% B/L baseline</th><th>% B/L midline</th><th>Gain (pp)</th><th>Still at B/L (calc.)</th><th>Context</th></tr></thead><tbody>${D.map((d,i)=>`<tr><td><input type="checkbox" id="tr${i}" aria-label="Visit ${d[0]}"></td><td class="rh"><label for="tr${i}">${d[0]}</label></td><td>${d[1]}</td><td>${d[2]}%</td><td>${d[3]}%</td><td>${d[2]-d[3]}</td><td>${Math.round(d[1]*d[3])/100}</td><td>${d[4]}</td></tr>`).join('')}</tbody></table></div><button class="btn" id="trB">Check my choice</button><div id="trR" style="margin-top:12px"></div>`;
  el.onchange=e=>{const c=$$('input:checked',el);if(c.length>2)e.target.checked=false};
  $('#trB',el).onclick=()=>{
    const sel=D.filter((d,i)=>$('#tr'+i).checked).map(d=>d[0]);
    if(sel.length!==2){$('#trR',el).innerHTML='<p>Choose exactly two schools first.</p>';return}
    const hit=sel.includes('School Beta')&&sel.includes('School Epsilon');
    $('#trR',el).innerHTML=`<p><b>You chose ${sel.join(' and ')}.</b> ${hit?'That matches the facilitator\'s key.':'The facilitator\'s key chose Beta and Epsilon. Check your reasoning against it below; a different choice is fine if the evidence supports it.'}</p>
    <div class="callout"><h4>Facilitator model answer</h4><p><b>Priority 1: School Beta.</b> It has the largest cohort (280 children) and the worst progression velocity, only 5 pp, leaving about 140 children at the lowest levels. Friday absenteeism needs immediate mentor intervention.</p><p><b>Priority 2: School Epsilon.</b> A moderate baseline, but an acute retention crisis: 40 adolescents dropped out during harvest, so it needs community engagement and flexible timetabling.</p><p>Alpha, Gamma and Delta show healthy gains of 25 to 30 pp and can be kept going with peer WhatsApp check-ins this week.</p></div>
    <p class="meta">The "still at B/L" column is simple arithmetic added for this course (learners x midline %). Alpha still has 54 children at the lowest levels, so it would be the first school to move up if a third visit day opened.</p>`};
}
function quizBody(el,qs,id,onDone){
  const render=()=>{el.innerHTML=`<h4>${id==='final'?'Final assessment':'Check your understanding'}</h4>`+qs.map((q,i)=>`<fieldset class="qq"><legend>${i+1}. ${esc(q[0])}</legend>${q[1].map((o,j)=>`<label class="opt"><input type="radio" name="q${i}" value="${j}"><span>${esc(o)}</span></label>`).join('')}<p class="why" hidden></p></fieldset>`).join('')+`<button class="btn" id="qB">Check answers</button><div id="qR" style="margin-top:14px"></div>`;
    $('#qB',el).onclick=()=>{
      let sc=0;qs.forEach((q,i)=>{const sel=$(`input[name=q${i}]:checked`,el);const f=$$('.qq',el)[i];const opts=$$('.opt',f);opts.forEach(o=>o.classList.remove('right','wrong'));opts[q[2]].classList.add('right');if(sel&&+sel.value===q[2])sc++;else if(sel)opts[+sel.value].classList.add('wrong');const w=$('.why',f);w.hidden=false;w.textContent=(sel?(+sel.value===q[2]?'Correct. ':'Not quite. '):'Not answered. ')+q[3]});
      const p=Math.round(100*sc/qs.length);onDone(sc,p);
      $('#qR',el).innerHTML=`<p class="score">${sc} / ${qs.length} (${p}%)</p><button class="btn ghost sm" id="qRe">Retry</button>`;$('#qRe',el).onclick=()=>{if(id==='final')finalExam(el);else render()};
    }};
  render();
}
function quiz(el,id){
  quizBody(el,Q[id],id,(sc,p)=>{S.scores[id]=Math.max(S.scores[id]||0,p);const l=ALL.find(x=>x.quiz===id);if(p>=60){S.done[l.id]=true}save();buildNav();updateProg();
    });
  if(S.scores[id]!=null)el.insertAdjacentHTML('afterbegin',`<p class="meta">Best score so far: ${S.scores[id]}%. A score of 60% or more completes the quiz.</p>`);
}
function finalExam(el){
  const pool=Object.values(Q).flat().map(x=>x);for(let i=pool.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[pool[i],pool[j]]=[pool[j],pool[i]]}
  const qs=pool.slice(0,12);
  quizBody(el,qs,'final',(sc,p)=>{if(p>=70){S.passed=true;save()}cert()});
  cert();
}
function cert(){
  let box=$('#certBox');if(!box){box=document.createElement('div');box.id='certBox';box.className='nr';$('[data-w=final]').after(box)}
  const rest=COUNTED.filter(l=>!S.done[l.id]).length;
  if(!S.passed){box.innerHTML=`<p class="meta">Pass the final assessment with 70% or more to unlock your certificate.</p>`;return}
  if(rest){box.innerHTML=`<div class="callout"><h4>Assessment passed</h4><p>Complete the remaining ${rest} lesson${rest>1?'s':''} to unlock your certificate. Your outline on the left shows which are unchecked.</p></div>`;return}
  const nm=S.name||'';
  box.innerHTML=`<label for="nm">Your name for the certificate</label><br><input id="nm" class="nameIn" value="${esc(nm)}" placeholder="Full name"><div class="cert"><p class="meta">Certificate of completion</p><h2>TaRL Mentor Academy</h2><p>This certifies that</p><div class="nm" id="nmOut">${esc(nm||'Your name')}</div><p>has completed all five modules on coaching, mentoring and data-driven monitoring in Teaching at the Right Level, and passed the final assessment.</p><p class="meta">${new Date().toLocaleDateString(undefined,{year:'numeric',month:'long',day:'numeric'})}. Take a screenshot to keep or share this page.</p></div>`;
  $('#nm').oninput=e=>{S.name=e.target.value;save();$('#nmOut').textContent=e.target.value||'Your name'};
}
/* copy templates */
const TPL={A:'MASTER CLASSROOM OBSERVATION CHECKLIST\nSchool name and location: ____\nTeacher name and grade: ____\nObserver / mentor name: ____\nDate: ____ Start: ____ End: ____\nPupils enrolled: ____ Present: Boys ____ Girls ____\n1. Assessment and grouping: Learning Level Chart visible? [Yes/No] Accurate groups? [Yes/No]\n2. Pacing: Warm-up mins ____ Group work mins ____ Writing mins ____\n3. CAMaL active: [ ] Listening [ ] Observing [ ] Speaking [ ] Doing [ ] Reading [ ] Writing\n4. Materials (TLMs) actively handled by learners? [Yes/No]\n5. Agreed coaching target: ____',
 B:'MENTOR VISIT LOGBOOK\nVisit date | School | Teacher coached | Focus of debrief (GROW) | Agreed action target | Next follow-up date\n____ | ____ | ____ | ____ | ____ | ____',
 C:'COACHING AGREEMENT AND PROFESSIONAL GROWTH CHARTER\nMutual purpose: To collaborate as professional partners dedicated to accelerating foundational literacy and numeracy for every child.\nConfidentiality: All observations and debriefs remain strictly confidential and developmental, never used for punitive appraisal.\nOpen communication: Both commit to honest reflection, active listening and respectful feedback.\nAction commitment: Both honour agreed co-created action targets and maintain consistent follow-through.\nMentor signature: ________  Teacher signature: ________'};
document.addEventListener('click',e=>{
  const c=e.target.closest('[data-copy]');
  if(c){const t=TPL[c.dataset.copy];const ok=()=>{$('#copied').textContent='Copied.'};
    (navigator.clipboard?navigator.clipboard.writeText(t):Promise.reject()).then(ok).catch(()=>{const ta=document.createElement('textarea');ta.value=t;document.body.appendChild(ta);ta.select();try{document.execCommand('copy');ok()}catch(_){$('#copied').textContent='Select the table text and copy it manually.'}ta.remove()})}
  const g=e.target.closest('[data-go]');if(g)go(g.dataset.go);
  const a=e.target.closest('a.li');if(a){e.preventDefault();go(a.dataset.id)}
});
$('#brandBtn').onclick=()=>go('home');
$('#menuBtn').onclick=()=>{const o=document.body.classList.toggle('menu');$('#menuBtn').setAttribute('aria-expanded',o)};

/* ---------- read aloud ---------- */
let queue=[],qi=-1,playing=false,tok=0;const syn=window.speechSynthesis;
function textOf(el){
  if(el.tagName==='TR'){const th=$$('th',el.closest('table')).map(x=>x.textContent.trim());return $$('td',el).map((c,i)=>(i&&th[i]?th[i]+': ':'')+c.textContent.trim()).filter(Boolean).join('. ')}
  return el.textContent.replace(/\s+/g,' ').trim();
}
function prepAudio(){
  const ok=!!syn&&'SpeechSynthesisUtterance' in window;
  $('#aPlay').disabled=$('#aPrev').disabled=$('#aNext').disabled=!ok;
  $('#astat').textContent=ok?'Read this lesson aloud':'Read-aloud is not available in this browser.';
  $('#aPlay').textContent='Listen';
}
function build(){queue=$$('#body h1,#body h3,#body p,#body li,#body tbody tr,#body summary').filter(el=>!el.closest('.nr,[hidden],.rl,.meta,.crumb,.foot,.reflect')&&!(el.matches('p')&&el.closest('li'))&&textOf(el).length>1)}
function mark(){$$('.reading').forEach(x=>x.classList.remove('reading'));if(queue[qi]){queue[qi].classList.add('reading');queue[qi].scrollIntoView({block:'center',behavior:'smooth'});$('#astat').textContent=`Reading ${qi+1} of ${queue.length}`}}
function say(i){
  if(i<0)i=0;if(i>=queue.length){stopAudio(true);$('#astat').textContent='Lesson finished';return}
  syn.cancel();qi=i;const my=++tok;mark();
  const u=new SpeechSynthesisUtterance(textOf(queue[i]));u.rate=+$('#rate').value;
  const v=voices.find(v=>v.voiceURI===$('#vsel').value);if(v){u.voice=v;u.lang=v.lang}
  u.onend=()=>{if(my===tok&&playing)say(qi+1)};u.onerror=()=>{if(my===tok&&playing&&queue[qi])setTimeout(()=>say(qi+1),50)};
  syn.speak(u);
}
function stopAudio(keep){tok++;playing=false;if(syn)syn.cancel();$$('.reading').forEach(x=>x.classList.remove('reading'));qi=-1;const b=$('#aPlay');if(b)b.textContent='Listen'}
$('#aPlay').onclick=()=>{
  if(!playing){build();playing=true;$('#aPlay').textContent='Pause';if(syn.paused&&qi>=0){syn.resume()}else say(qi>=0?qi:0)}
  else{playing=false;$('#aPlay').textContent='Resume';syn.pause()}
};
$('#aNext').onclick=()=>{if(!queue.length||qi<0)build();playing=true;$('#aPlay').textContent='Pause';say(qi+1)};
$('#aPrev').onclick=()=>{if(!queue.length||qi<0)build();playing=true;$('#aPlay').textContent='Pause';say(Math.max(0,qi-1))};
$('#rate').onchange=()=>{if(playing&&qi>=0)say(qi)};
$('#vsel').onchange=()=>{try{localStorage.setItem(KEY+'-voice',$('#vsel').value)}catch(e){};if(playing&&qi>=0)say(qi)};
let voices=[];
function loadVoices(){
  if(!syn)return;voices=syn.getVoices();if(!voices.length)return;
  let saved='';try{saved=localStorage.getItem(KEY+'-voice')||''}catch(e){}
  const pref=voices.find(v=>v.voiceURI===saved)||voices.find(v=>/^en/i.test(v.lang)&&v.localService)||voices.find(v=>/^en/i.test(v.lang))||voices[0];
  $('#vsel').innerHTML=voices.map(v=>`<option value="${esc(v.voiceURI)}" ${v===pref?'selected':''}>${esc(v.name)} (${esc(v.lang)})</option>`).join('');
}
if(syn){loadVoices();syn.onvoiceschanged=loadVoices}
window.addEventListener('beforeunload',()=>syn&&syn.cancel());

/* ---------- boot ---------- */
function route(){const h=location.hash.slice(1);const id=ALL.find(l=>l.id===h)?h:'home';if(id===cur&&main.innerHTML.trim())return;go(id,true)}
window.addEventListener('hashchange',route);
route();
</script>

</body></html>
