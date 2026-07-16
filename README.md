<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Untuk Cintaku ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Poppins',sans-serif;
    background:linear-gradient(135deg,#1a001f,#3d0c4d,#8b104e);
    overflow:hidden;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
    color:white;
}

/* Bintang */
.star{
    position:absolute;
    width:2px;
    height:2px;
    background:white;
    border-radius:50%;
    animation:twinkle 2s infinite alternate;
}

@keyframes twinkle{
from{opacity:.2;}
to{opacity:1;}
}

/* Amplop */
.envelope{
    position:relative;
    width:340px;
    height:220px;
    cursor:pointer;
    transition:.5s;
}

.back{
    position:absolute;
    width:100%;
    height:100%;
    background:#d93c70;
    border-radius:0 0 12px 12px;
}

.front{
    position:absolute;
    width:100%;
    height:100%;
    background:#e64c82;
    clip-path:polygon(0 0,50% 55%,100% 0,100% 100%,0 100%);
}

.flap{
    position:absolute;
    width:100%;
    height:110px;
    background:#ff6b9c;
    transform-origin:top;
    transition:1.2s;
    clip-path:polygon(0 0,100% 0,50% 100%);
    z-index:3;
}

.envelope.open .flap{
    transform:rotateX(180deg);
}

/* Surat */

.letter{
    position:absolute;
    left:50%;
    top:20px;
    transform:translateX(-50%);
    width:300px;
    height:420px;
    background:white;
    color:#444;
    border-radius:18px;
    padding:25px;
    overflow:auto;
    transition:1.5s;
    z-index:2;
    transform-origin:bottom;
    opacity:0;
}

.envelope.open .letter{
    top:-390px;
    opacity:1;
}

h1{
    font-family:'Great Vibes';
    color:#e91e63;
    text-align:center;
    font-size:52px;
}

h2{
    text-align:center;
    margin-bottom:20px;
    color:#d81b60;
}

p{
    line-height:1.9;
    text-align:justify;
}

.signature{
    margin-top:30px;
    text-align:center;
    font-family:'Great Vibes';
    font-size:42px;
    color:#e91e63;
}

.note{
    position:absolute;
    bottom:40px;
    font-size:14px;
    color:#ffd6e6;
}

/* Hati */
.heart{
    position:absolute;
    color:#ff5c93;
    animation:float 6s linear forwards;
}

@keyframes float{
0%{
transform:translateY(0);
opacity:1;
}
100%{
transform:translateY(-100vh);
opacity:0;
}
}
</style>

</head>

<body>

<div class="envelope" onclick="openEnvelope()" id="env">

<div class="flap"></div>

<div class="back"></div>

<div class="front"></div>

<div class="letter">

<h1>Untuk Kamu ❤️</h1>

<h2>Cinta Terindahku</h2>

<p>

Sayang...

Jika surat ini sampai di hadapanmu,
berarti aku sedang ingin mengingatkanmu satu hal...

Bahwa di antara jutaan manusia di dunia ini,
aku bersyukur karena dipertemukan denganmu.

Terima kasih telah menjadi tempatku pulang,
tempatku tertawa,
dan tempatku menemukan ketenangan.

Aku tidak bisa menjanjikan hidup tanpa masalah,
tetapi aku berjanji akan selalu berada di sampingmu
untuk melewati semuanya bersama.

Aku mencintaimu lebih dari kata-kata yang bisa kutulis.

Semoga suatu hari nanti kita membaca surat ini
sambil tersenyum mengenang perjalanan cinta kita.

❤️

</p>

<div class="signature">
Selamanya Milikmu
</div>

</div>

</div>

<div class="note">
Klik amplop untuk membuka surat 💌
</div>

<audio id="music" loop>
<source src="https://music.youtube.com/watch?v=imGaOIm5HOk&si=rhWrT0lp54v2z7fn" type="audio/mpeg">
</audio>

<script>

for(let i=0;i<120;i++){

let star=document.createElement("div");
star.className="star";

star.style.left=Math.random()*100+"vw";
star.style.top=Math.random()*100+"vh";

star.style.animationDelay=Math.random()*3+"s";

document.body.appendChild(star);

}

function openEnvelope(){

document.getElementById("env").classList.add("open");

document.querySelector(".note").style.display="none";

document.getElementById("music").play();

}

setInterval(()=>{

let h=document.createElement("div");

h.className="heart";

h.innerHTML="❤";

h.style.left=Math.random()*100+"vw";

h.style.bottom="-20px";

h.style.fontSize=(20+Math.random()*20)+"px";

document.body.appendChild(h);

setTimeout(()=>{

h.remove();

},6000);

},300);

</script>

</body>
</html>
