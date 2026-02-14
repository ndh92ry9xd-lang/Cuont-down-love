<!DOCTYPE html>  
<html lang="ar">  
<head>  
<meta charset="UTF-8">  
<title>سومتي ❤️</title>  
<style>  
body{  
margin:0;  
padding:0;  
background:black;  
color:white;  
text-align:center;  
font-family:Arial;  
overflow:hidden;  
}  
.container{  
margin-top:100px;  
}  
input,button{  
padding:12px;  
font-size:18px;  
border-radius:10px;  
border:none;  
margin:10px;  
}  
button{  
background:red;  
color:white;  
cursor:pointer;  
}  
.hidden{  
display:none;  
}  
.heart{  
position:fixed;  
color:red;  
font-size:20px;  
animation:float 5s linear infinite;  
}  
@keyframes float{  
0%{transform:translateY(100vh);opacity:1;}  
100%{transform:translateY(-10vh);opacity:0;}  
}  
</style>  
</head>  
<body>  
  
<div class="container" id="login">  
<h2>اكتبي الرمز لفتح قلب محمد ❤️</h2>  
<input type="password" id="code" placeholder="اكتبي الرمز هنا">  
<br>  
<button onclick="checkCode()">فتح</button>  
<p id="error" style="color:red;"></p>  
</div>  
  
<div class="container hidden" id="content">  
<h1>من يوم ما عرفتك يا سومتي ❤️</h1>  
<h2 id="days"></h2>  
  
<audio autoplay controls>  
<source src="PUT_YOUR_SONG_LINK_HERE.mp3" type="audio/mpeg">  
</audio>  
</div>  
  
<script>  
function checkCode(){  
let code=document.getElementById("code").value;  
if(code==="612025"){  
document.getElementById("login").classList.add("hidden");  
document.getElementById("content").classList.remove("hidden");  
calculateDays();  
startHearts();  
}else{  
document.getElementById("error").innerHTML="الرمز غلط ❤️";  
}  
}  
  
function calculateDays(){  
let start=new Date("2025-01-06");  
let today=new Date();  
let diff=today-start;  
let days=Math.floor(diff/(1000*60*60*24));  
document.getElementById("days").innerHTML=  
"صارلنا مع بعض "+days+" يوم ❤️";  
}  
  
function startHearts(){  
setInterval(function(){  
let heart=document.createElement("div");  
heart.classList.add("heart");  
heart.innerHTML="❤️";  
heart.style.left=Math.random()*100+"vw";  
heart.style.fontSize=(Math.random()*20+10)+"px";  
document.body.appendChild(heart);  
setTimeout(()=>heart.remove(),5000);  
},300);  
}  
</script>  
  
</body>  
</html>  
