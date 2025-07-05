# Capstone-Project-Fitkhana
Capstone Project 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>FitKhana – Smart Meal Plans, Freshly Made & Delivered to You</title>
  <!-- Google Fonts: Modern, Rounded Typography -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@500;700&family=Nunito:wght@400;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
  <style>
    :root {
      --yellow: #ffe259;
      --orange: #ffa726;
      --yellow-orange: #ffb343;
      --deep-orange: #ff9100;
      --green: #22c55e;
      --leaf-green: #1db954;
      --white: #fff;
      --black: #181818;
      --gray: #f6f6f6;
      --shadow: 0 4px 24px rgba(255, 167, 38, 0.08);
      --radius: 1.5rem;
    }
    html {
      scroll-behavior: smooth;
    }
    body {
      margin: 0;
      font-family: 'Nunito', 'Montserrat', Arial, sans-serif;
      background: linear-gradient(135deg, var(--yellow), var(--orange) 90%);
      color: var(--black);
      min-height: 100vh;
      overflow-x: hidden;
    }
   header {
  position: fixed; /* more appropriate than absolute for sticky headers */
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999; /* higher for safety in stacking */
  background-color: rgba(255, 245, 100, 0.23); /* slightly more visible */
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1); /* better shadow if --shadow not defined */
  display: flex;
  align-items: center;
  justify-content: space-between;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
}

    .logo {
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    .logo img {
      height: 54px;
      width: 54px;
      border-radius: 50%;
      background: var(--yellow-orange);
      object-fit: cover;
      box-shadow: 0 2px 8px rgba(34,197,94,0.12);
    }
    .brand {
      font-size: 2rem;
      font-weight: 700;
      color: var(--deep-orange);
      letter-spacing: 1px;
      font-family: 'Montserrat', sans-serif;
    }
    nav {
      display: flex;
      gap: 1.5rem;
    }
    nav a {
      color: var(--black);
      text-decoration: none;
      font-weight: 600;
      font-size: 1.05rem;
      border-radius: 1rem;
      padding: 0.5rem 1rem;
      transition: background 0.2s;
    }
    nav a:hover {
      background: var(--yellow-orange);
      color: var(--white);
    }
    .hero {
      min-height: 90vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      background: linear-gradient(135deg, var(--yellow), var(--orange) 95%);
      position: relative;
      overflow: hidden;
    }
    .hero-content {
      position: relative;
      z-index: 2;
      margin-top: 2rem;
    }
    .hero h1 {
      font-size: 2.8rem;
      font-family: 'Montserrat', sans-serif;
      font-weight: 700;
      color: var(--deep-orange);
      margin-bottom: 1rem;
      letter-spacing: 1px;
      text-shadow: 0 2px 12px rgba(255, 167, 38, 0.10);
    }
    .hero .slogan {
      font-size: 1.3rem;
      font-weight: 500;
      color: var(--leaf-green);
      margin-bottom: 2rem;
    }
    .hero .cta-group {
      display: flex;
      gap: 1.2rem;
      justify-content: center;
      margin-bottom: 2rem;
    }
    .btn {
      background: linear-gradient(90deg, var(--yellow-orange), var(--deep-orange));
      color: var(--white);
      border: none;
      border-radius: var(--radius);
      padding: 0.85rem 2.2rem;
      font-size: 1.1rem;
      font-weight: 700;
      box-shadow: 0 2px 12px rgba(255, 167, 38, 0.10);
      cursor: pointer;
      transition: background 0.2s, transform 0.1s;
      outline: none;
    }
    .btn.secondary {
      background: var(--green);
      color: var(--white);
    }
    .btn:hover {
      transform: translateY(-2px) scale(1.03);
      filter: brightness(1.08);
    }
    /* About Section */
    .section {
      padding: 4rem 0 2.5rem 0;
      background: var(--gray);
      border-radius: 2rem 2rem 0 0;
      box-shadow: var(--shadow);
      margin: 2rem 0 0 0;
    }
    .section-title {
      font-size: 2.2rem;
      font-family: 'Montserrat', sans-serif;
      color: var(--deep-orange);
      margin-bottom: 1.2rem;
      text-align: center;
    }
    .about-content {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      gap: 2.5rem;
      max-width: 1100px;
      margin: 0 auto;
    }
    .about-text {
      flex: 1 1 320px;
      font-size: 1.2rem;
      color: var(--black);
      line-height: 1.7;
      font-weight: 500;
      padding: 0 1rem;
    }
    .about-img {
      flex: 1 1 320px;
      min-width: 260px;
      max-width: 350px;
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: 0 4px 24px rgba(34,197,94,0.10);
      background: var(--yellow-orange);
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .about-img img {
      width: 100%;
      border-radius: var(--radius);
      object-fit: cover;
      filter: brightness(1.04) saturate(1.1);
    }
    /* How It Works */
    .steps {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      margin-top: 2.5rem;
    }
    .step-card {
      background: var(--white);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 2rem 1.2rem;
      flex: 1 1 240px;
      max-width: 300px;
      text-align: center;
      transition: transform 0.18s;
    }
    .step-card:hover {
      transform: translateY(-6px) scale(1.04);
      box-shadow: 0 8px 32px rgba(255, 167, 38, 0.13);
    }
    .step-icon {
  font-size: 2rem; /* Slightly reduced for better card balance */
  margin-bottom: 0.75rem; /* Tighter spacing */
  color: var(--leaf-green);
  display: flex; /* Ensures alignment control */
  justify-content: center; /* Horizontally centers the icon */
  align-items: center; /* Vertically centers the icon */
  width: 3rem; /* Fixed width for consistency */
  height: 3rem; /* Fixed height for uniformity */
  background: rgba(0, 0, 0, 0.05); /* Optional: subtle background for visibility */
  border-radius: 50%; /* Circular container (adjust if needed) */
  padding: 0.5rem; /* Internal spacing */
  box-sizing: border-box; /* Prevents padding from affecting dimensions */
}
    .step-title {
      font-size: 1.15rem;
      font-weight: 700;
      color: var(--deep-orange);
      margin-bottom: 0.5rem;
    }
    .step-desc {
      font-size: 1rem;
      color: #444;
      line-height: 1.5;
    }
    /* Meal Plans */
    .plans {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      justify-content: center;
      margin-top: 2.5rem;
    }
    .plan-card {
      background: var(--white);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 2rem 1.2rem;
      flex: 1 1 260px;
      max-width: 320px;
      text-align: center;
      transition: transform 0.18s;
      border: 2px solid var(--yellow-orange);
      position: relative;
    }
    .plan-card:hover {
      transform: translateY(-6px) scale(1.04);
      box-shadow: 0 8px 32px rgba(255, 167, 38, 0.13);
      border-color: var(--deep-orange);
    }
    .plan-title {
      font-size: 1.3rem;
      font-weight: 700;
      color: var(--deep-orange);
      margin-bottom: 0.5rem;
    }
    .plan-price {
      font-size: 1.1rem;
      color: var(--green);
      font-weight: 700;
      margin-bottom: 0.5rem;
    }
    .plan-benefits {
      font-size: 1rem;
      color: #444;
      margin-bottom: 0.8rem;
      list-style: none;
      padding: 0;
    }
    .plan-benefits li {
      margin-bottom: 0.3rem;
      text-align: left;
      padding-left: 1.1rem;
      position: relative;
    }
    .plan-benefits li:before {
      content: '✔';
      color: var(--leaf-green);
      position: absolute;
      left: 0;
      font-size: 1rem;
    }
    .plan-sample {
      font-size: 0.98rem;
      color: var(--orange);
      margin-bottom: 1rem;
    }
    .plan-btn {
      margin-top: 0.5rem;
      background: var(--green);
      color: var(--white);
      border: none;
      border-radius: 2rem;
      padding: 0.6rem 1.5rem;
      font-size: 1rem;
      font-weight: 700;
      cursor: pointer;
      transition: background 0.18s;
    }
    .plan-btn:hover {
      background: var(--deep-orange);
    }
    /* Why Choose */
    .why-list {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      justify-content: center;
      margin-top: 2.5rem;
    }
    .why-card {
      background: var(--white);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 1.5rem 1rem;
      flex: 1 1 200px;
      max-width: 260px;
      text-align: center;
      transition: transform 0.18s;
    }
    .why-card:hover {
      transform: translateY(-4px) scale(1.03);
      box-shadow: 0 6px 24px rgba(34,197,94,0.13);
    }
    .why-icon {
      font-size: 2rem;
      color: var(--leaf-green);
      margin-bottom: 0.6rem;
    }
    .why-title {
      font-size: 1.1rem;
      font-weight: 700;
      color: var(--deep-orange);
      margin-bottom: 0.3rem;
    }
    .why-desc {
      font-size: 0.98rem;
      color: #444;
    }
    /* Testimonials */
    .testimonials {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      justify-content: center;
      margin-top: 2.5rem;
    }
    .testimonial-card {
      background: var(--white);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding: 1.7rem 1.2rem;
      flex: 1 1 220px;
      max-width: 300px;
      text-align: center;
      transition: transform 0.18s;
      position: relative;
    }
    .testimonial-card:hover {
      transform: scale(1.03);
      box-shadow: 0 8px 32px rgba(34,197,94,0.13);
    }
  .icon {
  font-size: 24px;   
  color: #333;       
  margin-right: 8px; 
  vertical-align: middle;
} 
    .testimonial-name {
      font-weight: 700;
      color: var(--deep-orange);
      margin-bottom: 0.2rem;
    }
    .testimonial-review {
      font-size: 1rem;
      color: #444;
      font-style: italic;
    footer {
      background: var(--yellow-orange);
      color: var(--black);
      text-align: center;
      padding: 2rem 1rem 1rem 1rem;
      border-radius: 2rem 2rem 0 0;
      margin-top: 2rem;
      box-shadow: 0 -2px 16px rgba(255, 167, 38, 0.08);
    }
    .footer-links, .footer-social {
      display: flex;
      gap: 1.5rem;
      justify-content: center;
      margin-bottom: 1rem;
      flex-wrap: wrap;
    }
    .footer-links a, .footer-social a {
      color: var(--black);
      text-decoration: none;
      font-weight: 600;
      font-size: 1rem;
      border-radius: 1rem;
      padding: 0.4rem 0.7rem;
      transition: background 0.2s;
    }
    .footer-links a:hover, .footer-social a:hover {
      background: var(--green);
      color: var(--white);
    }
    .footer-contact {
      font-size: 1rem;
      margin-bottom: 0.8rem;
    }
    .footer-apps {
      margin-top: 0.5rem;
    }
    .footer-apps img {
      height: 38px;
      margin: 0 0.5rem;
      border-radius: 0.6rem;
      box-shadow: 0 2px 8px rgba(34,197,94,0.10);
      background: var(--white);
    }
    .footer-copy {
      font-size: 0.92rem;
      color: #444;
      margin-top: 1rem;
    }
    /* Responsive */
    @media (max-width: 950px) {
      .about-content, .steps, .plans, .why-list, .testimonials {
        flex-direction: column;
        align-items: stretch;
      }
      .about-img { margin-bottom: 1.5rem; }
    }
    @media (max-width: 700px) {
      .section, .join-tribe, footer {
        border-radius: 1rem;
        padding: 2rem 0.5rem;
      }
      header { padding: 0.5rem 1rem; }
      .hero h1 { font-size: 2rem; }
      .section-title { font-size: 1.5rem; }
    }
    @media (max-width: 500px) {
      .hero h1 { font-size: 1.35rem; }
      .brand { font-size: 1.2rem; }
      nav { gap: 0.5rem; }
      .btn, .btn.secondary { font-size: 0.95rem; padding: 0.65rem 1.2rem; }
    }
  </style>
</head>
<body>
  <!-- Sticky Navigation -->
  <header>
    <div class="logo">
      <img src="FK.png" alt="FitKhana Logo">
      <span class="brand">FitKhana</span>
    </div>
    <nav>
      <a href="#about">About</a>
      <a href="#how">How It Works</a>
      <a href="#plans">Meal Plans</a>
      <a href="#why">Why Us</a>
      <a href="#testimonials">Testimonials</a>
    </nav>
  </header>

 <section class="hero" style="background-image: url('fit bg.png'); padding-top:180px; background-size: cover; background-position: center; background-repeat: no-repeat;">
  <div class="hero-content">
    <h1>Smart Meal Plans, Freshly Made & Delivered to You</h1>
    <div class="slogan">Your Health, Our Mission</div>
    <div class="cta-group">
      <a href="#join" class="btn">Get Started</a>
      <a href="#plans" class="btn secondary">See Plans</a>
    </div>
  </div>
</section>

  <!-- About FitKhana -->
  <section class="section" id="about">
    <h2 class="section-title">About FitKhana</h2>
    <h3 class="section-title">Smart Meal Plans, Freshly Made & Delivered to You</h3>
    <div class="about-content">
      <div class="about-text">
<p><b>At FITKHANA</b>, we make healthy eating simple, personalized, and effortless. Built for fitness enthusiasts, busy professionals, and anyone who cares about what they eat, FITKHANA takes the guesswork out of nutrition by delivering smart, homemade meals right to your door.

We believe that eating well shouldn’t mean spending hours in the kitchen or settling for bland, repetitive food. That’s why every <b>FITKHANA meal</b> is crafted by expert chefs and approved by certified nutritionists—designed to fuel your body and fit your goals.
</p>
      </div>
      <div class="about-img">
        <!-- Replace with real food photo if available -->
        <img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836?auto=format&fit=crop&w=400&q=80" alt="Healthy Homemade Food">
      </div>
    </div>
  </section>

  <!-- How It Works -->
  <section class="section" id="how" style="background: var(--white);">
  <h2 class="section-title">How It Works</h2>
  <div class="steps">
    <div class="step-card">
      <div class="step-icon">
        <i class="fi fi-tr-goals" aria-hidden="true"></i>
      </div>
      <div class="step-title">Choose Your Goal</div>
      <div class="step-desc">
        Select from Weight Loss, Muscle Gain, Balanced Diet, or Diabetic-Friendly plans to match your health journey.
      </div>
    </div>
    <div class="step-card">
      <div class="icon">
        <i class="fi fi-tr-salad" aria-hidden="true"></i>
      </div>
      <div class="step-title">We Cook Fresh</div>
      <div class="step-desc">
        Our certified cooks prepare meals daily using local, seasonal, and nutritionist-approved ingredients.
      </div>
    </div>
    <div class="step-card">
      <div class="icon">
                
      </div>
      <div class="step-title">Delivered to Your Door</div>
      <div class="step-desc">
        Enjoy freshly made, healthy meals delivered right to your doorstep, on your schedule.
      </div>
    </div>
  </div>
</section>
  <!-- Meal Plans -->
  <section class="section" id="plans">
    <h2 class="section-title">Meal Plans</h2>
    <div class="plans">
      <div class="plan-card">
        <div class="plan-title">Weight Loss</div>
        <div class="plan-price">₹199/day</div>
        <ul class="plan-benefits">
          <li>Low-calorie, high-fiber meals</li>
          <li>Portion controlled</li>
          <li>Weekly nutritionist check-ins</li>
        </ul>
        <div class="plan-sample">Sample: Quinoa salad, Grilled veggies, Fruit bowl</div>
        <button class="plan-btn">Select Plan</button>
      </div>
      <div class="plan-card">
        <div class="plan-title">Muscle Gain</div>
        <div class="plan-price">₹249/day</div>
        <ul class="plan-benefits">
          <li>High-protein, balanced carbs</li>
          <li>Post-workout snacks</li>
          <li>Personalized macros</li>
        </ul>
        <div class="plan-sample">Sample: Paneer tikka, Brown rice, Protein smoothie</div>
        <button class="plan-btn">Select Plan</button>
      </div>
      <div class="plan-card">
        <div class="plan-title">Balanced Diet</div>
        <div class="plan-price">₹179/day</div>
        <ul class="plan-benefits">
          <li>Wholesome, home-style meals</li>
          <li>Seasonal veggies & grains</li>
          <li>Perfect for families & students</li>
        </ul>
        <div class="plan-sample">Sample: Dal, Roti, Mixed sabzi, Salad,bananas , choco powder  </div>
        <button class="plan-btn">Select Plan</button>
      </div>
      <div class="plan-card">
        <div class="plan-title">Diabetic-Friendly</div>
        <div class="plan-price">₹229/day</div>
        <ul class="plan-benefits">
          <li>Low-GI, sugar-free meals</li>
          <li>Expert dietitian support</li>
          <li>Safe, tasty, and filling</li>
        </ul>
        <div class="plan-sample">Sample: Millet upma, Stir-fried greens, Yogurt</div>
        <button class="plan-btn">Select Plan</button>
      </div>
    </div>
  </section>

  <!-- Why Choose FitKhana -->
  <section class="section" id="why" style="background: var(--white);">
    <h2 class="section-title">Why Choose FitKhana?</h2>
    <div class="why-list">
      <div class="why-card">
        <div class="why-icon"><i class="fas fa-user chef-icon"></i>
</div>
        <div class="why-title">Homemade by Certified Cooks</div>
        <div class="why-desc">Every meal is lovingly prepared in hygienic home kitchens by certified cooks.</div>
      </div>
      <div class="why-card">
        <div class="why-icon"></div>
        <div class="why-title">Nutritionist-Approved</div>
        <div class="why-desc">Our meal plans are crafted and reviewed by expert nutritionists for balanced nutrition.</div>
      </div>
      <div class="why-card">
        <div class="why-icon"></div>
        <div class="why-title">Flexible Subscriptions</div>
        <div class="why-desc">Pause, skip, or change your plan anytime. No lock-ins, just healthy freedom!</div>
      </div>
      <div class="why-card">
        <div class="why-icon"></div>
        <div class="why-title">Local, Fresh Ingredients</div>
        <div class="why-desc">We source ingredients from local farms for maximum freshness and nutrition.</div>
      </div>
    </div>
  </section>

 <!-- Testimonials -->
<section class="section" id="testimonials">
  <h2 class="section-title">Customer Testimonials</h2>
  <div class="testimonials">
    <div class="testimonial-card">
      <i class="fas fa-user unknown-user-icon"></i>
      <div class="testimonial-name">Roshan Shaw </div>
      <div class="testimonial-review">“FitKhana has made my weight loss journey enjoyable. The meals are delicious, satisfying, and never feel like a diet—so easy to stick to!”</div>
    </div>
    <div class="testimonial-card">
      <i class="fas fa-user unknown-user-icon"></i>
      <div class="testimonial-name">Yash Sharma</div>
      <div class="testimonial-review">“FitKhana didn’t just change the way I eat—it changed the way I feel about myself. With every meal tailored to my goals, I feel healthier, more energized, and more confident in my own skin. It’s like having a personal nutritionist and chef by my side every day.”</div>
    </div>
    <div class="testimonial-card">
      <i class="fas fa-user unknown-user-icon"></i>
      <div class="testimonial-name">Rahul Kumar</div>
      <div class="testimonial-review">“As a busy professional in Patna, I really appreciate the convenience and quality of FitKhana. The muscle gain plan has really helped me see results!”</div>
    </div>
    <div class="testimonial-card">
      <i class="fas fa-user unknown-user-icon"></i>
      <div class="testimonial-name">Yukti Sharma</div>
      <div class="testimonial-review">“Since starting FitKhana’s diabetic-friendly plan, my sugar levels have improved and I feel much healthier. Highly recommended for Indian families!”</div>
    </div>
  </div>
</section>

  <!-- Footer -->
  <footer>
    <div class="footer-links">
      <a href="#">Home</a>
      <a href="#plans">Meal Plans</a>
      <a href="#faq">FAQs</a>
      <a href="#contact">Contact</a>
    </div>
    <div class="footer-social">
      <a href="#" title="Instagram"></a>
      <a href="#" title="Facebook">📘</a>
      <a href="#" title="WhatsApp">💬</a>
    </div>
    <div class="footer-contact">
      <span>Email: <a href="mailto:hello@fitkhana.com">hello@fitkhana.com</a></span> |
      <span>Phone: <a href="tel:+919999999999">+91 99999 99999</a></span>
    </div>
    <div class="footer-apps">
      <!-- Placeholder for app download badges -->
      <img src="image.png" alt="Google Play" height="38">
      <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" alt="App Store" height="38">
    </div>
    <div class="footer-copy">
      &copy; 2025 FitKhana. All rights reserved.
    </div>
  </footer>

  <!-- Lightweight Animations & JS -->
  <script>
    // Join Tribe email capture (demo only)
    function joinTribe() {
      var email = document.getElementById('email').value;
      var msg = document.getElementById('join-msg');
      if(email && email.includes('@')) {
        msg.innerHTML = "Thank you for joining the FitKhana Tribe!";
        document.getElementById('email').value = '';
      } else {
        msg.innerHTML = "Please enter a valid email address.";
      }
      setTimeout(() => { msg.innerHTML = ""; }, 4000);
    }

    // Smooth scroll for nav links
    document.querySelectorAll('nav a').forEach(link => {
      link.addEventListener('click', function(e) {
        if(this.hash) {
          e.preventDefault();
          document.querySelector(this.hash).scrollIntoView({ behavior: 'smooth' });
        }
      });
    });

    // Animate leaves (simple float)
    // Already handled by CSS keyframes
  </script>
</body>
</html>

