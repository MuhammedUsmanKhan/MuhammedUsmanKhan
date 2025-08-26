<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Usman's GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #f8f8f8;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            text-align: center;
            padding: 40px 20px;
            position: relative;
            overflow: hidden;
        }
        
        .stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .star {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            animation: twinkle 5s infinite;
        }
        
        @keyframes twinkle {
            0%, 100% { opacity: 0.2; }
            50% { opacity: 1; }
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45aaf2);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: gradientShift 8s ease infinite;
            background-size: 300% 300%;
        }
        
        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        h3 {
            font-size: 1.5rem;
            font-weight: 400;
            margin-bottom: 30px;
            color: #d1d1d1;
        }
        
        .profile-stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        
        .stat {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 10px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease;
        }
        
        .stat:hover {
            transform: translateY(-5px);
        }
        
        .trophy {
            margin: 30px 0;
            text-align: center;
        }
        
        .about {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 15px;
            margin: 30px 0;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease;
        }
        
        .about:hover {
            transform: translateY(-5px);
        }
        
        .about-item {
            margin-bottom: 20px;
            padding-left: 20px;
            border-left: 3px solid #4ecdc4;
        }
        
        .connect {
            text-align: center;
            margin: 40px 0;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 24px;
            text-decoration: none;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .social-icon:hover {
            transform: translateY(-8px) scale(1.1);
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
        }
        
        .skills {
            margin: 40px 0;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .skill {
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .skill:hover {
            transform: translateY(-8px) rotate(3deg);
            background: rgba(78, 205, 196, 0.2);
        }
        
        .skill i {
            font-size: 2rem;
            margin-bottom: 10px;
        }
        
        .stats {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin: 40px 0;
        }
        
        .stat-row {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .stat-chart {
            flex: 1;
            min-width: 300px;
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #a1a1a1;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            h3 {
                font-size: 1.2rem;
            }
            
            .profile-stats {
                flex-direction: column;
                align-items: center;
            }
            
            .stat-row {
                flex-direction: column;
            }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="stars" id="stars"></div>
            <h1 class="pulse">🌟 Hi, I'm Usman! I enjoy crafting web apps, exploring new tech, and contributing to open-source.</h1>
            <h3>Passionate Full-Stack Developer dedicated to mastering the modern tech stack and building impactful, user-centric applications. Open to new opportunities.</h3>
            
            <div class="profile-stats">
                <div class="stat floating">
                    <p><i class="fas fa-eye"></i> Profile Views: <span id="viewCount">0</span></p>
                </div>
            </div>
            
            <div class="trophy">
                <div class="stat">
                    <p><i class="fas fa-trophy"></i> GitHub Trophy Progress</p>
                </div>
            </div>
        </div>
        
        <div class="about">
            <div class="about-item">
                <h3><i class="fas fa-code"></i> Currently Working On</h3>
                <p>AssignBase - A modern assignment management system</p>
            </div>
            
            <div class="about-item">
                <h3><i class="fas fa-graduation-cap"></i> Currently Learning</h3>
                <p>Deepening my expertise in scalable backend architecture with NestJS, GraphQL, and TypeScript</p>
            </div>
            
            <div class="about-item">
                <h3><i class="fas fa-users"></i> Collaborating On</h3>
                <p>Student-Management-App - A freelance project for educational management</p>
            </div>
            
            <div class="about-item">
                <h3><i class="fas fa-folder-open"></i> Portfolio</h3>
                <p>All my projects are available at <a href="https://github.com/MuhammedUsmanKhan?tab=repositories" style="color: #4ecdc4;">GitHub Repositories</a></p>
            </div>
            
            <div class="about-item">
                <h3><i class="fas fa-pen-fancy"></i> Writing</h3>
                <p>I regularly write articles on <a href="#" style="color: #4ecdc4;">Medium</a></p>
            </div>
            
            <div class="about-item">
                <h3><i class="fas fa-envelope"></i> Contact</h3>
                <p>Reach me at: <a href="mailto:uktech0310@gmail.com" style="color: #4ecdc4;">uktech0310@gmail.com</a></p>
            </div>
            
            <div class="about-item">
                <h3><i class="fas fa-file-alt"></i> Resume</h3>
                <p>View my experiences: <a href="https://drive.google.com/file/d/1yl0PpJVQFYHOFqbOpq9ot05YNfpwWG3s/view?usp=sharing" style="color: #4ecdc4;">Download Resume</a></p>
            </div>
        </div>
        
        <div class="connect">
            <h2><i class="fas fa-handshake"></i> Connect With Me</h2>
            <div class="social-icons">
                <a href="#" class="social-icon"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
                <a href="#" class="social-icon"><i class="fas fa-envelope"></i></a>
            </div>
        </div>
        
        <div class="skills">
            <h2 align="center"><i class="fas fa-tools"></i> Languages and Tools</h2>
            <div class="skills-grid">
                <div class="skill">
                    <i class="fab fa-aws"></i>
                    <p>AWS</p>
                </div>
                <div class="skill">
                    <i class="fab fa-microsoft"></i>
                    <p>Azure</p>
                </div>
                <div class="skill">
                    <i class="fab fa-node-js"></i>
                    <p>Node.js</p>
                </div>
                <div class="skill">
                    <i class="fab fa-react"></i>
                    <p>React</p>
                </div>
                <div class="skill">
                    <i class="fab fa-js"></i>
                    <p>JavaScript</p>
                </div>
                <div class="skill">
                    <i class="fab fa-typescript"></i>
                    <p>TypeScript</p>
                </div>
                <div class="skill">
                    <i class="fas fa-database"></i>
                    <p>MongoDB</p>
                </div>
                <div class="skill">
                    <i class="fas fa-database"></i>
                    <p>PostgreSQL</p>
                </div>
                <div class="skill">
                    <i class="fab fa-python"></i>
                    <p>Python</p>
                </div>
                <div class="skill">
                    <i class="fab fa-git-alt"></i>
                    <p>Git</p>
                </div>
                <div class="skill">
                    <i class="fab fa-docker"></i>
                    <p>Docker</p>
                </div>
                <div class="skill">
                    <i class="fab fa-nestjs"></i>
                    <p>NestJS</p>
                </div>
            </div>
        </div>
        
        <div class="stats">
            <div class="stat-row">
                <div class="stat-chart">
                    <h3 align="center"><i class="fas fa-code-branch"></i> Most Used Languages</h3>
                    <p align="center">
                        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=muhammedusmankhan&layout=compact&theme=radical" alt="Most Used Languages">
                    </p>
                </div>
                <div class="stat-chart">
                    <h3 align="center"><i class="fas fa-chart-line"></i> GitHub Stats</h3>
                    <p align="center">
                        <img src="https://github-readme-stats.vercel.app/api?username=muhammedusmankhan&show_icons=true&theme=radical" alt="GitHub Stats">
                    </p>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <p>Made with ❤️ by Usman | © 2023</p>
        </div>
    </div>

    <script>
        // Create stars for background
        function createStars() {
            const starsContainer = document.getElementById('stars');
            const starsCount = 100;
            
            for (let i = 0; i < starsCount; i++) {
                const star = document.createElement('div');
                star.classList.add('star');
                
                // Random properties for each star
                const size = Math.random() * 3;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const delay = Math.random() * 5;
                
                star.style.width = `${size}px`;
                star.style.height = `${size}px`;
                star.style.left = `${posX}%`;
                star.style.top = `${posY}%`;
                star.style.animationDelay = `${delay}s`;
                
                starsContainer.appendChild(star);
            }
        }
        
        // Simulate view count with random number
        function simulateViewCount() {
            const baseCount = 123; // You can set your actual count here
            const randomIncrement = Math.floor(Math.random() * 50);
            document.getElementById('viewCount').textContent = baseCount + randomIncrement;
        }
        
        // Initialize everything when page loads
        window.addEventListener('load', function() {
            createStars();
            simulateViewCount();
            
            // Add hover effect to all skills
            const skills = document.querySelectorAll('.skill');
            skills.forEach(skill => {
                skill.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-8px) rotate(3deg)';
                    this.style.background = 'rgba(78, 205, 196, 0.2)';
                });
                
                skill.addEventListener('mouseleave', function() {
                    this.style.transform = '';
                    this.style.background = 'rgba(255, 255, 255, 0.1)';
                });
            });
        });
    </script>
</body>
</html>
