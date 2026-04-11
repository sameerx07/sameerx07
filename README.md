<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Muhammad Sameer | AI Engineer & Full Stack Architect</title>
  <!-- Google Fonts + Preconnect -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <!-- Font Awesome 6 (Free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #05070a;
      font-family: 'Inter', sans-serif;
      color: #eef2ff;
      line-height: 1.5;
      scroll-behavior: smooth;
      overflow-x: hidden;
    }

    /* animated gradient background */
    .bg-aura {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -2;
      background: radial-gradient(circle at 20% 30%, rgba(10, 25, 47, 0.9), #010101);
    }

    .bg-aura::before {
      content: '';
      position: absolute;
      width: 200%;
      height: 200%;
      top: -50%;
      left: -50%;
      background: radial-gradient(circle, rgba(0, 255, 255, 0.08) 0%, rgba(128, 0, 255, 0.03) 70%);
      animation: slowShift 24s infinite alternate;
      z-index: -1;
    }

    @keyframes slowShift {
      0% { transform: translate(0%, 0%) rotate(0deg); opacity: 0.4; }
      100% { transform: translate(5%, 3%) rotate(2deg); opacity: 0.8; }
    }

    /* modern glassmorphic container */
    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 2rem 1.5rem 4rem;
      position: relative;
    }

    /* hero section */
    .hero {
      text-align: center;
      margin-bottom: 4rem;
      animation: fadeUp 0.8s cubic-bezier(0.2, 0.9, 0.4, 1.1) forwards;
    }

    .badge-pill {
      display: inline-block;
      background: rgba(0, 255, 255, 0.12);
      backdrop-filter: blur(6px);
      border: 1px solid rgba(0, 255, 255, 0.25);
      padding: 0.3rem 1rem;
      border-radius: 60px;
      font-size: 0.75rem;
      font-weight: 500;
      letter-spacing: 0.3px;
      color: #9effff;
      margin-bottom: 1.2rem;
    }

    .glow-text {
      font-size: 3.8rem;
      font-weight: 800;
      background: linear-gradient(135deg, #FFFFFF 20%, #a0f0ff 50%, #b77eff 80%);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      letter-spacing: -0.02em;
      line-height: 1.2;
      margin-bottom: 0.5rem;
    }

    .subhead {
      font-size: 1.1rem;
      color: #a8b3cf;
      font-weight: 450;
      border-bottom: 1px dashed rgba(100, 150, 255, 0.3);
      display: inline-block;
      padding-bottom: 6px;
    }

    .bio-text {
      max-width: 680px;
      margin: 1.5rem auto 0;
      color: #b9c3e6;
      font-weight: 400;
      font-size: 1rem;
      background: rgba(15, 25, 45, 0.5);
      backdrop-filter: blur(8px);
      padding: 1rem 1.8rem;
      border-radius: 48px;
      border: 0.5px solid rgba(0, 255, 255, 0.2);
    }

    .social-links {
      margin-top: 2rem;
      display: flex;
      gap: 1.2rem;
      justify-content: center;
      flex-wrap: wrap;
    }

    .social-link {
      background: rgba(20, 30, 55, 0.6);
      backdrop-filter: blur(4px);
      padding: 0.6rem 1.3rem;
      border-radius: 40px;
      font-size: 0.9rem;
      font-weight: 500;
      color: #d6e3ff;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: all 0.25s ease;
      border: 1px solid rgba(0, 255, 255, 0.2);
    }

    .social-link i {
      font-size: 1.1rem;
    }

    .social-link:hover {
      background: rgba(0, 180, 255, 0.2);
      border-color: #0ff;
      color: white;
      transform: translateY(-3px);
      box-shadow: 0 10px 20px -8px rgba(0, 200, 255, 0.3);
    }

    /* cards */
    .section-title {
      font-size: 1.9rem;
      font-weight: 700;
      margin-bottom: 2rem;
      letter-spacing: -0.3px;
      background: linear-gradient(120deg, #f0f5ff, #9bc0ff);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      display: inline-block;
      border-left: 4px solid #0ff;
      padding-left: 1rem;
    }

    .card-modern {
      background: rgba(12, 20, 32, 0.55);
      backdrop-filter: blur(12px);
      border-radius: 2rem;
      border: 1px solid rgba(0, 255, 255, 0.2);
      padding: 1.8rem 2rem;
      margin-bottom: 3rem;
      transition: transform 0.2s ease, box-shadow 0.3s;
      box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
    }

    .card-modern:hover {
      border-color: rgba(0, 230, 250, 0.5);
      box-shadow: 0 20px 40px -12px rgba(0, 200, 255, 0.2);
    }

    /* bar graph container */
    .skill-item, .project-item {
      margin-bottom: 1.7rem;
    }

    .skill-header, .project-header {
      display: flex;
      justify-content: space-between;
      font-weight: 500;
      margin-bottom: 0.5rem;
      font-size: 0.95rem;
    }

    .skill-name i, .project-name i {
      width: 26px;
      color: #0ff;
      margin-right: 8px;
    }

    .bar-container {
      background: #1e2a3e;
      border-radius: 40px;
      height: 12px;
      overflow: hidden;
      box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.4);
    }

    .bar-fill {
      width: 0%;
      height: 100%;
      background: linear-gradient(90deg, #0ff, #b477ff);
      border-radius: 40px;
      transition: width 1.2s cubic-bezier(0.22, 0.97, 0.36, 1.02);
      position: relative;
      box-shadow: 0 0 6px #0ff;
    }

    .percent-value {
      font-family: 'Inter', monospace;
      font-weight: 600;
      background: rgba(0, 255, 255, 0.15);
      padding: 2px 10px;
      border-radius: 40px;
      font-size: 0.8rem;
    }

    /* tech grid */
    .tech-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem;
      justify-content: center;
      margin-top: 1.2rem;
    }

    .tech-badge {
      background: rgba(30, 40, 60, 0.7);
      backdrop-filter: blur(4px);
      padding: 0.6rem 1.2rem;
      border-radius: 50px;
      font-size: 0.85rem;
      font-weight: 500;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      transition: all 0.2s;
      border: 0.5px solid rgba(0, 200, 255, 0.3);
    }

    .tech-badge i {
      font-size: 1.2rem;
    }

    .tech-badge:hover {
      transform: translateY(-4px);
      background: #0a2540;
      border-color: #0ff;
    }

    .quote {
      text-align: center;
      margin-top: 3rem;
      font-size: 1.2rem;
      font-style: italic;
      color: #bdd3ff;
      border-top: 1px solid rgba(0, 255, 255, 0.2);
      padding-top: 2rem;
    }

    .cta-button {
      display: inline-block;
      background: linear-gradient(95deg, #0ff, #8a6eff);
      padding: 0.8rem 2rem;
      border-radius: 50px;
      font-weight: 700;
      text-decoration: none;
      color: #050a12;
      margin-top: 1rem;
      transition: all 0.25s;
      box-shadow: 0 5px 15px rgba(0, 255, 255, 0.2);
    }

    .cta-button:hover {
      transform: scale(1.02);
      box-shadow: 0 10px 25px rgba(0, 200, 255, 0.4);
    }

    @keyframes fadeUp {
      0% { opacity: 0; transform: translateY(18px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    /* responsive */
    @media (max-width: 760px) {
      .glow-text { font-size: 2.5rem; }
      .container { padding: 1.5rem 1rem 3rem; }
      .card-modern { padding: 1.5rem; }
      .section-title { font-size: 1.6rem; }
    }

    footer {
      text-align: center;
      font-size: 0.75rem;
      color: #5d7199;
      margin-top: 3rem;
    }
  </style>
</head>
<body>
<div class="bg-aura"></div>
<div class="container">
  <!-- Hero -->
  <div class="hero">
    <div class="badge-pill">
      <i class="fas fa-code-branch"></i>  REMOTE · 2+ YEARS
    </div>
    <div class="glow-text">
      Muhammad Sameer
    </div>
    <div class="subhead">
      <i class="fas fa-microchip"></i> AI Engineer &nbsp;|&nbsp; <i class="fas fa-layer-group"></i> Full Stack Architect
    </div>
    <div class="bio-text">
      Building intelligent production systems — LLM pipelines, RAG agents, and cloud-native full-stack applications. 
      I fuse AI engineering with high-performance frontends & backends.
    </div>
    <div class="social-links">
      <a href="mailto:sameersam.s199@gmail.com" class="social-link"><i class="fas fa-envelope"></i> Gmail</a>
      <a href="https://www.linkedin.com/in/muhammad-sameer-9767921b7/" target="_blank" class="social-link"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
      <a href="https://sameerdev.online/" target="_blank" class="social-link"><i class="fas fa-globe"></i> Portfolio</a>
    </div>
  </div>

  <!-- Core Skills + Bar Graph (Modern) -->
  <div class="card-modern" id="skillsCard">
    <div>
      <h2 class="section-title"><i class="fas fa-chart-line" style="margin-right: 12px;"></i> Core Engineering Radar</h2>
      <p style="margin-bottom: 2rem; color:#b8cbff;">Technical proficiency & real-world expertise — dynamic bar graph</p>
    </div>
    <div id="skillsGraphContainer">
      <!-- dynamic bars injected via JS -->
      <div class="skill-item skeleton-loader" style="height: 60px; background: rgba(255,255,255,0.02); border-radius: 20px;"></div>
    </div>
  </div>

  <!-- Projects with bar graph progress -->
  <div class="card-modern" id="projectsCard">
    <h2 class="section-title"><i class="fas fa-rocket"></i> Flagship Builds & Progress</h2>
    <p style="margin-bottom: 1.8rem; color:#b8cbff;">Live metrics, active development cycles — interactive bar tracking</p>
    <div id="projectsGraphContainer">
      <div class="project-item skeleton-loader" style="height: 60px; background: rgba(255,255,255,0.02); border-radius: 20px;"></div>
    </div>
  </div>

  <!-- Tech Ecosystem - modern icon strip -->
  <div class="card-modern">
    <h2 class="section-title"><i class="fas fa-cubes"></i> Tech Arsenal</h2>
    <div class="tech-grid" id="techStack">
      <!-- JS will populate with icons and labels for cleaner dynamic but also static fallback: will fill with elegant data -->
    </div>
  </div>

  <div class="quote">
    <i class="fas fa-quote-left" style="color: #0ff; margin-right: 8px;"></i> 
    "I architect at the intersection of AI and engineering — intelligent, scalable, and genuinely useful."
    <div style="margin-top: 1.5rem;">
      <a href="mailto:sameersam.s199@gmail.com" class="cta-button"><i class="fas fa-paper-plane"></i>  Let's build the future</a>
    </div>
  </div>
  <footer>
    © 2026 Muhammad Sameer — AI & Full Stack excellence.  Remote worldwide.
  </footer>
</div>

<script>
  // ---- MODERN SKILLS DATA (Bar Graph ready)
  const skillsData = [
    { name: "🤖 AI & ML (LLMs / RAG / Agents)", icon: "fas fa-brain", percent: 92 },
    { name: "⚛️ Frontend (React 18 / Next.js 14)", icon: "fab fa-react", percent: 88 },
    { name: "⚙️ Backend (Node.js / .NET 10 / GraphQL)", icon: "fas fa-server", percent: 90 },
    { name: "📱 Mobile (Flutter / Riverpod)", icon: "fab fa-flutter", percent: 78 },
    { name: "☁️ Cloud & DevOps (Azure / K8s / Docker)", icon: "fas fa-cloud", percent: 82 },
    { name: "🗄️ Databases (PostgreSQL / Pinecone / Redis)", icon: "fas fa-database", percent: 85 }
  ];

  const projectsData = [
    { name: "AI SaaS Platform (LLM orchestration)", icon: "fas fa-glasses", percent: 95, status: "Production" },
    { name: "RAG Search Engine (Vector + Semantic)", icon: "fas fa-search", percent: 75, status: "Open Source" },
    { name: "Realtime Collab Tool (WebRTC + CRDT)", icon: "fas fa-users", percent: 100, status: "Live" },
    { name: "Flutter UI Kit (pub.dev high quality)", icon: "fab fa-flutter", percent: 65, status: "Beta" },
    { name: "ASP.NET Core Boilerplate (SaaS starter)", icon: "fas fa-code", percent: 45, status: "In Progress" }
  ];

  const techStackList = [
    { name: "OpenAI", icon: "fab fa-openai", color: "#00a67e" },
    { name: "LangChain", icon: "fas fa-link", color: "#1C3C3C" },
    { name: "Python", icon: "fab fa-python", color: "#3776AB" },
    { name: "TypeScript", icon: "fab fa-js", color: "#3178C6" },
    { name: "React", icon: "fab fa-react", color: "#61DAFB" },
    { name: "Next.js", icon: "fas fa-code", color: "#fff" },
    { name: "Tailwind", icon: "fas fa-palette", color: "#06B6D4" },
    { name: "Node.js", icon: "fab fa-node", color: "#339933" },
    { name: ".NET", icon: "fab fa-microsoft", color: "#512BD4" },
    { name: "Flutter", icon: "fab fa-flutter", color: "#02569B" },
    { name: "GraphQL", icon: "fas fa-project-diagram", color: "#E10098" },
    { name: "PostgreSQL", icon: "fas fa-database", color: "#4169E1" },
    { name: "MongoDB", icon: "fas fa-leaf", color: "#47A248" },
    { name: "Redis", icon: "fas fa-bolt", color: "#DC382D" },
    { name: "Supabase", icon: "fas fa-fire", color: "#3ECF8E" },
    { name: "Azure", icon: "fab fa-microsoft", color: "#0078D4" },
    { name: "Kubernetes", icon: "fas fa-ship", color: "#326CE5" },
    { name: "Docker", icon: "fab fa-docker", color: "#2496ED" },
    { name: "GitHub Actions", icon: "fab fa-github", color: "#2088FF" }
  ];

  // Helper: render skills with bar graph (ensures animation via intersection observer)
  function renderSkills() {
    const container = document.getElementById('skillsGraphContainer');
    if (!container) return;
    container.innerHTML = '';
    skillsData.forEach(skill => {
      const skillDiv = document.createElement('div');
      skillDiv.classList.add('skill-item');
      skillDiv.setAttribute('data-percent', skill.percent);
      skillDiv.innerHTML = `
        <div class="skill-header">
          <div class="skill-name"><i class="${skill.icon}" style="width: 28px;"></i> ${skill.name}</div>
          <div class="percent-value" id="percent-label-${skill.name.replace(/\s/g, '')}">0%</div>
        </div>
        <div class="bar-container">
          <div class="bar-fill" data-target="${skill.percent}" style="width: 0%;"></div>
        </div>
      `;
      container.appendChild(skillDiv);
    });
  }

  function renderProjects() {
    const container = document.getElementById('projectsGraphContainer');
    if (!container) return;
    container.innerHTML = '';
    projectsData.forEach(proj => {
      const projDiv = document.createElement('div');
      projDiv.classList.add('project-item');
      projDiv.setAttribute('data-percent', proj.percent);
      projDiv.innerHTML = `
        <div class="project-header">
          <div class="project-name"><i class="${proj.icon}"></i> ${proj.name} <span style="font-size:0.7rem; background:#0ff22a20; margin-left:8px; padding:2px 6px; border-radius:20px;">${proj.status}</span></div>
          <div class="percent-value" id="proj-percent-${proj.name.replace(/\s/g, '')}">0%</div>
        </div>
        <div class="bar-container">
          <div class="bar-fill" data-target="${proj.percent}" style="width: 0%;"></div>
        </div>
      `;
      container.appendChild(projDiv);
    });
  }

  function renderTechStack() {
    const techContainer = document.getElementById('techStack');
    if (!techContainer) return;
    techContainer.innerHTML = '';
    techStackList.forEach(tech => {
      const badge = document.createElement('div');
      badge.classList.add('tech-badge');
      // using font awesome fallback for custom
      badge.innerHTML = `<i class="${tech.icon}" style="color: ${tech.color};"></i> ${tech.name}`;
      techContainer.appendChild(badge);
    });
  }

  // Intersection Observer to trigger bar animations & counting numbers
  let animatedSkills = false;
  let animatedProjects = false;

  function animateBars(containerSelector, isSkills = true) {
    const container = document.querySelector(containerSelector);
    if (!container) return;
    const items = container.querySelectorAll('.skill-item, .project-item');
    items.forEach(item => {
      const fillBar = item.querySelector('.bar-fill');
      const targetPercent = fillBar ? parseInt(fillBar.getAttribute('data-target')) : 0;
      const percentLabel = item.querySelector('.percent-value');
      if (fillBar && targetPercent) {
        // animate width
        fillBar.style.width = targetPercent + '%';
        // count-up animation for percentages
        if (percentLabel) {
          let current = 0;
          const step = Math.ceil(targetPercent / 45);
          const interval = setInterval(() => {
            current += step;
            if (current >= targetPercent) {
              current = targetPercent;
              percentLabel.innerText = targetPercent + '%';
              clearInterval(interval);
            } else {
              percentLabel.innerText = current + '%';
            }
          }, 18);
        }
      }
    });
  }

  // Observers for each card to trigger bar graph only once when visible
  const observerOptions = { threshold: 0.2, rootMargin: "0px 0px -40px 0px" };
  const skillsObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting && !animatedSkills) {
        animatedSkills = true;
        animateBars('#skillsCard', true);
        skillsObserver.disconnect();
      }
    });
  }, observerOptions);
  
  const projectsObserver = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting && !animatedProjects) {
        animatedProjects = true;
        animateBars('#projectsCard', false);
        projectsObserver.disconnect();
      }
    });
  }, observerOptions);
  
  // Initialize everything, render content, then attach observers
  function init() {
    renderSkills();
    renderProjects();
    renderTechStack();
    // Ensure that bars start at 0% and numbers at 0
    const skillsCard = document.getElementById('skillsCard');
    const projectsCard = document.getElementById('projectsCard');
    if (skillsCard) skillsObserver.observe(skillsCard);
    if (projectsCard) projectsObserver.observe(projectsCard);
    
    // Fallback: If user loads and already visible (direct load), trigger manually after a slight delay if needed
    setTimeout(() => {
      const skillsRect = skillsCard?.getBoundingClientRect();
      if (skillsRect && skillsRect.top < window.innerHeight - 100 && !animatedSkills) {
        animatedSkills = true;
        animateBars('#skillsCard', true);
        skillsObserver.disconnect();
      }
      const projRect = projectsCard?.getBoundingClientRect();
      if (projRect && projRect.top < window.innerHeight - 100 && !animatedProjects) {
        animatedProjects = true;
        animateBars('#projectsCard', false);
        projectsObserver.disconnect();
      }
    }, 300);
  }
  
  // also add window load double-check for extra smoothness
  window.addEventListener('load', () => {
    init();
    // small additional effect: resetting any visible glitch, plus ensure bar numbers
  });
  
  // extra: if the user clicks on anything or we want clean counters, we also enforce that percent labels start 0.
  // Manual: pre-set initial percent values to 0 via small mutation
  document.addEventListener('DOMContentLoaded', () => {
    // for safety, pre-render tech and structure
    if (!document.getElementById('skillsGraphContainer')?.children.length) init();
  });
</script>
</body>
</html>
