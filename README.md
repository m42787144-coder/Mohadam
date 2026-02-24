<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>برای تو 🤍</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Vazirmatn:wght@300;400&display=swap" rel="stylesheet">

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#f7f2eb,#e9dfd2,#d6c7b4);
font-family:'Vazirmatn',sans-serif;
padding:20px;
}

body::before{
content:"";
position:fixed;
width:700px;
height:700px;
background:radial-gradient(circle,rgba(255,255,255,0.6),transparent 70%);
top:-200px;
right:-150px;
animation:lightMove 15s infinite alternate ease-in-out;
z-index:0;
}

@keyframes lightMove{
to{transform:translate(-200px,150px);}
}

.card{
position:relative;
z-index:1;
width:100%;
max-width:900px;
background:rgba(255,255,255,0.9);
backdrop-filter:blur(25px);
border-radius:40px;
padding:clamp(30px,5vw,70px);
box-shadow:0 40px 120px rgba(0,0,0,.15);
text-align:center;
overflow:hidden;
transition:.8s ease;
}

.card::before{
content:"";
position:absolute;
top:0;
left:0;
width:100%;
height:5px;
background:linear-gradient(to right,#b79b7f,#d8c2a8,#b79b7f);
}

h1{
font-family:'Playfair Display',serif;
font-size:clamp(24px,4vw,34px);
color:#7b5e42;
margin-bottom:30px;
letter-spacing:1px;
}

.text{
font-size:clamp(15px,2.5vw,18px);
line-height:2.3;
color:#8c6f4e;
margin-bottom:40px;
transition:.6s ease;
}

.fade{
opacity:0;
transform:translateY(-15px);
}

.videoBox{
max-height:0;
opacity:0;
overflow:hidden;
transition:1s ease;
}

.videoBox.show{
max-height:1200px;
opacity:1;
margin-top:20px;
}

video{
width:100%;
height:auto;
border-radius:25px;
box-shadow:0 25px 70px rgba(0,0,0,.25);
display:block;
}
</style>
</head>

<body>

<div class="card">
<h1>بعضی آدم‌ها اتفاقی وارد زندگی نمی‌شوند...</h1>

<div class="text" id="text">
تو از آن لحظه‌هایی هستی که زندگی را آرام‌تر،
لبخند را واقعی‌تر
و دنیا را قابل‌دوست‌داشتن‌تر می‌کنی.
این فقط یک فیلم نیست،
یادآوریِ این است که حضورت
چقدر برایم ارزشمند است.
</div>

<button id="btn" onclick="showVideo()"
style="padding:14px 45px;border:none;border-radius:50px;background:linear-gradient(45deg,#b79b7f,#a8896b);color:white;cursor:pointer;transition:.4s;box-shadow:0 15px 40px rgba(0,0,0,.2);">
تماشا کن
</button>

<div class="videoBox" id="videoBox">
<video id="video" controls>
<source src="movie.mp4" type="video/mp4">
</video>
</div>

</div>

<script>
function showVideo(){
const text = document.getElementById("text");
const btn = document.getElementById("btn");
const videoBox = document.getElementById("videoBox");
const video = document.getElementById("video");

text.classList.add("fade");
btn.classList.add("fade");

setTimeout(function(){
btn.style.display="none";
videoBox.classList.add("show");
video.play();
},600);
}
</script>

</body>
</html>
