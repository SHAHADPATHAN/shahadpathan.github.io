<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="This Is The Page Which Contains Description about Shahad Pathan">
  <title>Shahad Pathan - Portfolio</title>
  <link rel="icon" href="sp.png" type="image/png">




 
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: #333;
      overflow-x: hidden;
      position: relative;
    }

    /* Enhanced Background */
    .animated-background {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -2;
      background: linear-gradient(45deg, #1e3c72, #2a5298, #764ba2, #667eea);
      background-size: 400% 400%;
      animation: gradientShift 15s ease infinite;
    }

    @keyframes gradientShift {
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

    /* Particle System */
    .particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
      pointer-events: none;
    }

    .particle {
      position: absolute;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 50%;
      animation: float 6s ease-in-out infinite;
    }

    @keyframes float {

      0%,
      100% {
        transform: translateY(0px) rotate(0deg);
      }

      50% {
        transform: translateY(-20px) rotate(180deg);
      }
    }

    /* Enhanced Navigation */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(0, 0, 0, 0.9);
      backdrop-filter: blur(15px);
      z-index: 1000;
      border-bottom: 1px solid rgba(255, 255, 255, 0.1);
      transition: all 0.3s ease;
    }

    .nav-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 70px;
    }

    .nav-logo .logo-text {
      font-size: 1.8em;
      font-weight: bold;
      color: #00ff88;
      text-decoration: none;
    }

    .nav-menu {
      display: flex;
      list-style: none;
      margin: 0;
      padding: 0;
    }

    .nav-menu li {
      margin: 0 20px;
    }

    .nav-link {
      color: white;
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s ease;
      position: relative;
    }

    .nav-link:hover {
      color: #00ff88;
    }

    .nav-link::after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 0;
      height: 2px;
      background: linear-gradient(90deg, #00ff88, #00d4ff);
      transition: width 0.3s ease;
    }

    .nav-link:hover::after {
      width: 100%;
    }

    .hamburger {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }

    .hamburger .bar {
      width: 25px;
      height: 3px;
      background: white;
      margin: 3px 0;
      transition: 0.3s;
    }

    header {
      background: rgba(0, 0, 0, 0.1);
      backdrop-filter: blur(10px);
      color: white;
      padding: 120px 40px 60px;
      text-align: center;
      position: relative;
      border-bottom: 1px solid rgba(255, 255, 255, 0.1);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .hero-content {
      max-width: 800px;
      margin: 0 auto;
    }

    .hero-text {
      margin-bottom: 40px;
    }

    header h1 {
      margin: 0;
      font-size: 3.5em;
      margin-bottom: 15px;
      animation: fadeInUp 1s ease-out;
      background: linear-gradient(45deg, #00ff88, #00d4ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .hero-subtitle {
      font-size: 1.5em;
      margin-bottom: 20px;
      color: #ffffff;
      animation: fadeInUp 1s ease-out 0.1s both;
    }

    .hero-description {
      font-size: 1.2em;
      opacity: 0.9;
      margin-bottom: 30px;
      animation: fadeInUp 1s ease-out 0.2s both;
      line-height: 1.6;
    }

    /* CTA Buttons */
    .cta-buttons {
      display: flex;
      gap: 20px;
      justify-content: center;
      margin-bottom: 30px;
      animation: fadeInUp 1s ease-out 0.3s both;
    }

    .btn {
      padding: 12px 30px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      transition: all 0.3s ease;
      display: inline-block;
      position: relative;
      overflow: hidden;
    }

    .btn-primary {
      background: linear-gradient(45deg, #00ff88, #00d4ff);
      color: #000;
      border: 2px solid transparent;
    }

    .btn-secondary {
      background: transparent;
      color: white;
      border: 2px solid #00ff88;
    }

    .btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 25px rgba(0, 255, 136, 0.3);
    }

    .btn-primary:hover {
      background: linear-gradient(45deg, #00d4ff, #00ff88);
    }

    .btn-secondary:hover {
      background: #00ff88;
      color: #000;
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    section {
      max-width: 1200px;
      margin: 60px auto;
      padding: 0 20px;
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 50px 40px;
      margin-bottom: 40px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      animation: slideInLeft 0.8s ease-out;
      color: white;
    }

    .section-header {
      text-align: center;
      margin-bottom: 50px;
    }

    .section-subtitle {
      color: rgba(255, 255, 255, 0.8);
      font-size: 1.1em;
      margin-top: 10px;
    }

    /* About Section Enhancements */
    .about-content {
      display: grid;
      gap: 40px;
      align-items: center;
    }

    .about-text p {
      font-size: 1.1em;
      line-height: 1.8;
      margin-bottom: 20px;
    }

    .stats-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 30px;
      margin-top: 40px;
    }

    .stat-item {
      text-align: center;
      padding: 20px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 15px;
      border: 1px solid rgba(0, 255, 136, 0.3);
    }

    .stat-item h3 {
      font-size: 2.5em;
      color: #00ff88;
      margin-bottom: 5px;
    }

    .stat-item p {
      color: rgba(255, 255, 255, 0.9);
      font-size: 0.9em;
    }

    /* Skills Section Enhancements */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 40px;
      margin-bottom: 40px;
    }

    .skill-category {
      background: rgba(255, 255, 255, 0.05);
      padding: 30px;
      border-radius: 15px;
      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    .skill-category h3 {
      color: #00ff88;
      margin-bottom: 25px;
      font-size: 1.3em;
    }

    .tech-stack {
      text-align: center;
      padding: 30px;
      background: rgba(0, 255, 136, 0.1);
      border-radius: 15px;
      border: 1px solid rgba(0, 255, 136, 0.3);
    }

    .tech-stack h3 {
      color: #00ff88;
      margin-bottom: 15px;
    }

    /* Projects Section Enhancements */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 30px;
    }

    .project-card {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 20px;
      padding: 30px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      text-align: center;
    }

    .project-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(0, 255, 136, 0.2);
    }

    .project-icon-display {
      font-size: 3em;
      margin-bottom: 20px;
    }

    .project-card h3 {
      color: #00ff88;
      margin-bottom: 15px;
      font-size: 1.4em;
    }

    .project-card p {
      line-height: 1.6;
      margin-bottom: 20px;
      color: rgba(255, 255, 255, 0.9);
    }

    .project-tech {
      display: flex;
      gap: 10px;
      justify-content: center;
      margin-bottom: 25px;
      flex-wrap: wrap;
    }

    .tech-tag {
      background: rgba(0, 255, 136, 0.2);
      color: #00ff88;
      padding: 5px 12px;
      border-radius: 20px;
      font-size: 0.85em;
      border: 1px solid rgba(0, 255, 136, 0.3);
    }

    .project-links {
      display: flex;
      gap: 15px;
      justify-content: center;
    }

    .project-link {
      color: #00d4ff;
      text-decoration: none;
      padding: 8px 20px;
      border: 1px solid #00d4ff;
      border-radius: 25px;
      transition: all 0.3s ease;
    }

    .project-link:hover {
      background: #00d4ff;
      color: #000;
    }

    /* Certificates Section Enhancements */
    .certificates-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 30px;
    }

    .certificate-card {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 20px;
      padding: 30px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      text-align: center;
      position: relative;
      overflow: hidden;
    }

    .certificate-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: linear-gradient(90deg, #00ff88, #00d4ff);
    }

    .certificate-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(0, 255, 136, 0.2);
    }

    .certificate-icon {
      font-size: 3em;
      margin-bottom: 20px;
      animation: float 3s ease-in-out infinite;
    }

    .certificate-card h3 {
      color: #00ff88;
      font-size: 1.4em;
      margin-bottom: 10px;
    }

    .certificate-card p {
      line-height: 1.6;
      margin-bottom: 20px;
      color: rgba(255, 255, 255, 0.9);
    }

    .certificate-details {
      display: flex;
      justify-content: space-between;
      margin-bottom: 20px;
      padding: 10px 0;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
      border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    }

    .cert-issuer {
      color: #00d4ff;
      font-weight: 600;
    }

    .cert-date {
      color: rgba(255, 255, 255, 0.8);
      font-size: 0.9em;
    }

    .certificate-link {
      display: inline-block;
      color: #00d4ff;
      text-decoration: none;
      padding: 10px 25px;
      border: 2px solid #00d4ff;
      border-radius: 25px;
      transition: all 0.3s ease;
      font-weight: 600;
    }

    .certificate-link:hover {
      background: #00d4ff;
      color: #000;
      transform: translateY(-2px);
    }

    /* Contact Section Enhancements */
    form {
      max-width: 500px;
      margin: auto;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    form input,
    form textarea {
      padding: 12px;
      font-size: 1rem;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    form button {
      background: #00d4ff;
      padding: 12px;
      border: none;
      border-radius: 8px;
      color: white;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }

    form button:hover {
      background: #00d4ff;
    }

    .contact-content {
      max-width: 600px;
      margin: 0 auto;
    }

    .contact-info {
      display: grid;
      gap: 30px;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 20px;
      padding: 25px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 15px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      transition: transform 0.3s ease;
    }

    .contact-item:hover {
      transform: translateX(10px);
    }

    .contact-icon {
      font-size: 2em;
      width: 60px;
      text-align: center;
    }

    .contact-details h4 {
      color: #00ff88;
      margin-bottom: 5px;
      font-size: 1.1em;
    }

    .contact-details p {
      margin: 0;
      color: rgba(255, 255, 255, 0.9);
    }

    .contact-details a {
      color: #00d4ff;
      text-decoration: none;
    }

    .contact-details a:hover {
      color: #00ff88;
    }

    @keyframes slideInLeft {
      from {
        opacity: 0;
        transform: translateX(-50px);
      }

      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    h2 {
      border-bottom: 2px solid #00ff88;
      padding-bottom: 10px;
      margin-bottom: 20px;
      color: #00ff88;
      position: relative;
    }

    h2::after {
      content: '';
      position: absolute;
      bottom: -2px;
      left: 0;
      width: 0;
      height: 2px;
      background: linear-gradient(90deg, #00ff88, #00d4ff);
      animation: expandWidth 2s ease-out 0.5s forwards;
    }

    @keyframes expandWidth {
      to {
        width: 100%;
      }
    }

    .projects ul {
      list-style: none;
      padding: 0;
    }

    .projects li {
      background: rgba(255, 255, 255, 0.1);
      margin: 15px 0;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
      border: 1px solid rgba(255, 255, 255, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .projects li:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
    }

    .projects a {
      color: #00d4ff;
      text-decoration: none;
    }

    footer {
      text-align: center;
      padding: 30px;
      background: rgba(0, 0, 0, 0.2);
      margin-top: 60px;
      color: white;
      backdrop-filter: blur(10px);
    }

    /* Python Code Animation */
    .python-animation {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: -1;
      overflow: hidden;
    }

    /* Programming Language Icons */
    .lang-icon {
      position: absolute;
      width: 50px;
      height: 50px;
      border-radius: 8px;
      animation: langFloat 20s linear infinite;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 16px;
      color: white;
    }

    .lang-icon.html {
      background: linear-gradient(45deg, #e34f26, #f06529);
    }

    .lang-icon.css {
      background: linear-gradient(45deg, #1572b6, #33a9dc);
    }

    .lang-icon.js {
      background: linear-gradient(45deg, #f7df1e, #ffda44);
      color: #000;
    }

    .lang-icon.python {
      background: linear-gradient(45deg, #3776ab, #ffd343);
    }

    .lang-icon.sql {
      background: linear-gradient(45deg, #00758f, #336791);
    }

    .lang-icon.git {
      background: linear-gradient(45deg, #f05032, #f14e32);
    }

    @keyframes langFloat {
      0% {
        transform: translateX(-80px) translateY(0) rotate(0deg);
        opacity: 0;
      }

      10% {
        opacity: 1;
      }

      90% {
        opacity: 1;
      }

      100% {
        transform: translateX(100vw) translateY(-80px) rotate(360deg);
        opacity: 0;
      }
    }

    /* Data Science Icons */
    .data-icon {
      position: absolute;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      animation: dataIconFloat 25s linear infinite;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
    }

    .data-icon.chart {
      background: linear-gradient(45deg, #ff6b6b, #ee5a52);
    }

    .data-icon.brain {
      background: linear-gradient(45deg, #4ecdc4, #44a08d);
    }

    .data-icon.database {
      background: linear-gradient(45deg, #45b7d1, #96c93d);
    }

    .data-icon.graph {
      background: linear-gradient(45deg, #f093fb, #f5576c);
    }

    @keyframes dataIconFloat {
      0% {
        transform: translateX(-100px) translateY(0) scale(0.5);
        opacity: 0;
      }

      15% {
        opacity: 1;
        transform: scale(1);
      }

      85% {
        opacity: 1;
      }

      100% {
        transform: translateX(100vw) translateY(-60px) scale(0.5);
        opacity: 0;
      }
    }

    /* Project Icons */
    .project-icon {
      position: absolute;
      width: 45px;
      height: 45px;
      border-radius: 10px;
      animation: projectFloat 18s linear infinite;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 14px;
      color: white;
      font-weight: bold;
    }

    .project-icon.web {
      background: linear-gradient(45deg, #667eea, #764ba2);
    }

    .project-icon.mobile {
      background: linear-gradient(45deg, #f093fb, #f5576c);
    }

    .project-icon.ai {
      background: linear-gradient(45deg, #4facfe, #00f2fe);
    }

    .project-icon.data {
      background: linear-gradient(45deg, #43e97b, #38f9d7);
    }

    @keyframes projectFloat {
      0% {
        transform: translateX(-70px) translateY(0) rotate(-10deg);
        opacity: 0;
      }

      12% {
        opacity: 1;
      }

      88% {
        opacity: 1;
      }

      100% {
        transform: translateX(100vw) translateY(-50px) rotate(350deg);
        opacity: 0;
      }
    }

    /* Computer and Tech Icons */
    .tech-icon {
      position: absolute;
      width: 55px;
      height: 55px;
      border-radius: 12px;
      animation: techFloat 22s linear infinite;
      box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 18px;
      color: white;
      font-weight: bold;
    }

    .tech-icon.computer {
      background: linear-gradient(45deg, #2c3e50, #34495e);
    }

    .tech-icon.laptop {
      background: linear-gradient(45deg, #8e44ad, #9b59b6);
    }

    .tech-icon.server {
      background: linear-gradient(45deg, #27ae60, #2ecc71);
    }

    .tech-icon.code {
      background: linear-gradient(45deg, #e74c3c, #c0392b);
    }

    .tech-icon.network {
      background: linear-gradient(45deg, #3498db, #2980b9);
    }

    @keyframes techFloat {
      0% {
        transform: translateX(-75px) translateY(0) rotate(0deg) scale(0.8);
        opacity: 0;
      }

      15% {
        opacity: 1;
        transform: scale(1);
      }

      85% {
        opacity: 1;
      }

      100% {
        transform: translateX(100vw) translateY(-70px) rotate(360deg) scale(0.8);
        opacity: 0;
      }
    }

    .code-snippet {
      position: absolute;
      background: rgba(0, 255, 136, 0.1);
      color: #00ff88;
      font-family: 'Courier New', monospace;
      font-size: 14px;
      padding: 15px;
      border-radius: 8px;
      border-left: 4px solid #00ff88;
      white-space: nowrap;
      animation: floatCode 20s linear infinite;
      box-shadow: 0 4px 15px rgba(0, 255, 136, 0.2);
    }

    .python-logo {
      position: absolute;
      width: 40px;
      height: 40px;
      background: linear-gradient(45deg, #3776ab, #ffd343);
      border-radius: 50%;
      animation: pythonFloat 25s linear infinite;
      box-shadow: 0 4px 15px rgba(55, 118, 171, 0.3);
    }

    @keyframes floatCode {
      0% {
        transform: translateX(-100%) translateY(0) rotate(0deg);
        opacity: 0;
      }

      10% {
        opacity: 1;
      }

      90% {
        opacity: 1;
      }

      100% {
        transform: translateX(100vw) translateY(-100px) rotate(360deg);
        opacity: 0;
      }
    }

    @keyframes pythonFloat {
      0% {
        transform: translateX(-60px) translateY(0) scale(0.5);
        opacity: 0;
      }

      10% {
        opacity: 1;
        transform: scale(1);
      }

      90% {
        opacity: 1;
      }

      100% {
        transform: translateX(100vw) translateY(-50px) scale(0.5);
        opacity: 0;
      }
    }

    .typing-animation {
      background: rgba(0, 0, 0, 0.6);
      color: #00ff88;
      font-family: 'Courier New', monospace;
      padding: 25px;
      border-radius: 15px;
      margin: 30px 0;
      position: relative;
      overflow: hidden;
      border: 1px solid rgba(0, 255, 136, 0.3);
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
    }

    .typing-text {
      overflow: hidden;
      border-right: 0.15em solid #00ff88;
      white-space: nowrap;
      margin: 0 auto;
      font-size: 1.2em;
      animation: typing 4s steps(40, end) infinite, blink-caret 0.75s step-end infinite;
    }

    @keyframes typing {
      0% {
        width: 0;
      }

      50% {
        width: 100%;
      }

      100% {
        width: 0;
      }
    }

    @keyframes blink-caret {

      from,
      to {
        border-color: transparent;
      }

      50% {
        border-color: #00ff88;
      }
    }

    .data-flow {
      position: absolute;
      width: 6px;
      height: 30px;
      background: linear-gradient(to bottom, #00d4ff, #00ff88);
      border-radius: 3px;
      animation: dataMove 10s linear infinite;
      box-shadow: 0 0 10px rgba(0, 212, 255, 0.5);
    }

    @keyframes dataMove {
      0% {
        transform: translateY(-100vh);
        opacity: 0;
      }

      10% {
        opacity: 1;
      }

      90% {
        opacity: 1;
      }

      100% {
        transform: translateY(100vh);
        opacity: 0;
      }
    }

    /* Matrix Effect */
    .matrix-effect {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: -1;
    }

    .matrix-char {
      position: absolute;
      color: rgba(0, 255, 136, 0.5);
      font-family: 'Courier New', monospace;
      font-size: 18px;
      animation: matrixRain 8s linear infinite;
    }

    @keyframes matrixRain {
      0% {
        transform: translateY(-100vh);
        opacity: 1;
      }

      100% {
        transform: translateY(100vh);
        opacity: 0;
      }
    }

    /* Skill bars animation */
    .skill-bar {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 10px;
      padding: 10px;
      margin: 10px 0;
      position: relative;
      overflow: hidden;
    }

    .skill-progress {
      height: 8px;
      background: linear-gradient(90deg, #00ff88, #00d4ff);
      border-radius: 4px;
      width: 0;
      animation: fillProgress 2s ease-out 1s forwards;
    }

    @keyframes fillProgress {
      to {
        width: var(--progress-width);
      }
    }

    /* Responsive Design */
    @media (max-width: 768px) {
      .nav-menu {
        position: fixed;
        left: -100%;
        top: 70px;
        flex-direction: column;
        background: rgba(0, 0, 0, 0.95);
        width: 100%;
        text-align: center;
        transition: 0.3s;
        box-shadow: 0 10px 27px rgba(0, 0, 0, 0.05);
        backdrop-filter: blur(15px);
      }

      .nav-menu.active {
        left: 0;
      }

      .nav-menu li {
        margin: 20px 0;
      }

      .hamburger {
        display: flex;
      }

      .hamburger.active .bar:nth-child(2) {
        opacity: 0;
      }

      .hamburger.active .bar:nth-child(1) {
        transform: translateY(8px) rotate(45deg);
      }

      .hamburger.active .bar:nth-child(3) {
        transform: translateY(-8px) rotate(-45deg);
      }




      header {
        padding: 100px 20px 40px;
      }

      header h1 {
        font-size: 2.5em;
      }

      .hero-subtitle {
        font-size: 1.2em;
      }

      .cta-buttons {
        flex-direction: column;
        align-items: center;
      }

      .btn {
        width: 200px;
      }

      section {
        margin: 30px 10px;
        padding: 30px 20px;
      }

      .typing-text {
        font-size: 1em;
      }

      .stats-container {
        grid-template-columns: 1fr;
      }

      .skills-grid {
        grid-template-columns: 1fr;
      }

      .projects-grid {
        grid-template-columns: 1fr;
      }

      .project-tech {
        justify-content: center;
      }

      .project-links {
        flex-direction: column;
        align-items: center;
      }

      .certificates-grid {
        grid-template-columns: 2fr;
      }

      .certificate-details {
        flex-direction: column;
        gap: 10px;
        text-align: center;

      }

      .contact-item {
        flex-direction: column;
        text-align: center;
      }
    }
  </style>
</head>

<body>

  <!-- Enhanced Animated Background -->
  <div class="animated-background"></div>

  <!-- Particle System -->
  <div class="particles" id="particles"></div>

  <!-- Matrix Effect -->
  <div class="matrix-effect" id="matrixEffect"></div>

  <!-- Python Programming Animation Background -->
  <div class="python-animation" id="pythonAnimation"></div>


  <!-- Enhanced Navigation Bar -->
  <nav class="navbar">
    <div class="nav-container">
      <div class="nav-logo">
        <span class="logo-text">SP</span>
      </div>
      <ul class="nav-menu">
        <li><a href="#home" class="nav-link">Home</a></li>
        <li><a href="#about" class="nav-link">About</a></li>
        <li><a href="#skills" class="nav-link">Skills</a></li>
        <li><a href="#projects" class="nav-link">Projects</a></li>
        <li><a href="#certificates" class="nav-link">Certificates</a></li>
        <li><a href="#contact" class="nav-link">Contact</a></li>
      </ul>
      <div class="hamburger">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
    </div>
  </nav>

  <header id="home">
    <div class="hero-content">
      <div class="hero-text">
        <h1>Shahad Pathan</h1>
        <h2 class="hero-subtitle">Frontend Developer | Data Scientist | Computer Engineering Student</h2>
        <p class="hero-description">Passionate about creating innovative solutions with Python, machine learning, and
          modern web technologies.</p>


        <!-- Call to Action Buttons -->
        <div class="cta-buttons">
          <a href="#projects" class="btn btn-primary">View Projects</a>
          <a href="#contact" class="btn btn-secondary">Get In Touch</a>
        </div>
      </div>

      <!-- Enhanced Typing Animation -->
      <div class="typing-animation">
        <div class="typing-text" id="typingText">print("Welcome to my advanced portfolio!")</div>
      </div>
    </div>
  </header>

  <section id="about" class="about">
    <div class="section-header">
      <h2>About Me</h2>
      <div class="section-subtitle">Get to know me better</div>
    </div>
    <div class="about-content">
      <div class="about-text">
        <p>I am Shahad Pathan, currently studying Computer Engineering at GTU-SET. I have a strong foundation in Python,
          HTML, and CSS, with a passion for creating innovative solutions.</p>
        <p>My goal is to become a successful Data Scientist with expertise in machine learning and web development. I
          enjoy solving complex problems and turning data into meaningful insights.</p>
        <div class="stats-container">
          <div class="stat-item">
            <h3>5+</h3>
            <p>Programming Languages</p>
          </div>
          <div class="stat-item">
            <h3>10+</h3>
            <p>Projects Completed</p>
          </div>
          <div class="stat-item">
            <h3>1</h3>
            <p>Hackathon Experience</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="skills" class="skills">
    <div class="section-header">
      <h2>Skills & Tools</h2>
      <div class="section-subtitle">Technologies I work with</div>
    </div>
    <div class="skills-grid">
      <div class="skill-category">
        <h3>Programming Languages</h3>
        <div class="skill-bar">
          <span>Python</span>
          <div class="skill-progress" style="--progress-width: 80%;"></div>
        </div>
        <div class="skill-bar">
          <span>SQL</span>
          <div class="skill-progress" style="--progress-width: 70%;"></div>
        </div>
        <div class="skill-bar">
          <span>HTML/CSS</span>
          <div class="skill-progress" style="--progress-width: 85%;"></div>
        </div>
        <div class="skill-bar">
          <span>JavaScript</span>
          <div class="skill-progress" style="--progress-width: 50%;"></div>
        </div>
      </div>
      <div class="skill-category">
        <h3>Data Science & Tools</h3>
        <div class="skill-bar">
          <span>Data Science</span>
          <div class="skill-progress" style="--progress-width: 75%;"></div>
        </div>
        <div class="skill-bar">
          <span>Machine Learning</span>
          <div class="skill-progress" style="--progress-width: 70%;"></div>
        </div>
        <div class="skill-bar">
          <span>Power BI</span>
          <div class="skill-progress" style="--progress-width: 80%;"></div>
        </div>
        <div class="skill-bar">
          <span>Git/GitHub</span>
          <div class="skill-progress" style="--progress-width: 75%;"></div>
        </div>
      </div>
    </div>
    <div class="tech-stack">
      <h3>Technology Stack</h3>
      <p>Pandas, BigQuery, Power BI, Tableau, Git, Cloud (AWS/GCP), Flask, NumPy, Matplotlib</p>
    </div>
  </section>

  <section id="projects" class="projects">
    <div class="section-header">
      <h2>Featured Projects</h2>
      <div class="section-subtitle">Hackathon & Personal Projects</div>
    </div>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-icon-display">💻</div>
        <h3>Portfolio Website</h3>
        <p>Responsive portfolio website with advanced animations, modern design, and interactive Python code
          visualizations.</p>
        <div class="project-tech">
          <span class="tech-tag">HTML</span>
          <span class="tech-tag">CSS</span>
          <span class="tech-tag">JavaScript</span>
        </div>
        <div class="project-links">
          <a href="https://shahadpathan.github.io/" class="project-link">Live Demo</a>
          <a href="https://github.com/SHAHADPATHAN/shahadpathan.github.io" class="project-link">GitHub</a>
        </div>
      </div>
      <div class="project-card">
        <div class="project-icon-display">🌐</div>
        <h3>Consultancy Website</h3>
        <p>Interactive and mobile-friendly consultancy platform for MBBS aspirants — built to highlight affordable
          global education options, NMC-approved universities, and personalized guidance.</p>
        <div class="project-tech">
          <span class="tech-tag">HTML</span>
          <span class="tech-tag">CSS</span>
          <span class="tech-tag">JavaScript</span>
        </div>
        <div class="project-links">
          <a href="https://hirconsultancy.github.io/" class="project-link">Live Demo</a>
          <a href="https://github.com/Hirconsultancy/hirconsultancy.github.io" class="project-link">GitHub</a>
        </div>
      </div>
    </div>
  </section>

  <section id="certificates" class="certificates">
    <div class="section-header">
      <h2>Certificates & Achievements</h2>
      <div class="section-subtitle">My professional certifications and accomplishments</div>
    </div>
    <div class="certificates-grid">
      <div class="certificate-card">
        <div class="certificate-icon">📱</div>
        <h3>Flutter Development</h3>
        <p>Successfully completed the Flutter Webinar Series: Build, Innovate, Launch! Demonstrated commitment to
          learning, innovation, and advancing skills in Flutter development.</p>
        <div class="certificate-details">
          <span class="cert-issuer">IEEE MMU CS & Ultron Technologies</span>
          <span class="cert-date">December 2024</span>
        </div>
        <a href="1 (24).PNG" target="_blank" class="certificate-link">View Certificate</a>
      </div>
      <div class="certificate-card">
        <div class="certificate-icon">⚡</div>
        <h3>JavaScript Mastery</h3>
        <p>Successfully completed the Mastering JS session under GDG SUI Tech Winter Break. Covered essential concepts
          and practical applications of JavaScript, modern frameworks, and effective coding practices.</p>
        <div class="certificate-details">
          <span class="cert-issuer">Google Developer Groups - SAGE University</span>
          <span class="cert-date">December 2024</span>
        </div>
        <a href="Blue and Gold Simple Certificate_20241216_195012_0000.png" target="_blank"
          class="certificate-link">View Certificate</a>
      </div>
      <div class="certificate-card">
        <div class="certificate-icon">🚀</div>
        <h3>Agnirva Space Internship Program</h3>
        <p>Successfully completed The Agnirva Space Internship Program, demonstrating commitment to space technology and
          innovation. Gained valuable experience in space-related projects and technologies.</p>
        <div class="certificate-details">
          <span class="cert-issuer">Agnirva</span>
          <span class="cert-date">January 2025</span>
        </div>
        <a href="THE AGNIRVA SPACE INTERNSHIP PROGRAM_page-0001.jpg" target="_blank" class="certificate-link">View
          Certificate</a>
      </div>
      <div class="certificate-card">
        <div class="certificate-icon">🐍</div>
        <h3>Python Assessment</h3>
        <p>Successfully completed Python Assessment from LearnTube by CareerNinja. Demonstrated proficiency in Python
          programming concepts, data structures, and problem-solving skills.</p>
        <div class="certificate-details">
          <span class="cert-issuer">LearnTube by CareerNinja</span>
          <span class="cert-date">September 2024</span>
        </div>
        <a href="Python_Certificate (1)_page-0001.jpg" target="_blank" class="certificate-link">View Certificate</a>
      </div>
      <div class="certificate-card">
        <div class="certificate-icon">📱</div>
        <h3>Flutter Workshop Participation</h3>
        <p>Participated in Flutter Workshop organized by Google Developer Groups On Campus R.V.R&J.C. Gained hands-on
          experience with Flutter for mobile application development and design.</p>
        <div class="certificate-details">
          <span class="cert-issuer">Google Developer Groups RVR&JC CE</span>
          <span class="cert-date">December 2024</span>
        </div>
        <a href="Pathan Shahad (2).pdf" target="_blank" class="certificate-link">View Certificate</a>
      </div>
      <div class="certificate-card">
        <div class="certificate-icon">🚧</div>
        <h3>National Road Safety Hackathon 2025</h3>
        <p>Participated in the National Road Safety Hackathon 2025 jointly organized by NHAI and HOAI. Contributed
          innovative solutions to enhance road safety using technology.</p>
        <div class="certificate-details">
          <span class="cert-issuer">Ministry of Road Transport & Highways | NHAI & HOAI</span>
          <span class="cert-date">June 2025</span>
        </div>
        <a href="hacathoncertificate.jpg" target="_blank" class="certificate-link">View Certificate</a>
      </div>
    </div>
  </section>

  <section id="contact" class="contact">
    <h2>Contact Us</h2>
    <form action="https://formspree.io/f/xovwgzev" method="POST">
      <input type="text" name="name" placeholder="Full Name" required>
      <input type="email" name="email" placeholder="Email" required>
      <textarea name="message" placeholder="Your Message" rows="4" required></textarea>
      <button type="submit">Submit</button>

    </form>
    <div class="section-header">
      <h2>Get In Touch</h2>
      <div class="section-subtitle">Let's connect and collaborate</div>
    </div>
    <div class="contact-content">
      <div class="contact-info">
        <div class="contact-item">
          <div class="contact-icon">📧</div>
          <div class="contact-details">
            <h4>Email</h4>
            <p><a href="mailto:241370107053@gtu.edu.in">241370107053@gtu.edu.in</a></p>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">📱</div>
          <div class="contact-details">
            <h4>Mobile</h4>
            <p><a href="tel:+919913031752">+91 9913031752</a></p>
          </div>
        </div>
        <div class="contact-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="#0077B5" viewBox="0 0 16 16">
            <path d="M0 1.146C0 .513.526 0 1.175 0h13.65C15.474 
  0 16 .513 16 1.146v13.708c0 .633-.526 1.146-1.175 
  1.146H1.175C.526 16 0 15.487 0 
  14.854V1.146zm4.943 12.248V6.169H2.542v7.225h2.401zm-1.2-8.212c.837 
  0 1.358-.554 1.358-1.248-.015-.709-.521-1.248-1.342-1.248-.821 
  0-1.358.54-1.358 1.248 0 .694.52 1.248 1.327 
  1.248h.015zm4.908 8.212V9.359c0-.214.016-.428.079-.582.173-.428.568-.872 
  1.232-.872.869 0 1.216.658 1.216 1.623v3.866h2.401V9.25c0-2.22-1.183-3.251-2.76-3.251-1.274 
  0-1.845.7-2.165 1.192v.025h-.015a5.56 5.56 0 0 1 
  .015-.025V6.169h-2.4c.03.7 0 7.225 0 7.225h2.4z" />
          </svg>

          <div class="contact-details">
            <h4>LinkedIn</h4>
            <p><a
                href="https://www.linkedin.com/in/shahad-pathan-a909972ba?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app"
                target="_blank">linkedin.com/in/shahad-pathan</a></p>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="#181717" viewBox="0 0 16 16">
              <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 
      6.53 5.47 7.59.4.07.55-.17.55-.38 
      0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52
      -.01-.53.63-.01 1.08.58 1.23.82.72 
      1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2
      -3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2
      -.36-1.01.08-2.11 0 0 .67-.21 2.2.82.64-.18 1.32-.27 
      2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 
      2.2-.82.44 1.1.16 1.91.08 2.11.51.56.82 
      1.27.82 2.15 0 3.07-1.87 3.75-3.65 
      3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 
      2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 
      8c0-4.42-3.58-8-8-8z" />
            </svg>
          </div>

          <div class="contact-details">
            <h4>GitHub</h4>
            <p><a href="https://github.com/SHAHADPATHAN" target="_blank"
                style="color: #00d4ff; text-decoration: none;">github.com/SHAHADPATHAN</a></p>
          </div>
        </div>
        <div class="contact-item">
          <div class="contact-icon">📍</div>
          <div class="contact-details">
            <h4>Location</h4>
            <p><a href="https://www.google.com/maps/search/Mehsana,+Gujarat,+India" target="_blank"
                style="color: #00d4ff; text-decoration: none;">Mehsana, Gujarat, India</a></p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 Shahad Pathan. All rights reserved.</p>
  </footer>

  <script>
    // Enhanced Python Code Animation
    function createCodeSnippet() {
      const snippets = [
        'def analyze_data(): return insights',
        'import pandas as pd',
        'model = train_ml_model(data)',
        'for i in range(len(dataset)):',
        'if accuracy > 0.95: deploy_model()',
        'class DataScientist: def __init__(self):',
        'result = process_big_data()',
        'print("Machine Learning Success!")',
        'df = pd.read_csv("data.csv")',
        'neural_network.fit(X_train, y_train)'
      ];

      const snippet = document.createElement('div');
      snippet.className = 'code-snippet';
      snippet.textContent = snippets[Math.floor(Math.random() * snippets.length)];
      snippet.style.top = Math.random() * 100 + 'vh';
      snippet.style.left = '-300px';
      snippet.style.animationDelay = Math.random() * 5 + 's';

      document.getElementById('pythonAnimation').appendChild(snippet);

      setTimeout(() => snippet.remove(), 20000);
    }

    // Create Python logos
    function createPythonLogo() {
      const logo = document.createElement('div');
      logo.className = 'python-logo';
      logo.style.top = Math.random() * 100 + 'vh';
      logo.style.left = '-50px';
      logo.style.animationDelay = Math.random() * 8 + 's';

      document.getElementById('pythonAnimation').appendChild(logo);

      setTimeout(() => logo.remove(), 25000);
    }

    // Create programming language icons
    function createLangIcon() {
      const languages = [
        { type: 'html', text: 'HTML' },
        { type: 'css', text: 'CSS' },
        { type: 'js', text: 'JS' },
        { type: 'python', text: 'PY' },
        { type: 'sql', text: 'SQL' },
        { type: 'git', text: 'GIT' }
      ];

      const lang = languages[Math.floor(Math.random() * languages.length)];
      const icon = document.createElement('div');
      icon.className = `lang-icon ${lang.type}`;
      icon.textContent = lang.text;
      icon.style.top = Math.random() * 100 + 'vh';
      icon.style.left = '-60px';
      icon.style.animationDelay = Math.random() * 5 + 's';

      document.getElementById('pythonAnimation').appendChild(icon);

      setTimeout(() => icon.remove(), 20000);
    }

    // Create data science icons
    function createDataIcon() {
      const dataTypes = [
        { type: 'chart', symbol: '📊' },
        { type: 'brain', symbol: '🧠' },
        { type: 'database', symbol: '🗄️' },
        { type: 'graph', symbol: '📈' }
      ];

      const data = dataTypes[Math.floor(Math.random() * dataTypes.length)];
      const icon = document.createElement('div');
      icon.className = `data-icon ${data.type}`;
      icon.textContent = data.symbol;
      icon.style.top = Math.random() * 100 + 'vh';
      icon.style.left = '-80px';
      icon.style.animationDelay = Math.random() * 6 + 's';

      document.getElementById('pythonAnimation').appendChild(icon);

      setTimeout(() => icon.remove(), 25000);
    }

    // Create project icons
    function createProjectIcon() {
      const projects = [
        { type: 'web', text: 'WEB' },
        { type: 'mobile', text: 'APP' },
        { type: 'ai', text: 'AI' },
        { type: 'data', text: 'DATA' }
      ];

      const project = projects[Math.floor(Math.random() * projects.length)];
      const icon = document.createElement('div');
      icon.className = `project-icon ${project.type}`;
      icon.textContent = project.text;
      icon.style.top = Math.random() * 100 + 'vh';
      icon.style.left = '-55px';
      icon.style.animationDelay = Math.random() * 4 + 's';

      document.getElementById('pythonAnimation').appendChild(icon);

      setTimeout(() => icon.remove(), 18000);
    }

    // Create computer and tech icons
    function createTechIcon() {
      const techItems = [
        { type: 'computer', symbol: '💻' },
        { type: 'laptop', symbol: '🖥️' },
        { type: 'server', symbol: '🖧' },
        { type: 'code', symbol: '⚙️' },
        { type: 'network', symbol: '🌐' }
      ];

      const tech = techItems[Math.floor(Math.random() * techItems.length)];
      const icon = document.createElement('div');
      icon.className = `tech-icon ${tech.type}`;
      icon.textContent = tech.symbol;
      icon.style.top = Math.random() * 100 + 'vh';
      icon.style.left = '-65px';
      icon.style.animationDelay = Math.random() * 5 + 's';

      document.getElementById('pythonAnimation').appendChild(icon);

      setTimeout(() => icon.remove(), 22000);
    }

    // Create data flow
    function createDataFlow() {
      const flow = document.createElement('div');
      flow.className = 'data-flow';
      flow.style.left = Math.random() * 100 + 'vw';
      flow.style.animationDelay = Math.random() * 3 + 's';

      document.getElementById('pythonAnimation').appendChild(flow);

      setTimeout(() => flow.remove(), 10000);
    }

    // Create particles
    function createParticles() {
      const particlesContainer = document.getElementById('particles');

      for (let i = 0; i < 50; i++) {
        const particle = document.createElement('div');
        particle.className = 'particle';
        particle.style.left = Math.random() * 100 + 'vw';
        particle.style.top = Math.random() * 100 + 'vh';
        particle.style.width = particle.style.height = (Math.random() * 5 + 2) + 'px';
        particle.style.animationDelay = Math.random() * 6 + 's';
        particle.style.animationDuration = (Math.random() * 3 + 3) + 's';

        particlesContainer.appendChild(particle);
      }
    }

    // Create matrix effect
    function createMatrixEffect() {
      const matrixContainer = document.getElementById('matrixEffect');
      const chars = '01';

      for (let i = 0; i < 20; i++) {
        const char = document.createElement('div');
        char.className = 'matrix-char';
        char.textContent = chars[Math.floor(Math.random() * chars.length)];
        char.style.left = Math.random() * 100 + 'vw';
        char.style.animationDelay = Math.random() * 8 + 's';

        matrixContainer.appendChild(char);

        setTimeout(() => char.remove(), 8000);
      }
    }

    // Enhanced typing animation
    function updateTypingText() {
      const texts = [
        'print("Welcome to my advanced portfolio!")',
        'def create_amazing_projects():',
        'import success, innovation',
        'while learning: improve_skills()',
        'class DataScientist(Professional):',
        'result = analyze_big_data()',
        'if dream == True: make_it_reality()'
      ];

      let currentIndex = 0;
      const typingElement = document.getElementById('typingText');

      setInterval(() => {
        typingElement.textContent = texts[currentIndex];
        currentIndex = (currentIndex + 1) % texts.length;
      }, 4000);
    }

    // Mobile Navigation
    function initMobileNav() {
      const hamburger = document.querySelector('.hamburger');
      const navMenu = document.querySelector('.nav-menu');
      const navLinks = document.querySelectorAll('.nav-link');

      hamburger.addEventListener('click', () => {
        hamburger.classList.toggle('active');
        navMenu.classList.toggle('active');
      });

      navLinks.forEach(link => {
        link.addEventListener('click', () => {
          hamburger.classList.remove('active');
          navMenu.classList.remove('active');
        });
      });
    }

    // Smooth Scrolling
    function initSmoothScroll() {
      const links = document.querySelectorAll('a[href^="#"]');

      links.forEach(link => {
        link.addEventListener('click', (e) => {
          e.preventDefault();
          const targetId = link.getAttribute('href');
          const targetSection = document.querySelector(targetId);

          if (targetSection) {
            const offsetTop = targetSection.offsetTop - 70;
            window.scrollTo({
              top: offsetTop,
              behavior: 'smooth'
            });
          }
        });
      });
    }

    // Navbar Scroll Effect
    function initNavbarScroll() {
      const navbar = document.querySelector('.navbar');

      window.addEventListener('scroll', () => {
        if (window.scrollY > 50) {
          navbar.style.background = 'rgba(0, 0, 0, 0.95)';
        } else {
          navbar.style.background = 'rgba(0, 0, 0, 0.9)';
        }
      });
    }

    // Initialize all animations and functionality
    document.addEventListener('DOMContentLoaded', function () {
      createParticles();
      updateTypingText();
      initMobileNav();
      initSmoothScroll();
      initNavbarScroll();

      // Start creating animations
      setInterval(createCodeSnippet, 2000);
      setInterval(createPythonLogo, 4000);
      setInterval(createDataFlow, 1500);
      setInterval(createMatrixEffect, 3000);
      setInterval(createLangIcon, 2500);
      setInterval(createDataIcon, 3500);
      setInterval(createProjectIcon, 3000);
      setInterval(createTechIcon, 2800);
    });
  </script>

</body>

</html>
