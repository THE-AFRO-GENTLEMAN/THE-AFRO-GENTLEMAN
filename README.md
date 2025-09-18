<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amazing GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Space Grotesk', sans-serif;
            background: linear-gradient(135deg, #0f0f1a 0%, #1a1a2e 100%);
            color: #e6e6ff;
            line-height: 1.6;
            padding: 2rem;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .github-profile {
            background: rgba(13, 17, 28, 0.8);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            overflow: hidden;
            border: 1px solid rgba(101, 119, 236, 0.3);
            padding: 2rem;
            position: relative;
        }

        .profile-header {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 2rem 0;
            position: relative;
            z-index: 2;
        }

        .profile-image {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 4px solid #6577ec;
            box-shadow: 0 0 30px rgba(101, 119, 236, 0.6);
            margin-bottom: 1.5rem;
            overflow: hidden;
            position: relative;
            transition: transform 0.5s ease;
        }

        .profile-image:hover {
            transform: scale(1.05);
        }

        .profile-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .profile-name {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            background: linear-gradient(90deg, #8a64d0, #6577ec, #4d8dea);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(101, 119, 236, 0.4);
        }

        .profile-tagline {
            font-size: 1.5rem;
            color: #aab2ff;
            margin-bottom: 1.5rem;
            font-weight: 400;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(101, 119, 236, 0.2);
            color: #aab2ff;
            font-size: 1.5rem;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .social-link:hover {
            background: #6577ec;
            color: #fff;
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(101, 119, 236, 0.4);
        }

        .profile-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-top: 2rem;
        }

        @media (max-width: 900px) {
            .profile-content {
                grid-template-columns: 1fr;
            }
        }

        .card {
            background: rgba(18, 22, 40, 0.6);
            border-radius: 15px;
            padding: 1.5rem;
            border: 1px solid rgba(101, 119, 236, 0.2);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .card-title {
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: #8a64d0;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .skill {
            background: rgba(101, 119, 236, 0.2);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }

        .skill:hover {
            background: #6577ec;
            transform: scale(1.05);
        }

        .achievement {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
            padding: 1rem;
            background: rgba(101, 119, 236, 0.1);
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .achievement:hover {
            background: rgba(101, 119, 236, 0.2);
            transform: translateX(5px);
        }

        .achievement-icon {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(138, 100, 208, 0.2);
            border-radius: 50%;
            font-size: 1.5rem;
            color: #8a64d0;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1rem;
        }

        .stat {
            text-align: center;
            padding: 1.5rem;
            background: rgba(18, 22, 40, 0.6);
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .stat:hover {
            background: rgba(101, 119, 236, 0.2);
            transform: scale(1.03);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #6577ec;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            color: #aab2ff;
            font-size: 1rem;
        }

        .highlight {
            color: #6577ec;
            font-weight: 500;
        }

        .quote {
            font-style: italic;
            text-align: center;
            margin: 2rem 0;
            padding: 1.5rem;
            border-radius: 15px;
            background: rgba(138, 100, 208, 0.1);
            border-left: 4px solid #8a64d0;
        }

        .footer {
            text-align: center;
            margin-top: 3rem;
            color: #aab2ff;
            font-size: 0.9rem;
        }

        .badge {
            display: inline-block;
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: 600;
            margin: 0.3rem;
        }

        .badge-primary {
            background: rgba(101, 119, 236, 0.2);
            color: #6577ec;
        }

        .badge-secondary {
            background: rgba(138, 100, 208, 0.2);
            color: #8a64d0;
        }

        .pulse {
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(101, 119, 236, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(101, 119, 236, 0); }
            100% { box-shadow: 0 0 0 0 rgba(101, 119, 236, 0); }
        }

        .typing-demo {
            width: max-content;
            animation: typing 3s steps(30), blink .5s step-end infinite alternate;
            white-space: nowrap;
            overflow: hidden;
            border-right: 3px solid;
            margin: 0 auto;
            font-family: 'JetBrains Mono', monospace;
            color: #aab2ff;
            margin-bottom: 2rem;
        }

        @keyframes typing {
            from { width: 0 }
        }

        @keyframes blink {
            50% { border-color: transparent }
        }

        .glow {
            text-shadow: 0 0 10px rgba(101, 119, 236, 0.7);
        }

        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
            overflow: hidden;
        }

        .particle {
            position: absolute;
            border-radius: 50%;
            background: rgba(101, 119, 236, 0.3);
            animation: float 15s infinite linear;
        }

        @keyframes float {
            0% { transform: translateY(0) translateX(0) rotate(0deg); }
            100% { transform: translateY(-1000px) translateX(100px) rotate(360deg); }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="github-profile">
            <!-- Animated background particles -->
            <div class="particles" id="particles"></div>
            
            <div class="profile-header">
                <div class="profile-image pulse">
                    <img src="https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80" alt="Profile Picture">
                </div>
                <h1 class="profile-name">Alex Morgan</h1>
                <p class="profile-tagline">Full-Stack Developer & UI/UX Enthusiast</p>
                
                <div class="social-links">
                    <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                    <a href="#" class="social-link"><i class="fab fa-dev"></i></a>
                    <a href="#" class="social-link"><i class="fas fa-envelope"></i></a>
                </div>
                
                <div class="typing-demo">
                    npm create amazing-profile@latest
                </div>
            </div>
            
            <div class="quote">
                <p>"First, solve the problem. Then, write the code." - John Johnson</p>
            </div>
            
            <div class="profile-content">
                <div class="card">
                    <h2 class="card-title"><i class="fas fa-user"></i> About Me</h2>
                    <p>Hello! I'm Alex, a passionate full-stack developer with over 5 years of experience creating digital experiences that users love.</p>
                    <p>I specialize in <span class="highlight">React, Node.js, Python, and Cloud Architecture</span>. When I'm not coding, you can find me contributing to open source, writing tech blogs, or hiking in the mountains.</p>
                    <p>I believe in writing clean, efficient code and creating applications that make a positive impact.</p>
                </div>
                
                <div class="card">
                    <h2 class="card-title"><i class="fas fa-rocket"></i> Achievements</h2>
                    
                    <div class="achievement">
                        <div class="achievement-icon">
                            <i class="fas fa-trophy"></i>
                        </div>
                        <div>
                            <h3>GitHub Star</h3>
                            <p>Awarded GitHub Star for open source contributions</p>
                        </div>
                    </div>
                    
                    <div class="achievement">
                        <div class="achievement-icon">
                            <i class="fas fa-medal"></i>
                        </div>
                        <div>
                            <h3>Hackathon Winner</h3>
                            <p>1st place at CodeFest 2022 with a real-time collaboration tool</p>
                        </div>
                    </div>
                    
                    <div class="achievement">
                        <div class="achievement-icon">
                            <i class="fas fa-code-branch"></i>
                        </div>
                        <div>
                            <h3>Open Source</h3>
                            <p>Maintainer of 3 popular open source projects with 500+ stars</p>
                        </div>
                    </div>
                </div>
                
                <div class="card">
                    <h2 class="card-title"><i class="fas fa-code"></i> Technologies & Skills</h2>
                    <div class="skills-container">
                        <span class="skill">JavaScript</span>
                        <span class="skill">TypeScript</span>
                        <span class="skill">React</span>
                        <span class="skill">Node.js</span>
                        <span class="skill">Python</span>
                        <span class="skill">GraphQL</span>
                        <span class="skill">AWS</span>
                        <span class="skill">Docker</span>
                        <span class="skill">Kubernetes</span>
                        <span class="skill">PostgreSQL</span>
                        <span class="skill">MongoDB</span>
                        <span class="skill">Redis</span>
                        <span class="skill">CI/CD</span>
                        <span class="skill">Jest</span>
                        <span class="skill">Cypress</span>
                    </div>
                </div>
                
                <div class="card">
                    <h2 class="card-title"><i class="fas fa-heart"></i> Current Interests</h2>
                    <p>I'm currently exploring and deepening my knowledge in:</p>
                    <ul style="margin-left: 1.5rem; margin-top: 0.5rem;">
                        <li>Web3 and Blockchain development</li>
                        <li>Machine Learning with TensorFlow</li>
                        <li>Serverless architecture patterns</li>
                        <li>Design systems and component libraries</li>
                    </ul>
                    <p style="margin-top: 1rem;">Always open to collaborating on innovative projects!</p>
                </div>
            </div>
            
            <h2 style="text-align: center; margin: 3rem 0 2rem 0; color: #8a64d0; font-size: 2rem;">
                <i class="fas fa-chart-line"></i> GitHub Stats
            </h2>
            
            <div class="stats">
                <div class="stat">
                    <div class="stat-number">2,548</div>
                    <div class="stat-label">Contributions</div>
                </div>
                <div class="stat">
                    <div class="stat-number">42</div>
                    <div class="stat-label">Repositories</div>
                </div>
                <div class="stat">
                    <div class="stat-number">18</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat">
                    <div class="stat-number">1.2k</div>
                    <div class="stat-label">Followers</div>
                </div>
            </div>
            
            <div class="footer">
                <p>Last Updated: October 2023 | <span class="glow">Made with ❤️ and CSS</span></p>
                <div style="margin-top: 1rem;">
                    <span class="badge badge-primary">PRO</span>
                    <span class="badge badge-secondary">DEV</span>
                    <span class="badge badge-primary">GitHub</span>
                    <span class="badge badge-secondary">Open Source</span>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Create animated particles
        document.addEventListener('DOMContentLoaded', function() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                const size = Math.random() * 20 + 5;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.top = `${Math.random() * 100}%`;
                
                particle.style.animationDuration = `${Math.random() * 15 + 10}s`;
                particle.style.animationDelay = `${Math.random() * 5}s`;
                particle.style.opacity = Math.random() * 0.5 + 0.1;
                
                particlesContainer.appendChild(particle);
            }
            
            // Add typing effect for the tagline
            const tagline = document.querySelector('.profile-tagline');
            const originalText = tagline.textContent;
            tagline.textContent = '';
            
            let i = 0;
            function typeWriter() {
                if (i < originalText.length) {
                    tagline.textContent += originalText.charAt(i);
                    i++;
                    setTimeout(typeWriter, 100);
                }
            }
            
            setTimeout(typeWriter, 2000);
        });
    </script>
</body>
</html>
