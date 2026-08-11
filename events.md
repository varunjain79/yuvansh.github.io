---
layout: default
title: "Events"
permalink: /events/
---

<style>
.events-page{position:relative;overflow:hidden}
.events-hero{text-align:center;padding:10px 0 28px}
.events-hero h1{font-size:clamp(2.3rem,7vw,4.8rem);margin:0 0 10px;background:linear-gradient(90deg,#38bdf8,#22c55e,#60a5fa);-webkit-background-clip:text;background-clip:text;color:transparent}
.events-hero p{color:#a7c0da;font-size:1.05rem}
.event-card{padding:28px;border:1px solid rgba(56,189,248,.25);border-radius:24px;background:rgba(7,18,32,.7);margin:20px 0}
.event-card.today{border-color:rgba(34,197,94,.65);box-shadow:0 0 35px rgba(34,197,94,.12)}
.event-date{color:#7dd3fc;font-weight:700}.event-card h2{margin:8px 0}.event-card p{color:#cbd5e1;line-height:1.65}
.cake-area{text-align:center;margin-top:34px;padding:28px;border-radius:24px;background:linear-gradient(135deg,rgba(56,189,248,.08),rgba(34,197,94,.08))}
.cake{font-size:7rem;cursor:pointer;display:inline-block;transition:transform .35s}.cake:hover{transform:scale(1.08) rotate(-2deg)}
.cake-message{min-height:1.8em;color:#86efac;font-weight:700}.piece{display:inline-block;font-size:3rem;margin:4px;animation:pop .45s ease both}
@keyframes pop{from{transform:scale(0);opacity:0}to{transform:scale(1);opacity:1}}
.confetti{position:fixed;top:-30px;pointer-events:none;z-index:9999;font-size:1.4rem;animation:fall linear forwards}
@keyframes fall{to{transform:translateY(110vh) rotate(720deg);opacity:0}}
.y-burst{position:fixed;z-index:9998;font-size:2rem;cursor:pointer;user-select:none;animation:appear .3s ease}
@keyframes appear{from{transform:scale(0);opacity:0}to{transform:scale(1);opacity:1}}
.y-hunt{position:relative;min-height:300px;margin-top:25px;padding:24px;border-radius:22px;border:1px dashed rgba(56,189,248,.35);background:rgba(2,6,23,.35);overflow:hidden;text-align:center}
.y-hunt button{margin:6px;padding:10px 15px;border-radius:999px;border:1px solid rgba(56,189,248,.35);background:#0b1e31;color:#eff6ff;cursor:pointer}
.y-status{color:#a7c0da}.hidden{display:none}
</style>

<div class="events-page">
  <div class="events-hero">
    <h1>🎉 Events</h1>
    <p id="event-status">Checking today’s events…</p>
  </div>

  <section id="today-event" class="event-card today">
    <div class="event-date">August 11, 2026 · TODAY</div>
    <h2>🎂 Yuvansh’s Birthday!</h2>
    <p>Today is a special event on Yuvansh’s Lab! Scroll down for the birthday challenge.</p>
  </section>

  <section class="cake-area">
    <h2>🎂 The Birthday Cake</h2>
    <p>Click the cake to cut it and get your piece!</p>
    <div id="cake" class="cake" role="button" tabindex="0" aria-label="Cut the birthday cake">🎂</div>
    <div id="cake-message" class="cake-message" aria-live="polite"></div>
    <div id="pieces"></div>
  </section>

  <section class="y-hunt">
    <h2>💙💚 Y Challenge</h2>
    <p class="y-status" id="y-status">Get ready… the Y's will start appearing after 11 seconds!</p>
    <div id="y-field" class="hidden"></div>
  </section>
</div>

<script>
(function(){
  const status=document.getElementById('event-status');
  const today=new Date();
  const isBirthday=today.getMonth()===7 && today.getDate()===11;
  status.textContent=isBirthday?'🎂 There is an event today — it’s Yuvansh’s birthday!':'No event is scheduled for today.';

  const cake=document.getElementById('cake');
  const message=document.getElementById('cake-message');
  const pieces=document.getElementById('pieces');
  let cut=false;
  function cutCake(){
    if(cut)return;
    cut=true;
    cake.textContent='🍰';
    message.textContent='You got a piece of Yuvansh’s birthday cake! 🎉';
    const piece=document.createElement('span');
    piece.className='piece'; piece.textContent='🍰'; pieces.appendChild(piece);
    for(let i=0;i<18;i++){
      const c=document.createElement('span'); c.className='confetti'; c.textContent=i%2?'💙':'💚';
      c.style.left=Math.random()*100+'vw'; c.style.animationDuration=(2+Math.random()*2)+'s';
      document.body.appendChild(c); setTimeout(()=>c.remove(),4500);
    }
  }
  cake.addEventListener('click',cutCake);
  cake.addEventListener('keydown',e=>{if(e.key==='Enter'||e.key===' ')cutCake()});

  const yStatus=document.getElementById('y-status');
  const field=document.getElementById('y-field');
  let ys=[]; let started=false;
  setTimeout(()=>{
    started=true; field.classList.remove('hidden');
    yStatus.textContent='The Y’s are appearing! Press every one! 💙💚';
    for(let i=0;i<24;i++)spawnY(i);
  },11000);

  function spawnY(i){
    const y=document.createElement('button'); y.className='y-burst'; y.textContent=i%2?'Y':'Y';
    y.style.left=(8+Math.random()*82)+'%'; y.style.top=(8+Math.random()*78)+'%';
    y.style.color=i%2?'#22c55e':'#38bdf8';
    y.addEventListener('click',()=>{y.remove();ys=ys.filter(x=>x!==y);if(!ys.length){yStatus.textContent='🎉 You pressed them all! Happy Birthday!';setTimeout(()=>{for(let j=0;j<12;j++)spawnY(j)},900)}});
    field.appendChild(y); ys.push(y);
  }
})();
</script>
