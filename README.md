<html lang="my">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Happy Birthday, Little Sis!</title>
<style>
:root{--pink:#ff7eb6;--rose:#ff4f91;--cream:#fff8f4;--ink:#6c3651}
*{box-sizing:border-box}
body{margin:0;min-height:100vh;font-family:system-ui,-apple-system,"Noto Sans Myanmar",sans-serif;color:var(--ink);background:radial-gradient(circle at top,#fff 0,#fff0f6 42%,#ffe0ed 100%);overflow-x:hidden}
.wrap{min-height:100vh;display:grid;place-items:center;padding:24px 14px;position:relative}
.card{width:min(100%,440px);background:#ffffffd9;border:1px solid #fff;box-shadow:0 18px 60px #c75b8b25;border-radius:30px;padding:26px 22px 30px;text-align:center;position:relative;z-index:2;backdrop-filter:blur(8px)}
.tag{font-size:.78rem;letter-spacing:3px;color:#d95b91;font-weight:800}
h1{font-size:clamp(2rem,9vw,3rem);line-height:1.1;margin:12px 0;color:#e94f91}
h2{font-size:1.15rem;margin:0 0 14px}
p{line-height:1.9;margin:10px 0}
.photo{width:190px;height:190px;border-radius:50%;margin:18px auto 20px;overflow:hidden;border:7px solid white;box-shadow:0 8px 25px #e47aa84c;background:linear-gradient(135deg,#ffe0ed,#fff7e9);display:grid;place-items:center;position:relative}
.photo img{width:100%;height:100%;object-fit:cover;display:none}
.photo .placeholder{font-size:4rem}
.upload{display:inline-block;margin:2px 0 15px;background:#fff0f6;border:1px dashed #e77ca7;border-radius:999px;padding:10px 15px;color:#b83f76;font-size:.9rem;font-weight:700;cursor:pointer}
input{display:none}
.message{background:#fff6fa;border-radius:20px;padding:16px 15px;margin-top:8px}
button{border:0;border-radius:999px;background:linear-gradient(135deg,#ff8fbd,#ef4d91);color:white;padding:13px 22px;font-weight:800;font-size:1rem;box-shadow:0 7px 18px #ed5c9b45;cursor:pointer;margin-top:17px}
button:active{transform:scale(.98)}
.small{font-size:.85rem;color:#a66a87}
.heart{position:fixed;top:-30px;z-index:1;pointer-events:none;animation:fall linear forwards}
@keyframes fall{to{transform:translateY(110vh) rotate(360deg);opacity:.15}}
.glow{animation:glow 2s ease-in-out infinite alternate}
@keyframes glow{from{filter:drop-shadow(0 0 2px #ffbad4)}to{filter:drop-shadow(0 0 12px #ff75ae)}}
.footer{margin-top:16px;font-size:.8rem;color:#bd7a99}
</style>
</head>
<body>
<div class="wrap">
  <main class="card">
    <div class="tag">A SPECIAL DAY FOR YOU</div>
    <h1 class="glow">Happy Birthday! 🎂</h1>
    <h2>မွေးနေ့မှာ ပျော်ရွှင်ပါစေ ညီမလေးရေ 💗</h2>
    <div class="photo" id="photoBox">
      <span class="placeholder" id="placeholder">🎀</span>
      <img id="photo" src="sis.png" alt="Little sister's photo" style="display:block">
    </div>
    <div class="message">
      လိုချင်တဲ့ဆန္ဒလေးတွေ အားလုံးပြည့်ဝပြီး<br>
      အမြဲပျော်ရွှင်ပြုံးရယ်နေနိုင်ပါစေ။ 🫶🏻<br>
      ကျန်းကျန်းမာမာနဲ့ နေ့ရက်တိုင်း လှပနေပါစေ။<br>
      <strong>💖🎁</strong>
    </div>
    <button id="wishBtn">🎉 ပျော်ရွှင်မှုလေးတွေ ဖွင့်ကြည့်မယ်</button>
    <p class="small" id="extra" hidden>ဒီနေ့လေးက ညီမလေးအတွက် အလှဆုံးနေ့လေး ဖြစ်ပါစေ! 🌷✨</p>
    <div class="footer">Made with love ♡ for my little sister</div>
  </main>
</div>
<script>
const photo=document.getElementById('photo'), placeholder=document.getElementById('placeholder');
photo.addEventListener('load',()=>{placeholder.style.display='none';});
photo.addEventListener('error',()=>{photo.style.display='none';placeholder.style.display='grid';});
document.getElementById('wishBtn').addEventListener('click',()=>{document.getElementById('extra').hidden=false;for(let i=0;i<28;i++){setTimeout(()=>{const el=document.createElement('div');el.className='heart';el.textContent=['💗','✨','🎀','💖','🌸'][Math.floor(Math.random()*5)];el.style.left=Math.random()*100+'vw';el.style.fontSize=(16+Math.random()*20)+'px';el.style.animationDuration=(3+Math.random()*4)+'s';document.body.appendChild(el);setTimeout(()=>el.remove(),7500)},i*90)}});
</script>
</body>
</html>
