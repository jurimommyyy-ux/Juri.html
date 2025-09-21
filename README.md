<!doctype html>

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>I ♥ Juri</title>
  <style>
    :root{
      --bg1:#0f0c29;
      --bg2:#302b63;
      --accent:#ff6b6b;
      --accent2:#ff9a9e;
      --glass: rgba(255,255,255,0.06);
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Inter,ui-sans-serif,system-ui,Segoe UI,Roboto,'Helvetica Neue',Arial}
    body{
      background: radial-gradient(1200px 600px at 10% 10%, rgba(255,105,135,0.08), transparent 8%),
                  radial-gradient(900px 400px at 90% 90%, rgba(255,150,180,0.05), transparent 10%),
                  linear-gradient(180deg,var(--bg1),var(--bg2));
      display:flex;align-items:center;justify-content:center;color:white;
      -webkit-font-smoothing:antialiased;text-rendering:optimizeLegibility;padding:32px;
    }
    .card{
      width:min(920px,96%);max-width:940px;padding:36px;border-radius:20px;background:linear-gradient(180deg,rgba(255,255,255,0.03),rgba(255,255,255,0.02));
      box-shadow:0 10px 40px rgba(2,6,23,0.6);backdrop-filter:blur(8px);position:relative;overflow:hidden;
    }
    header{display:flex;align-items:center;gap:18px}
    .logo{width:68px;height:68px;border-radius:14px;background:linear-gradient(135deg,var(--accent),var(--accent2));display:flex;align-items:center;justify-content:center;font-size:34px;box-shadow:0 6px 20px rgba(255,107,107,0.18);}
    h1{font-size:28px;margin:0}
    p.lead{opacity:0.84;margin:8px 0 22px}.cta{display:flex;gap:12px;align-items:center}
.link-look{
  --pad:16px 22px;display:inline-flex;align-items:center;gap:12px;padding:var(--pad);border-radius:12px;background:linear-gradient(90deg,rgba(255,255,255,0.04),rgba(255,255,255,0.02));cursor:pointer;border:1px solid rgba(255,255,255,0.04);text-decoration:none;color:inherit;font-weight:600;transition:transform .18s ease, box-shadow .18s ease;
}
.link-look:hover{transform:translateY(-4px);box-shadow:0 18px 40px rgba(0,0,0,0.4)}
.heart{display:inline-grid;place-items:center;width:40px;height:40px;border-radius:10px;background:linear-gradient(135deg,var(--accent),var(--accent2));color:white;font-size:18px}

/* center stage */
.stage{display:grid;grid-template-columns:1fr 380px;gap:28px;margin-top:18px}
.left{padding:18px}
.bigcard{border-radius:14px;padding:22px;background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03)}

.love-btn{display:inline-flex;align-items:center;gap:12px;padding:18px 22px;border-radius:14px;font-size:18px;font-weight:700;cursor:pointer;background:linear-gradient(90deg,var(--accent),var(--accent2));border:none;color:white;box-shadow:0 12px 40px rgba(255,107,107,0.2);transform:translateZ(0);transition:transform .12s ease;}
.love-btn:active{transform:translateY(2px) scale(.995)}

.decor{position:absolute;right:-120px;top:-60px;opacity:0.08;font-size:220px;transform:rotate(-18deg);}

/* modal */
.overlay{position:fixed;inset:0;display:none;align-items:center;justify-content:center;z-index:80}
.overlay.show{display:flex}
.modal{width:min(720px,94%);background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));border-radius:18px;padding:28px;box-shadow:0 24px 70px rgba(2,6,23,0.8);text-align:center;position:relative;overflow:hidden}
.modal h2{font-size:46px;margin:12px 0 6px;letter-spacing:1px}
.modal p{margin:0 0 18px;font-size:18px;opacity:0.95}
.close{position:absolute;right:14px;top:12px;background:transparent;border:0;color:rgba(255,255,255,0.7);font-size:20px;cursor:pointer}

/* animated hearts */
.floating-heart{position:absolute;pointer-events:none;will-change:transform,opacity}

/* responsive */
@media (max-width:880px){.stage{grid-template-columns:1fr;}.decor{display:none}.logo{width:56px;height:56px}}

  </style>
</head>
<body>
  <div class="card">
    <header>
      <div class="logo">♥</div>
      <div>
        <h1>For Juri — a tiny surprise</h1>
        <p class="lead">Click the heart below and watch something sweet happen. Made with love.</p>
      </div>
    </header><div class="stage">
  <div class="left">
    <div class="bigcard">
      <p style="font-size:16px;margin:0 0 14px">A little interactive message for Juri — click the heart link or the big button to reveal it.</p>
      <div style="display:flex;gap:12px;flex-wrap:wrap;margin-top:10px">
        <a class="link-look" id="linkReveal">
          <div class="heart">💖</div>
          <div>Open for Juri</div>
        </a>

        <button class="love-btn" id="heartBtn">Send my love ♥</button>
      </div>
    </div>

    <div style="margin-top:18px;color:rgba(255,255,255,0.75);font-size:14px">Tip: You can email or message this file to her, or host it on GitHub Pages for a permanent link.</div>
  </div>

  <div>
    <div style="display:grid;place-items:center;height:100%;min-height:220px">
      <svg viewBox="0 0 300 300" width="100%" style="max-width:320px">
        <defs>
          <linearGradient id="g1" x1="0" x2="1">
            <stop offset="0" stop-color="#ff6b6b"/>
            <stop offset="1" stop-color="#ff9a9e"/>
          </linearGradient>
        </defs>
        <g transform="translate(150,150)">
          <path d="M0 -50 C 40 -90, 120 -70, 120 -10 C 120 60, 40 110, 0 140 C -40 110, -120 60, -120 -10 C -120 -70, -40 -90, 0 -50 Z" fill="url(#g1)" opacity="0.95"/>
        </g>
      </svg>
    </div>
  </div>
</div>

<div class="decor">♥</div>

  </div>  <!-- modal + confetti canvas -->  <div class="overlay" id="overlay" aria-hidden="true">
    <div class="modal" role="dialog" aria-modal="true">
      <button class="close" id="closeBtn">✕</button>
      <h2 id="loveText">I love you, Juri</h2>
      <p>You're my sunshine. — <strong>From Koushik</strong></p>
      <canvas id="confetti" width="800" height="400" style="width:100%;height:160px;border-radius:12px;background:linear-gradient(180deg,rgba(255,255,255,0.01),transparent)"></canvas>
      <div style="margin-top:18px;display:flex;justify-content:center;gap:10px">
        <button class="love-btn" id="againBtn">Send again ♥</button>
      </div>
    </div>
  </div>  <script>
    // Elements
    const overlay = document.getElementById('overlay');
    const linkReveal = document.getElementById('linkReveal');
    const heartBtn = document.getElementById('heartBtn');
    const closeBtn = document.getElementById('closeBtn');
    const againBtn = document.getElementById('againBtn');
    const loveText = document.getElementById('loveText');
    const confettiCanvas = document.getElementById('confetti');
    const ctx = confettiCanvas.getContext('2d');

    function showLove(){
      overlay.classList.add('show');
      overlay.setAttribute('aria-hidden', 'false');
      playChime();
      startConfetti();
      burstHearts();
    }
    function hideLove(){
      overlay.classList.remove('show');
      overlay.setAttribute('aria-hidden', 'true');
      stopConfetti();
    }

    linkReveal.addEventListener('click', showLove);
    heartBtn.addEventListener('click', showLove);
    closeBtn.addEventListener('click', hideLove);
    againBtn.addEventListener('click', ()=>{ startConfetti(true); pulseText(); });
    overlay.addEventListener('click',(e)=>{ if(e.target===overlay) hideLove(); });

    // Tiny WebAudio chime (no external file)
    function playChime(){
      try{
        const ctx = new (window.AudioContext || window.webkitAudioContext)();
        const o = ctx.createOscillator();
        const g = ctx.createGain();
        o.type = 'sine';
        o.frequency.value = 440;
        o.connect(g);g.connect(ctx.destination);
        o.start();
        g.gain.setValueAtTime(0, ctx.currentTime);
        g.gain.linearRampToValueAtTime(0.12, ctx.currentTime+0.02);
        o.frequency.exponentialRampToValueAtTime(660, ctx.currentTime+0.22);
        g.gain.exponentialRampToValueAtTime(0.0001, ctx.currentTime+0.9);
        o.stop(ctx.currentTime+1);
      }catch(e){/* audio blocked */}
    }

    // Confetti implementation (lightweight)
    let confetti = [];
    let confettiTimer = null;
    function random(min,max){return Math.random()*(max-min)+min}
    function makeConfetti(){
      const w = confettiCanvas.width = confettiCanvas.clientWidth * devicePixelRatio;
      const h = confettiCanvas.height = confettiCanvas.clientHeight * devicePixelRatio;
      confetti = [];
      const colors = ['#ff6b6b','#ff9a9e','#ffd36b','#9ad3de','#b39cff'];
      for(let i=0;i<120;i++){
        confetti.push({
          x:Math.random()*w,
          y:Math.random()*h - h,
          r:random(6,14)*devicePixelRatio,
          d:random(1,3),
          tilt:random(-0.2,0.2),
          color:colors[Math.floor(Math.random()*colors.length)],
          rot:random(0,Math.PI*2)
        })
      }
    }
    function drawConfetti(){
      const w = confettiCanvas.width;
      const h = confettiCanvas.height;
      ctx.clearRect(0,0,w,h);
      confetti.forEach((p)=>{
        ctx.save();
        ctx.translate(p.x,p.y);
        ctx.rotate(p.rot);
        ctx.fillStyle = p.color;
        ctx.fillRect(-p.r/2, -p.r/6, p.r, p.r/3);
        ctx.restore();
        p.x += Math.sin(p.d) * 2 + p.tilt*4;
        p.y += 2 + p.d;
        p.rot += 0.04;
        if(p.y > h + 20){ p.y = -40; p.x = Math.random()*w; }
      })
    }
    function startConfetti(once=false){
      makeConfetti();
      if(confettiTimer) cancelAnimationFrame(confettiTimer);
      function loop(){ drawConfetti(); confettiTimer = requestAnimationFrame(loop); }
      loop();
      if(once) setTimeout(()=>{ stopConfetti(); }, 1400);
    }
    function stopConfetti(){ if(confettiTimer) cancelAnimationFrame(confettiTimer); ctx.clearRect(0,0,confettiCanvas.width,confettiCanvas.height); }

    // Floating hearts burst
    function burstHearts(){
      const n=18;
      for(let i=0;i<n;i++){
        const el = document.createElement('div');
        el.className='floating-heart';
        el.style.left = (50 + (Math.random()-0.5)*40) + '%';
        el.style.top = (50 + (Math.random()-0.5)*20) + '%';
        el.style.fontSize = (12+Math.random()*28)+'px';
        el.style.opacity = Math.random()*0.9 + 0.2;
        el.innerText = ['❤','💖','💘','💕'][Math.floor(Math.random()*4)];
        document.body.appendChild(el);
        const dx = (Math.random()-0.5)*240;
        const dy = - (80 + Math.random()*220);
        el.animate([
          { transform: 'translate(0,0) scale(1)', opacity:1 },
          { transform: `translate(${dx}px, ${dy}px) scale(1.2)`, opacity:0 }
        ],{duration:1500+Math.random()*900,easing:'cubic-bezier(.17,.67,.31,1)'});
        setTimeout(()=> el.remove(), 2000+Math.random()*500);
      }
    }

    // small pulse on the big text
    function pulseText(){
      loveText.animate([
        { transform: 'scale(1)' },
        { transform: 'scale(1.06)' },
        { transform: 'scale(1)' }
      ],{duration:650, easing:'ease-out'});
    }

    // initial accessibility: set focus to close when opened
    const observer = new MutationObserver(()=>{ if(overlay.classList.contains('show')) closeBtn.focus(); });
    observer.observe(overlay,{attributes:true,attributeFilter:['class']});

    // make link share-friendly by supporting ?open=1
    if(new URLSearchParams(location.search).get('open')){
      setTimeout(showLove, 700);
    }

    // Resize handling
    window.addEventListener('resize', ()=>{ if(overlay.classList.contains('show')) makeConfetti(); });

  </script></body>
</html>