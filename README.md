<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Yassa Hammam — Data Engineer & AI Enthusiast</title>
  <meta name="description" content="Portfolio of Yassa Hammam — Computer Science & AI student, Data Engineer, and Data Analyst building intelligent data systems." />
  <meta property="og:title" content="Yassa Hammam — Data Engineer & AI Enthusiast" />
  <meta property="og:description" content="Portfolio of Yassa Hammam — CS & AI student specializing in Data Engineering, ETL Pipelines, and AI-driven analytics." />
  <meta property="og:type" content="website" />
  <meta name="theme-color" content="#0a0e1a" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet" />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/tsparticles/2.12.0/tsparticles.bundle.min.js"></script>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #050810;
      --bg2: #080d1c;
      --bg3: #0d1530;
      --surface: rgba(255,255,255,0.04);
      --surface2: rgba(255,255,255,0.07);
      --border: rgba(99,179,237,0.15);
      --border2: rgba(99,179,237,0.3);
      --cyan: #38bdf8;
      --blue: #3b82f6;
      --purple: #a855f7;
      --electric: #06b6d4;
      --text: #e2e8f0;
      --text2: #94a3b8;
      --text3: #64748b;
      --glow: 0 0 30px rgba(56,189,248,0.25), 0 0 60px rgba(56,189,248,0.1);
      --glow-purple: 0 0 30px rgba(168,85,247,0.25), 0 0 60px rgba(168,85,247,0.1);
      --radius: 16px;
      --transition: 0.35s cubic-bezier(0.4,0,0.2,1);
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      overflow-x: hidden;
      line-height: 1.6;
    }

    ::-webkit-scrollbar { width: 4px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: linear-gradient(var(--cyan), var(--purple)); border-radius: 4px; }

    #scroll-progress {
      position: fixed; top: 0; left: 0; height: 3px; z-index: 9999;
      background: linear-gradient(90deg, var(--cyan), var(--purple), var(--blue));
      width: 0%; transition: width 0.1s linear;
    }

    #tsparticles { position: fixed; inset: 0; z-index: 0; pointer-events: none; }

    body::before {
      content: '';
      position: fixed; inset: 0; z-index: 1; pointer-events: none;
      background-image:
        linear-gradient(rgba(56,189,248,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(56,189,248,0.03) 1px, transparent 1px);
      background-size: 60px 60px;
    }

    .wrapper { position: relative; z-index: 2; }
  .avatar-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      border-radius: 50%;
      display: block;
    }
    /* NAV */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
      padding: 0 5%;
      display: flex; align-items: center; justify-content: space-between;
      height: 70px;
      background: rgba(5,8,16,0.75);
      backdrop-filter: blur(20px) saturate(1.8);
      border-bottom: 1px solid var(--border);
      transition: var(--transition);
    }
    nav.scrolled { background: rgba(5,8,16,0.94); }

    .nav-logo {
      font-family: 'Syne', sans-serif;
      font-weight: 800; font-size: 1.4rem;
      background: linear-gradient(135deg, var(--cyan), var(--purple));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      text-decoration: none; letter-spacing: -0.5px;
    }

    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      color: var(--text2); text-decoration: none; font-size: 0.875rem;
      font-weight: 500; letter-spacing: 0.03em;
      transition: color var(--transition);
      position: relative;
    }
    .nav-links a::after {
      content: ''; position: absolute; bottom: -4px; left: 0; right: 0;
      height: 1px; background: var(--cyan);
      transform: scaleX(0); transition: transform var(--transition);
      transform-origin: left;
    }
    .nav-links a:hover { color: var(--cyan); }
    .nav-links a:hover::after { transform: scaleX(1); }
    .nav-cta {
      padding: 0.5rem 1.25rem; border: 1px solid var(--border2);
      border-radius: 8px; color: var(--cyan) !important;
      background: rgba(56,189,248,0.07);
      transition: all var(--transition) !important;
    }
    .nav-cta:hover { background: rgba(56,189,248,0.15) !important; box-shadow: var(--glow); }
    .nav-cta::after { display: none !important; }

    .nav-toggle {
      display: none; flex-direction: column; gap: 5px;
      background: none; border: none; cursor: pointer; padding: 4px;
    }
    .nav-toggle span { display: block; width: 24px; height: 2px; background: var(--cyan); border-radius: 2px; transition: var(--transition); }

    @media (max-width: 768px) {
      .nav-links {
        position: fixed; top: 70px; left: 0; right: 0;
        flex-direction: column; gap: 0;
        background: rgba(5,8,16,0.97); backdrop-filter: blur(20px);
        border-bottom: 1px solid var(--border); padding: 1rem 0;
        transform: translateY(-110%); transition: transform var(--transition); z-index: 999;
      }
      .nav-links.open { transform: translateY(0); }
      .nav-links li { border-bottom: 1px solid var(--border); }
      .nav-links a { display: block; padding: 1rem 5%; font-size: 1rem; }
      .nav-toggle { display: flex; }
    }

    /* SECTIONS */
    section { padding: 100px 5%; position: relative; }
    .section-label {
      font-family: 'JetBrains Mono', monospace; font-size: 0.75rem; letter-spacing: 0.2em;
      color: var(--cyan); text-transform: uppercase; margin-bottom: 0.75rem;
      display: flex; align-items: center; gap: 0.75rem;
    }
    .section-label::before { content: ''; display: block; width: 32px; height: 1px; background: var(--cyan); }
    .section-title {
      font-family: 'Syne', sans-serif; font-size: clamp(2rem, 4vw, 3rem);
      font-weight: 800; line-height: 1.1; margin-bottom: 1rem;
    }
    .gradient-text {
      background: linear-gradient(135deg, var(--cyan) 0%, var(--purple) 60%, var(--blue) 100%);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }
    .glass {
      background: var(--surface); border: 1px solid var(--border);
      border-radius: var(--radius); backdrop-filter: blur(12px);
      transition: all var(--transition);
    }
    .glass:hover { border-color: var(--border2); background: var(--surface2); transform: translateY(-4px); box-shadow: var(--glow); }
    .btn {
      display: inline-flex; align-items: center; gap: 0.5rem;
      padding: 0.75rem 1.75rem; border-radius: 10px;
      font-family: 'DM Sans', sans-serif; font-weight: 500; font-size: 0.9rem;
      cursor: pointer; border: none; text-decoration: none;
      transition: all var(--transition); white-space: nowrap;
    }
    .btn-primary {
      background: linear-gradient(135deg, var(--cyan), var(--blue)); color: #fff;
      box-shadow: 0 4px 20px rgba(56,189,248,0.3);
    }
    .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 30px rgba(56,189,248,0.45); }
    .btn-outline { background: transparent; color: var(--cyan); border: 1px solid var(--border2); }
    .btn-outline:hover { background: rgba(56,189,248,0.08); box-shadow: var(--glow); transform: translateY(-2px); }
    .btn-ghost { background: rgba(168,85,247,0.12); color: var(--purple); border: 1px solid rgba(168,85,247,0.3); }
    .btn-ghost:hover { background: rgba(168,85,247,0.2); box-shadow: var(--glow-purple); transform: translateY(-2px); }
    .section-divider { width: 60px; height: 3px; background: linear-gradient(90deg, var(--cyan), var(--purple)); border-radius: 2px; margin: 1.25rem 0 2.5rem; }
    .content-wrap { max-width: 1100px; margin: 0 auto; }

    /* HERO */
    #hero { min-height: 100vh; padding-top: 70px; display: flex; align-items: center; position: relative; overflow: hidden; }
    .hero-inner {
      width: 100%; max-width: 1200px; margin: 0 auto;
      display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center;
    }
    .hero-badge {
      display: inline-flex; align-items: center; gap: 0.5rem;
      padding: 0.4rem 1rem; border-radius: 100px;
      border: 1px solid rgba(56,189,248,0.25); background: rgba(56,189,248,0.07);
      font-family: 'JetBrains Mono', monospace; font-size: 0.75rem; color: var(--cyan); margin-bottom: 1.5rem;
    }
    .hero-badge::before {
      content: ''; width: 6px; height: 6px; border-radius: 50%; background: var(--cyan);
      box-shadow: 0 0 8px var(--cyan); animation: blink 1.5s infinite;
    }
    @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.3} }
    .hero-name { font-family: 'Syne', sans-serif; font-size: clamp(2.5rem, 5vw, 4rem); font-weight: 800; line-height: 1.05; margin-bottom: 0.5rem; }
    .hero-title { font-size: clamp(1rem, 2vw, 1.2rem); color: var(--text2); margin-bottom: 1.5rem; height: 2rem; display: flex; align-items: center; gap: 0.5rem; }
    #typed-text { color: var(--cyan); font-family: 'JetBrains Mono', monospace; font-size: 0.95rem; }
    .typed-cursor { display: inline-block; width: 2px; height: 1.2em; background: var(--cyan); animation: cursor-blink 0.7s steps(1) infinite; vertical-align: middle; margin-left: 2px; }
    @keyframes cursor-blink { 0%,100%{opacity:1} 50%{opacity:0} }
    .hero-tagline { font-size: clamp(1.1rem, 2vw, 1.4rem); color: var(--text); font-weight: 300; margin-bottom: 2.5rem; max-width: 520px; line-height: 1.5; }
    .hero-buttons { display: flex; gap: 1rem; flex-wrap: wrap; }

    /* AVATAR */
    .hero-visual { display: flex; align-items: center; justify-content: center; position: relative; }
    .avatar-ring { position: relative; width: 340px; height: 340px; }
    .ring-outer {
      position: absolute; inset: -16px; border-radius: 50%;
      background: conic-gradient(from 0deg, var(--cyan), var(--purple), var(--blue), var(--cyan));
      animation: spin 6s linear infinite;
      mask: radial-gradient(farthest-side, transparent calc(100% - 3px), #fff calc(100% - 3px));
      -webkit-mask: radial-gradient(farthest-side, transparent calc(100% - 3px), #fff calc(100% - 3px));
    }
    @keyframes spin { to { transform: rotate(360deg); } }
    .ring-inner {
      position: absolute; inset: -4px; border-radius: 50%;
      border: 1px solid var(--border); animation: spin 12s linear infinite reverse;
    }
    .ring-inner::before {
      content: ''; position: absolute; top: -2px; left: 50%; transform: translateX(-50%);
      width: 6px; height: 6px; border-radius: 50%; background: var(--cyan); box-shadow: var(--glow);
    }
    .avatar-core {
      position: absolute; inset: 0; border-radius: 50%; overflow: hidden;
      background: linear-gradient(135deg, var(--bg3), #1e1b4b);
      display: flex; align-items: center; justify-content: center;
      border: 2px solid rgba(56,189,248,0.2);
      transition: transform 0.6s cubic-bezier(0.4,0,0.2,1);
    }
    .avatar-core:hover { transform: scale(1.03) rotate(-2deg); }
    .avatar-initials { font-family: 'Syne', sans-serif; font-size: 5rem; font-weight: 800; background: linear-gradient(135deg, var(--cyan), var(--purple)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; user-select: none; }
    .avatar-glow { position: absolute; inset: -40px; border-radius: 50%; background: radial-gradient(circle, rgba(56,189,248,0.12) 0%, transparent 70%); pointer-events: none; }
    .float-chip {
      position: absolute; padding: 0.4rem 0.85rem; border-radius: 100px;
      background: var(--surface); border: 1px solid var(--border2);
      font-size: 0.75rem; font-weight: 500; backdrop-filter: blur(12px);
      display: flex; align-items: center; gap: 0.4rem; white-space: nowrap;
    }
    .float-chip .chip-dot { width: 6px; height: 6px; border-radius: 50%; }
    .chip1 { top: 8%; right: -20px; animation: float 3s ease-in-out infinite; }
    .chip2 { bottom: 12%; left: -30px; animation: float 3.5s ease-in-out infinite 0.5s; }
    .chip3 { top: 50%; right: -40px; animation: float 4s ease-in-out infinite 1s; }
    @keyframes float { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-10px)} }

    @media (max-width: 900px) {
      .hero-inner { grid-template-columns: 1fr; text-align: center; gap: 3rem; }
      .hero-tagline { max-width: 100%; }
      .hero-buttons { justify-content: center; }
      .hero-visual { order: -1; }
      .avatar-ring { width: 260px; height: 260px; }
      .chip1,.chip2,.chip3 { display: none; }
    }

    /* ABOUT */
    #about { background: linear-gradient(180deg, transparent 0%, rgba(59,130,246,0.03) 100%); }
    .about-grid { max-width: 1100px; margin: 0 auto; display: grid; grid-template-columns: 1.2fr 1fr; gap: 3rem; align-items: start; }
    .about-text p { color: var(--text2); line-height: 1.8; margin-bottom: 1.25rem; font-size: 0.975rem; }
    .about-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-top: 1.5rem; }
    .tag { padding: 0.35rem 0.85rem; border-radius: 100px; font-size: 0.78rem; font-family: 'JetBrains Mono', monospace; border: 1px solid var(--border); color: var(--text2); transition: all var(--transition); cursor: default; }
    .tag:hover { border-color: var(--cyan); color: var(--cyan); background: rgba(56,189,248,0.07); }
    .about-stats { display: flex; flex-direction: column; gap: 1.25rem; }
    .stat-card { padding: 1.5rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); transition: all var(--transition); position: relative; overflow: hidden; }
    .stat-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, var(--cyan), var(--purple)); transform: scaleX(0); transform-origin: left; transition: transform var(--transition); }
    .stat-card:hover::before { transform: scaleX(1); }
    .stat-card:hover { border-color: var(--border2); transform: translateX(4px); }
    .stat-num { font-family: 'Syne', sans-serif; font-size: 2rem; font-weight: 800; background: linear-gradient(135deg, var(--cyan), var(--purple)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
    .stat-label { color: var(--text2); font-size: 0.875rem; margin-top: 0.25rem; }
    @media (max-width: 768px) { .about-grid { grid-template-columns: 1fr; } }

    /* SKILLS */
    #skills { background: var(--bg2); }
    .skills-grid { max-width: 1100px; margin: 0 auto; display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1.5rem; }
    .skill-cat { padding: 1.75rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); transition: all var(--transition); position: relative; overflow: hidden; }
    .skill-cat::after { content: ''; position: absolute; inset: 0; background: linear-gradient(135deg, rgba(56,189,248,0.04), transparent); opacity: 0; transition: opacity var(--transition); }
    .skill-cat:hover { border-color: var(--border2); box-shadow: var(--glow); }
    .skill-cat:hover::after { opacity: 1; }
    .skill-cat-icon { font-size: 1.75rem; margin-bottom: 0.75rem; display: block; }
    .skill-cat-title { font-family: 'Syne', sans-serif; font-weight: 700; margin-bottom: 1rem; font-size: 0.95rem; letter-spacing: 0.03em; color: var(--cyan); }
    .skill-pills { display: flex; flex-wrap: wrap; gap: 0.5rem; }
    .skill-pill { padding: 0.3rem 0.75rem; border-radius: 100px; font-size: 0.78rem; background: rgba(56,189,248,0.07); border: 1px solid rgba(56,189,248,0.18); color: var(--text2); transition: all var(--transition); font-family: 'JetBrains Mono', monospace; }
    .skill-pill:hover { background: rgba(56,189,248,0.15); border-color: var(--cyan); color: var(--cyan); transform: translateY(-2px); }

    /* EXPERIENCE */
    #experience { background: linear-gradient(180deg, transparent 0%, rgba(168,85,247,0.03) 100%); }
    .exp-card { max-width: 800px; margin: 0 auto; padding: 2.5rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); position: relative; overflow: hidden; }
    .exp-card::before { content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 3px; background: linear-gradient(180deg, var(--cyan), var(--purple)); }
    .exp-header { display: flex; align-items: flex-start; gap: 1.25rem; margin-bottom: 1.5rem; }
    .exp-logo { width: 54px; height: 54px; border-radius: 12px; background: linear-gradient(135deg, rgba(56,189,248,0.2), rgba(168,85,247,0.2)); border: 1px solid var(--border2); display: flex; align-items: center; justify-content: center; font-size: 1.5rem; flex-shrink: 0; }
    .exp-meta { flex: 1; }
    .exp-role { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 1.15rem; margin-bottom: 0.25rem; }
    .exp-company { color: var(--cyan); font-size: 0.9rem; margin-bottom: 0.25rem; }
    .exp-period { font-size: 0.8rem; color: var(--text3); font-family: 'JetBrains Mono', monospace; display: flex; align-items: center; gap: 0.4rem; }
    .exp-period::before { content: ''; width: 6px; height: 6px; border-radius: 50%; background: var(--purple); box-shadow: 0 0 6px var(--purple); }
    .exp-list { list-style: none; }
    .exp-list li { padding: 0.6rem 0; border-bottom: 1px solid var(--border); color: var(--text2); font-size: 0.9rem; display: flex; gap: 0.75rem; align-items: flex-start; }
    .exp-list li:last-child { border-bottom: none; }
    .exp-list li::before { content: '▸'; color: var(--cyan); flex-shrink: 0; margin-top: 1px; }

    /* PROJECTS */
    #projects { background: var(--bg2); }
    .projects-header { max-width: 1100px; margin: 0 auto 2.5rem; }
    .tab-switcher { display: flex; background: rgba(255,255,255,0.04); border: 1px solid var(--border); border-radius: 12px; padding: 4px; width: fit-content; margin-top: 2rem; }
    .tab-btn { padding: 0.6rem 1.5rem; border-radius: 8px; background: transparent; border: none; font-family: 'DM Sans', sans-serif; font-size: 0.875rem; font-weight: 500; color: var(--text2); cursor: pointer; transition: all var(--transition); }
    .tab-btn.active { background: linear-gradient(135deg, var(--cyan), var(--blue)); color: #fff; box-shadow: 0 4px 12px rgba(56,189,248,0.3); }
    .projects-pane { display: none; }
    .projects-pane.active { display: block; }
    .projects-grid { max-width: 1100px; margin: 0 auto; display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 1.5rem; }
    .proj-card { padding: 1.75rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); transition: all var(--transition); position: relative; overflow: hidden; display: flex; flex-direction: column; }
    .proj-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px; background: linear-gradient(90deg, transparent, var(--cyan), transparent); opacity: 0; transition: opacity var(--transition); }
    .proj-card:hover { border-color: var(--border2); transform: translateY(-6px); box-shadow: var(--glow); }
    .proj-card:hover::before { opacity: 1; }
    .proj-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 1rem; }
    .proj-number { font-family: 'JetBrains Mono', monospace; font-size: 0.7rem; color: var(--text3); }
    .proj-type-badge { padding: 0.2rem 0.6rem; border-radius: 100px; font-size: 0.68rem; font-family: 'JetBrains Mono', monospace; }
    .badge-web { background: rgba(59,130,246,0.15); border: 1px solid rgba(59,130,246,0.3); color: #60a5fa; }
    .badge-data { background: rgba(168,85,247,0.15); border: 1px solid rgba(168,85,247,0.3); color: #c084fc; }
    .proj-title { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 1.1rem; margin-bottom: 0.5rem; }
    .proj-problem { font-size: 0.85rem; color: var(--text2); line-height: 1.6; margin-bottom: 1rem; flex: 1; }
    .proj-stack { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-bottom: 1rem; }
    .stack-pill { padding: 0.2rem 0.6rem; border-radius: 100px; font-size: 0.72rem; font-family: 'JetBrains Mono', monospace; background: rgba(255,255,255,0.05); border: 1px solid var(--border); color: var(--text3); }
    .proj-insights { margin-bottom: 1rem; }
    .proj-insights h5 { font-size: 0.75rem; color: var(--cyan); font-family: 'JetBrains Mono', monospace; text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 0.5rem; }
    .proj-insights ul { list-style: none; }
    .proj-insights ul li { font-size: 0.82rem; color: var(--text2); padding: 0.2rem 0; display: flex; gap: 0.5rem; }
    .proj-insights ul li::before { content: '·'; color: var(--purple); }
    .proj-outcome { padding: 0.75rem; border-radius: 8px; background: rgba(56,189,248,0.05); border: 1px solid rgba(56,189,248,0.12); font-size: 0.82rem; color: var(--text2); }
    .proj-outcome strong { color: var(--cyan); }

    /* EDUCATION */
    #education { background: linear-gradient(180deg, transparent 0%, rgba(59,130,246,0.03) 100%); }
    .edu-cert-grid { max-width: 1000px; margin: 0 auto; display: grid; grid-template-columns: 1.5fr 1fr; gap: 2rem; align-items: start; }
    .edu-card { padding: 2rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); position: relative; overflow: hidden; }
    .edu-card::after { content: ''; position: absolute; bottom: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, var(--cyan), var(--purple)); }
    .edu-icon { font-size: 2.5rem; margin-bottom: 1rem; }
    .edu-degree { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 1.2rem; margin-bottom: 0.25rem; }
    .edu-uni { color: var(--cyan); margin-bottom: 0.5rem; font-size: 0.9rem; }
    .edu-meta { display: flex; gap: 1rem; flex-wrap: wrap; margin-top: 1rem; }
    .edu-badge { padding: 0.35rem 0.85rem; border-radius: 100px; font-size: 0.78rem; font-family: 'JetBrains Mono', monospace; border: 1px solid var(--border); color: var(--text2); }
    .edu-badge.gpa { border-color: rgba(56,189,248,0.3); background: rgba(56,189,248,0.07); color: var(--cyan); }
    .certs-list { display: flex; flex-direction: column; gap: 1rem; }
    .cert-item { padding: 1.25rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); transition: all var(--transition); display: flex; gap: 1rem; align-items: center; }
    .cert-item:hover { border-color: var(--border2); transform: translateX(4px); box-shadow: var(--glow); }
    .cert-icon { font-size: 1.5rem; flex-shrink: 0; }
    .cert-name { font-weight: 500; font-size: 0.9rem; margin-bottom: 0.2rem; }
    .cert-issuer { font-size: 0.78rem; color: var(--text3); font-family: 'JetBrains Mono', monospace; }
    @media (max-width: 768px) { .edu-cert-grid { grid-template-columns: 1fr; } }

    /* WHY */
    #why { background: var(--bg2); }
    .why-grid { max-width: 1100px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; align-items: center; }
    .why-traits { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    .why-trait { padding: 1.25rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); transition: all var(--transition); }
    .why-trait:hover { border-color: var(--border2); box-shadow: var(--glow); transform: translateY(-3px); }
    .why-trait-icon { font-size: 1.5rem; margin-bottom: 0.5rem; }
    .why-trait-name { font-weight: 600; font-size: 0.875rem; }
    .why-achievements { display: flex; flex-direction: column; gap: 1.25rem; }
    .achieve-card { padding: 1.5rem; border-radius: var(--radius); background: linear-gradient(135deg, rgba(56,189,248,0.08), rgba(168,85,247,0.08)); border: 1px solid var(--border2); display: flex; gap: 1rem; align-items: center; transition: all var(--transition); }
    .achieve-card:hover { transform: scale(1.02); box-shadow: var(--glow); }
    .achieve-num { font-family: 'Syne', sans-serif; font-size: 2.5rem; font-weight: 800; background: linear-gradient(135deg, var(--cyan), var(--purple)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; flex-shrink: 0; line-height: 1; }
    .achieve-label { color: var(--text2); font-size: 0.9rem; }
    @media (max-width: 900px) { .why-grid { grid-template-columns: 1fr; } }

    /* CONTACT */
    #contact { background: linear-gradient(180deg, transparent 0%, rgba(168,85,247,0.04) 100%); }
    .contact-grid { max-width: 1000px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1.3fr; gap: 3rem; align-items: start; }
    .contact-info { display: flex; flex-direction: column; gap: 1rem; }
    .contact-link { display: flex; align-items: center; gap: 1rem; padding: 1.25rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); text-decoration: none; color: var(--text); transition: all var(--transition); }
    .contact-link:hover { border-color: var(--border2); transform: translateX(4px); box-shadow: var(--glow); }
    .contact-link-icon { width: 42px; height: 42px; border-radius: 10px; background: linear-gradient(135deg, rgba(56,189,248,0.2), rgba(168,85,247,0.2)); border: 1px solid var(--border2); display: flex; align-items: center; justify-content: center; font-size: 1.1rem; flex-shrink: 0; }
    .contact-link-label { font-size: 0.75rem; color: var(--text3); font-family: 'JetBrains Mono', monospace; }
    .contact-link-val { font-size: 0.875rem; margin-top: 0.1rem; }
    .contact-form { padding: 2rem; border-radius: var(--radius); background: var(--surface); border: 1px solid var(--border); }
    .form-group { margin-bottom: 1.25rem; }
    .form-label { display: block; margin-bottom: 0.4rem; font-size: 0.8rem; color: var(--text2); font-family: 'JetBrains Mono', monospace; letter-spacing: 0.05em; }
    .form-control { width: 100%; padding: 0.75rem 1rem; border-radius: 10px; background: rgba(255,255,255,0.04); border: 1px solid var(--border); color: var(--text); font-family: 'DM Sans', sans-serif; font-size: 0.9rem; transition: all var(--transition); outline: none; resize: none; }
    .form-control:focus { border-color: var(--cyan); background: rgba(56,189,248,0.05); box-shadow: 0 0 0 3px rgba(56,189,248,0.12); }
    .form-control::placeholder { color: var(--text3); }
    textarea.form-control { min-height: 120px; }
    .btn-submit { width: 100%; display: flex; align-items: center; justify-content: center; gap: 0.5rem; padding: 0.85rem; border-radius: 10px; background: linear-gradient(135deg, var(--cyan), var(--blue)); color: #fff; border: none; font-family: 'DM Sans', sans-serif; font-size: 0.9rem; font-weight: 600; cursor: pointer; transition: all var(--transition); }
    .btn-submit:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(56,189,248,0.4); }
    .btn-submit:disabled { opacity: 0.6; cursor: not-allowed; transform: none; }
    .form-success { display: none; text-align: center; padding: 1rem; color: var(--cyan); font-size: 0.9rem; }
    @media (max-width: 768px) { .contact-grid { grid-template-columns: 1fr; } }

    /* FOOTER */
    footer { padding: 2rem 5%; border-top: 1px solid var(--border); background: var(--bg); display: flex; align-items: center; justify-content: flex-start;flex-direction: column-reverse; flex-wrap: wrap; gap: 1rem; }
    .footer-copy { font-size: 0.8rem; color: var(--text3); font-family: 'JetBrains Mono', monospace; }
    .footer-socials { display: flex; gap: 0.75rem; }
    .social-link { width: 38px; height: 38px; border-radius: 10px; background: var(--surface); border: 1px solid var(--border); display: flex; align-items: center; justify-content: center; text-decoration: none; color: var(--text2); font-size: 1rem; transition: all var(--transition); }
    .social-link:hover { border-color: var(--cyan); color: var(--cyan); box-shadow: var(--glow); transform: translateY(-2px); }

    /* BACK TO TOP */
    #back-top { position: fixed; bottom: 1rem; right: 1rem; z-index: 999; width: 46px; height: 46px; border-radius: 12px; background: linear-gradient(135deg, var(--cyan), var(--blue)); border: none; cursor: pointer; color: #fff; font-size: 1.1rem; box-shadow: 0 4px 20px rgba(56,189,248,0.35); transition: all var(--transition); opacity: 0; pointer-events: none; display: flex; align-items: center; justify-content: center; }
    #back-top.visible { opacity: 1; pointer-events: auto; }
    #back-top:hover { transform: translateY(-3px); box-shadow: 0 8px 28px rgba(56,189,248,0.5); }

    /* REVEAL */
    .reveal { opacity: 0; transform: translateY(30px); transition: opacity 0.7s cubic-bezier(0.4,0,0.2,1), transform 0.7s cubic-bezier(0.4,0,0.2,1); }
    .reveal.revealed { opacity: 1; transform: translateY(0); }
    .reveal-delay-1 { transition-delay: 0.1s; }
    .reveal-delay-2 { transition-delay: 0.2s; }
    .reveal-delay-3 { transition-delay: 0.3s; }
    .reveal-delay-4 { transition-delay: 0.4s; }
  </style>
</head>
<body>

<div id="scroll-progress"></div>
<div id="tsparticles"></div>
<button id="back-top" aria-label="Back to top">&#8593;</button>

<div class="wrapper">

  <!-- NAVBAR -->
  <nav id="navbar" role="navigation" aria-label="Main navigation">
    <a href="#hero" class="nav-logo">YH</a>
    <ul class="nav-links" id="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#education">Education</a></li>
      <li><a href="#contact" class="nav-cta">Contact</a></li>
    </ul>
    <button class="nav-toggle" id="nav-toggle" aria-label="Toggle navigation" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
  </nav>

  <!-- HERO -->
  <section id="hero" aria-label="Hero">
    <div class="hero-inner">
      <div class="hero-content">
        <div class="hero-badge">Knowledge isn't stored, it's engineered.</div>
        <h1 class="hero-name">
          <span class="gradient-text">Yassa</span><br>Hammam
        </h1>
        <div class="hero-title">
          <span id="typed-text"></span><span class="typed-cursor"></span>
        </div>
        <p class="hero-tagline">Transforming Data Into Insights &amp; Building Intelligent Systems</p>
        <div class="hero-buttons">
          <a href="#projects" class="btn btn-primary">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="7" height="7"/><rect x="14" y="3" width="7" height="7"/><rect x="14" y="14" width="7" height="7"/><rect x="3" y="14" width="7" height="7"/></svg>
            View Projects
          </a>
          <a href="#contact" class="btn btn-outline">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
            Contact Me
          </a>
          <a href="#" class="btn btn-ghost" id="cv-btn">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15v4a2 2 0 01-2 2H5a2 2 0 01-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
            Download CV
          </a>
        </div>
      </div>
      <div class="hero-visual">
        <div class="avatar-ring">
          <div class="ring-outer"></div>
          <div class="ring-inner"></div>
          <div class="avatar-core">
                   <img src="profile.png" alt="Yassa Hammam" class="avatar-img">

          </div>
          <div class="avatar-glow"></div>
          <div class="float-chip chip1">
            <span class="chip-dot" style="background:#38bdf8;box-shadow:0 0 6px #38bdf8"></span>Power BI
          </div>
          <div class="float-chip chip2">
            <span class="chip-dot" style="background:#a855f7;box-shadow:0 0 6px #a855f7"></span>Python
          </div>
          <div class="float-chip chip3">
            <span class="chip-dot" style="background:#06b6d4;box-shadow:0 0 6px #06b6d4"></span>SQL
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" aria-label="About">
    <div class="about-grid">
      <div class="about-text reveal">
        <div class="section-label">About Me</div>
        <h2 class="section-title">Building at the intersection of<br><span class="gradient-text">Data &amp; AI</span></h2>
        <div class="section-divider"></div>
        <p>I'm a Computer Science &amp; Artificial Intelligence student at Helwan University with a strong foundation in programming, data structures, databases, and analytics.</p>
        <p>Experienced with industry-standard tools including <strong style="color:var(--cyan)">Power BI, SQL, Excel,</strong> and <strong style="color:var(--cyan)">Tableau</strong>. My work spans end-to-end data workflows — from raw collection to actionable visual insights.</p>
        <p>Deeply interested in <strong style="color:var(--purple)">Data Engineering, ETL Pipelines, Cloud Data Systems,</strong> and <strong style="color:var(--purple)">AI-driven analytics</strong>. Currently seeking internship opportunities to turn academic foundations into real-world impact.</p>
        <div class="about-tags">
          <span class="tag">Data Engineering</span>
          <span class="tag">ETL Pipelines</span>
          <span class="tag">Machine Learning</span>
          <span class="tag">Cloud Systems</span>
          <span class="tag">AI Analytics</span>
          <span class="tag">Data Viz</span>
          <span class="tag">Problem Solving</span>
        </div>
      </div>
      <div class="about-stats reveal reveal-delay-2">
        <div class="stat-card">
          <div class="stat-num" data-count="10">0</div>
          <div class="stat-label">Projects Completed</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">3.15<span style="font-size:1rem;color:var(--text2)">/4.0</span></div>
          <div class="stat-label">Current GPA</div>
        </div>
        <div class="stat-card">
          <div class="stat-num" data-count="2">0</div>
          <div class="stat-label">Certifications Earned</div>
        </div>
        <div class="stat-card">
          <div class="stat-num" data-count="5">0</div>
          <div class="stat-label">Tools Mastered</div>
        </div>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills" aria-label="Skills">
    <div class="content-wrap">
      <div class="reveal">
        <div class="section-label">Technical Toolkit</div>
        <h2 class="section-title">Skills &amp; <span class="gradient-text">Technologies</span></h2>
        <div class="section-divider"></div>
      </div>
      <div class="skills-grid">
        <div class="skill-cat reveal reveal-delay-1">
          <span class="skill-cat-icon">&#x2328;&#xFE0F;</span>
          <div class="skill-cat-title">Programming Languages</div>
          <div class="skill-pills">
            <span class="skill-pill">Python</span><span class="skill-pill">Java</span>
            <span class="skill-pill">JavaScript</span><span class="skill-pill">HTML</span><span class="skill-pill">CSS</span>
          </div>
        </div>
        <div class="skill-cat reveal reveal-delay-2">
          <span class="skill-cat-icon">&#x1F5C4;&#xFE0F;</span>
          <div class="skill-cat-title">Databases</div>
          <div class="skill-pills">
            <span class="skill-pill">SQL</span><span class="skill-pill">MySQL</span><span class="skill-pill">DBMS</span>
          </div>
        </div>
        <div class="skill-cat reveal reveal-delay-3">
          <span class="skill-cat-icon">&#x1F4CA;</span>
          <div class="skill-cat-title">Data &amp; Analytics Tools</div>
          <div class="skill-pills">
            <span class="skill-pill">Power BI</span><span class="skill-pill">Excel</span>
            <span class="skill-pill">Tableau</span><span class="skill-pill">Kaggle</span>
          </div>
        </div>
        <div class="skill-cat reveal reveal-delay-4">
          <span class="skill-cat-icon">&#x1F52C;</span>
          <div class="skill-cat-title">Core Concepts</div>
          <div class="skill-pills">
            <span class="skill-pill">ETL</span><span class="skill-pill">Data Cleaning</span>
            <span class="skill-pill">Data Visualization</span><span class="skill-pill">Data Structures</span>
            <span class="skill-pill">OOP</span><span class="skill-pill">Data Mining</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE -->
  <section id="experience" aria-label="Experience">
    <div class="content-wrap">
      <div class="reveal">
        <div class="section-label">Work Experience</div>
        <h2 class="section-title">Professional <span class="gradient-text">Experience</span></h2>
        <div class="section-divider"></div>
      </div>
      <div class="exp-card reveal reveal-delay-1">
        <div class="exp-header">
          <div class="exp-logo">&#x1F4E1;</div>
          <div class="exp-meta">
            <div class="exp-role">Data Analysis Trainee</div>
            <div class="exp-company">National Telecommunication Institute (NTI)</div>
            <div class="exp-period">Remote Training &middot; 2024</div>
          </div>
        </div>
        <ul class="exp-list">
          <li>Data collection &amp; preprocessing for real-world datasets</li>
          <li>SQL-based analysis and query optimization</li>
          <li>Excel reporting with advanced formulas and pivot tables</li>
          <li>Power BI dashboard development and interactive visualizations</li>
          <li>Extracting statistical insights from complex datasets</li>
          <li>Completed end-to-end real-world data analysis projects</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects" aria-label="Projects">
    <div class="projects-header reveal">
      <div class="section-label">Portfolio</div>
      <h2 class="section-title">Featured <span class="gradient-text">Projects</span></h2>
      <div class="section-divider"></div>
      <div class="tab-switcher" role="tablist">
        <button class="tab-btn active" role="tab" aria-selected="true" data-tab="web">&#x1F310; Web Development</button>
        <button class="tab-btn" role="tab" aria-selected="false" data-tab="data">&#x1F4CA; Data Analytics</button>
      </div>
    </div>

    <div class="projects-pane active" id="pane-web">
      <div class="projects-grid">
        <div class="proj-card reveal">
          <div class="proj-header">
            <span class="proj-number">01</span>
            <span class="proj-type-badge badge-web">Web Dev</span>
          </div>
          <div class="proj-title">&#x1F374; Restaurant Website</div>
          <p class="proj-problem">Many small restaurants need a modern online presence to showcase menus and improve customer experience across digital touchpoints.</p>
          <div class="proj-stack">
            <span class="stack-pill">HTML5</span><span class="stack-pill">CSS3</span><span class="stack-pill">JavaScript</span>
          </div>
          <div class="proj-insights">
            <h5>Key Features</h5>
            <ul>
              <li>Fully responsive mobile-first design</li>
              <li>Interactive menu browsing system</li>
              <li>Smooth scroll navigation</li>
              <li>Clean modern UI layout</li>
            </ul>
          </div>
          <div class="proj-outcome"><strong>Outcome:</strong> Improved digital presence with a structured, conversion-friendly UI.</div>
        </div>
        <div class="proj-card reveal reveal-delay-2">
          <div class="proj-header">
            <span class="proj-number">02</span>
            <span class="proj-type-badge badge-web">Web Dev</span>
          </div>
          <div class="proj-title">&#x2708;&#xFE0F; Tourism Website</div>
          <p class="proj-problem">Tourism destinations need attractive digital platforms to showcase places, attractions, and encourage visitor exploration.</p>
          <div class="proj-stack">
            <span class="stack-pill">HTML5</span><span class="stack-pill">CSS3</span><span class="stack-pill">JavaScript</span>
          </div>
          <div class="proj-insights">
            <h5>Key Features</h5>
            <ul>
              <li>Responsive destination showcase sections</li>
              <li>Smooth scrolling navigation</li>
              <li>Interactive UI components</li>
              <li>Visual storytelling layout</li>
            </ul>
          </div>
          <div class="proj-outcome"><strong>Outcome:</strong> Enhanced user engagement through an immersive browsing experience.</div>
        </div>
      </div>
    </div>

    <div class="projects-pane" id="pane-data">
      <div class="projects-grid">
        <div class="proj-card reveal">
          <div class="proj-header">
            <span class="proj-number">03</span>
            <span class="proj-type-badge badge-data">Data Analytics</span>
          </div>
          <div class="proj-title">&#x1F3B5; Spotify Data Analysis</div>
          <p class="proj-problem">Analyze music streaming trends and user behavior patterns from a large Spotify dataset to uncover actionable insights.</p>
          <div class="proj-stack">
            <span class="stack-pill">Excel</span><span class="stack-pill">Power BI</span><span class="stack-pill">Kaggle</span>
          </div>
          <div class="proj-insights">
            <h5>Key Insights</h5>
            <ul>
              <li>Top artists and trending tracks</li>
              <li>Genre distribution analysis</li>
              <li>Listening trends over time</li>
              <li>User behavior patterns</li>
            </ul>
          </div>
          <div class="proj-outcome"><strong>Outcome:</strong> Clear insights into music consumption patterns via interactive dashboards.</div>
        </div>
        <div class="proj-card reveal reveal-delay-2">
          <div class="proj-header">
            <span class="proj-number">04</span>
            <span class="proj-type-badge badge-data">Data Analytics</span>
          </div>
          <div class="proj-title">&#x1F6D2; Amazon Sales Analysis</div>
          <p class="proj-problem">Analyze product sales performance and customer behavior to identify business opportunities and revenue growth drivers.</p>
          <div class="proj-stack">
            <span class="stack-pill">Excel</span><span class="stack-pill">Power BI</span><span class="stack-pill">Kaggle</span>
          </div>
          <div class="proj-insights">
            <h5>Key Insights</h5>
            <ul>
              <li>Top-performing products ranking</li>
              <li>Revenue trend analysis</li>
              <li>Category performance breakdown</li>
              <li>Customer segmentation</li>
            </ul>
          </div>
          <div class="proj-outcome"><strong>Outcome:</strong> Identified key business opportunities from sales data patterns.</div>
        </div>
        <div class="proj-card reveal reveal-delay-3">
          <div class="proj-header">
            <span class="proj-number">05</span>
            <span class="proj-type-badge badge-data">Data Analytics</span>
          </div>
          <div class="proj-title">&#x26A1; Electric Vehicles Dashboard</div>
          <p class="proj-problem">Analyze the EV market landscape — models, brands, range, and adoption trends — for comprehensive industry insight.</p>
          <div class="proj-stack">
            <span class="stack-pill">Excel</span><span class="stack-pill">Power BI</span>
            <span class="stack-pill">Tableau</span><span class="stack-pill">Kaggle</span>
          </div>
          <div class="proj-insights">
            <h5>Key Insights</h5>
            <ul>
              <li>264 EV models analyzed</li>
              <li>35+ brands comparison</li>
              <li>Range performance metrics</li>
              <li>Market trends overview</li>
            </ul>
          </div>
          <div class="proj-outcome"><strong>Outcome:</strong> Comprehensive view of EV industry landscape with actionable market insights.</div>
        </div>
      </div>
    </div>
  </section>

  <!-- EDUCATION -->
  <section id="education" aria-label="Education">
    <div class="content-wrap">
      <div class="reveal">
        <div class="section-label">Academic Background</div>
        <h2 class="section-title">Education &amp; <span class="gradient-text">Certifications</span></h2>
        <div class="section-divider"></div>
      </div>
      <div class="edu-cert-grid">
        <div class="edu-card reveal">
          <div class="edu-icon">&#x1F393;</div>
          <div class="edu-degree">Computer Science &amp; Artificial Intelligence</div>
          <div class="edu-uni">Helwan University</div>
          <p style="color:var(--text2);font-size:0.875rem;margin-top:0.5rem;line-height:1.7">Pursuing a Bachelor's degree with focus on algorithms, machine learning, data systems, and software engineering fundamentals.</p>
          <div class="edu-meta">
            <span class="edu-badge">2024 &ndash; 2028</span>
            <span class="edu-badge gpa">GPA: 3.15 / 4.0</span>
          </div>
        </div>
        <div class="certs-list reveal reveal-delay-2">
          <h3 style="font-family:'Syne',sans-serif;font-size:1.05rem;margin-bottom:0.75rem;color:var(--text2)">Certifications</h3>
          <div class="cert-item">
            <div class="cert-icon">&#x1F4C8;</div>
            <div>
              <div class="cert-name">Data Analytics Certification</div>
              <div class="cert-issuer">National Telecommunication Institute &middot; NTI</div>
            </div>
          </div>
          <div class="cert-item">
            <div class="cert-icon">&#x1F9E0;</div>
            <div>
              <div class="cert-name">Getting Started with Deep Learning</div>
              <div class="cert-issuer">NVIDIA &middot; Deep Learning Institute</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- WHY HIRE ME -->
  <section id="why" aria-label="Why hire me">
    <div class="why-grid">
      <div class="reveal">
        <div class="section-label">Value Proposition</div>
        <h2 class="section-title">Why <span class="gradient-text">Hire Me?</span></h2>
        <div class="section-divider"></div>
        <div class="why-traits">
          <div class="why-trait"><div class="why-trait-icon">&#x1F9E9;</div><div class="why-trait-name">Problem Solving</div></div>
          <div class="why-trait"><div class="why-trait-icon">&#x1F4D0;</div><div class="why-trait-name">Analytical Thinking</div></div>
          <div class="why-trait"><div class="why-trait-icon">&#x26A1;</div><div class="why-trait-name">Fast Learner</div></div>
          <div class="why-trait"><div class="why-trait-icon">&#x1F91D;</div><div class="why-trait-name">Team Player</div></div>
          <div class="why-trait"><div class="why-trait-icon">&#x1F916;</div><div class="why-trait-name">Passion for AI</div></div>
          <div class="why-trait"><div class="why-trait-icon">&#x1F504;</div><div class="why-trait-name">Adaptability</div></div>
          <div class="why-trait"><div class="why-trait-icon">&#x1F331;</div><div class="why-trait-name">Growth Mindset</div></div>
          <div class="why-trait"><div class="why-trait-icon">&#x1F3AF;</div><div class="why-trait-name">Goal-Oriented</div></div>
        </div>
      </div>
      <div class="why-achievements reveal reveal-delay-2">
        <div class="achieve-card">
          <div class="achieve-num" data-count="10">0</div>
          <div>
            <div class="achieve-label" style="font-weight:600;color:var(--text);margin-bottom:0.2rem">Projects Built</div>
            <div class="achieve-label">From web apps to data analytics dashboards</div>
          </div>
        </div>
        <div class="achieve-card">
          <div class="achieve-num">3.15</div>
          <div>
            <div class="achieve-label" style="font-weight:600;color:var(--text);margin-bottom:0.2rem">GPA Score</div>
            <div class="achieve-label">Strong academic performance in CS &amp; AI</div>
          </div>
        </div>
        <div class="achieve-card">
          <div class="achieve-num" data-count="2">0</div>
          <div>
            <div class="achieve-label" style="font-weight:600;color:var(--text);margin-bottom:0.2rem">Certifications</div>
            <div class="achieve-label">NTI Data Analytics + NVIDIA Deep Learning</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" aria-label="Contact">
    <div class="content-wrap">
      <div class="reveal" style="text-align:center;margin-bottom:3rem">
        <div class="section-label" style="justify-content:center;margin-bottom:0.75rem">
          <span style="font-family:'JetBrains Mono',monospace;font-size:0.75rem;letter-spacing:0.2em;color:var(--cyan);text-transform:uppercase">Get In Touch</span>
        </div>
        <h2 class="section-title">Let's <span class="gradient-text">Connect</span></h2>
        <p style="color:var(--text2);max-width:500px;margin:0 auto">Open to internship opportunities, data engineering roles, and collaborations. Let's build something impactful together.</p>
      </div>
      <div class="contact-grid">
        <div class="contact-info reveal">
          <a href="mailto:yassahammam.business@gmail.com" class="contact-link">
            <div class="contact-link-icon">&#x2709;&#xFE0F;</div>
            <div>
              <div class="contact-link-label">Email</div>
              <div class="contact-link-val">yassahammam.business@gmail.com</div>
            </div>
          </a>
          <a href="tel:010201010204011" class="contact-link">
            <div class="contact-link-icon">&#x1F4DE;</div>
            <div>
              <div class="contact-link-label">Phone</div>
              <div class="contact-link-val">01010204011</div>
            </div>
          </a>
          <a href="https://www.linkedin.com/in/yassa-hammam" target="_blank" rel="noopener noreferrer" class="contact-link">
            <div class="contact-link-icon">&#x1F4BC;</div>
            <div>
              <div class="contact-link-label">LinkedIn</div>
              <div class="contact-link-val">linkedin.com/in/yassa-hammam</div>
            </div>
          </a>
          <a href="https://github.com/Yassa-Hammam" target="_blank" rel="noopener noreferrer" class="contact-link">
            <div class="contact-link-icon">&#x1F419;</div>
            <div>
              <div class="contact-link-label">GitHub</div>
              <div class="contact-link-val">github.com/yassahammam</div>
            </div>
          </a>
        </div>
        <div class="contact-form reveal reveal-delay-2">
          <form id="contact-form" novalidate>
            <div class="form-group">
              <label class="form-label" for="cf-name">Your Name</label>
              <input type="text" id="cf-name" class="form-control" placeholder="Your Name" required autocomplete="name" />
            </div>
            <div class="form-group">
              <label class="form-label" for="cf-email">Email Address</label>
              <input type="email" id="cf-email" class="form-control" placeholder="Your Email" required autocomplete="email" />
            </div>
            <div class="form-group">
              <label class="form-label" for="cf-msg">Message</label>
              <textarea id="cf-msg" class="form-control" placeholder="Tell me about your opportunity..." required></textarea>
            </div>
            <button type="submit" class="btn-submit" id="submit-btn">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
              Send Message
            </button>
            <div class="form-success" id="form-success">&#x2705; Message sent! I'll get back to you soon.</div>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer role="contentinfo">
    <div class="footer-copy">&copy;  Yassa Hammam</div>
    <div class="footer-socials">
      <a href="https://www.linkedin.com/in/yassa-hammam" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="LinkedIn">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"/><circle cx="4" cy="4" r="2"/></svg>
      </a>
      <a href="https://github.com/Yassa-Hammam" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="GitHub">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 00-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0020 4.77 5.07 5.07 0 0019.91 1S18.73.65 16 2.48a13.38 13.38 0 00-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 005 4.77a5.44 5.44 0 00-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 009 18.13V22"/></svg>
      </a>
      <a href="mailto:yassahammam.business@gmail.com" class="social-link" aria-label="Email">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
      </a>
    </div>
  </footer>
</div>

<script>
/* PARTICLES */
tsParticles.load("tsparticles",{
  background:{color:{value:"transparent"}},
  fpsLimit:60,
  particles:{
    number:{value:55,density:{enable:true,area:900}},
    color:{value:["#38bdf8","#a855f7","#3b82f6"]},
    shape:{type:"circle"},
    opacity:{value:{min:0.1,max:0.4},animation:{enable:true,speed:1,minimumValue:0.05}},
    size:{value:{min:1,max:2.5}},
    links:{enable:true,distance:130,color:"#38bdf8",opacity:0.07,width:1},
    move:{enable:true,speed:0.5,direction:"none",random:true,outModes:{default:"bounce"}}
  },
  interactivity:{
    events:{onHover:{enable:true,mode:"grab"},onClick:{enable:true,mode:"push"}},
    modes:{grab:{distance:130,links:{opacity:0.2}},push:{quantity:2}}
  },
  detectRetina:true
});

/* TYPED TEXT */
(function(){
  const phrases=["Data Engineer","Data Analyst","AI Enthusiast","Python Developer","ETL Engineer","Power BI Developer"];
  let pi=0,ci=0,del=false,el=document.getElementById("typed-text");
  function tick(){
    const cur=phrases[pi];
    el.textContent=del?cur.substring(0,ci--):cur.substring(0,ci++);
    let spd=del?55:100;
    if(!del&&ci===cur.length+1){spd=1800;del=true;}
    else if(del&&ci===0){del=false;pi=(pi+1)%phrases.length;spd=400;}
    setTimeout(tick,spd);
  }
  setTimeout(tick,900);
})();

/* NAVBAR */
const navbar=document.getElementById("navbar");
window.addEventListener("scroll",()=>navbar.classList.toggle("scrolled",window.scrollY>50));

/* NAV TOGGLE */
const toggle=document.getElementById("nav-toggle"),links=document.getElementById("nav-links");
toggle.addEventListener("click",()=>{
  const open=links.classList.toggle("open");
  toggle.setAttribute("aria-expanded",open);
});
links.querySelectorAll("a").forEach(a=>a.addEventListener("click",()=>{
  links.classList.remove("open");
  toggle.setAttribute("aria-expanded","false");
}));

/* SCROLL PROGRESS */
const prog=document.getElementById("scroll-progress");
window.addEventListener("scroll",()=>{
  prog.style.width=((window.scrollY/(document.body.scrollHeight-window.innerHeight))*100)+"%";
});

/* BACK TO TOP */
const backTop=document.getElementById("back-top");
window.addEventListener("scroll",()=>backTop.classList.toggle("visible",window.scrollY>400));
backTop.addEventListener("click",()=>window.scrollTo({top:0,behavior:"smooth"}));

/* SCROLL REVEAL */
const revealObs=new IntersectionObserver((entries)=>{
  entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add("revealed");revealObs.unobserve(e.target);}});
},{threshold:0.12,rootMargin:"0px 0px -50px 0px"});
document.querySelectorAll(".reveal").forEach(el=>revealObs.observe(el));

/* COUNTERS */
const cntObs=new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(!e.isIntersecting)return;
    const el=e.target,target=parseInt(el.dataset.count);
    let n=0,dur=1500,step=Math.max(dur/target,16);
    const t=setInterval(()=>{n++;el.textContent=n;if(n>=target)clearInterval(t);},step);
    cntObs.unobserve(el);
  });
},{threshold:0.5});
document.querySelectorAll("[data-count]").forEach(el=>cntObs.observe(el));

/* TABS */
document.querySelectorAll(".tab-btn").forEach(btn=>{
  btn.addEventListener("click",()=>{
    document.querySelectorAll(".tab-btn").forEach(b=>{b.classList.remove("active");b.setAttribute("aria-selected","false");});
    document.querySelectorAll(".projects-pane").forEach(p=>p.classList.remove("active"));
    btn.classList.add("active");btn.setAttribute("aria-selected","true");
    const pane=document.getElementById("pane-"+btn.dataset.tab);
    pane.classList.add("active");
    pane.querySelectorAll(".reveal").forEach(el=>{if(!el.classList.contains("revealed"))revealObs.observe(el);});
  });
});

/* CONTACT FORM */
document.getElementById("contact-form").addEventListener("submit",function(e){
  e.preventDefault();
  const btn=document.getElementById("submit-btn"),suc=document.getElementById("form-success");
  btn.disabled=true;
  btn.innerHTML='<svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" style="animation:spin 1s linear infinite"><circle cx="12" cy="12" r="10" stroke-dasharray="31.4" stroke-dashoffset="10"/></svg> Sending...';
  setTimeout(()=>{btn.style.display="none";suc.style.display="block";this.reset();},1800);
});

/* CV DOWNLOAD */
document.getElementById("cv-btn").addEventListener("click",function(e){
  e.preventDefault();
  alert("To enable CV download: replace the href on this button with your actual PDF URL.\n\nExample: <a href='your-cv.pdf' download>");
});
</script>
</body>
</html>
