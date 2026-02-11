---
layout: default
title: Strona główna
---

<style>
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(-45deg, #0f2027, #203a43, #2c5364, #1c1c1c);
  background-size: 400% 400%;
  animation: gradient 15s ease infinite;
  color: white;
  padding-top: 60px; /* ODSTĘP NA HEADER */
}

@keyframes gradient {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
}

/* FIXED HEADER */
header {
  position: fixed;
  top: 0;
  width: 100%;
  height: 60px;
  line-height: 60px;
  backdrop-filter: blur(10px);
  background: rgba(0,0,0,0.4);
  display: flex;
  justify-content: center;
  padding: 0 20px;
  z-index: 1000;
  box-sizing: border-box;
}

nav a {
  color: white;
  text-decoration: none;
  margin: 0 20px;
  font-weight: 500;
  transition: color 0.3s, text-shadow 0.3s;
  cursor: pointer;
}

nav a:hover,
nav a.active {
  color: #00f2fe;
  text-shadow: 0 0 10px #00f2fe;
}

.hero {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.glass {
  background: rgba(255,255,255,0.08);
  padding: 60px;
  border-radius: 25px;
  backdrop-filter: blur(20px);
  box-shadow: 0 10px 40px rgba(0,0,0,0.4);
  max-width: 700px;
}

.typing {
  border-right: 3px solid #00f2fe;
  white-space: nowrap;
  overflow: hidden;
  display: inline-block;
  animation: typing 3s steps(30), blink .7s infinite;
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

section {
  padding: 120px 20px;
  text-align: center;
  opacity: 0;
  transform: translateY(60px);
  transition: opacity 1s, transform 1s;
  scroll-margin-top: 70px; /* ODSTĘP DLA PRZEWIJANIA DO ANCHORA */
}

section.visible {
  opacity: 1;
  transform: translateY(0);
}

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
  transition: transform 0.4s, box-shadow 0.4s;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 30px rgba(0,0,0,0.4);
}

footer {
  padding: 40px;
  text-align: center;
  background: rgba(0,0,0,0.4);
}

/* DODATKOWO - AKTYWNA ZAKŁADKA W MENU PODCZAS SCROLLA */
</style>

<header>
  <nav>
    <a href="#o-mnie" class="nav-link">O mnie</a>
    <a href="#oferta" class="nav-link">Usługi</a>
    <a href="#projekty" class="nav-link">Projekty</a>
    <a href="#kontakt" class="nav-link">Kontakt</a>
  </nav>
</header>

<div class="hero">
  <div class="glass">
    <h1>Witaj 👋</h1>
    <h2 class="typing">Tworzę nowoczesne rozwiązania webowe</h2>
    <p>Projektuję szybkie, estetyczne i responsywne strony internetowe.</p>
    <a href="#oferta"><button class="btn">Poznaj ofertę</button></a>
  </div>
</div>

<section id="o-mnie">
## O mnie

Jestem web developerem specjalizującym się w tworzeniu nowoczesnych aplikacji i stron internetowych.  
Łączę design, wydajność i dobre praktyki programistyczne.

</section>

<section id="oferta">
## Moje usługi

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
## Wybrane projekty

<div class="cards">
  <div class="card">
    <h3>Projekt 1</h3>
    <p>Nowoczesna strona dla startupu technologicznego.</p>
  </div>
  <div class="card">
    <h3>Projekt 2</h3>
    <p>Platforma rezerwacyjna z panelem administracyjnym.</p>
  </div>
  <div class="card">
    <h3>Projekt 3</h3>
    <p>Landing page generujący leady sprzedażowe.</p>
  </div>
</div>

</section>

<section id="kontakt">
## Kontakt

📧 email@example.com  
📱 +48 123 456 789  

<button class="btn">Napisz do mnie</button>

</section>

<footer>
© {{ site.time | date: "%Y" }} {{ site.title }}  
Wszystkie prawa zastrzeżone.
</footer>

<script>
// Animacja pojawiania się sekcji przy scrollu
const sections = document.querySelectorAll("section");

window.addEventListener("scroll", () => {
  sections.forEach(sec => {
    const top = sec.getBoundingClientRect().top;
    if(top < window.innerHeight - 100){
      sec.classList.add("visible");
    }
  });
});

// Podświetlanie aktywnej zakładki w menu
const navLinks = document.querySelectorAll('nav a');

window.addEventListener('scroll', () => {
  let fromTop = window.scrollY + 80; // offset na wysokość headera

  navLinks.forEach(link => {
    const section = document.querySelector(link.hash);
    if(section.offsetTop <= fromTop && (section.offsetTop + section.offsetHeight) > fromTop) {
      link.classList.add('active');
    } else {
      link.classList.remove('active');
    }
  });
});
</script>
