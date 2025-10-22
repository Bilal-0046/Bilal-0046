<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muhammad Bilal - AI Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 100%);
            color: #e4e4e7;
            overflow-x: hidden;
            line-height: 1.6;
        }

        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            pointer-events: none;
        }

        .particle {
            position: absolute;
            background: rgba(88, 166, 255, 0.3);
            border-radius: 50%;
            animation: float 20s infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) translateX(0); }
            25% { transform: translateY(-100px) translateX(50px); }
            50% { transform: translateY(-50px) translateX(100px); }
            75% { transform: translateY(-150px) translateX(25px); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
            position: relative;
            z-index: 1;
        }

        .hero {
            text-align: center;
            padding: 80px 20px;
            position: relative;
            margin-bottom: 60px;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(88, 166, 255, 0.1) 0%, transparent 70%);
            animation: pulse 4s ease-in-out infinite;
            pointer-events: none;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.5; transform: translateX(-50%) scale(1); }
            50% { opacity: 0.8; transform: translateX(-50%) scale(1.1); }
        }

        .avatar {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            margin: 0 auto 30px;
            position: relative;
            animation: fadeInDown 1s ease;
        }

        .avatar-circle {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 72px;
            font-weight: bold;
            color: white;
            box-shadow: 0 20px 60px rgba(102, 126, 234, 0.4);
            position: relative;
            overflow: hidden;
        }

        .avatar-circle::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
            animation: shine 3s infinite;
        }

        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 1s ease 0.2s both;
            font-weight: 800;
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

        .subtitle {
            font-size: 1.4em;
            color: #a1a1aa;
            margin-bottom: 20px;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .tagline {
            font-size: 1.1em;
            color: #71717a;
            max-width: 700px;
            margin: 0 auto 40px;
            animation: fadeInUp 1s ease 0.6s both;
        }

        .social-links {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.8s both;
        }

        .social-btn {
            padding: 12px 28px;
            background: rgba(88, 166, 255, 0.1);
            border: 2px solid rgba(88, 166, 255, 0.3);
            border-radius: 8px;
            color: #58a6ff;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .social-btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(88, 166, 255, 0.2);
            transform: translate(-50%, -50%);
            transition: width 0.5s, height 0.5s;
        }

        .social-btn:hover::before {
            width: 300px;
            height: 300px;
        }

        .social-btn:hover {
            border-color: #58a6ff;
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(88, 166, 255, 0.3);
        }

        .social-btn span {
            position: relative;
            z-index: 1;
        }

        .stats {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 40px;
            flex-wrap: wrap;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 12px;
            padding: 20px 30px;
            text-align: center;
            transition: all 0.3s ease;
            animation: fadeInUp 1s ease both;
        }

        .stat-card:nth-child(1) { animation-delay: 1s; }
        .stat-card:nth-child(2) { animation-delay: 1.1s; }
        .stat-card:nth-child(3) { animation-delay: 1.2s; }
        .stat-card:nth-child(4) { animation-delay: 1.3s; }

        .stat-card:hover {
            transform: translateY(-5px);
            border-color: #58a6ff;
            box-shadow: 0 10px 30px rgba(88, 166, 255, 0.2);
        }

        .stat-number {
            font-size: 2em;
            font-weight: bold;
            color: #58a6ff;
            margin-bottom: 5px;
        }

        .stat-label {
            font-size: 0.9em;
            color: #a1a1aa;
        }

        .section {
            margin-bottom: 60px;
            animation: fadeInUp 1s ease both;
        }

        .section-title {
            font-size: 2.2em;
            margin-bottom: 30px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section-title::before {
            content: '';
            width: 4px;
            height: 40px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 2px;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 16px;
            padding: 30px;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(88, 166, 255, 0.1), transparent);
            transition: left 0.5s;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: #58a6ff;
            box-shadow: 0 20px 60px rgba(88, 166, 255, 0.3);
        }

        .project-icon {
            font-size: 3em;
            margin-bottom: 15px;
        }

        .project-title {
            font-size: 1.5em;
            margin-bottom: 10px;
            color: #58a6ff;
        }

        .project-description {
            color: #a1a1aa;
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .tech-tag {
            padding: 5px 12px;
            background: rgba(88, 166, 255, 0.1);
            border: 1px solid rgba(88, 166, 255, 0.3);
            border-radius: 6px;
            font-size: 0.85em;
            color: #58a6ff;
        }

        .project-metrics {
            display: flex;
            gap: 20px;
            margin-bottom: 20px;
        }

        .metric {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }

        .metric-label {
            font-size: 0.85em;
            color: #71717a;
        }

        .metric-value {
            font-size: 1.3em;
            font-weight: bold;
            color: #58a6ff;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #58a6ff;
            text-decoration: none;
            font-weight: 600;
            transition: gap 0.3s ease;
        }

        .project-link:hover {
            gap: 12px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 12px;
            padding: 25px;
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            border-color: #58a6ff;
        }

        .skill-category-title {
            font-size: 1.2em;
            margin-bottom: 15px;
            color: #58a6ff;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill-item {
            padding: 8px 16px;
            background: rgba(88, 166, 255, 0.1);
            border-radius: 6px;
            font-size: 0.9em;
            transition: all 0.3s ease;
        }

        .skill-item:hover {
            background: rgba(88, 166, 255, 0.2);
            transform: scale(1.05);
        }

        .achievements {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .achievement-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 12px;
            padding: 25px;
            display: flex;
            gap: 15px;
            align-items: flex-start;
            transition: all 0.3s ease;
        }

        .achievement-card:hover {
            transform: translateX(10px);
            border-color: #58a6ff;
        }

        .achievement-icon {
            font-size: 2.5em;
            flex-shrink: 0;
        }

        .achievement-content h3 {
            font-size: 1.1em;
            margin-bottom: 5px;
            color: #58a6ff;
        }

        .achievement-content p {
            color: #a1a1aa;
            font-size: 0.95em;
        }

        .roadmap {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .roadmap-item {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 12px;
            padding: 25px;
            display: flex;
            gap: 20px;
            align-items: center;
            transition: all 0.3s ease;
        }

        .roadmap-item:hover {
            border-color: #58a6ff;
            transform: translateX(10px);
        }

        .status-indicator {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            flex-shrink: 0;
        }

        .status-progress {
            background: #fbbf24;
            animation: blink 2s infinite;
        }

        .status-active {
            background: #10b981;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.4; }
        }

        .roadmap-content {
            flex: 1;
        }

        .roadmap-title {
            font-size: 1.2em;
            margin-bottom: 5px;
            color: #e4e4e7;
        }

        .roadmap-tech {
            color: #a1a1aa;
            font-size: 0.9em;
        }

        .footer {
            text-align: center;
            padding: 60px 20px;
            border-top: 1px solid rgba(88, 166, 255, 0.1);
            margin-top: 80px;
        }

        .footer-quote {
            font-size: 1.2em;
            font-style: italic;
            color: #a1a1aa;
            max-width: 700px;
            margin: 0 auto 40px;
            line-height: 1.8;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2.5em;
            }

            .projects-grid,
            .skills-grid,
            .achievements {
                grid-template-columns: 1fr;
            }

            .section-title {
                font-size: 1.8em;
            }
        }

        .typing-effect {
            border-right: 2px solid #58a6ff;
            animation: blink-cursor 1s step-end infinite;
        }

        @keyframes blink-cursor {
            50% { border-color: transparent; }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>

    <div class="container">
        <div class="hero">
            <div class="avatar">
                <div class="avatar-circle">MB</div>
            </div>
            <h1>Muhammad Bilal</h1>
            <div class="subtitle">AI Engineer • ML Researcher • Healthcare AI Innovator</div>
            <p class="tagline">Architecting privacy-preserving AI systems that bridge cutting-edge research and clinical impact</p>
            
            <div class="social-links">
                <a href="https://www.linkedin.com/in/muhammadbilal0046" class="social-btn" target="_blank">
                    <span>💼 LinkedIn</span>
                </a>
                <a href="mailto:muhammadbilal0046@gmail.com" class="social-btn">
                    <span>✉️ Email</span>
                </a>
                <a href="https://github.com/bilal-0046" class="social-btn" target="_blank">
                    <span>💻 GitHub</span>
                </a>
                <a href="https://dev.to/bilal0046" class="social-btn" target="_blank">
                    <span>📝 Blog</span>
                </a>
            </div>

            <div class="stats">
                <div class="stat-card">
                    <div class="stat-number">92%</div>
                    <div class="stat-label">Model Accuracy</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">100</div>
                    <div class="stat-label">Lighthouse Score</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">15+</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">3rd</div>
                    <div class="stat-label">Year BS AI</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">🚀 Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-icon">🧠</div>
                    <h3 class="project-title">Brain Tumor Detection System</h3>
                    <p class="project-description">Production-grade diagnostic tool for MRI-based brain tumor classification deployed in clinical settings with enterprise architecture.</p>
                    <div class="project-tech">
                        <span class="tech-tag">TensorFlow</span>
                        <span class="tech-tag">EfficientNetB0</span>
                        <span class="tech-tag">Flask</span>
                        <span class="tech-tag">Docker</span>
                    </div>
                    <div class="project-metrics">
                        <div class="metric">
                            <span class="metric-label">Accuracy</span>
                            <span class="metric-value">92%</span>
                        </div>
                        <div class="metric">
                            <span class="metric-label">Latency</span>
                            <span class="metric-value">&lt;200ms</span>
                        </div>
                    </div>
                    <a href="https://github.com/bilal-0046/brain-tumor-detection" class="project-link" target="_blank">
                        View Project →
                    </a>
                </div>

                <div class="project-card">
                    <div class="project-icon">🌐</div>
                    <h3 class="project-title">AI-Powered Portfolio</h3>
                    <p class="project-description">Next-gen interactive portfolio with conversational AI assistant achieving perfect performance scores across all metrics.</p>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Dialogflow</span>
                        <span class="tech-tag">TailwindCSS</span>
                    </div>
                    <div class="project-metrics">
                        <div class="metric">
                            <span class="metric-label">Lighthouse</span>
                            <span class="metric-value">100/100</span>
                        </div>
                        <div class="metric">
                            <span class="metric-label">TTFB</span>
                            <span class="metric-value">&lt;100ms</span>
                        </div>
                    </div>
                    <a href="https://github.com/bilal-0046/portfolio" class="project-link" target="_blank">
                        View Project →
                    </a>
                </div>

                <div class="project-card">
                    <div class="project-icon">🔄</div>
                    <h3 class="project-title">Graph Cycle Detection</h3>
                    <p class="project-description">Efficient DFS-based cycle detection algorithm with comprehensive testing framework for complex graph structures.</p>
                    <div class="project-tech">
                        <span class="tech-tag">Java</span>
                        <span class="tech-tag">Algorithms</span>
                        <span class="tech-tag">Testing</span>
                    </div>
                    <div class="project-metrics">
                        <div class="metric">
                            <span class="metric-label">Complexity</span>
                            <span class="metric-value">O(V+E)</span>
                        </div>
                        <div class="metric">
                            <span class="metric-label">Tests</span>
                            <span class="metric-value">100+</span>
                        </div>
                    </div>
                    <a href="https://github.com/bilal-0046/graph-cycle-detection" class="project-link" target="_blank">
                        View Project →
                    </a>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">🛠️ Technology Stack</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <div class="skill-category-title">🤖 AI/ML</div>
                    <div class="skill-list">
                        <span class="skill-item">TensorFlow</span>
                        <span class="skill-item">PyTorch</span>
                        <span class="skill-item">Keras</span>
                        <span class="skill-item">OpenCV</span>
                        <span class="skill-item">scikit-learn</span>
                    </div>
                </div>
                <div class="skill-category">
                    <div class="skill-category-title">🌐 Web Dev</div>
                    <div class="skill-list">
                        <span class="skill-item">Next.js</span>
                        <span class="skill-item">React</span>
                        <span class="skill-item">TailwindCSS</span>
                        <span class="skill-item">JavaScript</span>
                    </div>
                </div>
                <div class="skill-category">
                    <div class="skill-category-title">📱 Mobile</div>
                    <div class="skill-list">
                        <span class="skill-item">Flutter</span>
                        <span class="skill-item">Dart</span>
                        <span class="skill-item">TFLite</span>
                        <span class="skill-item">Firebase</span>
                    </div>
                </div>
                <div class="skill-category">
                    <div class="skill-category-title">☁️ DevOps</div>
                    <div class="skill-list">
                        <span class="skill-item">Docker</span>
                        <span class="skill-item">AWS</span>
                        <span class="skill-item">Git</span>
                        <span class="skill-item">CI/CD</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">🏆 Key Achievements</h2>
            <div class="achievements">
                <div class="achievement-card">
                    <div class="achievement-icon">🥇</div>
                    <div class="achievement-content">
                        <h3>TensorFlow Contributor</h3>
                        <p>Active open source contributor to TensorFlow Models</p>
                    </div>
                </div>
                <div class="achievement-card">
                    <div class="achievement-icon">📜</div>
                    <div class="achievement-content">
                        <h3>Google Certified</h3>
                        <p>TensorFlow Developer & Data Science Professional</p>
                    </div>
                </div>
                <div class="achievement-card">
                    <div class="achievement-icon">🩺</div>
                    <div class="achievement-content">
                        <h3>Clinical Deployment</h3>
                        <p>AI system serving active medical facilities</p>
                    </div>
                </div>
                <div class="achievement-card">
                    <div class="achievement-icon">🌟</div>
                    <div class="achievement-content">
                        <h3>Top Contributor 2024</h3>
                        <p>University AI Hackathon recognition</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">🎯 Current Roadmap</h2>
            <div class="roadmap">
                <div class="roadmap-item">
                    <div class="status-indicator status-progress"></div>
                    <div class="roadmap-content">
                        <div class="roadmap-title">Federated Learning Integration</div>
                        <div class="roadmap-tech">TensorFlow Federated, PySyft, Privacy-Preserving ML</div>
                    </div>
                </div>
                <div class="roadmap-item">
                    <div class="status-indicator status-progress"></div>
                    <div class="roadmap-content">
                        <div class="roadmap-title">Flutter Medical Diagnostics App</div>
                        <div class="roadmap-tech">Flutter, TFLite, Firebase, Real-time AI</div>
                    </div>
                </div>
                <div class="roadmap-item">
                    <div class="status-indicator status-active"></div>
                    <div class="roadmap-content">
                        <div class="roadmap-title">"Demystifying Deep Learning" Blog Series</div>
                        <div class="roadmap-tech">Technical Writing on Dev.to & Medium</div>
                    </div>
                </div>
                <div class="roadmap-item">
                    <div class="status-indicator status-active"></div>
                    <div class="roadmap-content">
                        <div class="roadmap-title">Open Source ML Contributions</div>
                        <div class="roadmap-tech">TensorFlow, Keras, Community Projects</div>
                    </div>
                </div>
            </div>
        </div>

        <div class="footer">
            <div class="footer-quote">
                "The intersection of artificial intelligence and healthcare represents one of humanity's greatest opportunities to democratize world-class medical expertise. I'm committed to building systems that are not only technically excellent but also ethically sound and accessible."
            </div>
            <div class="social-links">
                <a href="mailto:muhammadbilal0046@gmail.com" class="social-btn">
                    <span>Get in Touch</span>
                </a>
                <a href="https://github.com/bilal-0046" class="social-btn" target="_blank">
                    <span>View All Projects</span>
                </a>
            </div>
            <p style="margin-top: 40px; color: #71717a; font-size: 0.9em;">
                ⚡ Powered by curiosity, driven by impact, committed to excellence
            </p>
        </div>
    </div>

    <script>
        // Create floating particles
        const particlesContainer = document.getElementById('particles');
        for (let i = 0; i < 50; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.width = Math.random() * 5 + 2 + 'px';
            particle.style.height = particle.style.width;
            particle.style.left = Math.random() * 100 + '%';
            particle.style.top = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 20 + 's';
            particle.style.animationDuration = (Math.random() * 10 + 15) + 's';
            particlesContainer.appendChild(particle);
        }

        // Intersection Observer for scroll animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            observer.observe(section);
        });

        // Animate stats on scroll
        const statCards = document.querySelectorAll('.stat-card');
        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    setTimeout(() => {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }, index * 100);
                }
            });
        }, { threshold: 0.5 });

        statCards.forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            statsObserver.observe(card);
        });

        // Project card hover effect with mouse tracking
        document.querySelectorAll('.project-card').forEach(card => {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                const centerX = rect.width / 2;
                const centerY = rect.height / 2;
                
                const rotateX = (y - centerY) / 20;
                const rotateY = (centerX - x) / 20;
                
                card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) translateY(-10px)`;
            });
            
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'perspective(1000px) rotateX(0) rotateY(0) translateY(0)';
            });
        });

        // Skill items animation on hover
        document.querySelectorAll('.skill-item').forEach(item => {
            item.addEventListener('mouseenter', function() {
                this.style.transition = 'all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55)';
            });
        });

        // Achievement cards stagger animation
        const achievementCards = document.querySelectorAll('.achievement-card');
        const achievementObserver = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    setTimeout(() => {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateX(0)';
                    }, index * 150);
                }
            });
        }, { threshold: 0.3 });

        achievementCards.forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateX(-30px)';
            achievementObserver.observe(card);
        });

        // Roadmap items animation
        const roadmapItems = document.querySelectorAll('.roadmap-item');
        const roadmapObserver = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    setTimeout(() => {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateX(0)';
                    }, index * 100);
                }
            });
        }, { threshold: 0.5 });

        roadmapItems.forEach(item => {
            item.style.opacity = '0';
            item.style.transform = 'translateX(-30px)';
            roadmapObserver.observe(item);
        });

        // Add smooth parallax effect to hero section
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const hero = document.querySelector('.hero');
            if (hero) {
                hero.style.transform = `translateY(${scrolled * 0.5}px)`;
                hero.style.opacity = 1 - (scrolled / 600);
            }
        });

        // Animate avatar on load
        window.addEventListener('load', () => {
            const avatar = document.querySelector('.avatar-circle');
            avatar.style.animation = 'fadeInDown 1s ease, pulse 2s ease-in-out infinite 1s';
        });

        // Add ripple effect to buttons
        document.querySelectorAll('.social-btn').forEach(button => {
            button.addEventListener('click', function(e) {
                const ripple = document.createElement('span');
                const rect = this.getBoundingClientRect();
                const size = Math.max(rect.width, rect.height);
                const x = e.clientX - rect.left - size / 2;
                const y = e.clientY - rect.top - size / 2;
                
                ripple.style.width = ripple.style.height = size + 'px';
                ripple.style.left = x + 'px';
                ripple.style.top = y + 'px';
                ripple.style.position = 'absolute';
                ripple.style.borderRadius = '50%';
                ripple.style.background = 'rgba(88, 166, 255, 0.5)';
                ripple.style.transform = 'scale(0)';
                ripple.style.animation = 'ripple 0.6s ease-out';
                ripple.style.pointerEvents = 'none';
                
                this.appendChild(ripple);
                
                setTimeout(() => ripple.remove(), 600);
            });
        });

        // Add CSS for ripple animation dynamically
        const style = document.createElement('style');
        style.textContent = `
            @keyframes ripple {
                to {
                    transform: scale(4);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);

        // Counter animation for stats
        function animateCounter(element, target, duration = 2000) {
            const start = 0;
            const increment = target / (duration / 16);
            let current = start;
            
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    element.textContent = target + (element.dataset.suffix || '');
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(current) + (element.dataset.suffix || '');
                }
            }, 16);
        }

        // Trigger counter animation when stats are visible
        const statsCounterObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting && !entry.target.dataset.animated) {
                    const number = entry.target.querySelector('.stat-number');
                    const value = parseInt(number.textContent);
                    if (!isNaN(value)) {
                        number.dataset.suffix = number.textContent.replace(/\d+/g, '');
                        animateCounter(number, value, 2000);
                        entry.target.dataset.animated = 'true';
                    }
                }
            });
        }, { threshold: 0.5 });

        statCards.forEach(card => statsCounterObserver.observe(card));

        // Add glow effect on tech tags
        document.querySelectorAll('.tech-tag, .skill-item').forEach(tag => {
            tag.addEventListener('mouseenter', function() {
                this.style.boxShadow = '0 0 20px rgba(88, 166, 255, 0.5)';
            });
            tag.addEventListener('mouseleave', function() {
                this.style.boxShadow = 'none';
            });
        });

        // Lazy load effect for images and heavy content
        if ('IntersectionObserver' in window) {
            const lazyObserver = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('loaded');
                        lazyObserver.unobserve(entry.target);
                    }
                });
            });

            document.querySelectorAll('.project-card, .skill-category').forEach(el => {
                lazyObserver.observe(el);
            });
        }

        // Add typing effect to subtitle (optional enhancement)
        const subtitle = document.querySelector('.subtitle');
        if (subtitle) {
            const text = subtitle.textContent;
            subtitle.textContent = '';
            subtitle.classList.add('typing-effect');
            let i = 0;
            
            function typeWriter() {
                if (i < text.length) {
                    subtitle.textContent += text.charAt(i);
                    i++;
                    setTimeout(typeWriter, 50);
                } else {
                    subtitle.classList.remove('typing-effect');
                }
            }
            
            setTimeout(typeWriter, 1000);
        }

        // Performance optimization: Reduce animations on low-end devices
        const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)');
        if (prefersReducedMotion.matches) {
            document.querySelectorAll('*').forEach(el => {
                el.style.animation = 'none';
                el.style.transition = 'none';
            });
        }
    </script>
