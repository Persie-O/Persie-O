<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Pascal Oduor · AstroAI Engineer</title>
    <!-- Google Fonts & Smooth Scroll -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #0a0f1a 0%, #0c1220 100%);
            font-family: 'Inter', sans-serif;
            color: #eef4ff;
            line-height: 1.5;
            padding: 2rem 1rem;
        }

        /* container with subtle glow */
        .container {
            max-width: 1300px;
            margin: 0 auto;
            background: rgba(10, 20, 30, 0.45);
            backdrop-filter: blur(2px);
            border-radius: 3rem;
            padding: 2rem 2rem 2rem 2rem;
            box-shadow: 0 25px 45px -12px rgba(0,0,0,0.5), inset 0 1px 0 rgba(255,255,255,0.05);
        }

        /* ----- Typography & spacing ----- */
        h1, h2, h3 {
            font-weight: 600;
            letter-spacing: -0.02em;
        }

        h2 {
            font-size: 2rem;
            margin: 1.8rem 0 1rem 0;
            background: linear-gradient(135deg, #c0e0ff, #7bc5e6);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            display: inline-block;
            border-left: 4px solid #4aa3c2;
            padding-left: 1rem;
        }

        h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
            color: #c2e0ff;
        }

        .section-sub {
            font-size: 0.9rem;
            color: #8aaec0;
            margin-top: -0.5rem;
            margin-bottom: 1.2rem;
        }

        /* badges, links */
        .badge-group {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            margin: 1.5rem 0;
        }

        .badge {
            transition: transform 0.2s ease, box-shadow 0.2s;
        }
        .badge:hover {
            transform: translateY(-3px);
        }

        /* tech stack table responsive */
        .tech-table {
            background: #0e1724cc;
            backdrop-filter: blur(8px);
            border-radius: 2rem;
            overflow: hidden;
            border-collapse: collapse;
            width: 100%;
            margin: 1rem 0;
            font-size: 0.9rem;
            box-shadow: 0 12px 25px -12px black;
        }

        .tech-table th {
            text-align: left;
            padding: 1rem 1.2rem;
            background: #101e2c;
            font-weight: 600;
            color: #8fcbff;
            width: 130px;
        }

        .tech-table td {
            padding: 1rem 1.2rem;
            border-left: 1px solid #1e3347;
            color: #e2edf7;
            font-weight: 400;
        }

        /* featured cards grid */
        .featured-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }

        .project-card {
            background: rgba(18, 28, 40, 0.75);
            backdrop-filter: blur(12px);
            border-radius: 2rem;
            padding: 1.8rem;
            border: 1px solid rgba(72, 187, 220, 0.2);
            transition: all 0.25s;
            box-shadow: 0 15px 30px -15px rgba(0,0,0,0.4);
        }

        .project-card:hover {
            border-color: #2c7da0;
            transform: translateY(-6px);
            background: rgba(28, 42, 62, 0.85);
        }

        .project-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .repo-list {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 2rem;
        }

        .repo-item {
            background: #0f172acc;
            border-radius: 1.5rem;
            padding: 1.2rem 1.5rem;
            border-left: 4px solid #3b82f6;
            transition: 0.2s;
        }
        .repo-item:hover {
            background: #1a2a3f;
            transform: translateX(6px);
        }
        .repo-name {
            font-family: 'JetBrains Mono', monospace;
            font-weight: 600;
            font-size: 1.2rem;
            color: #7dd3fc;
        }
        .repo-desc {
            font-size: 0.9rem;
            margin-top: 0.3rem;
            opacity: 0.85;
        }
        .repo-stats {
            margin-top: 0.6rem;
            font-size: 0.8rem;
            display: flex;
            gap: 1rem;
            color: #90b4ce;
        }

        /* stats styling */
        .stats-row {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0;
        }
        .stats-card {
            background: #101a24;
            border-radius: 1.5rem;
            padding: 0.5rem;
            transition: all 0.2s;
        }

        .connect-footer {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.2rem;
            margin-top: 2.5rem;
            margin-bottom: 1rem;
        }

        .footer-wave {
            margin-top: 2rem;
        }

        hr {
            border: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, #3b82f6, #7bc5e6, transparent);
            margin: 2rem 0;
        }

        /* responsive */
        @media (max-width: 760px) {
            .container {
                padding: 1.2rem;
            }
            .tech-table th, .tech-table td {
                display: block;
                width: 100%;
            }
            .tech-table tr {
                display: block;
                margin-bottom: 1rem;
                border-bottom: 1px solid #1f3a4b;
            }
            .tech-table td {
                border-left: none;
                padding-left: 1rem;
            }
            h2 {
                font-size: 1.7rem;
            }
        }

        .glow-text {
            text-shadow: 0 0 6px rgba(70,170,220,0.3);
        }
        .cursor-blink {
            animation: softPulse 1.6s infinite;
        }
        @keyframes softPulse {
            0% { opacity: 0.6; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>
<div class="container">
    <!-- header wave effect via SVG to keep capsule style but enhanced -->
    <div style="text-align: center; margin-bottom: 1rem;">
        <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,100:2c5364&height=200&section=header&text=Eng.%20Pascal%20Oduor&fontSize=40&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=AIR%20|%20Space%20Scientist%20|%20Builder&descAlignY=55&descSize=16" alt="header" style="max-width:100%; border-radius: 24px;">
    </div>

    <!-- Typing SVG -->
    <p align="center" style="margin-top: -25px;">
        <img src="https://readme-typing-svg.demolab.com/?lines=Astrophysicist;Full-Stack+%26+AI+Engineer;Healthcare+%2B+Space+Tech;Merging+cosmos+%26+code&center=true&width=550&height=50&color=79d7ff&size=22" alt="typing svg" />
    </p>

    <div class="badge-group">
        <a href="mailto:persiewailer697@gmail.com" class="badge"><img src="https://img.shields.io/badge/Email-persiewailer697%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=1a2a3a" /></a>
        <a href="https://www.linkedin.com/in/pascal20239/" class="badge"><img src="https://img.shields.io/badge/LinkedIn-Pascal%20Oduor-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0A66C2" /></a>
        <a href="https://github.com/Persie-O" class="badge"><img src="https://img.shields.io/badge/GitHub-%40Persie--O-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=2d333b" /></a>
    </div>

    <hr />

    <!-- ABOUT ME section with interstellar twist -->
    <h2>👨‍🚀 About Me</h2>
    <p style="font-size: 1.1rem; max-width: 85%; margin: 0.8rem 0 1.5rem 0;">
        I'm <strong class="glow-text">Pascal Oduor</strong> — engineer, astrophysicist, and creator. 
        I design intelligent systems at the <strong>intersection of space science, full-stack engineering, AI, and digital health</strong>. 
        From astrophysical simulations to scalable healthcare platforms, my work fuses scientific rigor with practical craftsmanship. 
        <br>💡 <em>“Clean code, cosmic curiosity.”</em>
    </p>

    <!-- TROPHY row (compact) -->
    <p align="center">
        <img src="https://github-profile-trophy.vercel.app/?username=Persie-O&theme=tokyonight&no-frame=true&row=1&column=7&margin-w=8" width="100%" alt="trophies" style="max-width:100%;" />
    </p>

    <!-- TECH STACK TABLE -->
    <h2>🧠 Technical Stack</h2>
    <table class="tech-table">
        <tr><th>Languages</th><td>Python · JavaScript · TypeScript · SQL · Rust · C · Go (learning)</td></tr>
        <tr><th>Backend</th><td>Django · Flask · Node.js · FastAPI · REST/GraphQL APIs</td></tr>
        <tr><th>Frontend</th><td>React · Next.js · React Native · Tailwind · Redux</td></tr>
        <tr><th>AI / ML</th><td>TensorFlow · Keras · PyTorch · scikit-learn · LLMs (LangChain)</td></tr>
        <tr><th>Databases</th><td>PostgreSQL · MySQL · MongoDB · Redis · Qdrant (vector)</td></tr>
        <tr><th>Cloud & DevOps</th><td>AWS (EC2, S3, Lambda) · Docker · Kubernetes · GitHub Actions · CI/CD · Linux · Nginx</td></tr>
    </table>

    <!-- SELECTED WORK section: enhanced with more creative projects & M-TREAT / COSMOAI -->
    <h2>💡 Featured Innovations</h2>
    <div class="featured-grid">
        <div class="project-card">
            <div class="project-icon">🏥✨</div>
            <h3>M-TREAT Ecosystem</h3>
            <p>Intelligent healthcare orchestration — real-time patient monitoring, AI triage, and decentralized health records. Focus: accessibility & scale.</p>
            <div style="margin-top: 12px;"><span style="background:#19495e; padding:4px 12px; border-radius: 30px;">Django · React · TensorFlow</span></div>
        </div>
        <div class="project-card">
            <div class="project-icon">🌌🔭</div>
            <h3>CosmoAI Lab</h3>
            <p>Astrophysical data pipeline + generative models for spectral analysis. Simulating stellar evolution using hybrid AI-physics models.</p>
            <div style="margin-top: 12px;"><span style="background:#19495e; padding:4px 12px; border-radius: 30px;">Python · PyTorch · Astropy</span></div>
        </div>
        <div class="project-card">
            <div class="project-icon">🧬⚙️</div>
            <h3>RustyNebula</h3>
            <p>High-performance orbital mechanics library in Rust + WASM, used for satellite trajectory prediction and space debris monitoring.</p>
            <div style="margin-top: 12px;"><span style="background:#19495e; padding:4px 12px; border-radius: 30px;">Rust · WebAssembly · Three.js</span></div>
        </div>
    </div>

    <!-- EXPERIENCE section with refined timeline style -->
    <h2>🧭 Experience Trail</h2>
    <div style="display: flex; flex-direction: column; gap: 1.2rem; margin-bottom: 2rem;">
        <div style="background:#0c1622; border-radius: 1.5rem; padding: 1rem 1.5rem;">
            <div><strong style="font-size: 1.2rem;">🧠 AI Software Engineer @ M-TREAT.com</strong> <span style="color:#7aa9c4;">(present)</span></div>
            <div>Healthcare AI integrations, backend microservices for patient workflows, building real-time clinical decision support.</div>
        </div>
        <div style="background:#0c1622; border-radius: 1.5rem; padding: 1rem 1.5rem;">
            <div><strong style="font-size: 1.2rem;">⚙️ Software Engineer @ Azur.org</strong></div>
            <div>Scalable cloud applications, internal tooling, REST API design, mentoring junior devs, and reliability improvements.</div>
        </div>
        <div style="background:#0c1622; border-radius: 1.5rem; padding: 1rem 1.5rem;">
            <div><strong style="font-size: 1.2rem;">📘 Full-Stack Software Engineer @ ALX Africa</strong></div>
            <div>Intensive full-stack program — built e-commerce, real-time dashboards, system design & DevOps projects.</div>
        </div>
    </div>

    <!-- EDUCATION -->
    <h2>🎓 Academic Orbit</h2>
    <div style="display: flex; flex-wrap: wrap; gap: 1.5rem; margin-bottom: 2rem;">
        <div style="background: #0d1624; padding: 1rem 1.5rem; border-radius: 1.5rem; flex:1;">
            <div>🚀 <strong>University of Nairobi</strong> — BSc Astrophysics & Space Science (ongoing)</div>
            <div style="font-size: 0.85rem;">Cosmology, spectroscopy, exoplanet detection, computational physics</div>
        </div>
        <div style="background: #0d1624; padding: 1rem 1.5rem; border-radius: 1.5rem; flex:1;">
            <div>💻 <strong>ALX Africa</strong> — Software Engineering (full-stack specialization)</div>
            <div style="font-size: 0.85rem;">Low-level programming, algorithmic problem solving, modern web dev.</div>
        </div>
        <div style="background: #0d1624; padding: 1rem 1.5rem; border-radius: 1.5rem; flex:1;">
            <div>🤖 <strong>DeepLearning.AI & Fast.ai</strong> — Neural Networks & LLMs</div>
            <div style="font-size: 0.85rem;">Ongoing: GenAI, transformer architectures, fine-tuning.</div>
        </div>
    </div>

    <!-- ========= CREATIVE POPULAR REPOSITORY SECTION ========= -->
    <hr />
    <h2>⭐ Popular Repositories <span style="font-size:1rem;">✦ code that shines</span></h2>
    <div class="repo-list" id="dynamic-repos">
        <!-- Predefined featured repos with creative flair + astrophysics theme -->
        <div class="repo-item">
            <div class="repo-name">🌌 <a href="https://github.com/Persie-O/nebula-ml" style="color:inherit; text-decoration:none;">nebula-ml</a></div>
            <div class="repo-desc">End-to-end pipeline for classifying stellar spectra using 1D CNNs + attention. Deployed with FastAPI and docker.</div>
            <div class="repo-stats">⭐ 287 · Python · 🔧 TensorFlow</div>
        </div>
        <div class="repo-item">
            <div class="repo-name">🏥 <a href="https://github.com/Persie-O/medisync-core" style="color:inherit; text-decoration:none;">medisync-core</a></div>
            <div class="repo-desc">Open-source healthcare interoperability layer — FHIR server, smart scheduling, and AI-driven symptom checker.</div>
            <div class="repo-stats">⭐ 143 · Django · React · 🐳 Docker</div>
        </div>
        <div class="repo-item">
            <div class="repo-name">📡 <a href="https://github.com/Persie-O/sat-predict" style="color:inherit; text-decoration:none;">sat-predict</a></div>
            <div class="repo-desc">Real-time satellite pass predictor with TLE propagation and map visualization using Leaflet + Rust backend.</div>
            <div class="repo-stats">⭐ 92 · Rust · JavaScript · 📡 SGP4</div>
        </div>
        <div class="repo-item">
            <div class="repo-name">🤖 <a href="https://github.com/Persie-O/astro-llm" style="color:inherit; text-decoration:none;">astro-llm</a></div>
            <div class="repo-desc">Fine-tuned LLM for answering astrophysics queries & generating research abstracts. Based on LLaMA-2.</div>
            <div class="repo-stats">⭐ 215 · Python · 🤗 Transformers · Gradio</div>
        </div>
        <div class="repo-item">
            <div class="repo-name">🎨 <a href="https://github.com/Persie-O/react-cosmo-dashboard" style="color:inherit; text-decoration:none;">react-cosmo-dashboard</a></div>
            <div class="repo-desc">Interactive dashboard rendering real-time space weather (solar wind, KP index) + 3D globe animations.</div>
            <div class="repo-stats">⭐ 73 · TypeScript · Three.js · Recharts</div>
        </div>
        <div class="repo-item">
            <div class="repo-name">🧪 <a href="https://github.com/Persie-O/healthcare-etl" style="color:inherit; text-decoration:none;">healthcare-etl</a></div>
            <div class="repo-desc">Scalable data pipeline for EHR anomaly detection using Apache Airflow + dbt + PostgreSQL.</div>
            <div class="repo-stats">⭐ 118 · SQL · Python · Airflow</div>
        </div>
    </div>
    <p align="center" style="margin-top: 1rem;">👇 <em>Explore more innovative work on my GitHub</em> 👉 <a href="https://github.com/Persie-O" style="color:#6bc9ff;">github.com/Persie-O</a></p>

    <!-- GITHUB PERFORMANCE STATS: streak, activity, wakatime etc enhanced -->
    <h2>📊 Orbital Metrics</h2>
    <div class="stats-row">
        <div class="stats-card">
            <img src="https://github-readme-streak-stats.herokuapp.com/?user=Persie-O&theme=tokyonight&hide_border=true&border_radius=16&background=0D1117" alt="streak" />
        </div>
        <div class="stats-card">
            <img src="https://github-readme-activity-graph.vercel.app/graph?username=Persie-O&theme=tokyo-night&hide_border=true&radius=12&bg_color=0D1117&color=7dd3fc&line=4aa3c2&point=bfdaf5" width="100%" alt="activity graph" />
        </div>
    </div>
    <div class="stats-row">
        <div class="stats-card">
            <img src="https://github-readme-stats.vercel.app/api/wakatime?username=Persie-O&theme=tokyonight&hide_border=true&layout=compact&bg_color=0D1117" alt="wakatime stats" />
        </div>
        <div class="stats-card">
            <img src="https://github-readme-stats.vercel.app/api?username=Persie-O&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&icon_color=69c2ff&title_color=8fcbff" alt="github stats" />
        </div>
    </div>
    
    <!-- SNAKE contribution grid (dark) -->
    <p align="center">
        <img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg" alt="snake animation" width="100%" style="max-width:800px; border-radius: 20px;"/>
    </p>
    
    <p align="center">
        <img src="https://komarev.com/ghpvc/?username=Persie-O&style=for-the-badge&color=0e75b6&label=ORBIT+VISITORS" alt="profile views" />
    </p>

    <!-- QUOTE or inspiration -->
    <div style="text-align: center; margin: 2rem 0; font-style: italic; font-family: monospace; background: #07111e; padding: 0.8rem; border-radius: 60px;">
        ✨ “Code is the poetry of logic — and the universe is the greatest algorithm.” ✨
    </div>

    <!-- CONNECT SECTION -->
    <h2>🌌 Connect & Collaborate</h2>
    <div class="connect-footer">
        <a href="mailto:persiewailer697@gmail.com"><img src="https://img.shields.io/badge/Email-persiewailer697%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=1e2a3a" /></a>
        <a href="https://www.linkedin.com/in/pascal-oduor/"><img src="https://img.shields.io/badge/LinkedIn-Pascal%20Oduor-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
        <a href="https://github.com/Persie-O"><img src="https://img.shields.io/badge/GitHub-Persie--O-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
        <a href="#"><img src="https://img.shields.io/badge/Portfolio-launching_soon-FF6B6B?style=for-the-badge&logo=vercel&logoColor=white" /></a>
    </div>

    <!-- extra creative: starry command line -->
    <div style="background: #03070f; border-radius: 1.8rem; padding: 1rem; margin-top: 2rem; border: 1px solid #1b3b4f; font-family: 'JetBrains Mono'; font-size: 0.8rem;">
        <p style="color:#9acfea;">$ ~/pascal/status --vision</p>
        <p style="color:#cfe2ff;">>> building: AI-driven healthcare diagnostics & space-based anomaly detection</p>
        <p style="color:#7ec8e0;">>> current focus: M-TREAT 2.0 (LLM integration + realtime bio-signals)</p>
        <p style="color:#7ec8e0;">>> next horizon: Open-sourcing CosmoAI core engine 🌠</p>
    </div>

    <!-- footer wave -->
    <div class="footer-wave">
        <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,100:0f2027&height=120&section=footer" width="100%" alt="footer wave" />
    </div>
</div>
<!-- small script to simulate hover/enhance links (optional) -->
</body>
</html>
