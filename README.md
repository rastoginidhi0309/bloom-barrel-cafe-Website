# bloom-barrel-cafe-Website
Bloom Barrel Café is a sleek, single-page website template for cafés and small restaurants, built with HTML, CSS, and JavaScript. 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Bloom Barrel Café</title>
  <!-- Font Awesome CDN for social icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  <style>
    * { margin:0; padding:0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #fffaf5;
      color: #333;
      line-height: 1.6;
    }
    header {
      background: #800000;
      padding: 1rem 2rem;
      position: sticky;
      top: 0;
      z-index: 10;
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      max-width: 1100px;
      margin: 0 auto;
    }
    nav .logo {
      color: white;
      font-weight: bold;
      font-size: 1.8rem;
    }
    nav ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
    }
    nav ul li a {
      text-decoration: none;
      color: white;
      font-weight: 600;
      transition: color 0.3s;
    }
    nav ul li a:hover {
      color: #ffd700;
    }
    #hero {
      background: url('https://images.unsplash.com/photo-1550317138-10000687a72b?auto=format&fit=crop&w=1350&q=80') no-repeat center/cover;
      height: 90vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      color: white;
      padding: 0 2rem;
    }
    #hero h1 {
      font-size: 3rem;
      text-shadow: 2px 2px 6px #000;
    }
    #hero p {
      font-size: 1.2rem;
      margin: 1rem 0 2rem;
      text-shadow: 1px 1px 4px #000;
    }
    #hero a.btn {
      padding: 1rem 2rem;
      background: #ffd700;
      color: #000;
      font-weight: bold;
      border-radius: 8px;
      text-decoration: none;
      transition: background 0.3s;
    }
    #hero a.btn:hover {
      background: #e6c200;
    }
    section {
      max-width: 1100px;
      margin: 3rem auto;
      padding: 0 1rem;
    }
    #menu h2 {
      text-align: center;
      margin-bottom: 1rem;
      color: #800000;
    }
    .menu-items {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      justify-content: center;
    }
    .menu-item {
      background: #fffaf4;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      width: 280px;
      padding: 1rem;
      text-align: center;
      transition: transform 0.3s;
    }
    .menu-item:hover {
      transform: translateY(-6px);
    }
    .menu-item img {
      max-width: 100%;
      border-radius: 6px;
    }
    .menu-item h3 {
      margin: 0.8rem 0 0.5rem;
    }
    .menu-item p {
      color: #555;
    }
    #about {
      background: #f7f0e7;
      border-radius: 8px;
      padding: 2rem;
      text-align: center;
    }
    #about h2 {
      color: #800000;
      margin-bottom: 1rem;
    }
    #about p {
      max-width: 700px;
      margin: 0 auto;
      font-size: 1.1rem;
      color: #444;
    }
    #about img {
      margin-top: 1.5rem;
      border-radius: 12px;
      width: 80%;
      max-width: 600px;
      box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    }
    #contact {
      text-align: center;
      padding-bottom: 2rem;
    }
    #contact h2 {
      color: #800000;
      margin-bottom: 1rem;
    }
    #contact form {
      max-width: 480px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
    #contact input, #contact textarea {
      padding: 0.75rem;
      font-size: 1rem;
      border-radius: 8px;
      border: 1.5px solid #ccc;
      resize: vertical;
      transition: border-color 0.3s;
    }
    #contact input:focus, #contact textarea:focus {
      outline: none;
      border-color: #800000;
    }
    #contact button {
      background: #800000;
      color: white;
      font-weight: 700;
      border: none;
      border-radius: 8px;
      padding: 1rem;
      cursor: pointer;
      font-size: 1.1rem;
      transition: background 0.3s;
    }
    #contact button:hover {
      background: #a02020;
    }
    #formMessage {
      margin-top: 1rem;
      font-weight: 700;
      min-height: 1.2rem;
    }
    /* Social icons styles */
    .social-icons {
      text-align: center;
      margin-bottom: 1rem;
    }
    .social-icons .fa {
      padding: 13px;
      font-size: 25px;
      width: 42px;
      text-align: center;
      text-decoration: none;
      margin: 0 6px;
      border-radius: 50%;
      background: #eee;
      color: #800000;
      transition: background 0.3s, color 0.3s;
      vertical-align: middle;
      display: inline-block;
    }
    .social-icons .fa:hover {
      background: #ffd700;
      color: #800000;
    }
    .fa-facebook { background: #3B5998; color: white; }
    .fa-instagram { background: #C13584; color: white; }
    .fa-twitter { background: #55ACEE; color: white; }
    footer {
      background: #800000;
      text-align: center;
      color: white;
      padding: 1.5rem 2rem;
      margin-top: 3rem;
    }
    @media (max-width: 768px) {
      .menu-items {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>
<body>

  <header>
    <nav>
      <div class="logo">Bloom Barrel Café</div>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section id="hero">
    <div class="hero-content">
      <h1>Welcome to Bloom Barrel Café</h1>
      <p>Where every bite tells a story</p>
      <a href="#menu" class="btn">Explore Menu</a>
    </div>
  </section>

  <section id="menu">
    <h2>Our Menu</h2>
    <div class="menu-items">
      <div class="menu-item">
        <img src="https://tse4.mm.bing.net/th/id/OIP.X7D0d0Ji0qFjPJRIgP2_mgHaFj?pid=Api&P=0&h=180" alt="Pizza" />
        <h3>Margherita Pizza</h3>
        <p>Classic delight with tomatoes, basil & mozzarella.</p>
      </div>
      <div class="menu-item">
        <img src="https://tse1.mm.bing.net/th/id/OIP.Lxlyc1a6J8a8R9wTMx_ADQHaFj?pid=Api&P=0&h=180" alt="Pasta" />
        <h3>Pasta Alfredo</h3>
        <p>Creamy alfredo sauce with fettuccine and parmesan.</p>
      </div>
      <div class="menu-item">
        <img src="https://media.istockphoto.com/id/1254672762/photo/delicious-homemade-hamburger-and-french-fries.jpg?s=612x612&w=0&k=20&c=9BgdcWXRMb8hPZd2049StXFqvhDRq3izLkXK7Cq2C9s=" alt="Burger" />
        <h3>Cheese Burger</h3>
        <p>Juicy beef patty with cheddar, lettuce & tomato.</p>
      </div>
    </div>
  </section>

  <section id="about">
    <h2>About Us</h2>
    <p>
      At Bloom Barrel Café, we believe food is love made visible.
      Established in 2010, we pride ourselves on fresh ingredients,
      classic recipes, and a welcoming atmosphere.
    </p>
    <img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836?auto=format&fit=crop&w=900&q=80" alt="Restaurant Interior" />
  </section>

  <section id="contact">
    <h2>Contact Us</h2>
    <form id="contactForm" novalidate>
      <input type="text" id="name" name="name" placeholder="Your Name" required />
      <input type="email" id="email" name="email" placeholder="Your Email" required />
      <textarea id="message" name="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="formMessage"></p>
  </section>

  <footer>
    <div class="social-icons">
      <a href="https://facebook.com/" class="fa fa-facebook" target="_blank" title="Facebook"></a>
      <a href="https://instagram.com/" class="fa fa-instagram" target="_blank" title="Instagram"></a>
      <a href="https://twitter.com/" class="fa fa-twitter" target="_blank" title="Twitter"></a>
    </div>
    <p>&copy; 2025 Delicious Bites. All rights reserved.</p>
  </footer>

  <script>
    // Smooth scrolling for nav links
    document.querySelectorAll('nav ul li a').forEach(link => {
      link.addEventListener('click', e => {
        e.preventDefault();
        const target = document.querySelector(link.getAttribute('href'));
        if (target) target.scrollIntoView({behavior: 'smooth'});
      });
    });

    // Contact form submission handler
    const form = document.getElementById('contactForm');
    const formMessage = document.getElementById('formMessage');

    form.addEventListener('submit', e => {
      e.preventDefault();

      const name = form.name.value.trim();
      const email = form.email.value.trim();
      const message = form.message.value.trim();

      if (!name || !email || !message) {
        formMessage.textContent = 'Please fill out all fields.';
        formMessage.style.color = 'red';
        return;
      }

      // Simple email validation regex
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!emailRegex.test(email)) {
        formMessage.textContent = 'Please enter a valid email.';
        formMessage.style.color = 'red';
        return;
      }

      formMessage.textContent = 'Thank you! Your message has been sent.';
      formMessage.style.color = 'green';
      form.reset();
    });
  </script>
</body>
</html>
