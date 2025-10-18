
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ayar Suresh - Creative Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: #ffffff;
            color: #1a1a1a;
            overflow-x: hidden;
        }

        /* Animated gradient background */
        .hero {
            position: relative;
            min-height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 25%, #f093fb 50%, #4facfe 75%, #00f2fe 100%);
            background-size: 400% 400%;
            animation: gradientShift 15s ease infinite;
            display: flex;
            align-items: center;
            justify-content: center;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
            overflow: hidden;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .hero-content {
            text-align: center;
            z-index: 10;
            color: white;
            animation: fadeInUp 1s ease-out;
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

        .hero-content h1 {
            font-size: 5rem;
            font-weight: 900;
            margin-bottom: 20px;
            text-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            letter-spacing: -2px;
        }

        .hero-content p {
            font-size: 1.8rem;
            font-weight: 300;
            margin-bottom: 40px;
            opacity: 0.95;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 16px 40px;
            font-size: 1.1rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: white;
            color: #667eea;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.3);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border: 2px solid white;
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover {
            background: white;
            color: #667eea;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 60px 20px;
        }

        /* Section styling */
        section {
            margin-bottom: 80px;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
            animation: fadeInUp 0.8s ease-out;
        }

        .section-header h2 {
            font-size: 3.5rem;
            margin-bottom: 15px;
            font-weight: 800;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-header p {
            font-size: 1.2rem;
            color: #666;
            max-width: 600px;
            margin: 0 auto;
        }

        /* About section */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .about-text h3 {
            font-size: 2.2rem;
            margin-bottom: 25px;
            color: #1a1a1a;
        }

        .about-text p {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #555;
            margin-bottom: 20px;
        }

        .about-features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 40px;
        }

        .feature-box {
            background: linear-gradient(135deg, #f5f7ff 0%, #f0e6ff 100%);
            padding: 25px;
            border-radius: 15px;
            border-left: 5px solid #667eea;
            transition: all 0.3s ease;
        }

        .feature-box:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.2);
        }

        .feature-box h4 {
            color: #667eea;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .feature-box p {
            color: #666;
            font-size: 0.95rem;
            margin: 0;
        }

        .about-image {
            position: relative;
            height: 400px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 150px;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(102, 126, 234, 0.3);
        }

        /* Skills section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 40px;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .skill-card {
            background: white;
            padding: 40px 30px;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            text-align: center;
            border-top: 5px solid transparent;
        }

        .skill-card:nth-child(1) { border-top-color: #667eea; }
        .skill-card:nth-child(2) { border-top-color: #764ba2; }
        .skill-card:nth-child(3) { border-top-color: #f093fb; }
        .skill-card:nth-child(4) { border-top-color: #4facfe; }

        .skill-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
        }

        .skill-icon {
            font-size: 4rem;
            margin-bottom: 20px;
        }

        .skill-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #1a1a1a;
        }

        .skill-list {
            list-style: none;
            text-align: left;
        }

        .skill-list li {
            padding: 8px 0;
            color: #666;
            display: flex;
            align-items: center;
        }

        .skill-list li::before {
            content: '✓';
            display: inline-block;
            width: 25px;
            height: 25px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 50%;
            text-align: center;
            line-height: 25px;
            margin-right: 12px;
            font-weight: bold;
            font-size: 0.8rem;
            flex-shrink: 0;
        }

        /* Projects section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .project-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            border: 1px solid #f0f0f0;
        }

        .project-card:hover {
            transform: translateY(-20px);
            box-shadow: 0 30px 80px rgba(102, 126, 234, 0.25);
        }

        .project-image {
            height: 200px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
        }

        .project-info {
            padding: 30px;
        }

        .project-info h3 {
            font-size: 1.5rem;
            margin-bottom: 12px;
            color: #1a1a1a;
        }

        .project-info p {
            color: #666;
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .tag {
            background: #f0e6ff;
            color: #667eea;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
        }

        /* Contact section */
        .contact-wrapper {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 30px;
            padding: 80px 40px;
            text-align: center;
            color: white;
            box-shadow: 0 30px 80px rgba(102, 126, 234, 0.3);
            animation: fadeInUp 1s ease-out 0.5s both;
        }

        .contact-wrapper h2 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .contact-wrapper p {
            font-size: 1.2rem;
            margin-bottom: 40px;
            opacity: 0.95;
        }

        .contact-links {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .contact-link {
            background: rgba(255, 255, 255, 0.15);
            color: white;
            padding: 14px 28px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            border: 2px solid rgba(255, 255, 255, 0.3);
        }

        .contact-link:hover {
            background: white;
            color: #667eea;
            transform: translateY(-3px);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px 20px;
            color: #999;
            border-top: 1px solid #f0f0f0;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 3rem;
            }

            .hero-content p {
                font-size: 1.2rem;
            }

            .section-header h2 {
                font-size: 2rem;
            }

            .about-grid {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .about-image {
                height: 300px;
            }

            .hero {
                clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
            }

            .contact-wrapper {
                padding: 50px 30px;
            }

            .contact-wrapper h2 {
                font-size: 2rem;
            }
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
            margin: 60px 0;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .stat {
            text-align: center;
            padding: 30px;
            background: linear-gradient(135deg, #f5f7ff 0%, #f0e6ff 100%);
            border-radius: 15px;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
        }

        .stat-label {
            color: #666;
            font-weight: 600;
        }

        @media (max-width: 768px) {
            .stats {
                grid-template-columns: repeat(2, 1fr);
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <div class="hero">
        <div class="hero-content">
            <h1>AYAR SURESH</h1>
            <p>Full Stack Developer & Mobile Innovator</p>
            <div class="cta-buttons">
                <button class="btn btn-primary">View My Work</button>
                <button class="btn btn-secondary">Get In Touch</button>
            </div>
        </div>
    </div>

    <div class="container">
        <!-- About Section -->
        <section>
            <div class="section-header">
                <h2>About Me</h2>
                <p>Crafting digital experiences with code and creativity</p>
            </div>

            <div class="about-grid">
                <div class="about-text">
                    <h3>Hi, I'm Ayar 👋</h3>
                    <p>I'm a passionate full-stack developer based in Ahmedabad, India. With years of experience in mobile and web development, I turn complex problems into elegant, user-friendly solutions.</p>
                    <p>My expertise spans from building stunning mobile apps with Flutter to creating robust backend systems with Python. I'm committed to writing clean, efficient code and staying at the forefront of technology trends.</p>
                    
                    <div class="about-features">
                        <div class="feature-box">
                            <h4>🚀 Innovation</h4>
                            <p>Pushing boundaries with cutting-edge tech</p>
                        </div>
                        <div class="feature-box">
                            <h4>🎯 Focus</h4>
                            <p>Delivering high-quality solutions</p>
                        </div>
                        <div class="feature-box">
                            <h4>🤝 Collaboration</h4>
                            <p>Working seamlessly with teams</p>
                        </div>
                        <div class="feature-box">
                            <h4>📚 Growth</h4>
                            <p>Constantly learning & evolving</p>
                        </div>
                    </div>
                </div>

                <div class="about-image">💻</div>
            </div>

            <div class="stats">
                <div class="stat">
                    <div class="stat-number">80%</div>
                    <div class="stat-label">Flutter/Dart</div>
                </div>
                <div class="stat">
                    <div class="stat-number">75%</div>
                    <div class="stat-label">Mobile Dev</div>
                </div>
                <div class="stat">
                    <div class="stat-number">80%</div>
                    <div class="stat-label">Python</div>
                </div>
                <div class="stat">
                    <div class="stat-number">70%</div>
                    <div class="stat-label">Web Dev</div>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section>
            <div class="section-header">
                <h2>My Skills</h2>
                <p>Technologies and tools I work with daily</p>
            </div>

            <div class="skills-container">
                <div class="skill-card">
                    <div class="skill-icon">📱</div>
                    <h3>Mobile Development</h3>
                    <ul class="skill-list">
                        <li>Flutter & Dart</li>
                        <li>Android Development</li>
                        <li>Cross-platform Apps</li>
                        <li>Native Integration</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">🌐</div>
                    <h3>Web Development</h3>
                    <ul class="skill-list">
                        <li>JavaScript & HTML5</li>
                        <li>CSS3 & Design</li>
                        <li>Responsive Design</li>
                        <li>UI/UX Implementation</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">⚡</div>
                    <h3>Backend & Tools</h3>
                    <ul class="skill-list">
                        <li>Python Programming</li>
                        <li>Firebase & Databases</li>
                        <li>Docker & DevOps</li>
                        <li>Git & Version Control</li>
                    </ul>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">🎨</div>
                    <h3>Design & More</h3>
                    <ul class="skill-list">
                        <li>Figma Design</li>
                        <li>UX/UI Design</li>
                        <li>Open Source</li>
                        <li>Tech Innovation</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section>
            <div class="section-header">
                <h2>Featured Projects</h2>
                <p>Showcasing my best work and innovations</p>
            </div>

            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-image">📱</div>
                    <div class="project-info">
                        <h3>WhatsApp Status Saver</h3>
                        <p>A revolutionary mobile app for managing and organizing WhatsApp statuses with cloud backup integration.</p>
                        <div class="project-tags">
                            <span class="tag">Flutter</span>
                            <span class="tag">Firebase</span>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-image">🏗️</div>
                    <div class="project-info">
                        <h3>Construction Portal</h3>
                        <p>Comprehensive web platform for construction project management with real-time tracking and resource allocation.</p>
                        <div class="project-tags">
                            <span class="tag">JavaScript</span>
                            <span class="tag">Python</span>
                            <span class="tag">Firebase</span>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-image">🚀</div>
                    <div class="project-info">
                        <h3>Tech Innovation Hub</h3>
                        <p>Personal portfolio platform showcasing tech projects, innovations, and contributions to the open-source community.</p>
                        <div class="project-tags">
                            <span class="tag">Web</span>
                            <span class="tag">Design</span>
                            <span class="tag">Innovation</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section>
            <div class="contact-wrapper">
                <h2>Let's Create Something Amazing</h2>
                <p>I'm always excited to collaborate on new projects and ideas</p>
                <div class="contact-links">
                    <a href="mailto:ahir385350@gmail.com" class="contact-link">📧 Email</a>
                    <a href="https://wa.me/918320097437" class="contact-link">💬 WhatsApp</a>
                    <a href="https://www.linkedin.com/in/ayar-suresh-itpro/" class="contact-link">💼 LinkedIn</a>
                    <a href="https://github.com/Ayar-Suresh" class="contact-link">🔗 GitHub</a>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>© 2025 Ayar Suresh. Crafted with passion and powered by code. 🚀</p>
    </footer>
</body>

