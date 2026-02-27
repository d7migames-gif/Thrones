[Thrones-1.html](https://github.com/user-attachments/files/25594349/Thrones-1.html)[Uploading <!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- حماية أساسية -->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; img-src 'self' https:; style-src 'self' 'unsafe-inline' https:; script-src 'self' 'unsafe-inline';">

<title>Thrones | Official Kingdom</title>

<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
background:#000;
color:#fff;
font-family:Arial, sans-serif;
overflow-x:hidden;
user-select:none;
}

canvas{
position:fixed;
top:0;
left:0;
z-index:-1;
}

header{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
text-align:center;
background:linear-gradient(to bottom,rgba(0,0,0,0.7),#000);
}

h1{
font-size:70px;
letter-spacing:5px;
text-shadow:0 0 20px orange;
}

p{
opacity:0.7;
margin-top:10px;
}

.section{
padding:60px 20px;
text-align:center;
}

.card{
background:#111;
margin:20px auto;
padding:20px;
width:260px;
border-radius:15px;
transition:0.3s;
box-shadow:0 0 20px rgba(255,80,0,0.3);
}

.card:hover{
transform:scale(1.07);
box-shadow:0 0 40px rgba(255,80,0,0.8);
}

button{
margin-top:10px;
padding:10px 20px;
border:none;
border-radius:10px;
cursor:pointer;
background:linear-gradient(45deg,#ff3c00,#ff8800);
color:white;
font-weight:bold;
}

footer{
padding:20px;
text-align:center;
opacity:0.5;
font-size:14px;
}
</style>
</head>

<body>

<canvas id="rain"></canvas>

<header>
<h1>THRONES</h1>
<p>The Storm Is Guarded 🔥</p>
</header>

<section class="section">

<div class="card">
<h2>YouTube</h2>
<button onclick="secureOpen('https://www.youtube.com/@iThrones/featured')">دخول</button>
</div>

<div class="card">
<h2>Kick</h2>
<button onclick="secureOpen('https://kick.com/ithrones')">دخول</button>
</div>

<div class="card">
<h2>TikTok</h2>
<button onclick="secureOpen('https://www.tiktok.com/@ithrones')">دخول</button>
</div>

<div class="card">
<h2>X</h2>
<button onclick="secureOpen('https://x.com/iiThrones')">دخول</button>
</div>

<div class="card">
<h2>Discord</h2>
<button onclick="secureOpen('https://discord.gg/gcVTsUDPmA')">دخول</button>
</div>

</section>

<footer>
© 2026 Thrones | Secured Kingdom
</footer>

<script>

/* فتح روابط بطريقة آمنة */
function secureOpen(url){
const win = window.open(url, "_blank", "noopener,noreferrer");
if(win) win.opener = null;
}

/* منع نسخ بسيط */
document.addEventListener('contextmenu', e => e.preventDefault());
document.addEventListener('keydown', function(e){
if(e.ctrlKey && (e.key === 'u' || e.key === 's' || e.key === 'c')){
e.preventDefault();
}
});

/* تأثير المطر */
const canvas=document.getElementById("rain");
const ctx=canvas.getContext("2d");
canvas.width=window.innerWidth;
canvas.height=window.innerHeight;

let drops=[];
for(let i=0;i<250;i++){
drops.push({
x:Math.random()*canvas.width,
y:Math.random()*canvas.height,
length:Math.random()*20,
speed:4+Math.random()*4
});
}

function drawRain(){
ctx.clearRect(0,0,canvas.width,canvas.height);
ctx.strokeStyle="rgba(255,255,255,0.2)";
ctx.beginPath();
for(let d of drops){
ctx.moveTo(d.x,d.y);
ctx.lineTo(d.x,d.y+d.length);
}
ctx.stroke();

for(let d of drops){
d.y+=d.speed;
if(d.y>canvas.height){
d.y=0;
d.x=Math.random()*canvas.width;
}
}
requestAnimationFrame(drawRain);
}
drawRain();

</script>

</body>
</html>Thrones-1.html…]()
