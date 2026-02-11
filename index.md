---
layout: default
title: Strona główna
---

<style>
/* ===== BODY & GRADIENT HERO ===== */
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(-45deg, #0f2027, #203a43, #2c5364, #1c1c1c);
  background-size: 400% 400%;
  animation: gradient 15s ease infinite;
  color: white;
  scroll-behavior: smooth;
}

@keyframes gradient {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
}

/* ===== NAVIGATION ===== */
nav {
  position: fixed;
  width: 100%;
  padding: 20px 40px;
  display: flex;
  justify-content: space-between;
  background: rgba(0,0,0,0.4);
  backdrop-filter: blur(12px);
  z-index: 1000;
  transition: 0.4s;
}

nav:hover {
  background: rgba(0,0,0,0.6);
}

nav a {
  color: white;
  text-decoration: none;
  margin-left: 25px;
  font-weight: 500;
  transition: 0.3s;
}

nav a:hover {
  color: #00f2fe;
  transform: scale(1.05);
}

/* ===== HERO ===== */
.hero {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 20px;
}

.glass {
  background: rgba(255,255,255,0.08);
  padding: 60px;
  border-radius: 25px;
  backdrop-filter: blur(20px);
  box-shadow: 0 10px 40px rgba(0,0,0,0.5);
  max-width: 700px;
  animation: fadeIn 2s ease forwards;
}

@keyframes fadeIn {
  0% {opacity: 0; transform: translateY(50px);}
  100% {opacity: 1; transform: translateY(0);}
}

h1 {
  font-size: 3rem;
  margin-bottom: 20px;
}

.typing {
  border-right: 3px solid #00f2fe;
  white-space: nowrap;
  overflow: hidden;
  display: inline-block;
  animation: typing 3s steps(40), blink .7s infinite;
  font-size: 1.3rem;
}

@keyframes typing {
  from {width: 0}
  to {width: 100%}
}

@keyframes blink {
  50% {border-color: transparent}
}

.btn {
  margin-top: 30px;
  padding: 14px 35px;
  border-radius: 50px;
  border: none;
  cursor: pointer;
  font-size: 16px;
  background: linear-gradient(90deg,#00f2fe,#4facfe);
  color: white;
  transition: 0.4s;
}

.btn:hover {
  transform: scale(1.1);
  box-shadow: 0 0 25px #00f2fe;
}

/* ===== SEKCJE ===== */
section {
  padding: 120px 20px;
  text-align: center;
  opacity: 0;
  transform: translateY(60px);
  transition: 1s;
}

section.visible {
  opacity: 1;
  transform: translateY(0);
}

section h2 {
  font-size: 2.5rem;
  margin-bottom: 40px;
}

/* ===== GRID KART ===== */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
  gap: 30px;
  margin-top: 50px;
}

.card {
  background: rgba(255,255,255,0.08);
  padding: 30px;
  border-radius: 20px;
  backdrop-filter: blur(10px);
  transition: 0.4s;
  cursor: pointer;
}

.card:hover {
  transform: translateY(-10px) scale(1.03);
  box-shadow: 0 10px 30px rgba(0,0,0,0.5);
}

.card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 15px;
}

/* ===== FOOTER ===== */
footer {
  padding: 40px;
  text-align: center;
  background: rgba(0,0,0,0.4);
  margin-top: 50px;
}
</style>

<nav>
  <div><strong>Moja Strona</strong></div>
  <div>
    <a href="#o-mnie">O mnie</a>
    <a href="#oferta">Oferta</a>
    <a href="#projekty">Projekty</a>
    <a href="#kontakt">Kontakt</a>
  </div>
</nav>

<div class="hero">
  <div class="glass">
    <h1>Witaj 👋</h1>
    <h2 class="typing">Tworzę nowoczesne rozwiązania webowe</h2>
    <p>Projektuję szybkie, estetyczne i responsywne strony internetowe.</p>
    <a href="#oferta"><button class="btn">Poznaj ofertę</button></a>
  </div>
</div>

<section id="o-mnie">
  <h2>O mnie</h2>
  <p>Jestem web developerem specjalizującym się w tworzeniu nowoczesnych aplikacji i stron internetowych.<br>
  Łączę design, wydajność i dobre praktyki programistyczne.</p>
</section>

<section id="oferta">
  <h2>Moja oferta</h2>
  <div class="cards">
    <div class="card">
      <h3>🌐 Strony WWW</h3>
      <p>Nowoczesne, responsywne strony firmowe i landing page.</p>
    </div>
    <div class="card">
      <h3>⚡ Optymalizacja</h3>
      <p>Przyspieszam istniejące strony i poprawiam SEO.</p>
    </div>
    <div class="card">
      <h3>🛠 Aplikacje Web</h3>
      <p>Systemy, dashboardy i aplikacje online.</p>
    </div>
  </div>
</section>

<section id="projekty">
  <h2>Wybrane projekty</h2>
  <div class="cards">
    <div class="card">
      <img src="assets/projekt1.jpg" alt="Projekt 1">
      <h3>Projekt 1</h3>
      <p>Nowoczesna strona dla startupu technologicznego.</p>
    </div>
    <div class="card">
      <img src="assets/projekt2.jpg" alt="Projekt 2">
      <h3>Projekt 2</h3>
      <p>Platforma rezerwacyjna z panelem administracyjnym.</p>
    </div>
    <div class="card">
      <img src="assets/projekt3.jpg" alt="Projekt 3">
      <h3>Projekt 3</h3>
      <p>Landing page generujący leady sprzedażowe.</p>
    </div>
  </div>
</section>

<section id="kontakt">
  <h2>Kontakt</h2>
  <p>📧 email@example.com<br>📱 +48 123 456 789</p>
  <button class="btn">Napisz do mnie</button>
</section>

<footer>
  © {{ site.time | date: "%Y" }} Moja Strona  
  Wszystkie prawa zastrzeżone.
</footer>

<script>
// ===== ANIMACJA SCROLL =====
const sections = document.querySelectorAll("section");
window.addEventListener("scroll", () => {
  sections.forEach(sec => {
    const top = sec.getBoundingClientRect().top;
    if(top < window.innerHeight - 100){
      sec.classList.add("visible");
    }
  });
});
</script>
