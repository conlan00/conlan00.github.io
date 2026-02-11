layout: default
title: Strona główna
---

<style>
.hero {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.glass {
  background: rgba(255,255,255,0.1);
  padding: 50px;
  border-radius: 20px;
  backdrop-filter: blur(15px);
  box-shadow: 0 8px 32px rgba(0,0,0,0.3);
  color: white;
}

body {
  background: linear-gradient(-45deg, #0f2027, #203a43, #2c5364, #1c1c1c);
  background-size: 400% 400%;
  animation: gradient 12s ease infinite;
}

@keyframes gradient {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
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

section {
  padding: 100px 20px;
  text-align: center;
  opacity: 0;
  transform: translateY(50px);
  transition: 1s;
  color: white;
}

section.visible {
  opacity: 1;
  transform: translateY(0);
}

.btn {
  margin-top: 20px;
  padding: 12px 30px;
  border-radius: 50px;
  border: none;
  cursor: pointer;
  background: linear-gradient(90deg,#00f2fe,#4facfe);
  color: white;
  transition: 0.4s;
}

.btn:hover {
  transform: scale(1.1);
  box-shadow: 0 0 20px #00f2fe;
}
</style>

<div class="hero">
  <div class="glass">
    <h1>Witaj 👋</h1>
    <h2 class="typing">Tworzę nowoczesne strony internetowe</h2>
    <br>
    <button class="btn">Zobacz więcej</button>
  </div>
</div>

<section>
## O mnie
Tworzę szybkie i efektowne strony internetowe.
</section>

<section>
## Projekty
Tutaj możesz dodać swoje portfolio.
</section>

<section>
## Kontakt
kontakt@example.com
</section>

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
