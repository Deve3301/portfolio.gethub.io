# portfolio.gethub.io[portfolio.html](https://github.com/user-attachments/files/26380025/portfolio.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Developer Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #000000;
            --bg-secondary: #1a1a1a;
            --text-primary: #ffffff;
            --text-secondary: #aaaaaa;
            --accent: #ff4444;
            --accent-hover: #ff6666;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 0;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .hero {
            min-height: 80vh;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            gap: 3rem;
        }

        .hero-content {
            flex: 1;
        }

        .hero-image {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--accent);
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            margin-bottom: 1rem;
            line-height: 1.1;
        }

        .hero h1 span {
            color: var(--accent);
        }

        .typed-text {
            color: var(--accent);
        }

        .hero p {
            font-size: 1.5rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2rem;
            background: var(--accent);
            color: var(--bg-primary);
            text-decoration: none;
            border-radius: 6px;
            font-weight: 600;
            transition: background 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn:hover {
            background: var(--accent-hover);
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            background: var(--bg-secondary);
            border: 1px solid #30363d;
            border-radius: 50%;
            color: var(--text-secondary);
            font-size: 1.2rem;
            transition: all 0.3s;
            text-decoration: none;
        }

        .social-links a:hover {
            border-color: var(--accent);
            color: var(--accent);
            transform: translateY(-3px);
        }

        section {
            padding: 5rem 0;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 3rem;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .skill-tag {
            padding: 0.75rem 1.5rem;
            background: var(--bg-secondary);
            border: 1px solid #30363d;
            border-radius: 6px;
            font-size: 0.9rem;
            transition: all 0.3s;
            animation: fadeInUp 0.5s ease forwards;
            opacity: 0;
        }

        .skill-tag:hover {
            border-color: var(--accent);
            transform: translateY(-3px);
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

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--bg-secondary);
            border: 1px solid #30363d;
            border-radius: 8px;
            padding: 1.5rem;
            transition: transform 0.3s, border-color 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent);
        }

        .project-card h3 {
            margin-bottom: 0.5rem;
        }

        .project-card p {
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .project-card a {
            color: var(--accent);
            text-decoration: none;
        }

        .contact {
            text-align: center;
        }

        .contact p {
            color: var(--text-secondary);
            margin-bottom: 2rem;
        }

        .contact-form {
            max-width: 500px;
            margin: 0 auto;
            text-align: left;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1rem;
            background: var(--bg-secondary);
            border: 1px solid #30363d;
            border-radius: 6px;
            color: var(--text-primary);
            font-size: 1rem;
            font-family: inherit;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: var(--accent);
        }

        .contact-form textarea {
            min-height: 150px;
            resize: vertical;
        }

        footer {
            text-align: center;
            padding: 2rem 0;
            color: var(--text-secondary);
            border-top: 1px solid #30363d;
        }

        @media (max-width: 768px) {
            .hero {
                flex-direction: column-reverse;
                text-align: center;
            }
            .hero h1 {
                font-size: 2.5rem;
            }
            .hero-image {
                width: 200px;
                height: 200px;
            }
            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <nav>
            <div class="logo">DevPortfolio</div>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>

        <section class="hero" id="about">
            <div class="hero-content animate__animated animate__fadeInLeft">
                <h1>Hi, I'm <span>Dev</span></h1>
                <p>A 30-year-old passionate developer <span class="typed-text"></span></p>
                <a href="#contact" class="btn">Get In Touch</a>
                <div class="social-links">
                    <a href="#" title="GitHub"><i class="fab fa-github"></i></a>
                    <a href="#" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
                    <a href="#" title="Twitter"><i class="fab fa-twitter"></i></a>
                    <a href="mailto:dilwarsaeed1997@gmail.com" title="Email"><i class="fas fa-envelope"></i></a>
                </div>
            </div>
            <img src="/home/dev/Downloads/5936007732563479801.jpg" alt="Dev Profile" class="hero-image animate__animated animate__fadeInRight">
        </section>

        <section id="skills">
            <h2 class="section-title animate__animated animate__fadeInUp">Skills & Technologies</h2>
            <div class="skills">
                <div class="skill-tag" style="animation-delay: 0.1s">JavaScript</div>
                <div class="skill-tag" style="animation-delay: 0.2s">Python</div>
                <div class="skill-tag" style="animation-delay: 0.3s">React</div>
                <div class="skill-tag" style="animation-delay: 0.4s">Node.js</div>
                <div class="skill-tag" style="animation-delay: 0.5s">HTML/CSS</div>
                <div class="skill-tag" style="animation-delay: 0.6s">Git</div>
                <div class="skill-tag" style="animation-delay: 0.7s">SQL</div>
                <div class="skill-tag" style="animation-delay: 0.8s">TypeScript</div>
            </div>
        </section>

        <section id="projects">
            <h2 class="section-title animate__animated animate__fadeInUp">Projects</h2>
            <div class="projects-grid">
                <div class="project-card animate__animated animate__fadeInUp" style="animation-delay: 0.1s">
                    <h3>Project One</h3>
                    <p>A brief description of the project. What it does and the technologies used.</p>
                    <a href="#">View Project <i class="fas fa-arrow-right"></i></a>
                </div>
                <div class="project-card animate__animated animate__fadeInUp" style="animation-delay: 0.2s">
                    <h3>Project Two</h3>
                    <p>A brief description of the project. What it does and the technologies used.</p>
                    <a href="#">View Project <i class="fas fa-arrow-right"></i></a>
                </div>
                <div class="project-card animate__animated animate__fadeInUp" style="animation-delay: 0.3s">
                    <h3>Project Three</h3>
                    <p>A brief description of the project. What it does and the technologies used.</p>
                    <a href="#">View Project <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
        </section>

        <section id="contact" class="contact">
            <h2 class="section-title animate__animated animate__fadeInUp">Get In Touch</h2>
            <p>Have a project in mind or want to collaborate? Let's talk!</p>
            <form class="contact-form animate__animated animate__fadeInUp" action="https://formspree.io/f/xaqljjqz" method="POST">
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <textarea name="message" placeholder="Your Message" required></textarea>
                <button type="submit" class="btn">Send Message</button>
            </form>
        </section>

        <footer>
            <p>© 2026 Dev. Built with code and coffee</p>
        </footer>
    </div>

    <script>
        var typed = new Typed('.typed-text', {
            strings: ['building beautiful applications.', 'turning ideas into reality.', 'creating functional solutions.'],
            typeSpeed: 50,
            backSpeed: 50,
            loop: true
        });
    </script>
</body>
</html>
