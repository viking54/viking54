<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Piyush Chaudhary - Frontend Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            padding: 60px 0;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .profile-content {
            position: relative;
            z-index: 1;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid rgba(255, 255, 255, 0.3);
            margin: 0 auto 20px;
            display: block;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        .name {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .title {
            font-size: 1.5rem;
            opacity: 0.9;
            margin-bottom: 30px;
        }

        .typing-text {
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            transition: transform 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .section-icon {
            width: 40px;
            height: 40px;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .tech-category {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
        }

        .tech-category h4 {
            margin-bottom: 15px;
            color: #ff6b6b;
            font-size: 1.2rem;
        }

        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
        }

        .tech-icon {
            width: 40px;
            height: 40px;
            transition: transform 0.3s ease;
        }

        .tech-icon:hover {
            transform: scale(1.2);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .stat-card:hover {
            transform: scale(1.05);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #4ecdc4;
        }

        .stat-label {
            margin-top: 10px;
            opacity: 0.8;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 12px 24px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 30px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-3px);
        }

        .social-icon {
            width: 24px;
            height: 24px;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 25px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        .project-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: #ff6b6b;
        }

        .project-desc {
            opacity: 0.9;
            line-height: 1.6;
        }

        .about-content {
            font-size: 1.1rem;
            line-height: 1.8;
            text-align: center;
        }

        .highlight {
            color: #4ecdc4;
            font-weight: bold;
        }

        @media (max-width: 768px) {
            .name {
                font-size: 2rem;
            }
            
            .tech-grid {
                grid-template-columns: 1fr;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <div class="profile-content">
                <img src="https://avatars.githubusercontent.com/u/70807500?v=4" alt="Piyush Chaudhary" class="profile-img">
                <h1 class="name">Piyush Chaudhary</h1>
                <p class="title">Frontend Developer & Full-Stack Engineer</p>
                <div class="typing-text">
                    <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=20&pause=1000&color=FFFFFF&center=true&vCenter=true&width=600&lines=React.js+%26+TypeScript+Specialist;MERN+Stack+Developer;Building+Scalable+Web+Applications;Always+Learning+%F0%9F%9A%80" alt="Typing SVG" />
                </div>
            </div>
        </div>

        <!-- About Section -->
        <div class="section">
            <h2 class="section-title">
                <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/People%20with%20professions/Man%20Technologist%20Medium%20Skin%20Tone.png" class="section-icon" alt="👨‍💻">
                About Me
            </h2>
            <div class="about-content">
                <p>Hey there! I'm a passionate <span class="highlight">Frontend Developer</span> with 3+ years of experience building modern web applications. I specialize in <span class="highlight">React.js & TypeScript</span> while having strong expertise in the <span class="highlight">MERN stack</span>.</p>
                <br>
                <p>Currently working at <span class="highlight">Observance Solutions</span>, where I build enterprise-level applications and love turning complex problems into simple, beautiful solutions!</p>
            </div>
        </div>

        <!-- Tech Stack Section -->
        <div class="section">
            <h2 class="section-title">
                <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Laptop.png" class="section-icon" alt="💻">
                Tech Stack
            </h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <h4>Frontend</h4>
                    <div class="tech-icons">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" class="tech-icon" alt="React">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" class="tech-icon" alt="TypeScript">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" class="tech-icon" alt="JavaScript">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg" class="tech-icon" alt="Next.js">
                    </div>
                </div>
                <div class="tech-category">
                    <h4>Backend</h4>
                    <div class="tech-icons">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" class="tech-icon" alt="Node.js">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg" class="tech-icon" alt="Express">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" class="tech-icon" alt="MongoDB">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" class="tech-icon" alt="PostgreSQL">
                    </div>
                </div>
                <div class="tech-category">
                    <h4>Tools & Cloud</h4>
                    <div class="tech-icons">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" class="tech-icon" alt="Git">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/amazonwebservices/amazonwebservices-original.svg" class="tech-icon" alt="AWS">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/azure/azure-original.svg" class="tech-icon" alt="Azure">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" class="tech-icon" alt="Docker">
                    </div>
                </div>
            </div>
        </div>

        <!-- Stats Section -->
        <div class="section">
            <h2 class="section-title">
                <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Chart%20Increasing.png" class="section-icon" alt="📈">
                GitHub Activity
            </h2>
            <div style="text-align: center;">
                <img src="https://github-readme-stats.vercel.app/api?username=viking54&show_icons=true&theme=tokyonight&hide_border=true&bg_color=00000000" alt="GitHub Stats">
                <br><br>
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=viking54&layout=compact&theme=tokyonight&hide_border=true&bg_color=00000000" alt="Top Languages">
            </div>
        </div>

        <!-- Projects Section -->
        <div class="section">
            <h2 class="section-title">
                <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Rocket.png" class="section-icon" alt="🚀">
                Featured Projects
            </h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3 class="project-title">🤖 Hints+ AI Desktop App</h3>
                    <p class="project-desc">AI-powered desktop application with real-time transcription, meeting summaries, multi-language translation, and teleprompter functionality. Built with modern tech stack and AI APIs.</p>
                </div>
                <div class="project-card">
                    <h3 class="project-title">👟 Shoe ERP System</h3>
                    <p class="project-desc">Complete ERP solution for shoe manufacturing covering raw materials, workflow tracking, and finished goods management. Built from scratch with React & AG Grid.</p>
                </div>
                <div class="project-card">
                    <h3 class="project-title">💰 Expense Management System</h3>
                    <p class="project-desc">Enterprise-level expense tracking application with document handling, secure access control, and automated invoice generation using pdfmake integration.</p>
                </div>
            </div>
        </div>

        <!-- Contact Section -->
        <div class="section">
            <h2 class="section-title">
                <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Telephone.png" class="section-icon" alt="📞">
                Let's Connect!
            </h2>
            <div class="social-links">
                <a href="https://linkedin.com/in/piyush-chaudhary-819765197" class="social-link">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" class="social-icon" alt="LinkedIn">
                    LinkedIn
                </a>
                <a href="mailto:chaudharypiyush30@gmail.com" class="social-link">
                    <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/E-Mail.png" class="social-icon" alt="Email">
                    Email
                </a>
                <a href="https://github.com/viking54" class="social-link">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" class="social-icon" alt="GitHub">
                    GitHub
                </a>
            </div>
        </div>
    </div>

    <!-- Profile Views Counter -->
    <div style="text-align: center; padding: 20px;">
        <img src="https://komarev.com/ghpvc/?username=viking54&label=Profile%20views&color=blueviolet&style=flat" alt="Profile Views" />
    </div>
</body>
</html>
