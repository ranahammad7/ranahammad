<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hammad Raza - Senior Flutter Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 24px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            animation: slideUp 0.8s ease-out;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 60px 40px;
            text-align: center;
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
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="20" cy="20" r="2" fill="rgba(255,255,255,0.1)"/><circle cx="60" cy="30" r="1" fill="rgba(255,255,255,0.1)"/><circle cx="40" cy="70" r="1.5" fill="rgba(255,255,255,0.1)"/><circle cx="80" cy="60" r="1" fill="rgba(255,255,255,0.1)"/></svg>');
            animation: float 20s infinite linear;
        }

        @keyframes float {
            0% { transform: translate(-50%, -50%) rotate(0deg); }
            100% { transform: translate(-50%, -50%) rotate(360deg); }
        }

        .profile-name {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 10px;
            position: relative;
            z-index: 2;
        }

        .profile-title {
            font-size: 1.3rem;
            opacity: 0.9;
            margin-bottom: 20px;
            position: relative;
            z-index: 2;
        }

        .profile-summary {
            font-size: 1.1rem;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            opacity: 0.9;
            position: relative;
            z-index: 2;
        }

        .content {
            padding: 50px 40px;
        }

        .section {
            margin-bottom: 50px;
        }

        .section-title {
            font-size: 2rem;
            font-weight: 700;
            color: #2d3748;
            margin-bottom: 25px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 30px;
        }

        .skill-category {
            background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
            padding: 25px;
            border-radius: 16px;
            border-left: 4px solid #667eea;
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .skill-category h3 {
            color: #2d3748;
            font-weight: 600;
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .skill-tag {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: white;
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            border: 1px solid #e2e8f0;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.15);
        }

        .project-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: #2d3748;
            margin-bottom: 12px;
        }

        .project-description {
            color: #718096;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            color: #667eea;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            color: #764ba2;
            transform: translateX(5px);
        }

        .contact-section {
            background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
            padding: 40px;
            border-radius: 20px;
            text-align: center;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .contact-item {
            background: white;
            padding: 25px;
            border-radius: 16px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .contact-icon {
            font-size: 2rem;
            margin-bottom: 15px;
            color: #667eea;
        }

        .contact-label {
            font-weight: 600;
            color: #2d3748;
            margin-bottom: 8px;
        }

        .contact-value {
            color: #718096;
        }

        .contact-value a {
            color: #667eea;
            text-decoration: none;
        }

        .contact-value a:hover {
            text-decoration: underline;
        }

        .stats {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin: 30px 0;
            flex-wrap: wrap;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            color: white;
            display: block;
        }

        .stat-label {
            font-size: 0.9rem;
            opacity: 0.9;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        @media (max-width: 768px) {
            .container {
                margin: 10px;
                border-radius: 16px;
            }

            .header {
                padding: 40px 20px;
            }

            .profile-name {
                font-size: 2.5rem;
            }

            .content {
                padding: 30px 20px;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .stats {
                gap: 20px;
            }

            .stat-number {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1 class="profile-name">Hammad Raza</h1>
            <p class="profile-title">Senior Flutter Developer & Mobile App Architect</p>
            <div class="stats">
                <div class="stat">
                    <span class="stat-number">4+</span>
                    <span class="stat-label">Years Experience</span>
                </div>
                <div class="stat">
                    <span class="stat-number">45+</span>
                    <span class="stat-label">Published Apps</span>
                </div>
                <div class="stat">
                    <span class="stat-number">5+</span>
                    <span class="stat-label">Industries</span>
                </div>
            </div>
            <p class="profile-summary">
                Passionate about crafting beautiful UIs and scalable architectures. Specialized in cross-platform development for healthcare, fintech, real estate, and telecom industries using cutting-edge Flutter technology.
            </p>
        </div>

        <div class="content">
            <div class="section">
                <h2 class="section-title">💻 Technical Skills</h2>
                <div class="skills-grid">
                    <div class="skill-category">
                        <h3>Languages</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Dart</span>
                            <span class="skill-tag">JavaScript</span>
                        </div>
                    </div>
                    <div class="skill-category">
                        <h3>Frameworks & Architecture</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Flutter</span>
                            <span class="skill-tag">GetX</span>
                            <span class="skill-tag">Provider</span>
                            <span class="skill-tag">BLoC</span>
                        </div>
                    </div>
                    <div class="skill-category">
                        <h3>Backend & APIs</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Firebase</span>
                            <span class="skill-tag">REST APIs</span>
                            <span class="skill-tag">WebSockets</span>
                        </div>
                    </div>
                    <div class="skill-category">
                        <h3>Databases</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Firestore</span>
                            <span class="skill-tag">SQLite</span>
                            <span class="skill-tag">Hive</span>
                        </div>
                    </div>
                    <div class="skill-category">
                        <h3>Development Tools</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Git</span>
                            <span class="skill-tag">GitHub</span>
                            <span class="skill-tag">CI/CD</span>
                            <span class="skill-tag">Postman</span>
                        </div>
                    </div>
                    <div class="skill-category">
                        <h3>IDEs</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Android Studio</span>
                            <span class="skill-tag">VS Code</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="section">
                <h2 class="section-title">🚀 Featured Projects</h2>
                <div class="projects-grid">
                    <div class="project-card">
                        <h3 class="project-title">Seyyah Mobile</h3>
                        <p class="project-description">
                            International eSIM management application enabling seamless global connectivity and travel communication solutions.
                        </p>
                        <a href="https://play.google.com/store/apps/details?id=com.seyyahmobile" class="project-link" target="_blank">
                            View on Play Store →
                        </a>
                    </div>
                    <div class="project-card">
                        <h3 class="project-title">Connects App</h3>
                        <p class="project-description">
                            Comprehensive multi-level marketing platform with advanced referral systems and network management capabilities.
                        </p>
                        <a href="https://play.google.com/store/apps/details?id=com.connects.nsol" class="project-link" target="_blank">
                            View on Play Store →
                        </a>
                    </div>
                    <div class="project-card">
                        <h3 class="project-title">Joy App</h3>
                        <p class="project-description">
                            Revolutionary telemedicine platform providing healthcare services with real-time consultation and patient management.
                        </p>
                        <a href="https://play.google.com/store/apps/details?id=com.alrightech.ddf" class="project-link" target="_blank">
                            View on Play Store →
                        </a>
                    </div>
                    <div class="project-card">
                        <h3 class="project-title">YCBuzz</h3>
                        <p class="project-description">
                            Enterprise-grade messaging and productivity suite designed for seamless team collaboration and communication.
                        </p>
                        <a href="https://ycbuzz.com/" class="project-link" target="_blank">
                            Visit Website →
                        </a>
                    </div>
                    <div class="project-card">
                        <h3 class="project-title">Nour Alsham Restaurant</h3>
                        <p class="project-description">
                            Complete restaurant management solution with integrated delivery system and customer ordering platform.
                        </p>
                        <a href="https://play.google.com/store/apps/details?id=com.nouralshamapp.nour_alsham" class="project-link" target="_blank">
                            View on Play Store →
                        </a>
                    </div>
                    <div class="project-card">
                        <h3 class="project-title">YC Time Tracker</h3>
                        <p class="project-description">
                            Cross-platform desktop application for productivity tracking with advanced time management and reporting features.
                        </p>
                        <a href="https://snapcraft.io/yctimetracker" class="project-link" target="_blank">
                            View on Snapcraft →
                        </a>
                    </div>
                </div>
            </div>

            <div class="section">
                <div class="contact-section">
                    <h2 class="section-title">📬 Let's Connect</h2>
                    <p style="color: #718096; font-size: 1.1rem; margin-bottom: 20px;">
                        Ready to bring your mobile app vision to life? Let's discuss your next project!
                    </p>
                    <div class="contact-grid">
                        <div class="contact-item">
                            <div class="contact-icon">📧</div>
                            <div class="contact-label">Email</div>
                            <div class="contact-value">
                                <a href="mailto:ranahr5656@gmail.com">ranahr5656@gmail.com</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">📱</div>
                            <div class="contact-label">WhatsApp</div>
                            <div class="contact-value">
                                <a href="https://wa.me/923176558363">+92 317 655 8363</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">💼</div>
                            <div class="contact-label">LinkedIn</div>
                            <div class="contact-value">
                                <a href="https://www.linkedin.com/in/ranahammad7/" target="_blank">ranahammad7</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">🌐</div>
                            <div class="contact-label">Portfolio</div>
                            <div class="contact-value">Coming Soon</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Add smooth scrolling and animations
        document.addEventListener('DOMContentLoaded', function() {
            // Intersection Observer for animations
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };

            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);

            // Observe elements for animation
            const animatedElements = document.querySelectorAll('.project-card, .skill-category, .contact-item');
            animatedElements.forEach(el => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(20px)';
                el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
                observer.observe(el);
            });

            // Add hover effects for project cards
            const projectCards = document.querySelectorAll('.project-card');
            projectCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-8px) scale(1.02)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0) scale(1)';
                });
            });
        });
    </script>
</body>
</html>
