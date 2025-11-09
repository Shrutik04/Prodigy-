<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Landing Page</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- Navigation Bar -->
  <nav class="navbar">
    <div class="logo">MyBrand</div>
    <ul class="nav-links" id="navLinks">
      <li><a href="#home" class="active">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="menu-toggle" id="menuToggle">&#9776;</div>
  </nav>

  <!-- Hero Section -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1 class="fade-in">Welcome to <span>MyBrand</span></h1>
      <p class="fade-in-delay">Crafting beautiful, functional and responsive websites for modern businesses.</p>
      <a href="#about" class="btn fade-in-btn">Get Started</a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="section fade-section">
    <h2>About Us</h2>
    <p>
      At <strong>MyBrand</strong>, we combine creativity and technology to build web experiences that inspire action.
      Our team of designers and developers focus on clean design, fast performance, and user-friendly interfaces.
    </p>
    <div class="cards">
      <div class="card">
        <h3>Mission</h3>
        <p>To empower businesses by creating impactful digital experiences.</p>
      </div>
      <div class="card">
        <h3>Vision</h3>
        <p>To become a trusted global brand for web and app solutions.</p>
      </div>
      <div class="card">
        <h3>Values</h3>
        <p>Innovation, integrity, and excellence in everything we do.</p>
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="section fade-section">
    <h2>Our Services</h2>
    <div class="cards">
      <div class="card">
        <h3>Web Design</h3>
        <p>Modern, responsive, and visually appealing websites that adapt to all devices.</p>
      </div>
      <div class="card">
        <h3>App Development</h3>
        <p>Robust mobile and web applications built using the latest technologies.</p>
      </div>
      <div class="card">
        <h3>Digital Marketing</h3>
        <p>SEO, branding, and social media strategies to grow your online presence.</p>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="section fade-section">
    <h2>Contact Us</h2>
    <p>Have a project in mind? Let’s make it happen! Drop us a message below.</p>
    <a href="mailto:info@mybrand.com" class="btn">Say Hello 👋</a>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 MyBrand. Designed with ❤️ by MyBrand Team.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>



### css code


/* Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Body */
body {
  font-family: 'Poppins', sans-serif;
  line-height: 1.6;
  scroll-behavior: smooth;
  background: #fff;
}

/* Navbar */
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  background: transparent;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 50px;
  color: white;
  z-index: 1000;
  transition: all 0.3s ease;
}

.navbar.scrolled {
  background: #111;
  box-shadow: 0 4px 8px rgba(0,0,0,0.3);
}

.logo {
  font-size: 1.6em;
  font-weight: bold;
  color: #00bcd4;
}

/* Nav Links */
.nav-links {
  display: flex;
  list-style: none;
  gap: 25px;
}

.nav-links a {
  text-decoration: none;
  color: white;
  font-weight: 500;
  transition: color 0.3s, transform 0.2s;
}

.nav-links a:hover, .nav-links a.active {
  color: #00bcd4;
  transform: scale(1.1);
}

/* Mobile Menu */
.menu-toggle {
  display: none;
  font-size: 1.8em;
  cursor: pointer;
  color: white;
}

/* Hero Section */
.hero {
  height: 100vh;
  background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)),
              url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e') no-repeat center center/cover;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  padding: 0 20px;
}

.hero-content span {
  color: #00bcd4;
}

.hero-content h1 {
  font-size: 3.2em;
  animation: slideDown 1s ease-out;
}

.hero-content p {
  margin: 15px 0 25px;
  font-size: 1.2em;
  opacity: 0.9;
}

.btn {
  background: #00bcd4;
  color: white;
  padding: 12px 25px;
  border-radius: 25px;
  text-decoration: none;
  transition: all 0.3s ease;
}

.btn:hover {
  background: #008c9e;
  transform: translateY(-3px);
}

/* Sections */
.section {
  padding: 100px 20px;
  text-align: center;
}

.section:nth-child(even) {
  background: #f4f4f4;
}

.section h2 {
  font-size: 2.5em;
  color: #111;
  margin-bottom: 30px;
}

/* Cards */
.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 25px;
  margin-top: 20px;
}

.card {
  background: white;
  padding: 30px;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  width: 300px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

/* Footer */
footer {
  background: #111;
  color: white;
  text-align: center;
  padding: 20px;
}

/* Animations */
@keyframes slideDown {
  from { transform: translateY(-30px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

.fade-in {
  opacity: 0;
  animation: fadeIn 1s ease forwards;
}

.fade-in-delay {
  opacity: 0;
  animation: fadeIn 1.5s ease forwards;
  animation-delay: 0.3s;
}

.fade-in-btn {
  opacity: 0;
  animation: fadeIn 1.5s ease forwards;
  animation-delay: 0.6s;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Scroll reveal effect */
.fade-section {
  opacity: 0;
  transform: translateY(50px);
  transition: all 0.8s ease;
}

.fade-section.show {
  opacity: 1;
  transform: translateY(0);
}

/* Responsive */
@media (max-width: 768px) {
  .nav-links {
    position: absolute;
    top: 60px;
    right: 0;
    flex-direction: column;
    background: #111;
    width: 200px;
    display: none;
  }
  .nav-links.active {
    display: flex;
  }
  .menu-toggle {
    display: block;
  }
  .cards {
    flex-direction: column;
    align-items: center;
  }
}



### javascript code

// Change navbar color on scroll
window.addEventListener("scroll", () => {
  const navbar = document.querySelector(".navbar");
  navbar.classList.toggle("scrolled", window.scrollY > 50);

  // Highlight active link
  const sections = document.querySelectorAll("section");
  const links = document.querySelectorAll(".nav-links a");
  
  sections.forEach((sec) => {
    let top = window.scrollY;
    let offset = sec.offsetTop - 100;
    let height = sec.offsetHeight;
    let id = sec.getAttribute("id");
    
    if (top >= offset && top < offset + height) {
      links.forEach((link) => {
        link.classList.remove("active");
        document.querySelector(`.nav-links a[href*=${id}]`).classList.add("active");
      });
    }
  });
});

// Toggle mobile menu
const menuToggle = document.getElementById("menuToggle");
const navLinks = document.getElementById("navLinks");
menuToggle.addEventListener("click", () => {
  navLinks.classList.toggle("active");
});

// Scroll reveal animation
const fadeSections = document.querySelectorAll(".fade-section");

window.addEventListener("scroll", () => {
  fadeSections.forEach(section => {
    const rect = section.getBoundingClientRect();
    if (rect.top < window.innerHeight - 100) {
      section.classList.add("show");
    }
  });
});
