<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Suraj Singh Bayas — GitHub Profile</title>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: 'JetBrains Mono', 'Fira Code', 'Courier New', monospace;
    background: #0d1117;
    color: #c9d1d9;
    line-height: 1.6;
    min-height: 100vh;
  }
  .header {
    border-bottom: 1px solid #21262d;
    padding: 48px 40px 40px;
    position: relative;
    overflow: hidden;
  }
  .header::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, #58a6ff, #3fb950, #f0883e, #58a6ff);
    background-size: 200% 100%;
    animation: slide 4s linear infinite;
  }
  @keyframes slide { 0% { background-position: 0% 0 } 100% { background-position: 200% 0 } }
  .header-inner {
    max-width: 860px;
    margin: 0 auto;
    display: flex;
    align-items: flex-start;
    gap: 32px;
  }
  .avatar {
    width: 80px; height: 80px;
    border-radius: 50%;
    background: #161b22;
    border: 2px solid #30363d;
    display: flex; align-items: center; justify-content: center;
    font-size: 28px; font-weight: 700;
    color: #58a6ff;
    flex-shrink: 0;
  }
  .header-info h1 { font-size: 26px; font-weight: 700; color: #f0f6fc; margin-bottom: 4px; }
  .tagline { font-size: 13px; color: #8b949e; margin-bottom: 16px; }
  .badges { display: flex; flex-wrap: wrap; gap: 8px; }
  .badge {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 4px 12px;
    border: 1px solid #30363d;
    border-radius: 20px;
    font-size: 11px; color: #c9d1d9;
    text-decoration: none;
    background: #161b22;
    transition: border-color 0.15s, color 0.15s;
  }
  .badge:hover { border-color: #58a6ff; color: #58a6ff; }
  .dot { width: 6px; height: 6px; border-radius: 50%; background: currentColor; }
  .main { max-width: 860px; margin: 0 auto; padding: 0 40px 48px; }
  .section { padding: 32px 0; border-bottom: 1px solid #21262d; }
  .section:last-child { border-bottom: none; }
  .section-title {
    font-size: 11px; font-weight: 600;
    letter-spacing: 1.5px; text-transform: uppercase;
    color: #8b949e; margin-bottom: 20px;
    display: flex; align-items: center; gap: 10px;
  }
  .section-title::after { content: ''; flex: 1; height: 1px; background: #21262d; }
  .about-code {
    background: #161b22; border: 1px solid #30363d;
    border-radius: 8px; padding: 20px 24px;
    font-size: 12.5px; line-height: 1.8;
    margin-bottom: 20px;
  }
  .kw { color: #ff7b72; } .type { color: #ffa657; } .str { color: #a5d6ff; }
  .prop { color: #79c0ff; }
  .bullets { display: grid; grid-template-columns: 1fr 1fr; gap: 8px 24px; list-style: none; }
  .bullets li { font-size: 13px; padding-left: 16px; position: relative; }
  .bullets li::before { content: '→'; position: absolute; left: 0; color: #3fb950; font-size: 11px; }
  .stats-grid { display: grid; grid-template-columns: repeat(4,1fr); gap: 12px; margin-bottom: 20px; }
  .stat-card {
    background: #161b22; border: 1px solid #30363d;
    border-radius: 8px; padding: 16px; text-align: center;
  }
  .stat-num { font-size: 22px; font-weight: 700; display: block; margin-bottom: 4px; }
  .stat-label { font-size: 10px; color: #8b949e; letter-spacing: 0.5px; text-transform: uppercase; }
  .stat-card.blue .stat-num { color: #58a6ff; }
  .stat-card.green .stat-num { color: #3fb950; }
  .stat-card.orange .stat-num { color: #f0883e; }
  .stat-card.purple .stat-num { color: #bc8cff; }
  .contrib-bar { background: #161b22; border: 1px solid #30363d; border-radius: 8px; padding: 16px 20px; }
  .contrib-row { display: flex; align-items: center; gap: 12px; margin-bottom: 10px; }
  .contrib-row:last-child { margin-bottom: 0; }
  .lang-name { width: 80px; font-size: 12px; flex-shrink: 0; }
  .bar-bg { flex: 1; height: 6px; background: #21262d; border-radius: 3px; overflow: hidden; }
  .bar-fill { height: 100%; border-radius: 3px; }
  .lang-pct { font-size: 11px; color: #8b949e; width: 42px; text-align: right; flex-shrink: 0; }
  .tech-groups { display: flex; flex-direction: column; gap: 16px; }
  .tech-group-label { font-size: 10px; color: #8b949e; letter-spacing: 1px; text-transform: uppercase; margin-bottom: 8px; }
  .tech-pills { display: flex; flex-wrap: wrap; gap: 6px; }
  .pill { padding: 3px 10px; border: 1px solid #30363d; border-radius: 4px; font-size: 11px; color: #8b949e; background: #161b22; }
  .pill.blue { border-color: #58a6ff44; color: #58a6ff; }
  .pill.green { border-color: #3fb95044; color: #3fb950; }
  .pill.orange { border-color: #f0883e44; color: #f0883e; }
  .pill.purple { border-color: #bc8cff44; color: #bc8cff; }
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .project-card {
    background: #161b22; border: 1px solid #30363d;
    border-radius: 8px; padding: 16px 18px;
    transition: border-color 0.15s;
    text-decoration: none; display: block;
  }
  .project-card:hover { border-color: #58a6ff; }
  .project-name { font-size: 13px; font-weight: 600; color: #58a6ff; margin-bottom: 6px; }
  .project-desc { font-size: 11.5px; color: #8b949e; line-height: 1.5; margin-bottom: 12px; }
  .project-meta { display: flex; align-items: center; gap: 12px; }
  .lang-dot { display: flex; align-items: center; gap: 5px; font-size: 11px; color: #8b949e; }
  .ldot { width: 10px; height: 10px; border-radius: 50%; }
  .connect-grid { display: flex; flex-wrap: wrap; gap: 10px; }
  .connect-card {
    display: flex; align-items: center; gap: 10px;
    padding: 10px 16px;
    background: #161b22; border: 1px solid #30363d;
    border-radius: 8px; font-size: 12px; color: #c9d1d9;
    text-decoration: none;
    transition: border-color 0.15s, color 0.15s;
  }
  .connect-card:hover { border-color: #58a6ff; color: #58a6ff; }
  .footer {
    border-top: 1px solid #21262d;
    padding: 24px 40px;
    max-width: 860px; margin: 0 auto;
    display: flex; align-items: center; justify-content: space-between;
  }
  .footer-text { font-size: 11px; color: #8b949e; }
  .footer-tag { font-size: 11px; color: #3fb950; border: 1px solid #3fb95040; padding: 2px 10px; border-radius: 20px; }
  @media (max-width: 600px) {
    .header { padding: 32px 20px 28px; }
    .main { padding: 0 20px 40px; }
    .header-inner { flex-direction: column; gap: 16px; }
    .stats-grid { grid-template-columns: 1fr 1fr; }
    .projects-grid { grid-template-columns: 1fr; }
    .bullets { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<div class="header">
  <div class="header-inner">
    <div class="avatar">SS</div>
    <div class="header-info">
      <h1>Suraj Singh Bayas</h1>
      <p class="tagline">Full Stack Developer &nbsp;·&nbsp; AI Engineer &nbsp;·&nbsp; Open Source</p>
      <div class="badges">
        <a class="badge" href="https://linkedin.com/in/surajsinghbayas"><span class="dot" style="background:#0a66c2"></span>LinkedIn</a>
        <a class="badge" href="https://github.com/SurajsinghBayas"><span class="dot" style="background:#f0f6fc"></span>GitHub</a>
        <a class="badge" href="https://twitter.com/surajsinghbayas"><span class="dot" style="background:#1da1f2"></span>Twitter</a>
        <a class="badge" href="https://your-portfolio.vercel.app"><span class="dot" style="background:#58a6ff"></span>Portfolio</a>
        <a class="badge" href="mailto:your.email@example.com"><span class="dot" style="background:#f0883e"></span>Email</a>
        <span class="badge"><span class="dot" style="background:#3fb950"></span>India 🇮🇳</span>
      </div>
    </div>
  </div>
</div>

<div class="main">

  <div class="section">
    <div class="section-title">About</div>
    <div class="about-code">
      <span class="kw">const</span> <span class="prop">suraj</span>: <span class="type">Developer</span> = {<br>
      &nbsp;&nbsp;<span class="prop">role</span>: [<span class="str">"Full Stack Developer"</span>, <span class="str">"AI Engineer"</span>],<br>
      &nbsp;&nbsp;<span class="prop">building</span>: <span class="str">"AI-powered SaaS applications"</span>,<br>
      &nbsp;&nbsp;<span class="prop">learning</span>: [<span class="str">"System Design"</span>, <span class="str">"Cloud Architecture"</span>],<br>
      &nbsp;&nbsp;<span class="prop">openTo</span>: <span class="str">"innovative open source projects"</span>,<br>
      &nbsp;&nbsp;<span class="prop">funFact</span>: <span class="str">"every bug is an undocumented feature"</span><br>
      }
    </div>
    <ul class="bullets">
      <li>Daily DSA challenges to stay sharp</li>
      <li>Currently exploring advanced ML</li>
      <li>Computer Science Engineering grad</li>
      <li>Open to collabs and freelance work</li>
    </ul>
  </div>

  <div class="section">
    <div class="section-title">GitHub Stats</div>
    <div class="stats-grid">
      <div class="stat-card blue"><span class="stat-num">365+</span><span class="stat-label">Commits</span></div>
      <div class="stat-card green"><span class="stat-num">12+</span><span class="stat-label">Projects</span></div>
      <div class="stat-card orange"><span class="stat-num">8</span><span class="stat-label">Repos</span></div>
      <div class="stat-card purple"><span class="stat-num">3</span><span class="stat-label">Followers</span></div>
    </div>
    <div class="contrib-bar">
      <div class="contrib-row">
        <span class="lang-name">JavaScript</span>
        <div class="bar-bg"><div class="bar-fill" style="width:45%;background:#f1e05a"></div></div>
        <span class="lang-pct">45.32%</span>
      </div>
      <div class="contrib-row">
        <span class="lang-name">Python</span>
        <div class="bar-bg"><div class="bar-fill" style="width:22%;background:#3572A5"></div></div>
        <span class="lang-pct">22.18%</span>
      </div>
      <div class="contrib-row">
        <span class="lang-name">TypeScript</span>
        <div class="bar-bg"><div class="bar-fill" style="width:18%;background:#2b7489"></div></div>
        <span class="lang-pct">18.45%</span>
      </div>
      <div class="contrib-row">
        <span class="lang-name">Java</span>
        <div class="bar-bg"><div class="bar-fill" style="width:10%;background:#b07219"></div></div>
        <span class="lang-pct">10.22%</span>
      </div>
      <div class="contrib-row">
        <span class="lang-name">Other</span>
        <div class="bar-bg"><div class="bar-fill" style="width:4%;background:#8b949e"></div></div>
        <span class="lang-pct">3.83%</span>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-title">Tech Stack</div>
    <div class="tech-groups">
      <div>
        <div class="tech-group-label">Languages</div>
        <div class="tech-pills">
          <span class="pill blue">JavaScript</span><span class="pill blue">TypeScript</span><span class="pill blue">Python</span><span class="pill">Java</span><span class="pill">C++</span><span class="pill">C</span>
        </div>
      </div>
      <div>
        <div class="tech-group-label">Frontend</div>
        <div class="tech-pills">
          <span class="pill blue">React</span><span class="pill blue">Next.js</span><span class="pill">Tailwind CSS</span><span class="pill">HTML/CSS</span><span class="pill">Sass</span><span class="pill">Bootstrap</span>
        </div>
      </div>
      <div>
        <div class="tech-group-label">Backend</div>
        <div class="tech-pills">
          <span class="pill green">Node.js</span><span class="pill green">Express</span><span class="pill green">FastAPI</span><span class="pill">Flask</span><span class="pill">Django</span>
        </div>
      </div>
      <div>
        <div class="tech-group-label">Databases & Cloud</div>
        <div class="tech-pills">
          <span class="pill">MongoDB</span><span class="pill">PostgreSQL</span><span class="pill">MySQL</span><span class="pill">Redis</span><span class="pill">Firebase</span><span class="pill">Supabase</span><span class="pill blue">AWS</span>
        </div>
      </div>
      <div>
        <div class="tech-group-label">AI / ML</div>
        <div class="tech-pills">
          <span class="pill orange">OpenAI API</span><span class="pill orange">LangChain</span><span class="pill orange">Google Gemini</span><span class="pill">TensorFlow</span><span class="pill">PyTorch</span><span class="pill">Pandas</span><span class="pill">NumPy</span>
        </div>
      </div>
      <div>
        <div class="tech-group-label">DevOps & Tools</div>
        <div class="tech-pills">
          <span class="pill">Docker</span><span class="pill">Kubernetes</span><span class="pill">Git</span><span class="pill">Linux</span><span class="pill">Vercel</span><span class="pill">Netlify</span><span class="pill">Postman</span><span class="pill">Figma</span>
        </div>
      </div>
      <div>
        <div class="tech-group-label">Other</div>
        <div class="tech-pills">
          <span class="pill purple">Solidity</span><span class="pill purple">Web3.js</span><span class="pill">GraphQL</span><span class="pill">Prisma</span><span class="pill">Stripe</span><span class="pill">Razorpay</span><span class="pill">Appwrite</span>
        </div>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-title">Projects</div>
    <div class="projects-grid">
      <a class="project-card" href="https://github.com/SurajsinghBayas/dsa-365-days">
        <div class="project-name">dsa-365-days</div>
        <div class="project-desc">365 days of daily DSA problem solving — staying sharp one problem at a time.</div>
        <div class="project-meta">
          <span class="lang-dot"><span class="ldot" style="background:#f1e05a"></span>JavaScript</span>
          <span style="font-size:11px;color:#8b949e">☆ 0</span>
        </div>
      </a>
      <div class="project-card" style="border-style:dashed;display:flex;align-items:center;justify-content:center;cursor:default">
        <span style="font-size:12px;color:#8b949e">More coming soon...</span>
      </div>
    </div>
  </div>

  <div class="section">
    <div class="section-title">Connect</div>
    <div class="connect-grid">
      <a class="connect-card" href="https://linkedin.com/in/surajsinghbayas">💼 linkedin.com/in/surajsinghbayas</a>
      <a class="connect-card" href="https://github.com/SurajsinghBayas">🐙 github.com/SurajsinghBayas</a>
      <a class="connect-card" href="mailto:your.email@example.com">📧 your.email@example.com</a>
      <a class="connect-card" href="https://your-portfolio.vercel.app">🌐 your-portfolio.vercel.app</a>
    </div>
  </div>

</div>

<div class="footer">
  <span class="footer-text">surajsinghbayas · India 🇮🇳 · Computer Science Engineering</span>
  <span class="footer-tag">open to work</span>
</div>

</body>
</html>
