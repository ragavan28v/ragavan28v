<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RAGAVAN V — Full Stack + AI Systems Engineer</title>
    <link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Playfair+Display:wght@600;700;800&family=IBM+Plex+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #0a0e27;
            --secondary: #1a1f3a;
            --accent: #00d9ff;
            --accent-alt: #ff006e;
            --text-primary: #ffffff;
            --text-secondary: #b0b8d4;
            --border: rgba(0, 217, 255, 0.1);
            --glow: rgba(0, 217, 255, 0.2);
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'IBM Plex Sans', sans-serif;
            background: linear-gradient(135deg, var(--primary) 0%, #0f1b35 50%, var(--primary) 100%);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* HERO SECTION */
        /* ═══════════════════════════════════════════════════════════════ */

        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 60px 20px;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -20%;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(0, 217, 255, 0.15) 0%, transparent 70%);
            border-radius: 50%;
            animation: float 15s ease-in-out infinite;
            z-index: -1;
        }

        .hero::after {
            content: '';
            position: absolute;
            bottom: -30%;
            left: -15%;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(255, 0, 110, 0.1) 0%, transparent 70%);
            border-radius: 50%;
            animation: float 18s ease-in-out infinite reverse;
            z-index: -1;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-30px); }
        }

        .hero-content {
            text-align: center;
            max-width: 1000px;
            z-index: 1;
            animation: fadeInUp 1.2s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(3rem, 8vw, 5.5rem);
            font-weight: 800;
            margin-bottom: 12px;
            background: linear-gradient(135deg, var(--text-primary) 0%, var(--accent) 50%, var(--text-primary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -2px;
            animation: shimmer 3s ease-in-out infinite;
        }

        @keyframes shimmer {
            0%, 100% { filter: brightness(1); }
            50% { filter: brightness(1.1); }
        }

        .hero-subtitle {
            font-family: 'Space Mono', monospace;
            font-size: 1.1rem;
            color: var(--accent);
            margin-bottom: 40px;
            letter-spacing: 3px;
            text-transform: uppercase;
            font-weight: 400;
        }

        .tagline {
            font-size: 1.3rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto 50px;
            line-height: 1.8;
            font-weight: 300;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .btn {
            padding: 14px 32px;
            border: 2px solid var(--accent);
            background: transparent;
            color: var(--accent);
            font-family: 'Space Mono', monospace;
            font-size: 0.95rem;
            cursor: pointer;
            border-radius: 4px;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            position: relative;
            overflow: hidden;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: var(--accent);
            z-index: -1;
            transition: left 0.3s ease;
        }

        .btn:hover {
            color: var(--primary);
            transform: translateY(-3px);
        }

        .btn:hover::before {
            left: 0;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* SECTIONS */
        /* ═══════════════════════════════════════════════════════════════ */

        section {
            padding: 80px 20px;
            position: relative;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2rem, 5vw, 3.5rem);
            margin-bottom: 60px;
            text-align: center;
            position: relative;
            display: inline-block;
            width: 100%;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
            margin: 20px auto 0;
            border-radius: 2px;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* FLAGSHIP PROJECT */
        /* ═══════════════════════════════════════════════════════════════ */

        .flagship {
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.05) 0%, rgba(255, 0, 110, 0.05) 100%);
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 60px 40px;
            max-width: 900px;
            margin: 0 auto;
            backdrop-filter: blur(10px);
            position: relative;
            overflow: hidden;
        }

        .flagship::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(0, 217, 255, 0.1) 0%, transparent 70%);
            border-radius: 50%;
            z-index: -1;
        }

        .flagship-header {
            display: flex;
            align-items: center;
            gap: 30px;
            margin-bottom: 40px;
        }

        .flagship-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--accent), var(--accent-alt));
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
        }

        .flagship-meta h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            margin-bottom: 10px;
        }

        .flagship-meta p {
            color: var(--text-secondary);
            font-size: 1rem;
            margin-bottom: 15px;
        }

        .tech-stack {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-top: 15px;
        }

        .tech-badge {
            padding: 6px 14px;
            background: rgba(0, 217, 255, 0.1);
            border: 1px solid var(--accent);
            border-radius: 20px;
            font-size: 0.85rem;
            color: var(--accent);
            font-family: 'Space Mono', monospace;
        }

        .build-status {
            display: inline-block;
            padding: 8px 20px;
            background: rgba(255, 200, 0, 0.15);
            border: 1px solid rgba(255, 200, 0, 0.3);
            border-radius: 4px;
            color: #ffc800;
            font-family: 'Space Mono', monospace;
            font-size: 0.9rem;
            margin-top: 20px;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* PROJECTS GRID */
        /* ═══════════════════════════════════════════════════════════════ */

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .project-card {
            background: linear-gradient(135deg, rgba(26, 31, 58, 0.8) 0%, rgba(26, 31, 58, 0.5) 100%);
            border: 1px solid var(--border);
            border-radius: 10px;
            padding: 35px;
            transition: all 0.4s cubic-bezier(0.23, 1, 0.320, 1);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200px;
            height: 200px;
            background: radial-gradient(circle, var(--glow) 0%, transparent 70%);
            border-radius: 50%;
            opacity: 0;
            transition: opacity 0.4s ease;
            z-index: 0;
        }

        .project-card:hover {
            border-color: var(--accent);
            transform: translateY(-10px);
            background: linear-gradient(135deg, rgba(26, 31, 58, 0.95) 0%, rgba(26, 31, 58, 0.7) 100%);
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-content {
            position: relative;
            z-index: 1;
        }

        .project-icon {
            width: 50px;
            height: 50px;
            margin-bottom: 20px;
            opacity: 0.8;
        }

        .project-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.6rem;
            margin-bottom: 15px;
            color: var(--text-primary);
        }

        .project-description {
            color: var(--text-secondary);
            font-size: 0.95rem;
            line-height: 1.7;
            margin-bottom: 25px;
            flex-grow: 1;
        }

        .project-tech {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            margin-bottom: 25px;
        }

        .project-tech-item {
            padding: 4px 10px;
            background: rgba(0, 217, 255, 0.08);
            border: 1px solid rgba(0, 217, 255, 0.3);
            border-radius: 3px;
            font-size: 0.8rem;
            font-family: 'Space Mono', monospace;
            color: var(--accent);
        }

        .project-links {
            display: flex;
            gap: 12px;
        }

        .project-link {
            flex: 1;
            padding: 10px 16px;
            border: 1px solid var(--accent);
            background: transparent;
            color: var(--accent);
            border-radius: 4px;
            cursor: pointer;
            font-family: 'Space Mono', monospace;
            font-size: 0.85rem;
            text-decoration: none;
            text-align: center;
            transition: all 0.3s ease;
            display: inline-block;
        }

        .project-link:hover {
            background: var(--accent);
            color: var(--primary);
            transform: translateY(-2px);
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* UPCOMING PROJECT */
        /* ═══════════════════════════════════════════════════════════════ */

        .upcoming-section {
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.02) 0%, rgba(255, 0, 110, 0.02) 100%);
            border: 2px dashed var(--border);
            border-radius: 12px;
            padding: 60px 40px;
            text-align: center;
            max-width: 700px;
            margin: 0 auto;
            position: relative;
        }

        .upcoming-badge {
            display: inline-block;
            padding: 8px 20px;
            background: rgba(0, 217, 255, 0.15);
            border: 1px solid var(--accent);
            border-radius: 20px;
            color: var(--accent);
            font-family: 'Space Mono', monospace;
            font-size: 0.85rem;
            margin-bottom: 20px;
        }

        .upcoming-title {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--text-primary);
        }

        .upcoming-description {
            color: var(--text-secondary);
            font-size: 1rem;
            line-height: 1.8;
            margin-bottom: 25px;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* STATS SECTION */
        /* ═══════════════════════════════════════════════════════════════ */

        .stats-section {
            background: var(--secondary);
            padding: 100px 20px;
        }

        .stats-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.08) 0%, rgba(255, 0, 110, 0.08) 100%);
            border: 1px solid var(--border);
            padding: 40px;
            border-radius: 10px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
        }

        .stat-number {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            color: var(--accent);
            margin-bottom: 10px;
        }

        .stat-label {
            color: var(--text-secondary);
            font-family: 'Space Mono', monospace;
            font-size: 0.95rem;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .chart-container {
            background: linear-gradient(135deg, rgba(26, 31, 58, 0.8) 0%, rgba(26, 31, 58, 0.5) 100%);
            border: 1px solid var(--border);
            border-radius: 10px;
            padding: 30px;
            margin-bottom: 30px;
        }

        .chart-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            margin-bottom: 20px;
            color: var(--text-primary);
        }

        .chart-placeholder {
            height: 300px;
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.05) 0%, rgba(255, 0, 110, 0.05) 100%);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-secondary);
            font-family: 'Space Mono', monospace;
            font-size: 0.9rem;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* SKILLS & STACK */
        /* ═══════════════════════════════════════════════════════════════ */

        .stack-section {
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.02) 0%, rgba(15, 27, 53, 1) 100%);
        }

        .stack-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            gap: 20px;
            max-width: 1000px;
            margin: 0 auto;
        }

        .stack-item {
            background: rgba(26, 31, 58, 0.8);
            border: 1px solid var(--border);
            padding: 25px;
            border-radius: 8px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .stack-item::before {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(135deg, transparent, rgba(0, 217, 255, 0.1));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .stack-item:hover {
            border-color: var(--accent);
            transform: translateY(-8px);
            background: rgba(26, 31, 58, 0.95);
        }

        .stack-item:hover::before {
            opacity: 1;
        }

        .stack-icon {
            font-size: 2.5rem;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .stack-name {
            font-size: 0.9rem;
            color: var(--text-secondary);
            font-family: 'Space Mono', monospace;
            position: relative;
            z-index: 1;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* PHILOSOPHY SECTION */
        /* ═══════════════════════════════════════════════════════════════ */

        .philosophy {
            text-align: center;
            padding: 100px 40px;
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.08) 0%, rgba(255, 0, 110, 0.08) 100%);
            border: 1px solid var(--border);
            border-radius: 12px;
            max-width: 900px;
            margin: 0 auto;
            position: relative;
        }

        .philosophy::before {
            content: '"';
            position: absolute;
            top: 20px;
            left: 40px;
            font-size: 6rem;
            color: var(--accent);
            opacity: 0.1;
            font-family: 'Playfair Display', serif;
        }

        .philosophy-quote {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            font-style: italic;
            color: var(--text-primary);
            margin-bottom: 30px;
            line-height: 1.5;
        }

        .philosophy-subtitle {
            color: var(--accent);
            font-family: 'Space Mono', monospace;
            letter-spacing: 2px;
            text-transform: uppercase;
            font-size: 0.95rem;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* FOOTER */
        /* ═══════════════════════════════════════════════════════════════ */

        footer {
            background: var(--primary);
            border-top: 1px solid var(--border);
            padding: 40px 20px;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .footer-link {
            color: var(--accent);
            text-decoration: none;
            font-family: 'Space Mono', monospace;
            font-size: 0.9rem;
            transition: color 0.3s ease;
        }

        .footer-link:hover {
            color: var(--accent-alt);
        }

        .footer-text {
            color: var(--text-secondary);
            font-size: 0.9rem;
            font-family: 'Space Mono', monospace;
        }

        /* ═══════════════════════════════════════════════════════════════ */
        /* RESPONSIVE */
        /* ═══════════════════════════════════════════════════════════════ */

        @media (max-width: 768px) {
            .hero {
                min-height: auto;
                padding: 60px 20px;
            }

            .flagship-header {
                flex-direction: column;
                text-align: center;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .stats-grid {
                grid-template-columns: 1fr;
            }

            .footer-links {
                gap: 15px;
            }

            .hero-title {
                font-size: 2.5rem;
            }

            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- HERO SECTION -->
    <section class="hero">
        <div class="hero-content">
            <h1 class="hero-title">RAGAVAN V</h1>
            <p class="hero-subtitle">◦ Full Stack + AI Systems Engineer ◦</p>
            <p class="tagline">
                Architecting production-grade intelligence systems.
                <br>
                Multi-agent orchestration • Secure platforms • Intelligent backends
            </p>
            <div class="cta-buttons">
                <a href="#projects" class="btn">Explore Work</a>
                <a href="#stack" class="btn">View Stack</a>
            </div>
        </div>
    </section>

    <!-- FLAGSHIP PROJECT -->
    <section style="background: linear-gradient(135deg, rgba(10, 14, 39, 0.9) 0%, rgba(15, 27, 53, 0.9) 100%);">
        <h2 class="section-title">◦ Flagship Intelligent System ◦</h2>
        
        <div class="flagship">
            <div class="flagship-header">
                <div class="flagship-icon">🧠</div>
                <div class="flagship-meta">
                    <h3>LEARNING PATH AI</h3>
                    <p>Multi-agent career path planning platform</p>
                </div>
            </div>

            <p style="color: var(--text-secondary); margin-bottom: 30px; line-height: 1.8;">
                Adaptive learning roadmap generation engine powered by structured LLM reasoning and LangGraph orchestration. 
                Intelligently breaks down career progression into modular, personalized learning modules with real-time feedback loops.
            </p>

            <div class="tech-stack">
                <span class="tech-badge">React</span>
                <span class="tech-badge">FastAPI</span>
                <span class="tech-badge">LangGraph</span>
                <span class="tech-badge">LLaMA 3</span>
                <span class="tech-badge">Groq</span>
                <span class="tech-badge">Firebase</span>
                <span class="tech-badge">ReactFlow</span>
            </div>

            <div class="build-status">🟡 Actively Building</div>
        </div>
    </section>

    <!-- DEPLOYED PROJECTS -->
    <section id="projects">
        <h2 class="section-title">◦ Deployed Production Systems ◦</h2>
        
        <div class="projects-grid">
            <!-- ZERO2ELITE -->
            <div class="project-card">
                <div class="project-content">
                    <div class="project-icon">⚡</div>
                    <h3 class="project-title">ZERO2ELITE</h3>
                    <p class="project-description">
                        Gamified productivity engine inspired by RPG progression mechanics. Transform mundane tasks into engaging quests with dynamic reward systems and achievement tracking.
                    </p>
                    <div class="project-tech">
                        <span class="project-tech-item">React</span>
                        <span class="project-tech-item">Gamification</span>
                        <span class="project-tech-item">UI/UX</span>
                    </div>
                    <div class="project-links">
                        <a href="https://progresstracker28.netlify.app/" class="project-link" target="_blank">LIVE DEMO</a>
                        <a href="https://github.com/ragavan28v/zero2elite" class="project-link" target="_blank">REPO</a>
                    </div>
                </div>
            </div>

            <!-- ZAITO -->
            <div class="project-card">
                <div class="project-content">
                    <div class="project-icon">🏦</div>
                    <h3 class="project-title">ZAITO</h3>
                    <p class="project-description">
                        Secure MERN banking platform with enterprise-grade JWT authentication and PIN-protected transactions. Full-stack fintech implementation with real-time dashboards.
                    </p>
                    <div class="project-tech">
                        <span class="project-tech-item">MongoDB</span>
                        <span class="project-tech-item">Express</span>
                        <span class="project-tech-item">React</span>
                        <span class="project-tech-item">Node.js</span>
                        <span class="project-tech-item">JWT</span>
                    </div>
                    <div class="project-links">
                        <a href="https://zaito-bankingapplication.onrender.com/dashboard" class="project-link" target="_blank">LIVE DEMO</a>
                        <a href="https://github.com/ragavan28v/Zaito-BankingApplication" class="project-link" target="_blank">REPO</a>
                    </div>
                </div>
            </div>

            <!-- PHISHSIM -->
            <div class="project-card">
                <div class="project-content">
                    <div class="project-icon">🎯</div>
                    <h3 class="project-title">PHISHSIM</h3>
                    <p class="project-description">
                        AI-driven phishing simulation platform with geo-analytics and campaign tracking. Enterprise security training with intelligent pattern recognition and risk scoring.
                    </p>
                    <div class="project-tech">
                        <span class="project-tech-item">MERN</span>
                        <span class="project-tech-item">Groq API</span>
                        <span class="project-tech-item">Analytics</span>
                    </div>
                    <div class="project-links">
                        <a href="https://phishsim.onrender.com/login" class="project-link" target="_blank">LIVE DEMO</a>
                        <a href="https://github.com/ragavan28v/PhishSim" class="project-link" target="_blank">REPO</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- UPCOMING PROJECT -->
    <section>
        <h2 class="section-title">◦ Upcoming System ◦</h2>
        <div class="upcoming-section">
            <div class="upcoming-badge">🧠 Architecture Phase</div>
            <h3 class="upcoming-title">⚖ CONTRACT RISK RADAR</h3>
            <p class="upcoming-description">
                Explainable NLP engine detecting unfair clauses, hidden penalties, and vague liability traps in legal contracts. 
                Semantic risk scoring with interpretable AI for legal professionals and businesses.
            </p>
            <div class="tech-stack">
                <span class="tech-badge">React</span>
                <span class="tech-badge">NLP Pipelines</span>
                <span class="tech-badge">LLMs</span>
                <span class="tech-badge">Semantic Analysis</span>
            </div>
        </div>
    </section>

    <!-- NEURAL STACK -->
    <section id="stack" class="stack-section">
        <h2 class="section-title">◦ Neural Architecture Stack ◦</h2>
        <div class="stack-grid">
            <div class="stack-item">
                <div class="stack-icon">⚛️</div>
                <div class="stack-name">React</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">🟢</div>
                <div class="stack-name">Node.js</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">🐍</div>
                <div class="stack-name">Python</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">🧠</div>
                <div class="stack-name">TensorFlow</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">🔥</div>
                <div class="stack-name">PyTorch</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">🔥</div>
                <div class="stack-name">Firebase</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">☁️</div>
                <div class="stack-name">GCP</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">⚡</div>
                <div class="stack-name">FastAPI</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">JS</div>
                <div class="stack-name">JavaScript</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">🎨</div>
                <div class="stack-name">HTML/CSS</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">🍃</div>
                <div class="stack-name">MongoDB</div>
            </div>
            <div class="stack-item">
                <div class="stack-icon">📊</div>
                <div class="stack-name">Analytics</div>
            </div>
        </div>
    </section>

    <!-- STATS SECTION -->
    <section class="stats-section">
        <div class="stats-container">
            <h2 class="section-title">◦ System Performance Metrics ◦</h2>
            
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">420+</div>
                    <div class="stat-label">GitHub Contributions</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">8</div>
                    <div class="stat-label">Production Systems</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1.2k+</div>
                    <div class="stat-label">LeetCode Problems</div>
                </div>
            </div>

            <!-- Charts -->
            <div class="chart-container">
                <h3 class="chart-title">GitHub Contributions Heatmap</h3>
                <div class="chart-placeholder">
                    📊 [Insert GitHub Activity Graph - Full Width]
                </div>
            </div>

            <div class="chart-container">
                <h3 class="chart-title">Top Languages & Proficiency</h3>
                <div class="chart-placeholder">
                    📈 [Insert Language Breakdown - Full Width]
                </div>
            </div>

            <div class="chart-container">
                <h3 class="chart-title">LeetCode Heatmap & Progress</h3>
                <div class="chart-placeholder">
                    🔥 [Insert LeetCode Heatmap - Full Width]
                </div>
            </div>
        </div>
    </section>

    <!-- PHILOSOPHY -->
    <section style="padding: 80px 20px;">
        <div class="philosophy">
            <p class="philosophy-quote">
                Intelligence is engineered — not prompted.
            </p>
            <p class="philosophy-subtitle">Structure over shortcuts • Systems over scripts • Execution over noise</p>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-content">
            <div class="footer-links">
                <a href="https://github.com/ragavan28v" class="footer-link" target="_blank">GitHub</a>
                <a href="https://linkedin.com/in/ragavan-v" class="footer-link" target="_blank">LinkedIn</a>
                <a href="mailto:hello@ragavan.dev" class="footer-link">Email</a>
                <a href="#" class="footer-link">Blog</a>
            </div>
            <p class="footer-text">© 2024 RAGAVAN V. Architecting Tomorrow's Intelligence.</p>
        </div>
    </footer>

</body>
</html>
