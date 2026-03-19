<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>✨ Happy Birthday Begum ✨</title>
<style>
body {
  margin: 0;
  font-family: "Comic Sans MS", cursive;
  background: linear-gradient(135deg, #ffe4ec, #f8e1ff, #fff5e6);
  overflow: hidden;
}

/* Sparkles */
.sparkle {
  position: absolute;
  width: 6px;
  height: 6px;
  background: white;
  border-radius: 50%;
  opacity: 0.8;
  animation: fall 6s linear infinite;
}

@keyframes fall {
  0% { transform: translateY(-10px); opacity: 1; }
  100% { transform: translateY(100vh); opacity: 0; }
}

/* Container */
.container {
  text-align: center;
  padding-top: 50px;
}

/* Boxes */
.boxes {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-top: 50px;
}

.box {
  width: 100px;
  height: 100px;
  background: #fff;
  border-radius: 20px;
  cursor: pointer;
  box-shadow: 0 0 20px rgba(255, 182, 193, 0.5);
  transition: transform 0.3s;
}

.box:hover {
  transform: scale(1.1);
}

/* Hidden content */
.hidden {
  display: none;
}

/* Scrapbook page */
.page {
  position: absolute;
  width: 100%;
  height: 100%;
  background: #fff0f5;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  animation: fadeIn 1s ease;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

/* Banner */
.banner {
  font-size: 24px;
  background: #ffe4ec;
  padding: 10px 20px;
  border-radius: 15px;
  margin-bottom: 20px;
}

/* Photo placeholder */
.photo {
  width: 200px;
  height: 200px;
  background: #fff;
  border: 2px dashed #ccc;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 15px;
}

/* Bunny */
.bunny {
  position: absolute;
  bottom: 20px;
  left: 20px;
  width: 120px;
  animation: hop 2s infinite;
}

@keyframes hop {
  0%,100% { transform: translateY(0); }
  50% { transform: translateY(-20px); }
}
</style>
</head>

<body>

<div class="container" id="start">
  <h1>Open me... if you dare 👀✨</h1>

  <div class="boxes">
    <div class="box" onclick="openBox('flower')"></div>
    <div class="box" onclick="openBox('candy')"></div>
    <div class="box" onclick="openBox('cat')"></div>
    <div class="box" onclick="openBox('star')"></div>
    <div class="box" onclick="openMain()"></div>
  </div>
</div>

<!-- Scrapbook Page -->
<div id="page1" class="page hidden">
  <div class="banner">Your message here 💗</div>
  <div class="photo">Insert Photo 📷</div>
</div>

<!-- Bunny -->
<img class="bunny" src="https://i.imgur.com/8QfQZ6F.png">

<script>

/* Sparkles generator */
for(let i=0;i<40;i++){
  let s = document.createElement("div");
  s.className="sparkle";
  s.style.left=Math.random()*100+"vw";
  s.style.animationDuration=(3+Math.random()*3)+"s";
  document.body.appendChild(s);
}

/* Box actions */
function openBox(type){
  alert("You found: " + type + " ✨");
}

function openMain(){
  document.getElementById("start").style.display="none";
  document.getElementById("page1").classList.remove("hidden");
}

</script>

</body>
</html>
