<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manti Mokone - Animated README</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            overflow-x: hidden;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
        }

        /* Header Animation */
        .header {
            text-align: center;
            margin-bottom: 40px;
            animation: fadeInDown 1s ease-out;
        }

        .header h1 {
            font-size: 3em;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #ff6ec4, #7873f5, #4facfe);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradient 3s ease infinite;
            background-size: 200% 200%;
        }

        .wave {
            display: inline-block;
            animation: wave 2s ease-in-out infinite;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-15deg); }
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .profile-views {
            display: inline-block;
            padding: 8px 16px;
            background: rgba(138, 43, 226, 0.3);
            border-radius: 20px;
            margin-top: 10px;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        /* Stats Section */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 40px 0;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .stat-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: #ff6ec4;
            box-shadow: 0 10px 30px rgba(255, 110, 196, 0.3);
        }

        /* About Section */
        .section {
            margin: 40px 0;
            animation: fadeIn 1s ease-out;
        }

        .section h2 {
            font-size: 2em;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section h2::before {
            content: '';
            width: 5px;
            height: 30px;
            background: linear-gradient(180deg, #ff6ec4, #7873f5);
            border-radius: 10px;
            animation: grow 0.5s ease-out;
        }

        @keyframes grow {
            from { height: 0; }
            to { height: 30px; }
        }

        .about-grid {
            display: grid;
            gap: 20px;
        }

        .about-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #ff6ec4;
            animation: slideInLeft 0.6s ease-out;
            transition: all 0.3s ease;
        }

        .about-item:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateX(10px);
        }

        .about-item strong {
            color: #ff6ec4;
            font-size: 1.2em;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            gap: 30px;
        }

        .skill-category h3 {
            color: #4facfe;
            margin-bottom: 15px;
            font-size: 1.5em;
        }

        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .badge {
            padding: 10px 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 25px;
            font-weight: bold;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 2px solid transparent;
            animation: fadeInScale 0.5s ease-out;
        }

        .badge:hover {
            background: rgba(255, 110, 196, 0.3);
            border-color: #ff6ec4;
            transform: scale(1.1) rotate(2deg);
        }

        @keyframes fadeInScale {
            from {
                opacity: 0;
                transform: scale(0.8);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        /* Security Skills */
        .security-list {
            list-style: none;
            padding-left: 0;
        }

        .security-list li {
            padding: 15px;
            margin: 10px 0;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            border-left: 4px solid #7873f5;
            animation: slideInRight 0.6s ease-out;
            transition: all 0.3s ease;
        }

        .security-list li:hover {
            background: rgba(120, 115, 245, 0.2);
            transform: translateX(-10px);
        }

        /* Certifications */
        .cert-item {
            background: linear-gradient(135deg, rgba(255, 110, 196, 0.2), rgba(120, 115, 245, 0.2));
            padding: 20px;
            margin: 15px 0;
            border-radius: 10px;
            border: 2px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            animation: fadeIn 0.8s ease-out;
        }

        .cert-item:hover {
            transform: scale(1.02);
            border-color: #4facfe;
            box-shadow: 0 10px 30px rgba(79, 172, 254, 0.3);
        }

        /* Footer */
        .footer {
            text-align: center;
            margin-top: 60px;
            padding: 30px;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 15px;
            animation: fadeInUp 1s ease-out 0.5s both;
        }

        .footer h2 {
            justify-content: center;
        }

        .quote {
            font-size: 1.5em;
            font-style: italic;
            margin-top: 20px;
            color: #4facfe;
            animation: glow 2s ease-in-out infinite;
        }

        @keyframes glow {
            0%, 100% { text-shadow: 0 0 10px rgba(79, 172, 254, 0.5); }
            50% { text-shadow: 0 0 20px rgba(79, 172, 254, 0.8), 0 0 30px rgba(79, 172, 254, 0.6); }
        }

        /* Animations */
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

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        /* Floating particles */
        .particle {
            position: fixed;
            width: 4px;
            height: 4px;
            background: rgba(255, 255, 255, 0.5);
            border-radius: 50%;
            pointer-events: none;
            animation: float 4s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) translateX(0); }
            50% { transform: translateY(-20px) translateX(10px); }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1><span class="wave">👋</span> Hey there! I'm Manti Mokone</h1>
            <div class="profile-views">
                <img src="https://komarev.com/ghpvc/?username=Manti-techtalk&color=blueviolet" alt="Profile Views">
            </div>
        </div>

        <div class="section">
            <h2>📊 GitHub Stats</h2>
            <div class="stats">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=Manti-techtalk&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="GitHub Stats" style="width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://streak-stats.demolab.com?user=Manti-techtalk&theme=radical&hide_border=true" alt="GitHub Streak" style="width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Manti-techtalk&layout=compact&theme=radical&hide_border=true" alt="Top Languages" style="width: 100%; border-radius: 10px;">
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🚀 About Me</h2>
            <div class="about-grid">
                <div class="about-item">
                    <strong>💡 Who am I?</strong><br>
                    I'm Manti Mokone, a passionate Computer Science student at St. Lawrence University, living at the crossroads of Software Engineering and Offensive Security.
                </div>
                <div class="about-item">
                    <strong>❤️ What Drives Me:</strong><br>
                    My heart beats for Offensive Security — breaking systems to understand them — but my hands are deep in Software Engineering, bringing real-world ideas to life through code.
                </div>
                <div class="about-item">
                    <strong>🎯 My Vision:</strong><br>
                    To become a Cybersecurity Engineer who bridges the gap between development and hacking — protecting the systems I build from the attacks I can perform.
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🏆 Skills & Technologies</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>💬 Languages</h3>
                    <div class="badges">
                        <span class="badge">🐍 Python</span>
                        <span class="badge">☕ Java</span>
                        <span class="badge">⚡ JavaScript</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>🧠 Frameworks & Tools</h3>
                    <div class="badges">
                        <span class="badge">FastAPI</span>
                        <span class="badge">Django</span>
                        <span class="badge">Next.js</span>
                        <span class="badge">React</span>
                        <span class="badge">Node.js</span>
                        <span class="badge">TailwindCSS</span>
                        <span class="badge">Bootstrap</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>🗄️ Databases</h3>
                    <div class="badges">
                        <span class="badge">PostgreSQL</span>
                        <span class="badge">MongoDB</span>
                        <span class="badge">SQL</span>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>🔐 Security</h3>
                    <ul class="security-list">
                        <li>🌐 Network Hacking</li>
                        <li>🔑 Credentials Harvesting</li>
                        <li>💥 Active Bruteforcing (Kali Linux)</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🎓 Certifications</h2>
            <div class="cert-item">
                📜 <strong>Cybersecurity & Networking:</strong> Nmap, Wireshark, Network Devices, IP Addressing, Network Models | <em>Cybrary</em>
            </div>
            <div class="cert-item">
                📜 <strong>Web Development:</strong> Django, JavaScript, React.js, Java | <em>Codecademy</em>
            </div>
            <div class="cert-item">
                ⭐ <strong>Fun Fact:</strong> I enjoy Capture The Flag (CTF) games! 🛡️💻
            </div>
        </div>

        <div class="footer">
            <h2>💡 Let's Connect!</h2>
            <p>💬 Always open to <strong>collaboration</strong> and <strong>learning opportunities</strong> — feel free to reach out!</p>
            <div class="quote">
                "Hack the system. Build the future." 🛡️
            </div>
        </div>
    </div>

    <script>
        // Create floating particles
        function createParticles() {
            for (let i = 0; i < 20; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 4 + 's';
                particle.style.animationDuration = (Math.random() * 3 + 2) + 's';
                document.body.appendChild(particle);
            }
        }

        createParticles();

        // Add stagger animation to badges
        const badges = document.querySelectorAll('.badge');
        badges.forEach((badge, index) => {
            badge.style.animationDelay = (index * 0.05) + 's';
        });

        // Add stagger animation to security list
        const securityItems = document.querySelectorAll('.security-list li');
        securityItems.forEach((item, index) => {
            item.style.animationDelay = (index * 0.1) + 's';
        });

        // Add stagger animation to about items
        const aboutItems = document.querySelectorAll('.about-item');
        aboutItems.forEach((item, index) => {
            item.style.animationDelay = (index * 0.15) + 's';
        });
    </script>
</body>
</html>
