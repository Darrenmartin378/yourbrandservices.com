<template>
  <div id="app">
    <nav class="navbar">
      <div class="logo">ModernVue</div>
      <ul class="nav-links">
        <li><a href="#hero">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>

    <section id="hero" class="hero">
      <div class="hero-content">
        <h1>Build Modern Websites with Vue</h1>
        <p>Elegant, fast, and powerful front-end experiences.</p>
        <button class="cta">Get Started</button>
      </div>
    </section>

    <section id="services" class="services">
      <h2>Our Services</h2>
      <div class="cards">
        <div class="card">
          <h3>Web Design</h3>
          <p>Modern, responsive designs that look great on all devices.</p>
        </div>
        <div class="card">
          <h3>Development</h3>
          <p>Clean and efficient code built with Vue 3 and TypeScript.</p>
        </div>
        <div class="card">
          <h3>Branding</h3>
          <p>We help define your visual identity with elegance.</p>
        </div>
      </div>
    </section>

    <section id="about" class="about">
      <h2>About Us</h2>
      <p>
        We are a team of designers and developers passionate about creating
        visually appealing, user-friendly, and high-performance web experiences.
      </p>
    </section>

    <section id="contact" class="contact">
      <h2>Contact Us</h2>
      <form @submit.prevent="submitForm">
        <input type="text" placeholder="Your Name" required />
        <input type="email" placeholder="Your Email" required />
        <textarea placeholder="Message" required></textarea>
        <button type="submit">Send Message</button>
      </form>
    </section>

    <footer class="footer">
      <p>© 2025 ModernVue. All Rights Reserved.</p>
    </footer>
  </div>
</template>

<script setup>
const submitForm = () => {
  alert('Thank you for contacting us!');
};
</script>

<style>
#app {
  font-family: 'Poppins', sans-serif;
  color: #333;
  margin: 0;
  padding: 0;
  background-color: #fff;
}

/* NAVIGATION */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 3rem;
  background: #0d1117;
  color: #fff;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 2rem;
}
.nav-links a {
  text-decoration: none;
  color: #fff;
  transition: color 0.3s;
}
.nav-links a:hover {
  color: #1abc9c;
}

/* HERO */
.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 80vh;
  background: linear-gradient(135deg, #1abc9c, #16a085);
  color: white;
  text-align: center;
}
.cta {
  margin-top: 1.5rem;
  background: white;
  color: #16a085;
  border: none;
  padding: 0.8rem 2rem;
  font-size: 1rem;
  border-radius: 30px;
  cursor: pointer;
  transition: all 0.3s ease;
}
.cta:hover {
  background: #16a085;
  color: white;
}

/* SERVICES */
.services {
  padding: 5rem 2rem;
  background: #f8f9fa;
  text-align: center;
}
.cards {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 2rem;
  margin-top: 2rem;
}
.card {
  background: white;
  padding: 2rem;
  border-radius: 1rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  width: 280px;
  transition: transform 0.3s;
}
.card:hover {
  transform: translateY(-5px);
}

/* ABOUT */
.about {
  padding: 5rem 2rem;
  background: #ffffff;
  color: #333;
  text-align: center;
  line-height: 1.6;
}

/* CONTACT */
.contact {
  padding: 5rem 2rem;
  background: #f1f3f6;
  text-align: center;
}
form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-width: 400px;
  margin: auto;
}
input,
textarea {
  padding: 1rem;
  border: 1px solid #ccc;
  border-radius: 8px;
}
button {
  background: #16a085;
  color: white;
  border: none;
  padding: 1rem;
  border-radius: 8px;
  cursor: pointer;
}
button:hover {
  background: #1abc9c;
}

/* FOOTER */
.footer {
  background: #0d1117;
  color: white;
  text-align: center;
  padding: 1.5rem;
}
</style>
