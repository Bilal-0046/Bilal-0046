<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muhammad Bilal - AI Engineer & Researcher</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;
            background: #0d1117;
            color: #c9d1d9;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Animated Background */
        .background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            background: linear-gradient(135deg, #0d1117 0%, #161b22 50%, #1c2128 100%);
        }

        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .star {
            position: absolute;
            background: #58a6ff;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.2); }
        }

        .gradient-orb {
            position: fixed;
            border-radius: 50%;
            filter: blur(80px);
            opacity: 0.3;
            pointer-events: none;
            animation: float 20s infinite ease-in-out;
        }

        .orb-1 {
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, #58a6ff, transparent);
            top: -200px;
            left: -200px;
        }

        .orb-2 {
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, #1f6feb, transparent);
            bottom: -150px;
            right: -150px;
            animation-delay: -10s;
        }

        .orb-3 {
            width: 350px;
            height: 350px;
            background: radial-gradient(circle, #388bfd, transparent);
            top: 50%;
            left: 50%;
            animation-delay: -5s;
        }

        @keyframes float {
            0%, 100% { transform: translate(0, 0) scale(1); }
            33% { transform: translate(100px, -50px) scale(1.1); }
            66% { transform: translate(-50px, 100px) scale(0.9); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
            position: relative;
            z-index: 1;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 100px 20px 80px;
            position: relative;
        }

        .avatar-container {
            position: relative;
            width: 200px;
            height: 200px;
            margin: 0 auto 40px;
            animation: fadeInScale 1s ease both;
        }

        @keyframes fadeInScale {
            from {
                opacity: 0;
                transform: scale(0.5);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        .avatar-ring {
            position: absolute;
            width: 100%;
            height: 100%;
            border: 3px solid transparent;
            border-top-color: #58a6ff;
            border-right-color: #1f6feb;
            border-radius: 50%;
            animation: rotate 3s linear infinite;
        }

        .avatar-ring:nth-child(2) {
            animation-delay: -1.5s;
            opacity: 0.5;
        }

        @keyframes rotate {
            to { transform: rotate(360deg); }
        }

        .avatar {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 160px;
            height: 160px;
            border-radius: 50%;
            background: linear-gradient(135deg, #58a6ff, #1f6feb);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 64px;
            font-weight: 800;
            color: white;
            box-shadow: 0 20px 60px rgba(88, 166, 255, 0.4);
            overflow: hidden;
        }

        .avatar::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.3), transparent);
            animation: shine 4s infinite;
        }

        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }

        h1 {
            font-size: 4em;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #58a6ff 0%, #1f6feb 50%, #58a6ff 100%);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 1s ease 0.3s both, gradientShift 3s ease infinite;
            font-weight: 900;
            letter-spacing: -1px;
        }

        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
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
            font-size: 1.5em;
            color: #8b949e;
            margin-bottom: 20px;
            animation: fadeInUp 1s ease 0.5s both;
            font-weight: 500;
        }

        .tagline {
            font-size: 1.2em;
            color: #6e7681;
            max-width: 800px;
            margin: 0 auto 50px;
            animation: fadeInUp 1s ease 0.7s both;
            font-style: italic;
        }

        /* Badges */
        .badges {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 50px;
            animation: fadeInUp 1s ease 0.9s both;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 10px 20px;
            background: rgba(88, 166, 255, 0.1);
            border: 1px solid rgba(88, 166, 255, 0.3);
            border-radius: 20px;
            color: #58a6ff;
            text-decoration: none;
            font-size: 0.9em;
            font-weight: 600;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .badge::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(88, 166, 255, 0.2);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.4s, height 0.4s;
        }

        .badge:hover::before {
            width: 300px;
            height: 300px;
        }

        .badge:hover {
            border-color: #58a6ff;
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(88, 166, 255, 0.3);
        }

        .badge span {
            position: relative;
            z-index: 1;
        }

        /* Social Links */
        .social-links {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 1.1s both;
        }

        .social-btn {
            padding: 15px 35px;
            background: linear-gradient(135deg, rgba(88, 166, 255, 0.15), rgba(31, 111, 235, 0.15));
            border: 2px solid rgba(88, 166, 255, 0.4);
            border-radius: 12px;
            color: #58a6ff;
            text-decoration: none;
            font-weight: 700;
            font-size: 1em;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .social-btn::after {
            content: '→';
            position: absolute;
            right: 20px;
            opacity: 0;
            transition: all 0.3s ease;
        }

        .social-btn:hover::after {
            opacity: 1;
            right: 15px;
        }

        .social-btn:hover {
            border-color: #58a6ff;
            background: linear-gradient(135deg, rgba(88, 166, 255, 0.25), rgba(31, 111, 235, 0.25));
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 15px 40px rgba(88, 166, 255, 0.4);
        }

        /* Stats Section */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
            margin: 80px 0;
        }

        .stat-card {
            background: rgba(22, 27, 34, 0.6);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 16px;
            padding: 30px;
            text-align: center;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            animation: fadeInUp 1s ease both;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(88, 166, 255, 0.1), transparent);
            transition: left 0.5s;
        }

        .stat-card:hover::before {
            left: 100%;
        }

        .stat-card:nth-child(1) { animation-delay: 1.3s; }
        .stat-card:nth-child(2) { animation-delay: 1.4s; }
        .stat-card:nth-child(3) { animation-delay: 1.5s; }
        .stat-card:nth-child(4) { animation-delay: 1.6s; }

        .stat-card:hover {
            transform: translateY(-10px) scale(1.03);
            border-color: #58a6ff;
            box-shadow: 0 20px 60px rgba(88, 166, 255, 0.3);
        }

        .stat-number {
            font-size: 3em;
            font-weight: 900;
            background: linear-gradient(135deg, #58a6ff, #1f6feb);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            display: block;
        }

        .stat-label {
            color: #8b949e;
            font-size: 1em;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Section Headers */
        .section {
            margin: 100px 0;
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease;
        }

        .section.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .section-header {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 50px;
        }

        .section-icon {
            font-size: 3em;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .section-title {
            font-size: 2.5em;
            font-weight: 800;
            background: linear-gradient(135deg, #58a6ff, #c9d1d9);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-line {
            flex: 1;
            height: 3px;
            background: linear-gradient(90deg, rgba(88, 166, 255, 0.5), transparent);
            border-radius: 2px;
        }

        /* Achievement Cards */
        .achievements {
            background: rgba(22, 27, 34, 0.4);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 60px;
        }

        .achievement-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px 0;
            border-bottom: 1px solid rgba(88, 166, 255, 0.1);
            transition: all 0.3s ease;
        }

        .achievement-item:last-child {
            border-bottom: none;
        }

        .achievement-item:hover {
            transform: translateX(10px);
            padding-left: 10px;
        }

        .achievement-icon {
            font-size: 1.5em;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        .achievement-text {
            flex: 1;
            color: #c9d1d9;
            font-size: 1.1em;
        }

        /* Project Cards */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
            gap: 35px;
        }

        .project-card {
            background: rgba(22, 27, 34, 0.6);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 20px;
            padding: 40px;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(88, 166, 255, 0.15), transparent);
            transition: left 0.6s;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            transform: translateY(-15px) scale(1.02);
            border-color: #58a6ff;
            box-shadow: 0 30px 80px rgba(88, 166, 255, 0.4);
        }

        .project-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }

        .project-icon {
            font-size: 3em;
        }

        .project-title {
            font-size: 1.8em;
            font-weight: 800;
            color: #58a6ff;
            margin: 0;
        }

        .project-subtitle {
            color: #8b949e;
            font-size: 0.95em;
            margin-bottom: 20px;
            font-weight: 600;
        }

        .project-description {
            color: #c9d1d9;
            line-height: 1.8;
            margin-bottom: 25px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 25px;
        }

        .tech-tag {
            padding: 8px 16px;
            background: rgba(88, 166, 255, 0.15);
            border: 1px solid rgba(88, 166, 255, 0.3);
            border-radius: 8px;
            color: #58a6ff;
            font-size: 0.85em;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .tech-tag:hover {
            background: rgba(88, 166, 255, 0.25);
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(88, 166, 255, 0.3);
        }

        .project-metrics {
            display: flex;
            gap: 30px;
            margin-bottom: 25px;
            padding: 20px;
            background: rgba(88, 166, 255, 0.05);
            border-radius: 12px;
            border: 1px solid rgba(88, 166, 255, 0.1);
        }

        .metric {
            text-align: center;
        }

        .metric-value {
            font-size: 2em;
            font-weight: 800;
            color: #58a6ff;
            display: block;
        }

        .metric-label {
            color: #8b949e;
            font-size: 0.85em;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            color: #58a6ff;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.05em;
            transition: gap 0.3s ease;
        }

        .project-link:hover {
            gap: 15px;
        }

        /* Tech Stack Grid */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .tech-category {
            background: rgba(22, 27, 34, 0.6);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 16px;
            padding: 35px;
            transition: all 0.4s ease;
        }

        .tech-category:hover {
            transform: translateY(-8px);
            border-color: #58a6ff;
            box-shadow: 0 20px 60px rgba(88, 166, 255, 0.3);
        }

        .tech-category-header {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 25px;
        }

        .tech-emoji {
            font-size: 2em;
        }

        .tech-category-title {
            font-size: 1.4em;
            font-weight: 800;
            color: #58a6ff;
        }

        .tech-items {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .tech-item {
            padding: 10px 18px;
            background: rgba(88, 166, 255, 0.1);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 8px;
            color: #c9d1d9;
            font-size: 0.95em;
            font-weight: 600;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .tech-item:hover {
            background: rgba(88, 166, 255, 0.2);
            border-color: #58a6ff;
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 20px rgba(88, 166, 255, 0.3);
        }

        /* Roadmap */
        .roadmap {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .roadmap-item {
            background: rgba(22, 27, 34, 0.6);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 16px;
            padding: 30px;
            display: flex;
            align-items: center;
            gap: 25px;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .roadmap-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 5px;
            background: linear-gradient(135deg, #58a6ff, #1f6feb);
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .roadmap-item:hover::before {
            opacity: 1;
        }

        .roadmap-item:hover {
            transform: translateX(15px);
            border-color: #58a6ff;
            box-shadow: 0 15px 40px rgba(88, 166, 255, 0.3);
        }

        .status-badge {
            padding: 8px 18px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            flex-shrink: 0;
        }

        .status-progress {
            background: rgba(251, 191, 36, 0.2);
            color: #fbbf24;
            border: 1px solid rgba(251, 191, 36, 0.4);
            animation: pulseGlow 2s infinite;
        }

        .status-active {
            background: rgba(16, 185, 129, 0.2);
            color: #10b981;
            border: 1px solid rgba(16, 185, 129, 0.4);
        }

        @keyframes pulseGlow {
            0%, 100% { box-shadow: 0 0 10px rgba(251, 191, 36, 0.3); }
            50% { box-shadow: 0 0 20px rgba(251, 191, 36, 0.6); }
        }

        .roadmap-content {
            flex: 1;
        }

        .roadmap-title {
            font-size: 1.3em;
            font-weight: 800;
            color: #c9d1d9;
            margin-bottom: 8px;
        }

        .roadmap-tech {
            color: #8b949e;
            font-size: 0.95em;
        }

        /* GitHub Stats */
        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .stat-image {
            width: 100%;
            border-radius: 16px;
            border: 1px solid rgba(88, 166, 255, 0.2);
            transition: all 0.4s ease;
        }

        .stat-image:hover {
            transform: scale(1.03);
            border-color: #58a6ff;
            box-shadow: 0 20px 60px rgba(88, 166, 255, 0.4);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 80px 20px;
            border-top: 1px solid rgba(88, 166, 255, 0.1);
            margin-top: 100px;
        }

        .footer-quote {
            font-size: 1.4em;
            font-style: italic;
            color: #8b949e;
            max-width: 900px;
            margin: 0 auto 50px;
            line-height: 1.9;
            position: relative;
        }

        .footer-quote::before,
        .footer-quote::after {
            content: '"';
            font-size: 3em;
            color: #58a6ff;
            opacity: 0.3;
        }

        .footer-cta {
            font-size: 1.2em;
            color: #c9d1d9;
            margin-top: 40px;
            font-weight: 600;
        }

        .footer-tagline {
            margin-top: 60px;
            color: #6e7681;
            font-size: 1em;
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5em;
            }

            .projects-grid,
            .tech-grid,
            .github-stats {
                grid-template-columns: 1fr;
            }

            .section-title {
                font-size: 2em;
            }

            .project-metrics {
                flex-direction: column;
                gap: 15px;
            }
        }

        /* Scroll to top button */
        .scroll-top {
            position: fixed;
            bottom: 40px;
            right: 40px;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #58a6ff, #1f6feb);
            border: none;
            border-radius: 50%;
            color: white;
            font-size: 1.5em;
            cursor: pointer;
            opacity: 0;
            transition: all 0.4s ease;
            z-index: 1000;
            box-shadow: 0 10px 30px rgba(88, 166, 255, 0.4);
        }

        .scroll-top.visible {
            opacity: 1;
        }

        .scroll-top:hover {
            transform: translateY(-5px) scale(1.1);
            box-shadow: 0 15px 40px rgba(88, 166, 255, 0.6);
        }
    </style>
</head>
<body>
    <!-- Animated Background -->
    <div class="background">
        <div class="gradient-orb orb-1"></div>
        <div class="gradient-orb orb-2"></div>
        <div class="gradient-orb orb-3"></div>
        <div class="stars" id="stars"></div>
    </div>

    <div class="container">
        <!-- Hero Section -->
        <div class="hero">
            <div class="avatar-container">
                <div class="avatar-ring"></div>
                <div class="avatar-ring"></div>
                <div class="avatar">MB</div>
            </div>

            <h1>Muhammad Bilal</h1>
            <div class="subtitle">Artificial Intelligence Engineer | Machine Learning Researcher | Healthcare AI Innovator</div>
            <p class="tagline">Architecting privacy-preserving AI systems that bridge the gap between cutting-edge research and clinical impact</p>

            <div class="badges">
                <a href="#" class="badge">
                    <span>👁️ Profile Views</span>
                </a>
                <a href="https://github.com/bilal-0046" class="badge" target="_blank">
                    <span>⭐ GitHub Stars</span>
                </a>
                <a href="https://github.com/bilal-0046" class="badge" target="_blank">
                    <span>👥 Followers</span>
                </a>
            </div>

            <div class="social-links">
                <a href="https://www.linkedin.com/in/muhammadbilal0046" class="social-btn" target="_blank">
                    LinkedIn
                </a>
                <a href="mailto:muhammadbilal0046@gmail.com" class="social-btn">
                    Email
                </a>
                <a href="https://github.com/bilal-0046/portfolio" class="social-btn" target="_blank">
                    Portfolio
                </a>
            </div>
        </div>

        <!-- Stats -->
        <div class="stats">
            <div class="stat-card">
                <span class="stat-number" data-target="92">0</span>
                <span class="stat-label">% Model Accuracy</span>
            </div>
            <div class="stat-card">
                <span class="stat-number" data-target="100">0</span>
                <span class="stat-label">Lighthouse Score</span>
            </div>
            <div class="stat-card">
                <span class="stat-number" data-target="15">0</span>
                <span class="stat-label">+ Projects</span>
            </div>
            <div class="stat-card">
                <span class="stat-number">3rd</span>
                <span class="stat-label">Year BS AI</span>
            </div>
        </div>

        <!-- Achievements Section -->
        <div class="section">
            <div class="section-header">
                <span class="section-icon">🏆</span>
                <h2 class="section-title">Key Achievements</h2>
                <div class="section-line"></div>
            </div>
            <div class="achievements">
                <div class="achievement-item">
                    <span class="achievement-icon">✓</span>
                    <span class="achievement-text">Deployed clinical-grade brain tumor detection system (92% accuracy)</span>
                </div>
                <div class="achievement-item">
                    <span class="achievement-icon">✓</span>
                    <span class="achievement-text">TensorFlow Open Source Contributor</span>
                </div>
                <div class="achievement-item">
                    <span class="achievement-icon">✓</span>
                    <span class="achievement-text">Google Certified: TensorFlow Developer & Data Science Professional</span>
                </div>
                <div class="achievement-item">
                    <span class="achievement-icon">✓</span>
                    <span class="achievement-text">Healthcare AI systems serving active medical facilities</span>
                </div>
                <div class="achievement-item">
                    <span class="achievement-icon">✓</span>
                    <span class="achievement-text">100/100 Lighthouse score on production web applications</span>
                </div>
            </div>
        </div>

        <!-- Featured Projects -->
        <div class="section">
            <div class="section-header">
                <span class="section-icon">🚀</span>
                <h2 class="section-title">Featured Projects</h2>
                <div class="section-line"></div>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <span class="project-icon">🧠</span>
                        <h3 class="project-title">Brain Tumor Detection</h3>
                    </div>
                    <div class="project-subtitle">Production Medical AI | TensorFlow, EfficientNetB0, Flask, Docker</div>
                    <p class="project-description">
                        Enterprise-grade diagnostic tool for MRI-based brain tumor classification deployed in clinical settings. 
                        Features transfer learning with EfficientNetB0 and custom CNN layers for optimal performance.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">TensorFlow</span>
                        <span class="tech-tag">Keras</span>
                        <span class="tech-tag">OpenCV</span>
                        <span class="tech-tag">Flask</span>
                        <span class="tech-tag">Docker</span>
                    </div>
                    <div class="project-metrics">
                        <div class="metric">
                            <span class="metric-value">92%</span>
                            <span class="metric-label">Accuracy</span>
                        </div>
                        <div class="metric">
                            <span class="metric-value">&lt;200ms</span>
                            <span class="metric-label">Latency</span>
                        </div>
                    </div>
                    <a href="https://github.com/bilal-0046/brain-tumor-detection" class="project-link" target="_blank">
                        View Project →
                    </a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <span class="project-icon">🌐</span>
                        <h3 class="project-title">AI-Powered Portfolio</h3>
                    </div>
                    <div class="project-subtitle">Next-Gen Web Experience | React, Dialogflow, TailwindCSS</div>
                    <p class="project-description">
                        Intelligent portfolio with conversational AI assistant achieving perfect performance scores. 
                        Features natural language project navigation and dynamic content generation.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Dialogflow</span>
                        <span class="tech-tag">TailwindCSS</span>
                        <span class="tech-tag">Vercel</span>
                    </div>
                    <div class="project-metrics">
                        <div class="metric">
                            <span class="metric-value">100/100</span>
                            <span class="metric-label">Lighthouse</span>
                        </div>
                        <div class="metric">
                            <span class="metric-value">&lt;100ms</span>
                            <span class="metric-label">TTFB</span>
                        </div>
                    </div>
                    <a href="https://github.com/bilal-0046/portfolio" class="project-link" target="_blank">
                        View Project →
                    </a>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <span class="project-icon">🔄</span>
                        <h3 class="project-title">Graph Cycle Detection</h3>
                    </div>
                    <div class="project-subtitle">Algorithm Engineering | Java, Graph Theory</div>
                    <p class="project-description">
                        Efficient implementation of DFS-based cycle detection with comprehensive testing framework. 
                        Applications in dependency resolution, deadlock detection, and workflow validation.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">Java</span>
                        <span class="tech-tag">Algorithms</span>
                        <span class="tech-tag">Testing</span>
                        <span class="tech-tag">Graph Theory</span>
                    </div>
                    <div class="project-metrics">
                        <div class="metric">
                            <span class="metric-value">O(V+E)</span>
                            <span class="metric-label">Complexity</span>
                        </div>
                        <div class="metric">
                            <span class="metric-value">100+</span>
                            <span class="metric-label">Tests</span>
                        </div>
                    </div>
                    <a href="https://github.com/bilal-0046/graph-cycle-detection" class="project-link" target="_blank">
                        View Project →
                    </a>
                </div>
            </div>
        </div>

        <!-- Technology Stack -->
        <div class="section">
            <div class="section-header">
                <span class="section-icon">🛠️</span>
                <h2 class="section-title">Technology Ecosystem</h2>
                <div class="section-line"></div>
            </div>
            <div class="tech-grid">
                <div class="tech-category">
                    <div class="tech-category-header">
                        <span class="tech-emoji">🤖</span>
                        <h3 class="tech-category-title">AI/ML</h3>
                    </div>
                    <div class="tech-items">
                        <span class="tech-item">TensorFlow</span>
                        <span class="tech-item">PyTorch</span>
                        <span class="tech-item">Keras</span>
                        <span class="tech-item">OpenCV</span>
                        <span class="tech-item">scikit-learn</span>
                    </div>
                </div>

                <div class="tech-category">
                    <div class="tech-category-header">
                        <span class="tech-emoji">🌐</span>
                        <h3 class="tech-category-title">Web Development</h3>
                    </div>
                    <div class="tech-items">
                        <span class="tech-item">Next.js</span>
                        <span class="tech-item">React</span>
                        <span class="tech-item">TailwindCSS</span>
                        <span class="tech-item">JavaScript</span>
                    </div>
                </div>

                <div class="tech-category">
                    <div class="tech-category-header">
                        <span class="tech-emoji">📱</span>
                        <h3 class="tech-category-title">Mobile</h3>
                    </div>
                    <div class="tech-items">
                        <span class="tech-item">Flutter</span>
                        <span class="tech-item">Dart</span>
                        <span class="tech-item">TFLite</span>
                        <span class="tech-item">Firebase</span>
                    </div>
                </div>

                <div class="tech-category">
                    <div class="tech-category-header">
                        <span class="tech-emoji">☁️</span>
                        <h3 class="tech-category-title">DevOps</h3>
                    </div>
                    <div class="tech-items">
                        <span class="tech-item">Docker</span>
                        <span class="tech-item">AWS</span>
                        <span class="tech-item">Git</span>
                        <span class="tech-item">CI/CD</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Current Roadmap -->
        <div class="section">
            <div class="section-header">
                <span class="section-icon">🎯</span>
                <h2 class="section-title">Current Initiatives</h2>
                <div class="section-line"></div>
            </div>
            <div class="roadmap">
                <div class="roadmap-item">
                    <span class="status-badge status-progress">In Progress</span>
                    <div class="roadmap-content">
                        <div class="roadmap-title">Federated Learning Integration</div>
                        <div class="roadmap-tech">TensorFlow Federated, PySyft, Privacy-Preserving ML</div>
                    </div>
                </div>
                <div class="roadmap-item">
                    <span class="status-badge status-progress">In Progress</span>
                    <div class="roadmap-content">
                        <div class="roadmap-title">Flutter Medical Diagnostics App</div>
                        <div class="roadmap-tech">Flutter, TFLite, Firebase, Real-time AI</div>
                    </div>
                </div>
                <div class="roadmap-item">
                    <span class="status-badge status-active">Active</span>
                    <div class="roadmap-content">
                        <div class="roadmap-title">"Demystifying Deep Learning" Blog Series</div>
                        <div class="roadmap-tech">Technical Writing on Dev.to & Medium</div>
                    </div>
                </div>
                <div class="roadmap-item">
                    <span class="status-badge status-active">Active</span>
                    <div class="roadmap-content">
                        <div class="roadmap-title">Open Source ML Contributions</div>
                        <div class="roadmap-tech">TensorFlow Models, Keras, Community Projects</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- GitHub Analytics -->
        <div class="section">
            <div class="section-header">
                <span class="section-icon">📊</span>
                <h2 class="section-title">GitHub Analytics</h2>
                <div class="section-line"></div>
            </div>
            <div class="github-stats">
                <img src="https://github-readme-stats.vercel.app/api?username=bilal-0046&show_icons=true&theme=dark&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=1F6FEB&text_color=C9D1D9&count_private=true" alt="GitHub Stats" class="stat-image">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=bilal-0046&theme=dark&hide_border=true&background=0D1117&stroke=58A6FF&ring=1F6FEB&fire=FF6B6B&currStreakLabel=C9D1D9" alt="GitHub Streak" class="stat-image">
                <img src="https://github-readme-stats.vercel.app/api/top-langs?username=bilal-0046&layout=compact&theme=dark&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9&langs_count=8" alt="Top Languages" class="stat-image">
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="footer-quote">
                The intersection of artificial intelligence and healthcare represents one of humanity's greatest opportunities to democratize world-class medical expertise. I'm committed to building systems that are not only technically excellent but also ethically sound and accessible.
            </div>
            
            <div class="social-links">
                <a href="mailto:muhammadbilal0046@gmail.com" class="social-btn">
                    Get in Touch
                </a>
                <a href="https://github.com/bilal-0046" class="social-btn" target="_blank">
                    View All Projects
                </a>
                <a href="https://www.linkedin.com/in/muhammadbilal0046" class="social-btn" target="_blank">
                    Connect on LinkedIn
                </a>
            </div>

            <div class="footer-cta">
                <strong>Open to:</strong> Research Collaborations • Speaking Engagements • Technical Consulting • Open Source Contributions
            </div>

            <div class="footer-tagline">
                ⚡ Powered by curiosity, driven by impact, committed to excellence
            </div>
        </div>
    </div>

    <!-- Scroll to Top Button -->
    <button class="scroll-top" id="scrollTop">↑</button>

    <script>
        // Create animated stars
        const starsContainer = document.getElementById('stars');
        for (let i = 0; i < 100; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            star.style.width = Math.random() * 3 + 1 + 'px';
            star.style.height = star.style.width;
            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 100 + '%';
            star.style.animationDelay = Math.random() * 3 + 's';
            star.style.animationDuration = (Math.random() * 2 + 2) + 's';
            starsContainer.appendChild(star);
        }

        // Intersection Observer for sections
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.section').forEach(section => {
            observer.observe(section);
        });

        // Counter animation for stats
        function animateCounter(element) {
            const target = parseInt(element.dataset.target);
            const duration = 2000;
            const step = target / (duration / 16);
            let current = 0;

            const timer = setInterval(() => {
                current += step;
                if (current >= target) {
                    element.textContent = target;
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(current);
                }
            }, 16);
        }

        // Trigger counter animation when stats are visible
        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting && !entry.target.dataset.animated) {
                    const counter = entry.target.querySelector('.stat-number[data-target]');
                    if (counter) {
                        animateCounter(counter);
                        entry.target.dataset.animated = 'true';
                    }
                }
            });
        }, { threshold: 0.5 });

        document.querySelectorAll('.stat-card').forEach(card => {
            statsObserver.observe(card);
        });

        // Project card 3D tilt effect
        document.querySelectorAll('.project-card').forEach(card => {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                const centerX = rect.width / 2;
                const centerY = rect.height / 2;
                
                const rotateX = (y - centerY) / 15;
                const rotateY = (centerX - x) / 15;
                
                card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) translateY(-15px) scale(1.02)`;
            });
            
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'perspective(1000px) rotateX(0) rotateY(0) translateY(0) scale(1)';
            });
        });

        // Scroll to top button
        const scrollTopBtn = document.getElementById('scrollTop');

        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 500) {
                scrollTopBtn.classList.add('visible');
            } else {
                scrollTopBtn.classList.remove('visible');
            }
        });

        scrollTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        // Smooth scroll for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add parallax effect to gradient orbs
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const orbs = document.querySelectorAll('.gradient-orb');
            
            orbs.forEach((orb, index) => {
                const speed = 0.1 * (index + 1);
                orb.style.transform = `translateY(${scrolled * speed}px)`;
            });
        });

        // Optimize animations for reduced motion preference
        const prefersReducedMotion = window.matchMedia('(prefers-reduced-motion: reduce)');
        
        if (prefersReducedMotion.matches) {
            document.querySelectorAll('*').forEach(el => {
                el.style.animation = 'none';
                el.style.transition = 'none';
            });
        }

        // Add loading animation
        window.addEventListener('load', () => {
            document.body.style.opacity = '1';
        });
    </script>
</body>
</html>
