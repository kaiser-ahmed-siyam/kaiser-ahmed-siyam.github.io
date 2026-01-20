<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kaiser Ahmed | AI/ML Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&family=Orbitron:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #0a0a0a;
            --secondary: #00ff88;
            --accent: #0099ff;
            --text: #ffffff;
            --gray: #1a1a1a;
            --glass: rgba(255, 255, 255, 0.05);
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: var(--primary);
            color: var(--text);
            overflow-x: hidden;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            background: rgba(10, 10, 10, 0.9);
            backdrop-filter: blur(10px);
            padding: 20px 0;
            transition: all 0.3s ease;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.8rem;
            font-weight: 600;
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--text);
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            padding-top: 100px;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 30% 20%, rgba(0, 255, 136, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 70% 80%, rgba(0, 153, 255, 0.1) 0%, transparent 50%);
            z-index: -1;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .hero h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 4rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #fff, var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 0 0 10px rgba(0, 255, 136, 0.5);
            }
            to {
                text-shadow: 0 0 20px rgba(0, 255, 136, 0.8),
                             0 0 30px rgba(0, 255, 136, 0.3);
            }
        }

        .hero h2 {
            font-size: 1.8rem;
            font-weight: 300;
            margin-bottom: 30px;
            color: var(--secondary);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 40px;
            opacity: 0.9;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 15px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .btn-primary {
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            color: var(--primary);
        }

        .btn-secondary {
            border: 2px solid var(--secondary);
            color: var(--secondary);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 255, 136, 0.2);
        }

        /* Sections */
        section {
            padding: 100px 0;
        }

        .section-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 50px;
            color: var(--secondary);
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .skill-card {
            background: var(--glass);
            padding: 30px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 255, 136, 0.1);
        }

        .skill-icon {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: var(--gray);
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        .project-img {
            height: 200px;
            background: linear-gradient(45deg, var(--secondary), var(--accent));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: var(--primary);
        }

        .project-content {
            padding: 20px;
        }

        .project-tech {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin: 15px 0;
        }

        .tech-tag {
            background: rgba(0, 255, 136, 0.1);
            color: var(--secondary);
            padding: 5px 15px;
            border-radius: 15px;
            font-size: 0.9rem;
        }

        /* Contact */
        .contact-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }

        .contact-item {
            text-align: center;
            padding: 30px;
            background: var(--glass);
            border-radius: 15px;
            transition: transform 0.3s;
        }

        .contact-item:hover {
            transform: translateY(-5px);
        }

        .contact-item i {
            font-size: 2rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        /* Footer */
        footer {
            background: var(--gray);
            padding: 50px 0 20px;
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .social-links a {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--glass);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text);
            font-size: 1.2rem;
            transition: all 0.3s;
        }

        .social-links a:hover {
            background: var(--secondary);
            color: var(--primary);
            transform: translateY(-5px);
        }

        .copyright {
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero h2 {
                font-size: 1.3rem;
            }

            .nav-links {
                position: fixed;
                top: 70px;
                left: 0;
                width: 100%;
                background: var(--primary);
                flex-direction: column;
                align-items: center;
                padding: 20px;
                gap: 15px;
                transform: translateY(-100%);
                opacity: 0;
                transition: all 0.3s;
                display: none;
            }

            .nav-links.active {
                transform: translateY(0);
                opacity: 1;
                display: flex;
            }

            .mobile-menu-btn {
                display: block;
            }

            .section-title {
                font-size: 2rem;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn {
                width: 100%;
                max-width: 300px;
                justify-content: center;
            }
        }

        /* Animations */
        .fade-in {
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .neon-line {
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--secondary), transparent);
            margin: 40px auto;
            max-width: 200px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">KAISER</div>
                <div class="nav-links" id="navLinks">
                    <a href="#home">Home</a>
                    <a href="#about">About</a>
                    <a href="#skills">Skills</a>
                    <a href="#projects">Projects</a>
                    <a href="#contact">Contact</a>
                </div>
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-bg"></div>
        <div class="container hero-content fade-in">
            <h1>Kaiser Ahmed Siyam</h1>
            <h2>AI & Machine Learning Engineer</h2>
            <p>Specializing in Computer Vision, Generative AI, and Deep Learning solutions that push the boundaries of artificial intelligence.</p>
            <div class="cta-buttons">
                <a href="#projects" class="btn btn-primary">
                    <i class="fas fa-rocket"></i> View Projects
                </a>
                <a href="#contact" class="btn btn-secondary">
                    <i class="fas fa-paper-plane"></i> Contact Me
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="container">
        <h2 class="section-title">About Me</h2>
        <div class="neon-line"></div>
        <div style="max-width: 800px; margin: 0 auto;" class="fade-in">
            <p style="font-size: 1.2rem; margin-bottom: 30px;">
                Passionate AI/ML Engineer with comprehensive expertise in Machine Learning, Computer Vision, Generative AI, and Deep Learning. I thrive on solving complex problems using cutting-edge AI technologies.
            </p>
            <p style="font-size: 1.2rem;">
                My journey in AI began with a fascination for how machines can learn and perceive the world. Now, I build intelligent systems that can see, create, and understand - transforming data into meaningful insights and innovative solutions.
            </p>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" style="background: rgba(0,0,0,0.5);">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="neon-line"></div>
            <div class="skills-grid">
                <div class="skill-card fade-in">
                    <div class="skill-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3>Machine Learning</h3>
                    <p>Supervised & Unsupervised Learning, Regression, Classification, Clustering, Model Evaluation</p>
                </div>
                <div class="skill-card fade-in">
                    <div class="skill-icon">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h3>Computer Vision</h3>
                    <p>Image Processing, Object Detection, Image Segmentation, CNN Architectures, OpenCV</p>
                </div>
                <div class="skill-card fade-in">
                    <div class="skill-icon">
                        <i class="fas fa-robot"></i>
                    </div>
                    <h3>Generative AI</h3>
                    <p>GANs, VAEs, Diffusion Models, Stable Diffusion, Text-to-Image Generation</p>
                </div>
                <div class="skill-card fade-in">
                    <div class="skill-icon">
                        <i class="fas fa-layer-group"></i>
                    </div>
                    <h3>Deep Learning</h3>
                    <p>Neural Networks, TensorFlow, PyTorch, Transformers, NLP, Reinforcement Learning</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <h2 class="section-title">AI/ML Projects</h2>
            <div class="neon-line"></div>
            <div class="projects-grid">
                <div class="project-card fade-in">
                    <div class="project-img">
                        <i class="fas fa-image"></i>
                    </div>
                    <div class="project-content">
                        <h3>Intelligent Image Generator</h3>
                        <p>AI-powered image generation system using Stable Diffusion with custom-trained models for specific domains.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">PyTorch</span>
                            <span class="tech-tag">Stable Diffusion</span>
                        </div>
                    </div>
                </div>
                <div class="project-card fade-in">
                    <div class="project-img">
                        <i class="fas fa-car"></i>
                    </div>
                    <div class="project-content">
                        <h3>Real-time Object Detection</h3>
                        <p>Advanced computer vision system for real-time object detection and tracking using YOLOv8 architecture.</p>
                        <div class="project-tech">
                            <span class="tech-tag">OpenCV</span>
                            <span class="tech-tag">YOLOv8</span>
                            <span class="tech-tag">TensorFlow</span>
                        </div>
                    </div>
                </div>
                <div class="project-card fade-in">
                    <div class="project-img">
                        <i class="fas fa-comment-medical"></i>
                    </div>
                    <div class="project-content">
                        <h3>Medical Image Analysis</h3>
                        <p>Deep learning model for automated medical image diagnosis with 95% accuracy in disease detection.</p>
                        <div class="project-tech">
                            <span class="tech-tag">CNN</span>
                            <span class="tech-tag">Transfer Learning</span>
                            <span class="tech-tag">Scikit-learn</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" style="background: rgba(0,0,0,0.5);">
        <div class="container">
            <h2 class="section-title">Let's Connect</h2>
            <div class="neon-line"></div>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item fade-in">
                        <i class="fas fa-envelope"></i>
                        <h3>Email</h3>
                        <p>kaiser.siyam@example.com</p>
                    </div>
                    <div class="contact-item fade-in">
                        <i class="fas fa-map-marker-alt"></i>
                        <h3>Location</h3>
                        <p>Available Worldwide</p>
                    </div>
                    <div class="contact-item fade-in">
                        <i class="fas fa-briefcase"></i>
                        <h3>Status</h3>
                        <p>Open to Opportunities</p>
                    </div>
                </div>
                
                <div style="text-align: center;" class="fade-in">
                    <p style="font-size: 1.2rem; margin-bottom: 30px;">
                        Interested in collaborating on AI projects or have opportunities in ML/Computer Vision?
                    </p>
                    <a href="mailto:kaiser.siyam@example.com" class="btn btn-primary">
                        <i class="fas fa-envelope"></i> Send Message
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="logo" style="font-size: 2rem;">KAS</div>
            <p style="margin: 20px 0; opacity: 0.8;">Building Intelligent Systems for Tomorrow</p>
            
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-kaggle"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
            </div>
            
            <div class="copyright">
                <p>&copy; 2024 Kaiser Ahmed Siyam. All rights reserved.</p>
                <p style="font-size: 0.9rem; margin-top: 10px;">AI & ML Engineer Portfolio</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navLinks = document.getElementById('navLinks');

        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            mobileMenuBtn.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });

        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if(navLinks.classList.contains('active')) {
                        navLinks.classList.remove('active');
                        mobileMenuBtn.innerHTML = '<i class="fas fa-bars"></i>';
                    }
                }
            });
        });

        // Header Scroll Effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if(window.scrollY > 100) {
                header.style.padding = '10px 0';
                header.style.background = 'rgba(10, 10, 10, 0.95)';
            } else {
                header.style.padding = '20px 0';
                header.style.background = 'rgba(10, 10, 10, 0.9)';
            }
        });

        // Fade-in Animation on Scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);

        // Observe all elements with fade-in class
        document.querySelectorAll('.skill-card, .project-card, .contact-item').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
