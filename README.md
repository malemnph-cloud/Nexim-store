# Nexim-store
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #030918;
  color: white;
}

.container {
  max-width: 1200px;
  margin: auto;
  padding: 20px;
}

header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 18px;
  flex-wrap: wrap;
  padding-bottom: 25px;
  border-bottom: 1px solid #13254a;
}

.logo {
  font-size: 27px;
  font-weight: 900;
  font-style: italic;
  background: linear-gradient(90deg,#00eaff,#ffffff,#c300ff);
  -webkit-background-clip: text;
  color: transparent;
}

.search {
  flex: 1;
  min-width: 160px;
  padding: 14px;
  border: 1px solid #243b68;
  border-radius: 13px;
  background: #101b35;
  color: white;
  font-size: 15px;
  outline: none;
}

.icons {
  color: #b7caff;
  font-size: 21px;
}

h3 {
  margin-top: 28px;
  font-size: 17px;
}

.flash {
  display: flex;
  align-items: center;
  gap: 15px;
  max-width: 530px;
  padding: 12px;
  border: 1px solid #6e32ff;
  border-radius: 15px;
  background: linear-gradient(120deg,#111a3b,#090d21);
  box-shadow: 0 0 12px #4a1b9b44;
}

.flash img {
  width: 100px;
  height: 95px;
  object-fit: cover;
  border-radius: 12px;
}

.flash-info {
  flex: 1;
}

.flash-info strong {
  font-size: 15px;
}

.button {
  display: inline-block;
  margin-top: 12px;
  padding: 8px 15px;
  border-radius: 8px;
  background: linear-gradient(90deg,#7918ff,#ad27ed);
  color: white;
  text-decoration: none;
  font-weight: bold;
  font-size: 12px;
  border: 0;
  cursor: pointer;
}

.section-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.section-title a {
  color: #648cff;
  text-decoration: none;
  font-size: 13px;
}

.games {
  display: grid;
  grid-template-columns: repeat(6,minmax(0,1fr));
  gap: 20px 15px;
}

.game {
  min-width: 0;
  text-decoration: none;
  color: white;
  cursor: pointer;
}

.game img {
  display: block;
  width: 100%;
  aspect-ratio: 1 / 1;
  object-fit: cover;
  border: 1px solid #2457bd;
  border-radius: 13px;
  background: #101a35;
  transition: .2s;
}

.game:hover img {
  transform: translateY(-4px);
  border-color: #b13cff;
  box-shadow: 0 0 15px #693cff77;
}

.game span {
  display: block;
  margin-top: 9px;
  font-size: 12px;
  font-weight: bold;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

footer {
  margin-top: 40px;
  padding: 30px 0 15px;
  border-top: 2px solid #4522ff;
  background: #050b1c;
}

.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1.2fr 1.2fr 1.5fr;
  gap: 25px;
}

footer h4 {
  font-size: 13px;
  margin-top: 5px;
}

footer p, footer a {
  font-size: 12px;
  line-height: 1.8;
  color: #9bb3e8;
}

footer a {
  display: block;
  text-decoration: none;
}

.copyright {
  margin-top: 25px;
  padding-top: 15px;
  border-top: 1px solid #26355a;
  color: #91a7d4;
  font-size: 11px;
}

@media(max-width:700px) {
  .container {
    padding: 13px;
  }

  header {
    gap: 12px;
  }

  .logo {
    font-size: 23px;
  }

  .games {
    grid-template-columns: repeat(3,minmax(0,1fr));
    gap: 18px 12px;
  }

  .footer-grid {
    grid-template-columns: repeat(2,minmax(0,1fr));
    gap: 20px;
  }

  .flash img {
    width: 80px;
    height: 80px;
  }
}
</style>
</head>

<body>
<div class="container">

<header>
  <div class="logo">◢ NEXIM<br>
    <small style="font-size:11px;letter-spacing:5px">STORE</small>
  </div>

  <input id="search" class="search"
    placeholder="⌕  Search games..."
    oninput="filterGames()">

  <div class="icons">☼　♙　🛒</div>
</header>

<h3>🔥 Flash Sale <small>①</small></h3>

<div class="flash">
  <img src="https://placehold.co/200x200/17294b/ffffff?text=BGMI"
       alt="BGMI">
  <div class="flash-info">
    <strong>BGMI PROMO UC ⭐⭐⭐⭐⭐</strong><br>
    <a class="button" href="#games">BGMI PROMO UC</a>
  </div>
  <span style="color:#00cfff;font-size:25px">›</span>
</div>

<div class="section-title">
  <h3>Popular Games <small>13</small></h3>
  <a href="#games">View All →</a>
</div>

<div class="games" id="games"></div>

<footer>
  <div class="footer-grid">

    <div>
      <div class="logo">◢ NEXIM<br>
        <small style="font-size:11px;letter-spacing:5px">STORE</small>
      </div>
      <p>
        Nexim Store is your one-stop destination
        for instant game top-ups. Access your
        favourite games anytime, anywhere,
        with secure payments and instant delivery.
      </p>
    </div>

    <div>
      <h4>HOT GAMES</h4>
      <a href="#games">🎮 BGMI</a>
      <a href="#games">🎮 BGMI PROMO</a>
      <a href="#games">🎮 Call of Duty Mobile</a>
      <a href="#games">🎮 Genshin Impact</a>
      <a href="#games">🎮 Honkai Star Rail</a>
    </div>

    <div>
      <h4>USEFUL LINKS</h4>
      <a href="#about">About Us</a>
      <a href="#privacy">Privacy Policy</a>
      <a href="#terms">Terms & Conditions</a>
      <a href="#help">Help Center</a>
      <a href="#faq">General FAQs</a>
    </div>

    <div>
      <h4>CONTACT</h4>
      <p>✉ support@neximstore.in</p>
      <p>📍 Manipur, India</p>
      <a href="#contact" class="button">🛒 24/7 Chat</a>
    </div>

  </div>

  <div class="copyright">
    © 2026 Nexim Store. All rights reserved.
    <span style="float:right">Play More · Pay Less · With Nexim</span>
  </div>
</footer>

</div>

<script>
const games = [
  ["BGMI","https://placehold.co/300x300/25354b/ffffff?text=BGMI"],
  ["BGMI PROMO","https://placehold.co/300x300/24364c/ffffff?text=BGMI+PROMO"],
  ["HONOR OF KINGS","https://placehold.co/300x300/38234f/ffffff?text=HONOR+OF+KINGS"],
  ["MLBB DOUBLE DIAMOND","https://placehold.co/300x300/153d79/ffffff?text=DOUBLE+DIAMOND"],
  ["MLBB INDONESIA","https://placehold.co/300x300/48215d/ffffff?text=MLBB+INDONESIA"],
  ["MLBB MALAYSIA","https://placehold.co/300x300/30265e/ffffff?text=MLBB+MALAYSIA"],
  ["MLBB PHILIPPINES","https://placehold.co/300x300/183e80/ffffff?text=MLBB+PHILIPPINES"],
  ["MLBB RUSSIA","https://placehold.co/300x300/1e3c72/ffffff?text=MLBB+RUSSIA"],
  ["MLBB SINGAPORE","https://placehold.co/300x300/5a2345/ffffff?text=MLBB+SINGAPORE"],
  ["MLBB SMALL PACK","https://placehold.co/300x300/5d4380/ffffff?text=MLBB+PACK"],
  ["MLBB WEEKLY PASS","https://placehold.co/300x300/3d1679/ffffff?text=WEEKLY+PASS"],
  ["MOBILE LEGENDS MOONTON","https://placehold.co/300x300/1a4178/ffffff?text=MOONTON"],
  ["SPECIAL BUNDLE","https://placehold.co/300x300/4a1874/ffffff?text=SPECIAL+BUNDLE"],
  ["Call of Duty Mobile","https://placehold.co/300x300/393920/ffffff?text=CALL+OF+DUTY"],
  ["GENSHIN IMPACT","https://placehold.co/300x300/1766a8/ffffff?text=GENSHIN+IMPACT"],
  ["HONKAI STAR RAIL","https://placehold.co/300x300/34236c/ffffff?text=HONKAI+STAR+RAIL"],
  ["Magic Chess","https://placehold.co/300x300/3d287b/ffffff?text=MAGIC+CHESS"],
  ["PUBG MOBILE","https://placehold.co/300x300/685331/ffffff?text=PUBG+MOBILE"],
  ["VALORANT","https://placehold.co/300x300/7b203c/ffffff?text=VALORANT"]
];

const gameContainer = document.getElementById("games");

function renderGames(list) {
  gameContainer.innerHTML = "";

  list.forEach(game => {
    const card = document.createElement("a");
    card.className = "game";
    card.href = "#order";

    const img = document.createElement("img");
    img.src = game[1];
    img.alt = game[0];
    img.loading = "lazy";

    const label = document.createElement("span");
    label.textContent = game[0];

    card.appendChild(img);
    card.appendChild(label);
    gameContainer.appendChild(card);
  });
}

function filterGames() {
  const query = document.getElementById("search")
    .value.toLowerCase();

  renderGames(
    games.filter(game => game[0].toLowerCase().includes(query))
  );
}

renderGames(games);
</script>
</body>
</html>
