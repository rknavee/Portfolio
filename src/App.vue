
<script setup lang="ts">
import rveePhoto from './assets/rvee.jpg'

const skills = ['C',
  'C++',
  'Python',
  'Microsoft Office',
  'Figma',
  'Canva',
  'AutoCAD 2D',
  'Proteus',
  'Arduino',
  'Communication',
  'Teamwork',
  'Problem-Solving',
  'Time Management']


const projects = [
  {
    title: 'Durian – Quiamco Dental Clinic System',
    category: 'Web Development',
    description:
      'Collaborated on a web-based appointment and patient record monitoring system. Contributed to interface design using Figma, workflow planning, and documentation.'
  },
  {
    title: 'Power Supply PCB',
    category: 'Electronics',
    description:
      'An electronics project focused on power-supply circuitry and printed circuit board design.'
  },
  {
    title: 'Personal Portfolio Website',
    category: 'Web Design',
    description:
      'A personal portfolio built with Vue 3 and TypeScript to present my skills, academic background, and projects in a responsive design.'
  }
]
</script>

<template>

  <div class="portfolio">
    <header class="navbar">
      <a class="logo" href="#home">my portfolio ♡</a>

      <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <main>
      
<section id="home" class="hero">
  <div class="hero-text">
    <p class="eyebrow">WELCOME TO MY PORTFOLIO</p>

    <h1>Hi, I'm <span>Rvee Abuzo</span> ♡</h1>

    <h2>Computer Engineering Student | Aspiring Engineer</h2>

    <p class="intro">
      pwede nang mangarap
    </p>

    <div class="hero-buttons">
      <a class="button" href="#projects">
        Projects →
      </a>

      <a
        class="button"
        href="#contact"
      >
        Contact Me 
      </a>

      <a
        class="button cv-button"
        href="/Rvee-Abuzo-CV.pdf"
        download="Rvee-Abuzo-CV.pdf"
      >
        Download My CV 
      </a>
    </div>
  </div>

  <<div class="profile photo-frame">
  <span class="bow bow-top">🎀</span>

  <img
    :src="rveePhoto"
    alt="Rvee Abuzo profile photo"
    class="profile-photo"
  />

  <p>Rvee Abuzo ♡</p>

  <span class="bow bow-bottom">୨୧</span>
</div>
</section>

      <section id="about" class="section">
        <p class="eyebrow">GET TO KNOW ME</p>
        <h2>About Me</h2>
        <p class="section-text">
          I'm a Computer Engineering student at Cagayan State University with an interest in programming, web design, and embedded systems. Through academic projects and student organization involvement, I've developed skills in technical problem-solving, collaboration, and interface design. I'm eager to apply what I've learned, gain hands-on industry experience, and continue growing as a future engineer.
        </p>
      </section>

      <section id="skills" class="section">
        <p class="eyebrow">WHAT I CAN DO</p>
        <h2>My Skills</h2>
        <div class="skills">
          <span v-for="skill in skills" :key="skill">{{ skill }}</span>
        </div>
      </section>

      <section id="projects" class="section">
        <p class="eyebrow">MY RECENT WORK</p>
        <h2>Featured Projects</h2>
        <div class="projects">
          <article v-for="project in projects" :key="project.title" class="project-card">
            <div class="project-icon">🎀</div>
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
          </article>
        </div>
      </section>

      

<section id="contact" class="section contact">
  <p class="eyebrow">LET'S CONNECT ♡</p>

  <h2>Let's Create Something Lovely!</h2>

  <p>
    I'm open to opportunities, collaborations,
    and new learning experiences in Computer Engineering.
    Feel free to reach out!
  </p>

  <div class="contact-details">
    <p>
      <span>Email:</span>
      <a href="mailto:abuzorvee1315@gmail.com">
        abuzorvee1315@gmail.com
      </a>
    </p>

    <p>
      <span>Contact Number:</span>
      <a href="tel:+639564967297">
        0956 496 7297
      </a>
    </p>

    <p>
      <span>LinkedIn:</span>
      <a
        href="https://www.linkedin.com/in/abuzorvee1315"
        target="_blank"
        rel="noopener noreferrer"
      >
        linkedin.com/in/abuzorvee1315
      </a>
    </p>
  </div>

  <div class="contact-buttons">
    <a class="button" href="mailto:abuzorvee1315@gmail.com">
      Email Me ♡
    </a>

    <a
      class="button"
      href="https://www.linkedin.com/in/abuzorvee1315"
      target="_blank"
      rel="noopener noreferrer"
    >
      Connect on LinkedIn 🎀
    </a>
    
  </div>
</section>
    </main>

    
<footer class="site-footer">
  <div class="footer-bow">୨୧ 🎀 ୨୧</div>

  <p class="footer-name">Rvee Abuzo</p>

  <p class="footer-tagline">
    Made with love, creativity, and a little pink magic.
  </p>

  <div class="footer-links">
    <a href="#home">Home</a>
    <span>♡</span>
    <a href="#about">About</a>
    <span>♡</span>
    <a href="#skills">Skills</a>
    <span>♡</span>
    <a href="#projects">Projects</a>
    <span>♡</span>
    <a href="#contact">Contact</a>
  </div>

  <p class="footer-copyright">
    © 2026 Rvee Abuzo. All rights reserved.
  </p>
</footer>
  </div>
</template>

<style>
:root {
  font-family: Arial, Helvetica, sans-serif;
  color: #59424e;
  background: #fff8fb;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  scroll-behavior: smooth;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-width: 320px;
}

a {
  text-decoration: none;
}

.portfolio {
  min-height: 100vh;
  background: #fff8fb;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
  padding: 22px 8%;
  background: #ffffff;
  border-bottom: 1px solid #f6e3ec;
}

.logo {
  color: #c76e98;
  font-size: 20px;
  font-weight: 800;
}

.navbar nav {
  display: flex;
  flex-wrap: wrap;
  gap: 22px;
}

.navbar nav a {
  color: #735968;
  font-size: 14px;
}

.navbar nav a:hover {
  color: #d77da4;
}

.hero-buttons {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 12px;
  margin-top: 20px;
}

.hero-buttons .button {
  box-sizing: border-box;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-width: 170px;
  min-height: 48px;
  padding: 12px 20px;
  margin: 0;
  border: 1px solid #e9a9c6;
  border-radius: 30px;
  background: #fff5fa;
  color: #b65f88;
  font: inherit;
  font-weight: 600;
  line-height: 1.2;
  text-align: center;
  text-decoration: none;
  transition:
    background-color 0.2s ease,
    color 0.2s ease,
    box-shadow 0.2s ease;
}

.hero-buttons .button:hover {
  background: #fce5ef;
  color: #98486f;
  box-shadow: 0 4px 12px rgba(198, 110, 152, 0.18);
  transform: none;
}

.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
  max-width: 1100px;
  min-height: 570px;
  margin: auto;
  padding: 70px 35px;
}

.hero-text {
  max-width: 600px;
}

.eyebrow {
  color: #c76e98;
  font-size: 12px;
  font-weight: 800;
  letter-spacing: 3px;
}

.hero h1 {
  margin: 18px 0;
  font-size: clamp(36px, 5vw, 58px);
  line-height: 1.15;
}

.hero h1 span {
  color: #d77da4;
}

.hero h2 {
  font-size: 23px;
  font-weight: 500;
}

.intro,
.section-text {
  max-width: 580px;
  color: #856f7b;
  font-size: 16px;
  line-height: 1.9;
}

.button {
  display: inline-block;
  margin-top: 22px;
  padding: 14px 24px;
  border-radius: 30px;
  background: #d77da4;
  color: white;
  font-size: 14px;
  font-weight: 700;
  transition: 0.2s;
}

.button:hover {
  background: #bd638b;
  transform: translateY(-2px);
}

.profile {
  display: flex;
  flex-shrink: 0;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 270px;
  height: 300px;
  border: 8px solid white;
  border-radius: 45% 45% 42% 42%;
  background: #f9dce9;
  box-shadow: 0 15px 40px #edc4d7;
  color: #9b6881;
}

.flower {
  font-size: 85px;
}

.profile p {
  font-size: 13px;
}

.section {
  max-width: 1100px;
  margin: auto;
  padding: 75px 35px;
  scroll-margin-top: 30px;
}

.section h2 {
  margin-top: 10px;
  font-size: 34px;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
  margin-top: 28px;
}

.skills span {
  padding: 13px 20px;
  border: 1px solid #f3dce7;
  border-radius: 25px;
  background: white;
  color: #b65f88;
  font-size: 14px;
}

.projects {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 24px;
  margin-top: 28px;
}

.project-card {
  padding: 28px;
  border: 1px solid #f5e2eb;
  border-radius: 22px;
  background: white;
  box-shadow: 0 8px 25px #f8eaf0;
  transition: 0.2s;
}

.project-card:hover {
  transform: translateY(-4px);
}

.project-icon {
  font-size: 30px;
}

.project-card h3 {
  margin-bottom: 10px;
}

.project-card p,
.contact > p:not(.eyebrow) {
  color: #856f7b;
  line-height: 1.8;
}

.contact {
  margin-bottom: 50px;
  padding: 55px 30px;
  border-radius: 28px;
  background: #fbe6ef;
  text-align: center;
}

.contact > p:not(.eyebrow) {
  max-width: 550px;
  margin: 15px auto;
}

.contact-details {
  margin: 24px auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

.contact-details p {
  margin: 0;
  overflow-wrap: anywhere;
}

.contact-details span {
  font-weight: bold;
  color: #b65f88;
}

.contact-details a {
  color: #795568;
  text-decoration: none;
}

.contact-details a:hover {
  color: #c76e98;
  text-decoration: underline;
}

.contact-buttons {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 14px;
  margin-top: 24px;
}

.contact-buttons .button {
  text-decoration: none;
  cursor: pointer;
  transition: transform 0.2s ease;
}

.contact-buttons .button:hover {
  transform: translateY(-3px);
}


.site-footer {
  margin-top: 40px;
  padding: 36px 20px 24px;
  text-align: center;
  background: linear-gradient(180deg, #fff7fb, #f9e1ed);
  border-top: 1px solid #f0c5d9;
  color: #795568;
}

.footer-bow {
  margin-bottom: 10px;
  color: #c76e98;
  font-size: 24px;
}

.footer-name {
  margin: 8px 0;
  color: #b65f88;
  font-size: 22px;
  font-weight: bold;
}

.footer-tagline {
  margin: 8px 0 20px;
  font-size: 14px;
  line-height: 1.7;
}

.footer-links {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 10px;
  margin-bottom: 22px;
  font-size: 14px;
}

.footer-links a {
  color: #795568;
  text-decoration: none;
  transition: color 0.2s ease;
}

.footer-links a:hover {
  color: #c76e98;
  text-decoration: underline;
}

.footer-links span {
  color: #d99ab8;
}

.footer-copyright {
  margin: 0;
  padding-top: 16px;
  border-top: 1px solid #edc7d9;
  font-size: 12px;
  color: #98758a;
}

@media (max-width: 700px) {
  .navbar {
    align-items: flex-start;
    flex-direction: column;
  }

  .navbar nav {
    gap: 14px;
  }

  .hero {
    flex-direction: column-reverse;
    align-items: flex-start;
    gap: 35px;
    padding-top: 50px;
  }

  .profile {
    align-self: center;
    width: 220px;
    height: 240px;
  }

  .projects {
    grid-template-columns: 1fr;
  }

  .section {
    padding: 55px 25px;
  }
}

.photo-frame {
  position: relative;
  overflow: visible;
  border: 5px solid white;
  outline: 2px dashed #e7a6c2;
  outline-offset: 7px;
  background: #fbe6ef;
}

.profile-photo {
  display: block;
  width: 175px;
  height: 190px;
  object-fit: cover;
  object-position: center;
  border: 4px solid white;
  border-radius: 48% 48% 18px 18px;
  box-shadow: 0 6px 18px #e8b9ce;
}

.photo-frame p {
  margin-top: 12px;
  font-weight: bold;
  color: #b65f88;
}

.bow {
  position: absolute;
  z-index: 2;
  color: #c76e98;
  font-size: 36px;
}

.bow-top {
  top: -24px;
  right: -14px;
}

.bow-bottom {
  bottom: 4px;
  left: -18px;
  font-size: 30px;
}
</style>