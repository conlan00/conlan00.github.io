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
    0% {
      background-position: 0% 50%;
    }

    50% {
      background-position: 100% 50%;
    }

    100% {
      background-position: 0% 50%;
    }
  }

  /* ===== MINIMA HEADER – WHITE ===== */
  /* ===== MINIMA HEADER – WHITE ===== */
  .site-header {
    padding: 10px 20px;
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 999;
    background: rgba(255, 255, 255, 0.9) !important;
    backdrop-filter: blur(12px);
    border-top: none !important;
    border-bottom: none !important;
    box-sizing: border-box;
  }

  .site-title {
    font-size: 1.2rem;
  }

  .site-nav a {
    font-size: 0.95rem;
    padding: 6px 10px;
  }

  .site-nav a:hover,
  .site-nav a.active {
    color: #00bcd4 !important;
  }

  .menu-icon svg path {
    fill: #111;
  }

  /* MOBILE NAV */
  @media (max-width: 768px) {
    .site-nav {
      display: none;
    }
  }



  /* ===== HERO ===== */
  .hero {
    width: 100%;
    /* Pełna szerokość */
    padding: 20px;
    /* Margines wewnętrzny na małych ekranach */
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    box-sizing: border-box;
    /* Zapobiega wyciekaniu paddingu */
  }

  @media (min-width: 1024px) {
    .hero {
      height: calc(120vh - 64px);
    }
  }

  .glass {
    width: 100%;
    /* Pełna szerokość kontenera */
    max-width: 1000px;
    /* Limit szerokości na dużych ekranach */
    padding: 40px 20px;
    /* Dopasowany padding do telefonów */
    border-radius: 20px;
    backdrop-filter: blur(20px);
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.4);
  }

  /* MOBILE */
  @media (max-width: 768px) {
    .hero {
      height: auto;
      /* Wysokość dopasowana do zawartości */
      padding: 40px 10px;
    }

    .glass {
      padding: 30px 15px;
      border-radius: 15px;
    }

    .typing {
      font-size: 1.2rem;
      /* Mniejsze litery na telefonach */
      white-space: normal;
      /* tekst może się zawijać */
      display: inline;
      /* lub block, jeśli chcesz osobną linię */
      animation: none;
      /* opcjonalnie wyłącz animację typing, bo może źle działać przy zawijaniu */
      border-right: none;
    }

    .btn {
      padding: 12px 25px;
      font-size: 14px;
    }
  }

  /* ===== TYPING ===== */
  .typing {
    border-right: 3px solid #00f2fe;
    white-space: nowrap;
    overflow: hidden;
    display: inline-block;
    animation: typing 3s steps(30), blink .7s infinite;
    max-width: 100%;
    /* dopasowanie do kontenera */
  }

  @keyframes typing {
    from {
      width: 0
    }

    to {
      width: 100%
    }
  }

  @keyframes blink {
    50% {
      border-color: transparent
    }
  }

  /* ===== BUTTON ===== */
  .btn {
    margin-top: 30px;
    padding: 14px 35px;
    border-radius: 50px;
    border: none;
    cursor: pointer;
    font-size: 16px;
    background: linear-gradient(90deg, #00f2fe, #4facfe);
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
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
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

    .hero {
      width: 100%;
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
    background: rgba(255, 255, 255, 0.08);
    padding: 40px;
    border-radius: 24px;
    backdrop-filter: blur(12px);
    transition: transform 0.4s, box-shadow 0.4s;
  }

  .card:hover {
    transform: translateY(-12px);
    box-shadow: 0 14px 35px rgba(0, 0, 0, 0.45);
  }

  /* ===== PROJECT CARDS ===== */
  .projects {
    margin-top: 60px;
  }

  .project-card {
    padding: 0;
    overflow: hidden;
  }

  .project-image img {
    width: 100%;
    display: block;
    border-radius: 20px 20px 0 0;
    transition: transform .5s;
  }

  .project-card:hover .project-image img {
    transform: scale(1.05);
  }

  .project-card h3 {
    margin-top: 20px;
  }

  .project-card p {
    padding: 0 30px 30px;
  }

  /* MOBILE */
  @media (max-width: 640px) {
    .project-card p {
      padding: 0 20px 25px;
    }
  }

  /* ===== PROCESS / WSPÓŁPRACA ===== */

  .process-section {
    max-width: 1200px;
    margin: 0 auto;
  }

  .process-section h2 {
    font-size: 2.2rem;
    margin-bottom: 20px;
  }

  .section-intro {
    max-width: 700px;
    margin: 0 auto 70px auto;
    opacity: 0.85;
    line-height: 1.7;
  }

  /* GRID */
  .process-steps {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
  }

  /* TABLET */
  @media (max-width: 1024px) {
    .process-steps {
      grid-template-columns: repeat(2, 1fr);
      gap: 35px;
    }
  }

  /* MOBILE */
  @media (max-width: 640px) {
    .process-steps {
      grid-template-columns: 1fr;
      gap: 30px;
    }
  }

  /* STEP CARD */
  .step {
    position: relative;
    background: rgba(255, 255, 255, 0.08);
    padding: 40px;
    border-radius: 24px;
    backdrop-filter: blur(12px);
    transition: transform 0.4s, box-shadow 0.4s;
    text-align: left;
  }

  .step:hover {
    transform: translateY(-12px);
    box-shadow: 0 14px 35px rgba(0, 0, 0, 0.45);
  }

  /* NUMBER BADGE */
  .step-number {
    position: absolute;
    top: -18px;
    left: 30px;
    background: linear-gradient(90deg, #00f2fe, #4facfe);
    padding: 8px 18px;
    border-radius: 50px;
    font-weight: 600;
    font-size: 0.9rem;
    color: #fff;
    box-shadow: 0 5px 20px rgba(0, 242, 254, 0.4);
  }

  /* TEXT */
  .step h3 {
    margin-top: 25px;
    margin-bottom: 15px;
    font-size: 1.3rem;
  }

  .step p {
    opacity: 0.9;
    line-height: 1.7;
    font-size: 0.95rem;
  }

  /* Subtelny efekt podświetlenia */
  .step::before {
    content: "";
    position: absolute;
    inset: 0;
    border-radius: 24px;
    background: linear-gradient(120deg, rgba(0, 242, 254, 0.15), transparent 60%);
    opacity: 0;
    transition: opacity 0.4s;
    pointer-events: none;
  }

  .step:hover::before {
    opacity: 1;
  }

/*===========================================================*/
/* ===== AI CARD ===== */
.ai-card {
  position: relative;
  background: rgba(255, 255, 255, 0.05);
  border: 2px solid #00f2fe;
  box-shadow: 0 0 20px rgba(0, 242, 254, 0.4);
  backdrop-filter: blur(18px);
  padding: 50px 30px;
  border-radius: 24px;
  transition: transform 0.5s, box-shadow 0.5s;
}

.ai-card:hover {
  transform: translateY(-12px) scale(1.03);
  box-shadow: 0 20px 50px rgba(0, 242, 254, 0.6);
}

/* Neonowy badge AI */
.ai-badge {
  position: absolute;
  top: -20px;
  right: -20px;
  background: linear-gradient(135deg, #00f2fe, #4facfe);
  color: white;
  font-weight: 700;
  font-size: 1.5rem;
  padding: 15px 25px;
  border-radius: 50%;
  box-shadow: 0 0 25px #00f2fe, 0 0 50px #4facfe;
  text-align: center;
}

/* Dodatkowe wyróżnienie nagłówka */
.ai-card h3 {
  color: #00f2fe;
  margin-top: 40px; /* żeby nie nachodziło na badge */
}

/* Dostosowanie przycisku */
.ai-card .btn {
  background: linear-gradient(90deg, #00f2fe, #4facfe);
  box-shadow: 0 0 20px #00f2fe;
}



  
</style>

<div class="hero">
  <div class="glass">
    <h1>Witaj 👋</h1>
    <h2 class="typing">Tworzę nowoczesne rozwiązania</h2>
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
      <img src="/assets/corporate-user-icon.png" alt="Moje zdjęcie">
    </div>
  </div>
</section>

<section id="wspolpraca" class="process-section">
  <div class="container">
    <h2>Jak wygląda współpraca z klientem?</h2>
    <p class="section-intro">
      Stawiamy na partnerskie podejście i iteracyjny proces pracy.
      Od pierwszego pomysłu aż po gotowy produkt – działamy razem.
    </p>

  <div class="process-steps">

  <div class="step">
        <div class="step-number">01</div>
        <h3>Pomysł i potrzeby</h3>
        <p>
          Klient przedstawia swój pomysł, cele biznesowe oraz oczekiwania.
          Analizujemy potrzeby, grupę docelową i kluczowe funkcjonalności.
        </p>
      </div>

  <div class="step">
        <div class="step-number">02</div>
        <h3>Analiza i koncepcja</h3>
        <p>
          Proponujemy rozwiązania technologiczne i wstępną koncepcję projektu.
          Omawiamy zakres prac, harmonogram oraz estymację kosztów.
        </p>
      </div>

  <div class="step">
        <div class="step-number">03</div>
        <h3>Iteracyjny rozwój</h3>
        <p>
          Projekt realizujemy etapami (iteracjami). Po każdym etapie klient
          otrzymuje działającą wersję produktu, którą może przetestować i
          przekazać feedback.
        </p>
      </div>

  <div class="step">
        <div class="step-number">04</div>
        <h3>Feedback i usprawnienia</h3>
        <p>
          Na podstawie uwag wprowadzamy poprawki i rozwijamy kolejne funkcje.
          Dzięki temu produkt ewoluuje zgodnie z wizją klienta i realnymi
          potrzebami użytkowników.
        </p>
      </div>

  <div class="step">
        <div class="step-number">05</div>
        <h3>Wdrożenie i wsparcie</h3>
        <p>
          Po zakończeniu prac wdrażamy projekt na środowisko produkcyjne.
          Oferujemy również dalszy rozwój, utrzymanie i wsparcie techniczne.
        </p>
      </div>
      
  <div class="step">
        <div class="step-number">06</div>
        <h3>Monitoring i optymalizacja</h3>
        <p>
          Po wdrożeniu monitorujemy działanie systemu, analizujemy wydajność
          oraz zachowania użytkowników. Na podstawie danych wprowadzamy
          optymalizacje, poprawiamy szybkość działania i dbamy o bezpieczeństwo
          aplikacji, aby projekt działał stabilnie i efektywnie.
        </p>
      </div>
      </div>
  </div>
</section>

<section id="oferta">
  <h2>Moje usługi</h2>

  <div class="cards">

 <div class="card ai-card">
    <div class="ai-badge">AI</div>
    <h3>Implementacja Sztucznej Inteligencji</h3>
    <p>
      Wprowadzamy inteligentne algorytmy do Twojego projektu – od 
      automatyzacji procesów, przez analizę danych, po rekomendacje 
      wspierające decyzje biznesowe.
    </p>
  </div>
  
    <div class="card">
      <h3>⚡ Optymalizacja & SEO</h3>
      <p>
        Poprawa wydajności, Core Web Vitals i widoczności w Google.
        <br><strong>Technologie:</strong> Lighthouse, PageSpeed, SEO on-page
      </p>
    </div>

  <div class="card">
      <h3>🛠 Aplikacje Web i strony <strong>WWW</strong></h3>
      <p>
        Systemy webowe, dashboardy, panele administracyjne.
        <br><strong>Technologie:</strong> Angular, .NET, REST API
      </p>
    </div>

  <div class="card">
      <h3>📱 Aplikacje Front-end</h3>
      <p>
        Interfejsy użytkownika oparte o komponenty.
        <br><strong>Technologie:</strong> React, Next, Angular
      </p>
    </div>

  <div class="card">
      <h3>🔌 Integracje API</h3>
      <p>
        Integracja z zewnętrznymi usługami i systemami.
        <br><strong>Technologie:</strong> REST, JSON, Webhooks
      </p>
    </div>

  <div class="card">
      <h3>☁️ Deploy & Hosting</h3>
      <p>
        Wdrażanie aplikacji i konfiguracja serwerów.
        <br><strong>Technologie:</strong> GitHub Pages, Netlify, Vercel i inne.
      </p>
    </div>

  <div class="card">
      <h3>🧠 Konsultacje Programistyczne</h3>
      <p>
        Doradztwo techniczne i code review.
        <br><strong>Technologie:</strong> JavaScript, Git, architektura aplikacji
      </p>
    </div>
  </div>
</section>

<section id="projekty">
  <h2>Wybrane projekty</h2>

  <div class="cards projects">
    <div class="card project-card">
      <div class="project-image">
        <img src="/assets/xxx.png" alt="Projekt 1 – strona www">
      </div>
      <h3>Strona WWW</h3>
      <p>Nowoczesna strona internetowa warsztatu samochodowego</p>
      <a href="https://dziuplawarsztat.pl">LIVE DEMO</a>
    </div>

  <div class="card project-card">
      <div class="project-image">
        <img src="/assets/yyy.png" alt="Projekt 2">
      </div>
      <h3>Projekt 2</h3>
      <p>Nowoczesna strona internetowa centrum urody</p>
    </div>

  <div class="card project-card">
      <div class="project-image">
        <img src="/assets/zzz.png" alt="Projekt 3">
      </div>
      <h3>Projekt 3</h3>
      <p>Nowoczesna strona internetowa agencji nieruchomości</p>
    </div>
    </div>
</section>

<section id="kontakt">
  <h2>Kontakt</h2>
  📧 email@example.com
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
