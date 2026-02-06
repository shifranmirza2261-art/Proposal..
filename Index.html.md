<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<title>Just One Question 💍</title>  
  
<style>  
body {  
    margin: 0;  
    height: 100vh;  
    background: linear-gradient(135deg, #ffd1dc, #ff9a9e);  
    display: flex;  
    align-items: center;  
    justify-content: center;  
    font-family: 'Georgia', serif;  
    overflow: hidden;  
    transition: background 1s;  
}  
  
/* Proposal Card */  
.card {  
    background: #fff;  
    padding: 40px 30px;  
    border-radius: 25px;  
    box-shadow: 0 15px 40px rgba(0,0,0,0.25);  
    text-align: center;  
    width: 320px;  
    position: relative;  
}  
  
.card::before {  
    content: "💍";  
    font-size: 40px;  
    position: absolute;  
    top: -20px;  
    left: 50%;  
    transform: translateX(-50%);  
    background: white;  
    border-radius: 50%;  
    padding: 5px 10px;  
}  
  
h1 {  
    color: #d6336c;  
    margin-bottom: 20px;  
}  
  
button {  
    padding: 12px 26px;  
    margin: 10px;  
    font-size: 18px;  
    border: none;  
    border-radius: 25px;  
    cursor: pointer;  
    background: #ff4d88;  
    color: white;  
    position: relative;  
}  
  
#yesBtn {  
    background: #ff85a2;  
}  
  
button:hover {  
    transform: scale(1.1);  
}  
  
/* Hearts */  
.heart {  
    position: absolute;  
    font-size: 26px;  
    animation: float 4s linear infinite;  
}  
  
@keyframes float {  
    0% { transform: translateY(100vh); opacity: 1; }  
    100% { transform: translateY(-10vh); opacity: 0; }  
}  
  
/* Pop text */  
.popup {  
    position: absolute;  
    font-size: 38px;  
    color: white;  
    font-weight: bold;  
    animation: pop 1.5s ease-out forwards;  
}  
  
@keyframes pop {  
    0% { transform: scale(0); opacity: 0; }  
    50% { transform: scale(1.2); opacity: 1; }  
    100% { transform: scale(1); opacity: 0; }  
}  
</style>  
</head>  
  
<body>  
  
<!-- Romantic Music -->  
<audio autoplay loop>  
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">  
</audio>  
  
<div class="card" id="card">  
    <h1>Will you be the love of my life? 💖</h1>  
  
    <button id="yesBtn">Yes</button>  
    <button onclick="celebrate()">Of course</button>  
</div>  
  
<script>  
// Yes button runs away  
const yesBtn = document.getElementById("yesBtn");  
  
yesBtn.addEventListener("mouseover", () => {  
    const x = Math.random() * 200 - 100;  
    const y = Math.random() * 200 - 100;  
    yesBtn.style.transform = `translate(${x}px, ${y}px)`;  
});  
  
// Celebration  
function celebrate() {  
    document.body.style.background = "linear-gradient(135deg, #ff4d6d, #ff99ac)";  
    document.getElementById("card").style.display = "none";  
  
    setInterval(() => {  
        const heart = document.createElement("div");  
        heart.className = "heart";  
        heart.innerHTML = "💖";  
        heart.style.left = Math.random() * 100 + "vw";  
        document.body.appendChild(heart);  
        setTimeout(() => heart.remove(), 4000);  
    }, 200);  
  
    setInterval(() => {  
        const text = document.createElement("div");  
        text.className = "popup";  
        text.innerText = "MY BEBUUUUUU SPOTTED 💘";  
        text.style.left = Math.random() * 60 + 20 + "vw";  
        text.style.top = Math.random() * 60 + 20 + "vh";  
        document.body.appendChild(text);  
        setTimeout(() => text.remove(), 1500);  
    }, 900);  
}  
</script>  
  
</body>  
</html>  
