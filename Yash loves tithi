<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sorry Tithi ❤️</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    height: 100vh;
    background: radial-gradient(circle at top, #ff9a9e, #fad0c4, #fbc2eb);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-family: 'Courier New', monospace;
    color: #fff;
    text-align: center;
}

/* Floating background hearts */
.bg-heart {
    position: fixed;
    bottom: -30px;
    font-size: 24px;
    animation: floatUp linear infinite;
    opacity: 0.8;
}

@keyframes floatUp {
    0% { transform: translateY(0); opacity: 0.8; }
    100% { transform: translateY(-120vh); opacity: 0; }
}

/* Big heart text */
pre {
    font-size: 5vw;
    line-height: 1.1;
    white-space: pre;
    user-select: none;
}

/* Sorry section */
.sorry {
    display: none;
    animation: fadeIn 2s ease forwards;
}

.sorry h1 {
    font-size: 12vw;
    margin: 10px 0;
}

.sorry h2 {
    font-size: 7vw;
}

.sorry p {
    font-size: 5vw;
    max-width: 90%;
    margin: 10px auto;
}

@keyframes fadeIn {
    from { opacity: 0; transform: scale(0.7); }
    to { opacity: 1; transform: scale(1); }
}

/* Tap hint */
.tap {
    position: fixed;
    bottom: 15px;
    font-size: 14px;
    opacity: 0.8;
}
</style>
</head>

<body>

<!-- Music -->
<audio id="music" loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3" type="audio/mpeg">
</audio>

<div class="tap">💖 Tap anywhere 💖</div>

<pre id="heart"></pre>

<div class="sorry" id="sorryText">
    <h1>💔 SORRY 💔</h1>
    <h2>Tithi 💖</h2>
    <p>😔 I’m really sorry for irritating you</p>
    <p>😞 I spoke badly and said wrong things about your female best friend</p>
    <p>🙏 I should have respected your feelings</p>
    <p>💌 Please message me back soon</p>
    <p>— Yash ❤️</p>
</div>

<script>
/* Music play on first tap */
document.body.addEventListener('click', () => {
    document.getElementById("music").play();
}, { once: true });

/* Background hearts */
setInterval(() => {
    const h = document.createElement("div");
    h.className = "bg-heart";
    h.innerHTML = "❤️";
    h.style.left = Math.random() * 100 + "vw";
    h.style.fontSize = (20 + Math.random() * 30) + "px";
    h.style.animationDuration = (5 + Math.random() * 4) + "s";
    document.body.appendChild(h);
    setTimeout(() => h.remove(), 9000);
}, 350);

/* Big heart text */
const heartLines = [
"        I LOVE YOU        I LOVE YOU",
"    I LOVE YOU                            I LOVE YOU",
" I LOVE YOU                                  I LOVE YOU",
" I LOVE YOU                                  I LOVE YOU",
"    I LOVE YOU                            I LOVE YOU",
"        I LOVE YOU        I LOVE YOU",
"                I LOVE YOU",
"                    I LOVE YOU",
"",
"               💖 TITHI 💖"
];

let line = 0, char = 0;
const heartEl = document.getElementById("heart");

function typeHeart() {
    if (line < heartLines.length) {
        if (char < heartLines[line].length) {
            heartEl.innerHTML += heartLines[line][char];
            char++;
            setTimeout(typeHeart, 25);
        } else {
            heartEl.innerHTML += "\n";
            line++;
            char = 0;
            setTimeout(typeHeart, 40);
        }
    } else {
        setTimeout(() => {
            document.getElementById("sorryText").style.display = "block";
        }, 1000);
    }
}

typeHeart();
</script>

</body>
</html>
