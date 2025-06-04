
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Shahzaib Hanjra Portfolio</title>
  <style>
    /* RESET */
    * {
      margin: 0; padding: 0; box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #0a0f2c;
      color: #c0c8ff;
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    a {
      color: #00ffff;
      text-decoration: none;
      transition: color 0.3s ease;
    }
    a:hover {
      color: #ff00ff;
    }

    /* NAVIGATION */
    header {
      background: #061142;
      padding: 1.5rem 1rem;
      position: sticky;
      top: 0;
      z-index: 10;
      box-shadow: 0 0 15px #00ffff;
    }

    nav {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 1.8rem;
      font-weight: 700;
      color: #00ffff;
      text-shadow: 0 0 10px #00ffff;
      user-select: none;
    }

    .nav-links {
      list-style: none;
      display: flex;
      gap: 2rem;
    }

    .nav-links li a {
      font-weight: 600;
      font-size: 1rem;
      text-shadow: 0 0 5px #00ffff;
    }

    .menu-toggle {
      display: none;
      font-size: 2.2rem;
      cursor: pointer;
      color: #00ffff;
    }

    /* HERO */
    .hero-text {
      max-width: 700px;
      margin: 3rem auto 4rem auto;
      text-align: center;
    }

    .neon-glow {
      font-size: 3.2rem;
      font-weight: 900;
      color: #00ffff;
      text-shadow:
        0 0 5px #00ffff,
        0 0 10px #00ffff,
        0 0 20px #00ffff,
        0 0 40px #0ff,
        0 0 80px #0ff;
      animation: flicker 2.5s infinite alternate;
    }

    @keyframes flicker {
      0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% {
        opacity: 1;
        text-shadow:
          0 0 5px #00ffff,
          0 0 10px #00ffff,
          0 0 20px #00ffff,
          0 0 40px #0ff,
          0 0 80px #0ff;
      }
      20%, 22%, 24%, 55% {
        opacity: 0.5;
        text-shadow: none;
      }
    }

    .typed-text {
      font-size: 1.4rem;
      color: #ff00ff;
      text-shadow: 0 0 8px #ff00ff;
      margin: 1rem 0 3rem 0;
      height: 30px; /* prevent layout shift */
    }

    /* BUTTON */
    .btn {
      display: inline-block;
      background: linear-gradient(45deg, #00ffff, #ff00ff);
      color: #0a0f2c;
      font-weight: 700;
      padding: 0.8rem 2.5rem;
      border-radius: 50px;
      box-shadow:
        0 0 10px #00ffff,
        0 0 20px #ff00ff;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      cursor: pointer;
      transition: background 0.3s ease;
      user-select: none;
    }
    .btn:hover {
      background: linear-gradient(45deg, #ff00ff, #00ffff);
      color: white;
      box-shadow:
        0 0 15px #ff00ff,
        0 0 30px #00ffff;
    }

    /* SECTIONS */
    section {
      max-width: 900px;
      margin: 3rem auto;
      padding: 0 1rem;
      text-align: center;
    }

    h2 {
      font-size: 2.8rem;
      margin-bottom: 1.2rem;
      color: #ff00ff;
      text-shadow: 0 0 10px #ff00ff;
    }

    /* ABOUT */
    .about-content {
      display: flex;
      align-items: center;
      gap: 2.5rem;
      justify-content: center;
      text-align: left;
      flex-wrap: wrap;
    }

    .about-content img {
      border-radius: 50%;
      width: 250px;
      box-shadow:
        0 0 15px #00ffff,
        0 0 30px #ff00ff;
      flex-shrink: 0;
    }

    .about-content p {
      max-width: 500px;
      font-size: 1.2rem;
      line-height: 1.5;
    }

    /* PROJECTS */
    .projects-grid {
      display: grid;
      gap: 2rem;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    }

    .project-card {
      background: #192a67;
      padding: 1.8rem;
      border-radius: 12px;
      box-shadow:
        0 0 12px #00ffff;
      color: white;
      text-shadow: 0 0 5px #0ff;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: default;
    }

    .project-card:hover {
      transform: translateY(-8px);
      box-shadow:
        0 0 25px #ff00ff,
        0 0 40px #00ffff;
    }

    /* CONTACT */
    #contact p, #contact a {
      font-size: 1.2rem;
      margin: 0.6rem 0;
      color: #c0c8ff;
      text-shadow: 0 0 6px #0ff;
      user-select: text;
    }

    .social-links {
      margin-top: 1.5rem;
      display: flex;
      justify-content: center;
      gap: 2rem;
    }

    .social-links a {
      font-weight: 700;
      font-size: 1.1rem;
      padding: 0.5rem 1.2rem;
      border: 2px solid #00ffff;
      border-radius: 30px;
      box-shadow:
        0 0 12px #00ffff;
      transition: all 0.3s ease;
    }

    .social-links a:hover {
      background: #00ffff;
      color: #0a0f2c;
      box-shadow:
        0 0 20px #00ffff,
        0 0 40px #ff00ff;
    }

    /* Responsive Nav */
    @media (max-width: 768px) {
      .nav-links {
        position: fixed;
        top: 70px;
        right: 0;
        background: #061142;
        height: calc(100% - 70px);
        width: 200px;
        flex-direction: column;
        padding: 2rem;
        transform: translateX(100%);
        transition: transform 0.3s ease-in-out;
        box-shadow: -2px 0 10px rgba(0,0,0,0.7);
      }

      .nav-links.active {
        transform: translateX(0);
      }

      .nav-links li {
        margin-bottom: 1.5rem;
      }

      .menu-toggle {
        display: block;
      }
    }
  </style>
</head>
<body>

<header>
  <nav>
    <div class="logo">Shahzaib Hanjra</div>
    <ul class="nav-links" id="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="menu-toggle" id="menu-toggle">&#9776;</div>
  </nav>
</header>

<section class="hero-text">
  <h1 class="neon-glow">Hi, I'm Shahzaib Hanjra</h1>
  <div class="typed-text" id="typed-text"></div>
  <button class="btn" onclick="scrollToSection('projects')">View My Work</button>
</section>

<section id="about">
  <h2>About Me</h2>
  <div class="about-content">
    <img src="https://via.placeholder.com/250" alt="Shahzaib Hanjra" />
    <p>
      I’m a professional editor with 4+ years of experience in video, podcast, and content editing.
      Whether it’s storytelling, promotional reels, or polishing up social media clips — I turn raw footage into impactful content.
    </p>
  </div>
</section>

<section id="projects">
  <h2>Featured Work</h2>
  <div class="projects-grid">
    <div class="project-card">
      <strong>📽️ Travel Documentary (2024)</strong><br>
      Edited for YouTube series “WanderWide” – 100k+ views
    </div>
    <div class="project-card">
      <strong>🎙️ Podcast: Startup Talks</strong><br>
      Edited 30+ episodes, mixed audio, created teaser cuts for social
    </div>
    <div class="project-card">
      <strong>📱
```

