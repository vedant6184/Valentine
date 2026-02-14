<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Just a Small Effort ❤️</title>

<style>
body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(to top, #0b0f2f, #1c1f4a, #3a0f4f);
    overflow-x: hidden;
    color: white;
    text-align: center;
    position: relative;
}

/* 🌌 Night Stars */
.stars {
    position: fixed;
    width: 100%;
    height: 100%;
    background: transparent;
    z-index: -3;
}

.stars::after {
    content: "";
    position: absolute;
    width: 2px;
    height: 2px;
    background: white;
    box-shadow:
        50px 100px white, 150px 200px white, 300px 400px white,
        500px 150px white, 700px 250px white, 900px 300px white,
        1100px 450px white, 1300px 100px white, 200px 500px white,
        600px 600px white, 800px 50px white, 1000px 200px white;
    animation: twinkle 2s infinite alternate;
}

@keyframes twinkle {
    from { opacity: 0.5; }
    to { opacity: 1; }
}

body::before {
    content: "";
    position: fixed;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle at center, rgba(255,255,255,0.15), transparent 60%);
    animation: glowMove 8s infinite alternate;
    z-index: -2;
}

@keyframes glowMove {
    from { transform: translate(-10%, -10%) scale(1); }
    to { transform: translate(-20%, -20%) scale(1.2); }
}

section {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 40px;
    transition: 1s;
    position: relative;
    z-index: 2;
}

h1 { font-size: 40px; margin-bottom: 20px; }
p { font-size: 20px; max-width: 700px; line-height: 1.6; }

button {
    margin-top: 20px;
    padding: 12px 30px;
    font-size: 18px;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    background: white;
    color: #ff2e63;
    transition: 0.3s;
}
button:hover { transform: scale(1.1); }

/* 🖼 Horizontal Image Layout */
.image-row {
    display: flex;
    gap: 25px;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    margin-top: 20px;
}

.image-row img {
    width: 250px;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    cursor: pointer;
    transition: transform 0.3s ease;
}

.image-row img:hover {
    transform: scale(1.05);
}

/* 🔍 Lightbox */
.lightbox {
    position: fixed;
    display: none;
    justify-content: center;
    align-items: center;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.9);
    backdrop-filter: blur(5px);
    z-index: 9999;
}

.lightbox img {
    max-width: 90%;
    max-height: 85%;
    border-radius: 20px;
    animation: zoomIn 0.4s ease;
}

@keyframes zoomIn {
    from { transform: scale(0.6); opacity: 0; }
    to { transform: scale(1); opacity: 1; }
}

/* Confetti */
.confetti {
    position: fixed;
    width: 12px;
    height: 12px;
    top: -10px;
    animation: fall 3s linear forwards;
}
@keyframes fall {
    to {
        transform: translateY(100vh) rotate(720deg);
        opacity: 0;
    }
}

/* Petals */
.petal {
    position: fixed;
    top: -50px;
    font-size: 24px;
    animation: fallPetals linear infinite;
    z-index: 0;
}
@keyframes fallPetals {
    0% { transform: translateY(-50px) rotate(0deg); opacity: 1; }
    100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
}

/* Hearts */
.heart {
    position: fixed;
    bottom: -50px;
    font-size: 20px;
    animation: floatHearts linear infinite;
    opacity: 0.7;
    z-index: -1;
}
@keyframes floatHearts {
    0% { transform: translateY(0) scale(1); opacity: 0.7; }
    100% { transform: translateY(-110vh) scale(1.5); opacity: 0; }
}
</style>
</head>

<body>

<div class="stars"></div>

<audio autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_5f5b0b4a28.mp3?filename=romantic-background-112191.mp3" type="audio/mpeg">
</audio>

<section>
    <h1>Hey, My Cutuuu ❤️</h1>
    <p>
        The way you smile makes my worst days disappear.
        The way you talk feels like my favorite song on repeat.
        And the way you simply exist… it makes my world softer, sweeter, and so much more beautiful.
        You didn’t just change my life you became the best part of it. 💕
    </p>
    <button onclick="nextPage()">Next ➜</button>
    <button onclick="playMusic()">Play Our Song 🎵</button>
</section>

<section style="background: rgba(0,0,0,0.2);">
    <h1>Our Only moments 📸</h1>
    <div class="image-row">
        <img src="ourpicture.jpg">
        <img src="ourpicture1.jpeg">
        <img src="ourpicature2.jpeg">
    </div>
    <p>
        Every memory with you is becoming my favorite chapter.
        This picture isn’t just a photo… it’s proof that my happiest place is right beside you.
    </p>
    <button onclick="nextPage()">Next ➜</button>
</section>

<!-- Lightbox -->
<div class="lightbox" id="lightbox">
    <img id="lightbox-img">
</div>

<section>
    <h1>What You Mean To Me 💖</h1>
    <p>
        You are my peace on chaotic days.
        My smile without reason.
        My comfort, my heart.
        And today, I want to make something official…
    </p>
    <button onclick="nextPage()">Next ➜</button>
</section>

<section style="background: rgba(0,0,0,0.3);">
    <h1>So Will You Be My Valentine? 💍</h1>
    <p>
        Not just for a day.
        But for every sunrise, every laugh,
        and every beautiful moment we haven’t lived yet.
    </p>
    <button onclick="sayYes()">Yes, Always ❤️</button>
    <button id="noBtn">No 🙈</button>
    <h2 id="finalMessage"></h2>
</section>

<script>
let currentPage = 0;
const sections = document.querySelectorAll("section");

function nextPage() {
    if (currentPage < sections.length - 1) {
        currentPage++;
        window.scrollTo({
            top: sections[currentPage].offsetTop,
            behavior: "smooth"
        });
    }
}

function playMusic() {
    window.open("https://open.spotify.com/track/22jbgc9BtV1uiV7hKYTyDx?si=b44404f1eeb74368", "_blank");
}

function sayYes() {
    document.getElementById("finalMessage").innerHTML =
    `You didn’t just make me happy…
you made my heart feel like it finally found its home. ❤️

With you, even the smallest moments feel magical.
Your love feels safe, warm, and endlessly beautiful.

I promise to cherish you, protect what we have,
and choose you today, tomorrow, and every day after. ✨`;

    createConfetti();
}

/* 🔍 Lightbox JS */
const lightbox = document.getElementById("lightbox");
const lightboxImg = document.getElementById("lightbox-img");

document.querySelectorAll(".image-row img").forEach(img => {
    img.addEventListener("click", () => {
        lightbox.style.display = "flex";
        lightboxImg.src = img.src;
    });
});

lightbox.addEventListener("click", () => {
    lightbox.style.display = "none";
});

const noBtn = document.getElementById("noBtn");
noBtn.addEventListener("mouseover", () => {
    noBtn.style.position = "absolute";
    noBtn.style.left = Math.random() * window.innerWidth + "px";
    noBtn.style.top = Math.random() * window.innerHeight + "px";
});

/* Confetti */
function createConfetti() {
    for (let i = 0; i < 150; i++) {
        const confetti = document.createElement("div");
        confetti.classList.add("confetti");
        confetti.style.left = Math.random() * window.innerWidth + "px";
        confetti.style.backgroundColor = "hsl(" + Math.random() * 360 + ",100%,50%)";
        confetti.style.animationDuration = (Math.random() * 3 + 2) + "s";
        document.body.appendChild(confetti);
        setTimeout(() => confetti.remove(), 4000);
    }
}

/* Petals */
function createPetals() {
    for (let i = 0; i < 20; i++) {
        const petal = document.createElement("div");
        petal.classList.add("petal");
        petal.innerHTML = "🌹";
        petal.style.left = Math.random() * window.innerWidth + "px";
        petal.style.animationDuration = (Math.random() * 5 + 5) + "s";
        petal.style.fontSize = (Math.random() * 20 + 15) + "px";
        document.body.appendChild(petal);
    }
}
createPetals();

/* Hearts */
function createHearts() {
    for (let i = 0; i < 25; i++) {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.animationDuration = (Math.random() * 8 + 6) + "s";
        heart.style.fontSize = (Math.random() * 20 + 15) + "px";
        document.body.appendChild(heart);
    }
}
createHearts();
</script>

</body>
</html>
