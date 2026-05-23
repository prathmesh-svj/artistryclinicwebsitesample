<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Artistry Clinics | Cunningham Road, Bangalore</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #C9A84C;
    --gold-light: #E2C97E;
    --gold-dark: #8B6914;
    --black: #0A0A0A;
    --dark: #111111;
    --cream: #F5EFE6;
    --cream-dark: #E8DDD0;
    --white: #FFFFFF;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--black);
    color: var(--cream);
    font-family: 'Montserrat', sans-serif;
    overflow-x: hidden;
  }

  /* NAVBAR */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 20px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(10,10,10,0.95);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid rgba(201,168,76,0.2);
  }

  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px;
    font-weight: 600;
    color: var(--gold);
    letter-spacing: 3px;
    text-transform: uppercase;
  }

  .nav-links {
    display: flex;
    gap: 32px;
    list-style: none;
  }

  .nav-links a {
    color: var(--cream);
    text-decoration: none;
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    font-weight: 400;
    transition: color 0.3s;
  }

  .nav-links a:hover { color: var(--gold); }

  .nav-cta {
    background: transparent;
    border: 1px solid var(--gold);
    color: var(--gold) !important;
    padding: 8px 20px;
    font-size: 10px !important;
    letter-spacing: 2px !important;
    cursor: pointer;
    transition: all 0.3s !important;
  }

  .nav-cta:hover {
    background: var(--gold) !important;
    color: var(--black) !important;
  }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
    padding: 120px 40px 80px;
  }

  .hero-bg {
    position: absolute;
    inset: 0;
    background: 
      radial-gradient(ellipse at 20% 50%, rgba(201,168,76,0.08) 0%, transparent 60%),
      radial-gradient(ellipse at 80% 20%, rgba(201,168,76,0.05) 0%, transparent 50%),
      var(--black);
  }

  .hero-lines {
    position: absolute;
    inset: 0;
    background-image: 
      linear-gradient(rgba(201,168,76,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(201,168,76,0.03) 1px, transparent 1px);
    background-size: 60px 60px;
  }

  .hero-content {
    position: relative;
    z-index: 1;
    text-align: center;
    max-width: 900px;
  }

  .hero-badge {
    display: inline-block;
    border: 1px solid rgba(201,168,76,0.4);
    padding: 8px 24px;
    font-size: 10px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 32px;
    animation: fadeInDown 0.8s ease both;
  }

  .hero-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(52px, 8vw, 96px);
    font-weight: 300;
    line-height: 1;
    color: var(--white);
    margin-bottom: 8px;
    animation: fadeInUp 0.8s ease 0.2s both;
  }

  .hero-title span {
    color: var(--gold);
    font-style: italic;
  }

  .hero-subtitle {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(18px, 3vw, 28px);
    font-weight: 300;
    color: rgba(245,239,230,0.6);
    letter-spacing: 6px;
    text-transform: uppercase;
    margin-bottom: 40px;
    animation: fadeInUp 0.8s ease 0.3s both;
  }

  .hero-desc {
    font-size: 13px;
    line-height: 1.9;
    color: rgba(245,239,230,0.7);
    max-width: 560px;
    margin: 0 auto 48px;
    letter-spacing: 0.5px;
    animation: fadeInUp 0.8s ease 0.4s both;
  }

  .hero-btns {
    display: flex;
    gap: 16px;
    justify-content: center;
    flex-wrap: wrap;
    animation: fadeInUp 0.8s ease 0.5s both;
  }

  .btn-primary {
    background: var(--gold);
    color: var(--black);
    padding: 16px 40px;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    font-weight: 600;
    text-decoration: none;
    transition: all 0.3s;
    display: inline-block;
  }

  .btn-primary:hover {
    background: var(--gold-light);
    transform: translateY(-2px);
  }

  .btn-secondary {
    background: transparent;
    color: var(--cream);
    padding: 16px 40px;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    font-weight: 400;
    text-decoration: none;
    border: 1px solid rgba(245,239,230,0.3);
    transition: all 0.3s;
    display: inline-block;
  }

  .btn-secondary:hover {
    border-color: var(--gold);
    color: var(--gold);
  }

  .hero-stats {
    display: flex;
    justify-content: center;
    gap: 60px;
    margin-top: 80px;
    padding-top: 60px;
    border-top: 1px solid rgba(201,168,76,0.15);
    animation: fadeInUp 0.8s ease 0.6s both;
  }

  .stat { text-align: center; }

  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 42px;
    font-weight: 300;
    color: var(--gold);
    display: block;
  }

  .stat-label {
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: rgba(245,239,230,0.5);
    margin-top: 4px;
  }

  /* MARQUEE */
  .marquee {
    background: var(--gold);
    padding: 14px 0;
    overflow: hidden;
    white-space: nowrap;
  }

  .marquee-track {
    display: inline-block;
    animation: marquee 20s linear infinite;
  }

  .marquee span {
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--black);
    font-weight: 600;
    padding: 0 40px;
  }

  .marquee span::after {
    content: '✦';
    padding-left: 40px;
  }

  @keyframes marquee {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); }
  }

  /* SECTIONS */
  section { padding: 100px 40px; }

  .section-label {
    font-size: 10px;
    letter-spacing: 4px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 16px;
    display: block;
  }

  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(36px, 5vw, 64px);
    font-weight: 300;
    color: var(--white);
    line-height: 1.1;
    margin-bottom: 24px;
  }

  .section-title em {
    color: var(--gold);
    font-style: italic;
  }

  /* ABOUT */
  .about {
    background: var(--dark);
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
  }

  .about-text p {
    font-size: 14px;
    line-height: 1.9;
    color: rgba(245,239,230,0.7);
    margin-bottom: 20px;
  }

  .about-features {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin-top: 40px;
  }

  .feature {
    border-left: 2px solid var(--gold);
    padding-left: 16px;
  }

  .feature-title {
    font-size: 12px;
    letter-spacing: 1px;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 4px;
  }

  .feature-desc {
    font-size: 12px;
    color: rgba(245,239,230,0.5);
  }

  .about-visual {
    position: relative;
  }

  .about-card {
    background: rgba(201,168,76,0.05);
    border: 1px solid rgba(201,168,76,0.15);
    padding: 48px;
    text-align: center;
  }

  .rating-big {
    font-family: 'Cormorant Garamond', serif;
    font-size: 80px;
    color: var(--gold);
    font-weight: 300;
    line-height: 1;
  }

  .stars {
    color: var(--gold);
    font-size: 20px;
    letter-spacing: 4px;
    margin: 8px 0;
  }

  .rating-count {
    font-size: 12px;
    color: rgba(245,239,230,0.5);
    letter-spacing: 2px;
    text-transform: uppercase;
  }

  .about-card-divider {
    border: none;
    border-top: 1px solid rgba(201,168,76,0.2);
    margin: 32px 0;
  }

  .about-card-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px;
    font-style: italic;
    color: rgba(245,239,230,0.7);
    line-height: 1.6;
  }

  /* SERVICES */
  .services-section {
    background: var(--black);
    max-width: 1200px;
    margin: 0 auto;
  }

  .services-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    margin-bottom: 60px;
    flex-wrap: wrap;
    gap: 20px;
  }

  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
    gap: 2px;
  }

  .service-card {
    background: var(--dark);
    padding: 40px;
    border: 1px solid rgba(201,168,76,0.08);
    transition: all 0.4s;
    position: relative;
    overflow: hidden;
  }

  .service-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 2px;
    background: var(--gold);
    transform: scaleX(0);
    transition: transform 0.4s;
  }

  .service-card:hover::before { transform: scaleX(1); }
  .service-card:hover { background: rgba(201,168,76,0.05); }

  .service-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 48px;
    color: rgba(201,168,76,0.15);
    font-weight: 300;
    line-height: 1;
    margin-bottom: 16px;
  }

  .service-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 26px;
    color: var(--white);
    font-weight: 400;
    margin-bottom: 8px;
  }

  .service-detail {
    font-size: 11px;
    color: rgba(245,239,230,0.4);
    letter-spacing: 1px;
    margin-bottom: 20px;
  }

  .service-price {
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px;
    color: var(--gold);
    font-weight: 300;
  }

  .service-duration {
    font-size: 10px;
    color: rgba(245,239,230,0.35);
    letter-spacing: 1px;
    margin-top: 4px;
  }

  /* REVIEWS */
  .reviews-section {
    background: var(--dark);
    max-width: 1200px;
    margin: 0 auto;
  }

  .reviews-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 24px;
    margin-top: 60px;
  }

  .review-card {
    background: rgba(201,168,76,0.03);
    border: 1px solid rgba(201,168,76,0.12);
    padding: 32px;
  }

  .review-stars {
    color: var(--gold);
    font-size: 14px;
    letter-spacing: 2px;
    margin-bottom: 16px;
  }

  .review-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: 17px;
    font-style: italic;
    color: rgba(245,239,230,0.8);
    line-height: 1.7;
    margin-bottom: 20px;
  }

  .review-author {
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold);
  }

  /* CONTACT */
  .contact-section {
    background: var(--black);
    max-width: 1200px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }

  .contact-info { }

  .contact-item {
    display: flex;
    gap: 20px;
    margin-bottom: 32px;
    align-items: flex-start;
  }

  .contact-icon {
    width: 40px;
    height: 40px;
    border: 1px solid rgba(201,168,76,0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--gold);
    font-size: 16px;
    flex-shrink: 0;
  }

  .contact-label {
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 6px;
  }

  .contact-value {
    font-size: 14px;
    color: rgba(245,239,230,0.8);
    line-height: 1.6;
  }

  .hours-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 8px;
    margin-top: 8px;
  }

  .hour-item {
    font-size: 12px;
    color: rgba(245,239,230,0.5);
  }

  .hour-item span { color: var(--gold); }

  .contact-cta {
    background: rgba(201,168,76,0.05);
    border: 1px solid rgba(201,168,76,0.2);
    padding: 48px;
    text-align: center;
  }

  .contact-cta h3 {
    font-family: 'Cormorant Garamond', serif;
    font-size: 36px;
    font-weight: 300;
    color: var(--white);
    margin-bottom: 16px;
  }

  .contact-cta p {
    font-size: 13px;
    color: rgba(245,239,230,0.6);
    margin-bottom: 32px;
    line-height: 1.7;
  }

  .whatsapp-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: #25D366;
    color: white;
    padding: 16px 36px;
    font-size: 12px;
    letter-spacing: 2px;
    text-transform: uppercase;
    font-weight: 600;
    text-decoration: none;
    transition: all 0.3s;
    margin-bottom: 16px;
    width: 100%;
    justify-content: center;
  }

  .whatsapp-btn:hover { background: #1ea952; transform: translateY(-2px); }

  .call-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: transparent;
    color: var(--gold);
    padding: 16px 36px;
    font-size: 12px;
    letter-spacing: 2px;
    text-transform: uppercase;
    font-weight: 500;
    text-decoration: none;
    border: 1px solid var(--gold);
    transition: all 0.3s;
    width: 100%;
    justify-content: center;
  }

  .call-btn:hover { background: var(--gold); color: var(--black); }

  /* FOOTER */
  footer {
    background: var(--dark);
    border-top: 1px solid rgba(201,168,76,0.15);
    padding: 40px;
    text-align: center;
  }

  .footer-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 24px;
    color: var(--gold);
    letter-spacing: 4px;
    text-transform: uppercase;
    margin-bottom: 16px;
  }

  .footer-tagline {
    font-size: 11px;
    letter-spacing: 3px;
    color: rgba(245,239,230,0.35);
    text-transform: uppercase;
    margin-bottom: 24px;
  }

  .footer-links {
    display: flex;
    justify-content: center;
    gap: 32px;
    flex-wrap: wrap;
  }

  .footer-links a {
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: rgba(245,239,230,0.4);
    text-decoration: none;
    transition: color 0.3s;
  }

  .footer-links a:hover { color: var(--gold); }

  .footer-copy {
    font-size: 11px;
    color: rgba(245,239,230,0.2);
    margin-top: 24px;
  }

  /* ANIMATIONS */
  @keyframes fadeInDown {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* DIVIDER */
  .gold-divider {
    width: 60px;
    height: 1px;
    background: var(--gold);
    margin: 24px 0;
  }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    nav { padding: 16px 20px; }
    .nav-links { display: none; }
    section { padding: 70px 20px; }
    .about { grid-template-columns: 1fr; gap: 40px; }
    .contact-section { grid-template-columns: 1fr; gap: 40px; }
    .hero-stats { gap: 30px; flex-wrap: wrap; }
    .services-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- NAVBAR -->
<nav>
  <div class="nav-logo">Artistry Clinics</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#reviews">Reviews</a></li>
    <li><a href="#contact" class="nav-cta">Book Now</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-lines"></div>
  <div class="hero-content">
    <div class="hero-badge">Cunningham Road · Bangalore</div>
    <h1 class="hero-title">Artistry <span>Clinics</span></h1>
    <p class="hero-subtitle">Skin · Hair · Lash · Botox & Fillers</p>
    <p class="hero-desc">Where science meets artistry. Expert aesthetic treatments delivered by certified professionals in the heart of Bangalore's most prestigious address.</p>
    <div class="hero-btns">
      <a href="https://wa.me/917795257887" class="btn-primary">Book Appointment</a>
      <a href="#services" class="btn-secondary">Our Services</a>
    </div>
    <div class="hero-stats">
      <div class="stat">
        <span class="stat-num">4.6★</span>
        <span class="stat-label">Google Rating</span>
      </div>
      <div class="stat">
        <span class="stat-num">169+</span>
        <span class="stat-label">Happy Clients</span>
      </div>
      <div class="stat">
        <span class="stat-num">10+</span>
        <span class="stat-label">Treatments</span>
      </div>
    </div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee">
  <div class="marquee-track">
    <span>Microblading</span>
    <span>Dermal Fillers</span>
    <span>Botox</span>
    <span>Lash Extensions</span>
    <span>Lip Pigmentation</span>
    <span>Carbon Laser Facial</span>
    <span>PRP & GFC</span>
    <span>Glutathione IV Drip</span>
    <span>Microblading</span>
    <span>Dermal Fillers</span>
    <span>Botox</span>
    <span>Lash Extensions</span>
    <span>Lip Pigmentation</span>
    <span>Carbon Laser Facial</span>
    <span>PRP & GFC</span>
    <span>Glutathione IV Drip</span>
  </div>
</div>

<!-- ABOUT -->
<section id="about" style="background: var(--dark); padding: 100px 40px;">
  <div class="about">
    <div class="about-text">
      <span class="section-label">About Us</span>
      <h2 class="section-title">Where Beauty Meets <em>Science</em></h2>
      <div class="gold-divider"></div>
      <p>Artistry Clinics Cunningham Road is Bangalore's premier aesthetic clinic, led by certified dermatologists and aesthetic specialists. We offer a comprehensive range of skin, hair, and cosmetic treatments tailored to your unique needs.</p>
      <p>Located in the heart of Cunningham Road, opposite Fortis Hospital, we combine cutting-edge technology with personalised care to deliver results that speak for themselves.</p>
      <div class="about-features">
        <div class="feature">
          <div class="feature-title">Certified Experts</div>
          <div class="feature-desc">Board-certified specialists</div>
        </div>
        <div class="feature">
          <div class="feature-title">Premium Products</div>
          <div class="feature-desc">Only FDA-approved materials</div>
        </div>
        <div class="feature">
          <div class="feature-title">Private & Safe</div>
          <div class="feature-desc">100% confidential treatments</div>
        </div>
        <div class="feature">
          <div class="feature-title">LGBTQ+ Friendly</div>
          <div class="feature-desc">Inclusive & welcoming space</div>
        </div>
      </div>
    </div>
    <div class="about-visual">
      <div class="about-card">
        <div class="rating-big">4.6</div>
        <div class="stars">★★★★★</div>
        <div class="rating-count">169 Google Reviews</div>
        <hr class="about-card-divider">
        <p class="about-card-text">"Super professional staff, knowledgeable doctor, and a very calm, clean setup. 10/10 would recommend!"</p>
        <div style="font-size: 11px; color: var(--gold); letter-spacing: 2px; margin-top: 16px;">— Verified Client</div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services" style="padding: 100px 40px; background: var(--black);">
  <div class="services-section">
    <div class="services-header">
      <div>
        <span class="section-label">What We Offer</span>
        <h2 class="section-title">Our <em>Treatments</em></h2>
      </div>
      <a href="https://wa.me/917795257887" class="btn-primary">Book a Treatment</a>
    </div>
    <div class="services-grid">

      <div class="service-card">
        <div class="service-num">01</div>
        <div class="service-name">Microblading</div>
        <div class="service-detail">Entire Treatment · 2 Sessions</div>
        <div class="service-price">₹9,990/-</div>
        <div class="service-duration">Permanent brow perfection</div>
      </div>

      <div class="service-card">
        <div class="service-num">02</div>
        <div class="service-name">Dermal Fillers</div>
        <div class="service-detail">Per mL · Lasts up to 1.5 Years</div>
        <div class="service-price">₹14,999/-</div>
        <div class="service-duration">Nose, Lip, Chin & Under Eye</div>
      </div>

      <div class="service-card">
        <div class="service-num">03</div>
        <div class="service-name">Botox</div>
        <div class="service-detail">Per Unit</div>
        <div class="service-price">₹349/-</div>
        <div class="service-duration">FDA approved · Instant results</div>
      </div>

      <div class="service-card">
        <div class="service-num">04</div>
        <div class="service-name">Lash Extension</div>
        <div class="service-detail">Classic Variant</div>
        <div class="service-price">₹1,999/-</div>
        <div class="service-duration">Fuller, longer lashes instantly</div>
      </div>

      <div class="service-card">
        <div class="service-num">05</div>
        <div class="service-name">Lip Pigmentation</div>
        <div class="service-detail">Entire Treatment · 3 Sessions</div>
        <div class="service-price">₹9,990/-</div>
        <div class="service-duration">Natural-looking lip colour</div>
      </div>

      <div class="service-card">
        <div class="service-num">06</div>
        <div class="service-name">Carbon Laser Facial</div>
        <div class="service-detail">Full Treatment</div>
        <div class="service-price">₹2,999/-</div>
        <div class="service-duration">Reduces pigmentation & acne</div>
      </div>

      <div class="service-card">
        <div class="service-num">07</div>
        <div class="service-name">Lip Blush</div>
        <div class="service-detail">3 Sessions</div>
        <div class="service-price">₹9,990/-</div>
        <div class="service-duration">Semi-permanent colour treatment</div>
      </div>

      <div class="service-card">
        <div class="service-num">08</div>
        <div class="service-name">Glutathione IV Drip</div>
        <div class="service-detail">Per Session</div>
        <div class="service-price">On Consultation</div>
        <div class="service-duration">Skin brightening from within</div>
      </div>

    </div>
  </div>
</section>

<!-- REVIEWS -->
<section id="reviews" style="padding: 100px 40px; background: var(--dark);">
  <div class="reviews-section">
    <div style="text-align: center; margin-bottom: 20px;">
      <span class="section-label">Client Stories</span>
      <h2 class="section-title">What Our <em>Clients Say</em></h2>
    </div>
    <div class="reviews-grid">
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"Absolutely loved my experience. Got hydrafacial done, my skin was glowing. Super professional staff, knowledgeable doctor, and a very calm, clean setup."</p>
        <div class="review-author">Christlyn S. · Local Guide</div>
      </div>
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"I had a truly reassuring experience for my GFC hair treatment. The team was patient, informative, and made sure I understood every step of the procedure."</p>
        <div class="review-author">Rahul G. · Verified Client</div>
      </div>
      <div class="review-card">
        <div class="review-stars">★★★★★</div>
        <p class="review-text">"The staff and manager were extremely professional, attentive, and kind throughout my visit. Their warm approach and genuine care made me feel very comfortable."</p>
        <div class="review-author">Carol B. · Verified Client</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" style="padding: 100px 40px; background: var(--black);">
  <div class="contact-section">
    <div class="contact-info">
      <span class="section-label">Find Us</span>
      <h2 class="section-title">Visit <em>Artistry</em></h2>
      <div class="gold-divider"></div>

      <div class="contact-item">
        <div class="contact-icon">📍</div>
        <div>
          <div class="contact-label">Address</div>
          <div class="contact-value">No 101, Chicago Avenue, 37/2<br>Cunningham Road, opposite Fortis Hospital<br>Vasanth Nagar, Bengaluru 560052<br><small style="color: var(--gold); font-size: 11px;">(Cubbon Park Metro Station Stop)</small></div>
        </div>
      </div>

      <div class="contact-item">
        <div class="contact-icon">📞</div>
        <div>
          <div class="contact-label">Phone</div>
          <div class="contact-value">+91 77952 57887<br>+91 77952 01887</div>
        </div>
      </div>

      <div class="contact-item">
        <div class="contact-icon">🕐</div>
        <div>
          <div class="contact-label">Opening Hours</div>
          <div class="contact-value">
            <div class="hours-grid">
              <div class="hour-item"><span>Mon–Fri</span><br>11am – 8pm</div>
              <div class="hour-item"><span>Saturday</span><br>11am – 8pm</div>
              <div class="hour-item"><span>Sunday</span><br>1pm – 8:30pm</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="contact-cta">
      <h3>Ready to Transform?</h3>
      <p>Book your consultation today. Our specialists are ready to create your personalised treatment plan.</p>
      <a href="https://wa.me/917795257887" class="whatsapp-btn">
        💬 WhatsApp Us
      </a>
      <a href="tel:+917795257887" class="call-btn">
        📞 Call Now
      </a>
      <p style="margin-top: 20px; font-size: 11px; color: rgba(245,239,230,0.3); letter-spacing: 1px;">Walk-ins welcome · Free consultation available</p>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Artistry Clinics</div>
  <div class="footer-tagline">Skin · Hair · Lash · Botox & Fillers · Cunningham Road, Bangalore</div>
  <div class="footer-links">
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#reviews">Reviews</a>
    <a href="#contact">Contact</a>
    <a href="https://www.instagram.com/artistryclinics.cunninghamroad" target="_blank">Instagram</a>
    <a href="https://wa.me/917795257887" target="_blank">WhatsApp</a>
  </div>
  <div class="footer-copy">© 2025 Artistry Clinics Cunningham Road · All Rights Reserved</div>
</footer>

</body>
</html>
