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
  scroll-behavior: smooth;
}

@keyframes gradient {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
}

/* ===== MENU ===== */

nav {
  position: fixed;
  width: 100%;
  padding: 20px 40px;
  display: flex;
  justify-content: space-between;
  background: rgba(0,0,0,0.4);
  backdrop-filter: blur(10px);
  z-index: 1000;
}

nav a {
  color: white;
  text-decoration: none;
  margin-left: 25px;
  transition: 0.3s;
  font-weight: 500;
}

nav a:hover {
  color: #00f2fe;
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
  box-shadow: 0 10px 40px rgba(0,0,0,0.4);
  max-width: 700px;
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

/* ===== KARTY ===== */

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
  gap: 40px;
  margin-top: 60px;
}

.card {
  background: rgba(255,255,255,0.08);
  border-radius: 20px;
  overflow: hidden;
  backdrop-filter: blur(10px);
  transition: 0.4s;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 30px rgba(0,0,0,0.4);
}

.card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.card-content {
  padding: 25px;
}

footer {
  padding: 40px;
  text-align: center;
  background: rgba(0,0,0,0.4);
}
</style>

<nav>
  <div><strong>{{ site.title }}</strong></div>
  <div>
    <a href="#projekty">Projekty</a>
    <a href="#uslugi">Usługi</a>
    <a href="#kontakt">Kontakt</a>
  </div>
</nav>

<div class="hero">
  <div class="glass">
    <h1>Nowoczesne strony internetowe 🚀</h1>
    <p>Projektuję i tworzę estetyczne, szybkie i responsywne rozwiązania webowe.</p>
    <a href="#projekty"><button class="btn">Zobacz projekty</button></a>
  </div>
</div>

<section id="projekty">
<h2>Wybrane projekty</h2>

<div class="grid">

  <div class="card">
    <img src="assets/projekt1.jpg" alt="Projekt 1">
    <div class="card-content">
      <h3>Strona firmowa</h3>
      <p>Nowoczesna witryna dla firmy technologicznej.</p>
    </div>
  </div>

  <div class="card">
    <img src="assets/projekt2.jpg" alt="Projekt 2">
    <div class="card-content">
      <h3>Landing page</h3>
      <p>Strona sprzedażowa generująca leady.</p>
    </div>
  </div>

  <div class="card">
    <img src="assets/projekt3.jpg" alt="Projekt 3">
    <div class="card-content">
      <h3>Aplikacja webowa</h3>
      <p>Panel administracyjny z dashboardem.</p>
    </div>
  </div>

</div>
</section>

<section id="uslugi">
<h2>Usługi</h2>

<div class="grid">

  <div class="card">
    <div class="card-content">
      <h3>🌐 Tworzenie stron</h3>
      <p>Responsywne strony firmowe i portfolio.</p>
    </div>
  </div>

  <div class="card">
    <div class="card-content">
      <h3>⚡ Optymalizacja SEO</h3>
      <p>Przyspieszanie stron i poprawa widoczności w Google.</p>
    </div>
  </div>

  <div class="card">
    <div class="card-content">
      <h3>🛠 Aplikacje webowe</h3>
      <p>Systemy rezerwacyjne, dashboardy, dedykowane rozwiązania.</p>
    </div>
  </div>

</div>
</section>

<section id="kontakt">
<h2>Kontakt</h2>
<p>📧 email@example.com</p>
<p>📱 +48 123 456 789</p>
<button class="btn">Napisz do mnie</button>
</section>

<footer>
© {{ site.time | date: "%Y" }} {{ site.title }}
</footer>

<script>
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
