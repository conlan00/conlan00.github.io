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
      padding-top: 64px; /* wysokość headera desktop */
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
      position: fixed;
      width: 100%;
      top: 0;
      left: 0;
      z-index: 999;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 20px;
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
      cursor: pointer;
    }
    
    /* ===== HERO ===== */
    .hero {
      height: calc(100vh - 64px);
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 20px;
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
    
    /* ===== CARDS ===== */
    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 40px;
      margin-top: 60px;
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
    
    /* ===== RESPONSIVE ===== */
    @media (max-width: 1024px) {
      .cards {
        grid-template-columns: repeat(2, 1fr);
        gap: 35px;
      }
    }
    
    @media (max-width: 768px) {
      /* Hero */
      .hero {
        height: calc(100vh - 56px);
        padding: 20px;
      }
    
      .glass {
        padding: 40px 20px;
      }
    
      .typing {
        font-size: 18px;
      }
    
      .btn {
        padding: 12px 25px;
        font-size: 14px;
      }
    
      /* About section */
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
    
      /* Cards */
      .cards {
        grid-template-columns: 1fr;
        gap: 30px;
      }
    
      /* Navbar mobile menu */
      .site-nav {
        display: none;
        flex-direction: column;
        background: rgba(255, 255, 255, 0.95);
        position: absolute;
        top: 56px;
        right: 20px;
        width: 180px;
        padding: 10px;
        border-radius: 8px;
        z-index: 1000;
      }
    
      .site-nav.active {
        display: flex;
      }
    
      .menu-icon {
        display: block;
        cursor: pointer;
      }
    
      .site-nav a {
        padding: 10px 0;
        color: #111 !important;
      }
    }
    
    @media (max-width: 640px) {
      .project-card p {
        padding: 0 20px 25px;
      }
    }
    </style>
    
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
    
    // Hamburger menu mobile
    const menuIcon = document.querySelector('.menu-icon');
    const siteNav = document.querySelector('.site-nav');
    
    if(menuIcon){
      menuIcon.addEventListener('click', () => {
        siteNav.classList.toggle('active');
      });
    }
    </script>
    
