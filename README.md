<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saran Kumar - Senior SDET</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', sans-serif;
            background: linear-gradient(135deg, #0f172a 0%, #1e3a8a 50%, #1e40af 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .banner {
            width: 100%;
            max-width: 1200px;
            background: linear-gradient(135deg, rgba(15, 23, 42, 0.95) 0%, rgba(30, 58, 138, 0.95) 100%);
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(59, 130, 246, 0.3);
            position: relative;
        }

        .animated-bg {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 20% 50%, rgba(59, 130, 246, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(139, 92, 246, 0.1) 0%, transparent 50%);
            animation: shimmer 8s ease-in-out infinite;
        }

        @keyframes shimmer {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        .content {
            position: relative;
            z-index: 1;
            padding: 60px 50px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        @media (max-width: 768px) {
            .content {
                grid-template-columns: 1fr;
                padding: 40px 30px;
                gap: 30px;
            }
        }

        .left-section h1 {
            font-size: 3.5em;
            font-weight: 800;
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            animation: fadeInDown 0.8s ease-out;
        }

        .title {
            font-size: 1.4em;
            color: #93c5fd;
            font-weight: 600;
            margin-bottom: 20px;
            animation: fadeInDown 0.8s ease-out 0.2s both;
        }

        .tagline {
            font-size: 1.1em;
            color: #cbd5e1;
            line-height: 1.6;
            margin-bottom: 30px;
            animation: fadeInDown 0.8s ease-out 0.4s both;
        }

        .highlight-box {
            background: rgba(59, 130, 246, 0.15);
            border-left: 4px solid #60a5fa;
            padding: 15px 20px;
            border-radius: 8px;
            margin-bottom: 25px;
            animation: fadeInLeft 0.8s ease-out 0.6s both;
        }

        .highlight-box p {
            color: #e0e7ff;
            font-size: 0.95em;
            font-style: italic;
        }

        .tech-section {
            animation: fadeInUp 0.8s ease-out 0.8s both;
        }

        .tech-label {
            color: #a78bfa;
            font-size: 0.9em;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 8px;
        }

        .tech-items {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        .tech-item {
            background: rgba(99, 102, 241, 0.2);
            border: 1px solid rgba(139, 92, 246, 0.4);
            color: #c4b5fd;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .tech-item:hover {
            background: rgba(139, 92, 246, 0.3);
            border-color: rgba(139, 92, 246, 0.8);
            transform: translateY(-2px);
        }

        .right-section {
            display: flex;
            flex-direction: column;
            gap: 25px;
            animation: fadeInRight 0.8s ease-out 0.4s both;
        }

        .stats-box {
            background: rgba(30, 64, 175, 0.5);
            border: 1px solid rgba(59, 130, 246, 0.4);
            padding: 25px;
            border-radius: 12px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .stats-box:hover {
            background: rgba(30, 64, 175, 0.7);
            border-color: rgba(59, 130, 246, 0.8);
            transform: translateY(-4px);
        }

        .stats-number {
            font-size: 2.2em;
            font-weight: 800;
            background: linear-gradient(135deg, #60a5fa 0%, #a78bfa 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 8px;
        }

        .stats-label {
            color: #cbd5e1;
            font-size: 0.95em;
            font-weight: 500;
        }

        .cta-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 12px 28px;
            border-radius: 8px;
            font-weight: 600;
            font-size: 0.95em;
            text-decoration: none;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            display: inline-block;
            text-align: center;
        }

        .btn-primary {
            background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(59, 130, 246, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: #60a5fa;
            border: 2px solid #60a5fa;
        }

        .btn-secondary:hover {
            background: rgba(59, 130, 246, 0.1);
            transform: translateY(-2px);
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInLeft {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeInRight {
            from {
                opacity: 0;
                transform: translateX(20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <div class="banner">
        <div class="animated-bg"></div>
        <div class="content">
            <div class="left-section">
                <h1>Saran Kumar</h1>
                <div class="title">🚀 Senior SDET | Test Automation Engineer</div>
                <p class="tagline">Crafting intelligent, scalable, and robust test automation solutions that ensure quality at every level.</p>
                
                <div class="highlight-box">
                    <p>"Quality is not just a checkpoint — it's a mindset"</p>
                </div>

                <div class="tech-section">
                    <div class="tech-label">🧪 Expertise</div>
                    <div class="tech-items">
                        <div class="tech-item">Selenium</div>
                        <div class="tech-item">Cypress</div>
                        <div class="tech-item">Playwright</div>
                        <div class="tech-item">REST Assured</div>
                        <div class="tech-item">BDD/Cucumber</div>
                        <div class="tech-item">AI Automation</div>
                    </div>
                </div>

                <div class="tech-section">
                    <div class="tech-label">💻 Stack</div>
                    <div class="tech-items">
                        <div class="tech-item">Java</div>
                        <div class="tech-item">JavaScript/TypeScript</div>
                        <div class="tech-item">Python</div>
                        <div class="tech-item">Docker</div>
                        <div class="tech-item">Jenkins</div>
                        <div class="tech-item">GitHub Actions</div>
                    </div>
                </div>
            </div>

            <div class="right-section">
                <div class="stats-box">
                    <div class="stats-number">10+</div>
                    <div class="stats-label">Featured Frameworks</div>
                </div>

                <div class="stats-box">
                    <div class="stats-number">🤖</div>
                    <div class="stats-label">AI-Powered Automation Focus</div>
                </div>

                <div class="stats-box">
                    <div class="stats-number">∞</div>
                    <div class="stats-label">Continuous Learning Mindset</div>
                </div>

                <div class="cta-buttons">
                    <a href="#" class="btn btn-primary">📂 Explore Projects</a>
                    <a href="#" class="btn btn-secondary">💬 Connect</a>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
