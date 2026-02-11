---
layout: home
---

<style>
/* ===== GLOBAL ===== */
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(-45deg, #0f2027, #203a43, #2c5364, #1c1c1c);
  background-size: 400% 400%;
  animation: gradient 15s ease infinite;
  color: white;
  padding-top: 64px;
}

@keyframes gradient {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
}

/* ===== MINIMA HEADER – WHITE ===== */
.site-header {
  background: rgba(255,255,255,0.9) !important;
  backdrop-filter: blur(12px);
  border-top: none !important;
  border-bottom: none !important;
}

.site-title,
.site-nav a {
  color: #111 !important;
  font-weight: 500;
}

.site-nav a:hover,
.site-nav a.active {
  color: #00bcd4 !important;
}

.menu-icon svg path {
  fill: #111;
}

/* ===== HERO ===== */
.hero {
  height: calc(100vh - 64px);
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

@media (min-width: 1024px) {
  .hero {
    height: calc(120vh - 64px);
  }
}

.glass {
  background: rgba(255,255,255,0.08);
  padding: 60px;
  border-radius: 25px;
  backdrop-filter: blur(20px);
  box-shadow: 0 10px 40px rgba(0,0,0,0.4);
  max-width: 700px;
}

/* ===== TYPING ===== */
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

/* ===== BUTTON ===== */
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

/* ===== SECTIONS ===== */
section {
  padding: 120px 20px;
  text-align: center;
  opacity: 0;
  transform: translateY(60px);
  transition: opacity 1s, transform 1s;
  scroll-margin-top: 90px;
}

section.visible {
  opacity: 1;
  transform: translateY(0);
}
/* ===== ABOUT SECTION ===== */
.about-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
  max-width: 1100px;
  margin: 0 auto;
}

.about-text {
  text-align: left;
}

.about-text h2 {
  margin-bottom: 20px;
}

.about-image img {
  width: 100%;
  max-width: 360px;
  border-radius: 24px;
  box-shadow: 0 20px 40px rgba(0,0,0,0.4);
}

/* MOBILE */
@media (max-width: 768px) {
  .about-wrapper {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .about-text {
    text-align: center;
  }

  .about-image img {
    margin: 0 auto;
  }
}

/* ===== CARDS ===== */
.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
  margin-top: 60px;
}

/* TABLET */
@media (max-width: 1024px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
    gap: 35px;
  }
}

/* MOBILE */
@media (max-width: 640px) {
  .cards {
    grid-template-columns: 1fr;
    gap: 30px;
  }
}

.card {
  background: rgba(255,255,255,0.08);
  padding: 40px;
  border-radius: 24px;
  backdrop-filter: blur(12px);
  transition: transform 0.4s, box-shadow 0.4s;
}

.card:hover {
  transform: translateY(-12px);
  box-shadow: 0 14px 35px rgba(0,0,0,0.45);
}
</style>

<div class="hero">
  <div class="glass">
    <h1>Witaj 👋</h1>
    <h2 class="typing">Tworzę nowoczesne rozwiązania webowe</h2>
    <p>Projektuję szybkie, estetyczne i responsywne strony internetowe.</p>
    <a href="#oferta"><button class="btn">Poznaj ofertę</button></a>
  </div>
</div>

<section id="o-mnie" class="about">
    <div class="about-wrapper">
      <div class="about-text">
        <h2>O mnie</h2>
        <p>
          Jestem web developerem specjalizującym się w tworzeniu nowoczesnych aplikacji
          i stron internetowych.<br>
          Łączę design, wydajność i dobre praktyki programistyczne.
        </p>
      </div>
  
      <div class="about-image">
        <img src="/assets/img/me.jpg" alt="Moje zdjęcie">
      </div>
    </div>
  </section>
  

<section id="oferta">
<h2> Moje usługi</h2>
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
  <div class="card">
    <h3>Konsultacje programistyczne</h3>
    <p>Sdsfaaaaaaaaaa aaaaaaaaaaaaaa aaaaaafdsaa</p>
  </div>
</div>
</section>

<section id="projekty">
<h2> Wybrane projekty</h2>
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
  <div class="card">
    <h3>Projekt 4</h3>
    <p>Landing page generujący leady sprzedażowe.</p>
  </div>
</div>
</section>

<section id="kontakt">
<h2>Kontakt</h2>
📧 email@example.com  
📱 +48 123 456 789  
<br><br>
<button class="btn">Napisz do mnie</button>
</section>

<script>
// reveal sections
const sections = document.querySelectorAll("section");

window.addEventListener("scroll", () => {
  sections.forEach(sec => {
    if (sec.getBoundingClientRect().top < window.innerHeight - 100) {
      sec.classList.add("visible");
    }
  });
});

// active link in Minima navbar
const navLinks = document.querySelectorAll('.site-nav a');

window.addEventListener('scroll', () => {
  let fromTop = window.scrollY + 100;

  navLinks.forEach(link => {
    const section = document.querySelector(link.getAttribute('href'));
    if (!section) return;

    if (
      section.offsetTop <= fromTop &&
      section.offsetTop + section.offsetHeight > fromTop
    ) {
      link.classList.add('active');
    } else {
      link.classList.remove('active');
    }
  });
});
</script>
