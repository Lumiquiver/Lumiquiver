    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* ------------------- */
        /* --- GLOBAL STYLES --- */
        /* ------------------- */
        :root {
            --primary-color: #ff4d00;
            --background-color: #000000;
            --text-color: #ffffff;
            --secondary-text-color: #a0a0a0;
            --card-color: #1a1a1a;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            max-width: 1100px;
            margin: auto;
            padding: 0 2rem;
            overflow: hidden;
        }

        h1, h2, h3 {
            color: var(--text-color);
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            text-align: center;
            color: var(--primary-color);
        }

        p {
            color: var(--secondary-text-color);
            font-size: 1rem;
            margin-bottom: 1rem;
        }

        .btn {
            display: inline-block;
            padding: 12px 28px;
            background-color: var(--primary-color);
            color: var(--text-color);
            text-decoration: none;
            border-radius: 5px;
            font-weight: 500;
            transition: transform 0.3s ease;
        }

        .btn:hover {
            transform: scale(1.05);
        }

        section {
            padding: 6rem 0;
        }

        /* ------------------- */
        /* --- HEADER & NAV --- */
        /* ------------------- */
        #main-header {
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            background-color: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
        }

        #navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        #navbar .logo {
            font-size: 1.5rem;
            font-weight: 600;
        }

        #navbar .logo span {
            color: var(--primary-color);
        }

        #navbar ul {
            display: flex;
            list-style: none;
        }

        #navbar ul li {
            margin-left: 1.5rem;
        }

        #navbar ul li a {
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        #navbar ul li a:hover, #navbar ul li a.active {
            color: var(--primary-color);
        }
        
        /* ------------------- */
        /* --- HERO SECTION --- */
        /* ------------------- */
        #hero {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            padding-top: 80px; /* Offset for fixed header */
        }
        
        .hero-content {
            flex: 1;
        }

        .hero-content .subtitle {
            font-size: 1.2rem;
            color: var(--primary-color);
        }

        .hero-content h1 {
            font-size: 4rem;
            line-height: 1.2;
            margin: 0.5rem 0 1.5rem;
        }
        
        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .image-glow-container {
            position: relative;
            width: 300px;
            height: 300px;
        }

        .image-glow-container::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, var(--primary-color) 20%, transparent 70%);
            filter: blur(50px);
            transform: translate(-50%, -50%);
            z-index: -1;
            opacity: 0.6;
        }

        .image-glow-container img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
        }

        /* ------------------- */
        /* --- ABOUT SECTION --- */
        /* ------------------- */
        #about .container {
            display: flex;
            align-items: center;
            gap: 4rem;
        }
        
        .about-image, .about-content {
            flex: 1;
        }
        
        .about-image .image-glow-container{
             width: 250px;
             height: 250px;
             margin: 0 auto;
        }

        .about-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        /* ------------------- */
        /* --- SKILLS SECTION --- */
        /* ------------------- */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 3rem;
            align-items: center;
        }
        
        .skills-info .highlight {
            font-size: 4rem;
            color: var(--primary-color);
            font-weight: 700;
        }

        .skill-item {
            margin-bottom: 1.5rem;
        }
        
        .skill-item .skill-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
        }

        .progress-bar {
            width: 100%;
            height: 8px;
            background-color: var(--card-color);
            border-radius: 5px;
        }

        .progress {
            height: 100%;
            background-color: var(--primary-color);
            border-radius: 5px;
        }
        
        /* ------------------- */
        /* -- SERVICES SECTION - */
        /* ------------------- */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            text-align: center;
        }
        
        .service-card {
            background-color: var(--card-color);
            padding: 2.5rem 1.5rem;
            border-radius: 10px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(255, 77, 0, 0.2);
        }

        .service-card h3 {
            font-size: 1.2rem;
            color: var(--primary-color);
            margin-top: 1rem;
        }

        /* ------------------- */
        /* -- CONTACT SECTION -- */
        /* ------------------- */
        #contact {
            text-align: center;
        }

        #contact h3 {
            font-size: 1.5rem;
            color: var(--secondary-text-color);
        }

        #contact .btn {
            margin-top: 1.5rem;
            padding: 15px 40px;
            font-size: 1.2rem;
        }

        /* ------------------- */
        /* ------ FOOTER ------ */
        /* ------------------- */
        #main-footer {
            text-align: center;
            padding: 2rem 0;
            background-color: var(--card-color);
            color: var(--secondary-text-color);
            font-size: 0.9rem;
        }
        
        /* ------------------- */
        /* -- RESPONSIVENESS -- */
        /* ------------------- */
        @media(max-width: 768px) {
            #navbar {
                flex-direction: column;
            }
            #navbar ul {
                padding: 1rem 0;
            }
            #hero, #about .container {
                flex-direction: column;
                text-align: center;
                height: auto;
            }
            .hero-image {
                margin-top: 3rem;
            }
            .skills-grid, .services-grid {
                grid-template-columns: 1fr;
            }
            h1 { font-size: 3rem; }
            h2 { font-size: 2rem; }
        }

    </style>
</head>
<body>

    <header id="main-header">
        <nav id="navbar" class="container">
            <a href="#" class="logo">Portfolio<span>.</span></a>
            <ul>
                <li><a href="#hero" class="active">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero">
        <div class="container">
            <div class="hero-content">
                <p class="subtitle">Hello,</p>
                <h1>I'm LUMIQUIVER</h1>
                <p>UI/UX Designer</p>
                <a href="#contact" class="btn">Hire Me</a>
            </div>
            <div class="hero-image">
                <div class="image-glow-container">
                    <img src="https://i.imgur.com/mJzJq3D.png" alt="LUMIQUIVER Profile">
                </div>
            </div>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <div class="about-image">
                <div class="image-glow-container">
                     <img src="https://i.imgur.com/mJzJq3D.png" alt="LUMIQUIVER Profile">
                </div>
            </div>
            <div class="about-content">
                <h2>About Me</h2>
                <h3>Developing With a Passion</h3>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
                <a href="#" class="btn">Download CV</a>
            </div>
        </div>
    </section>
    
    <section id="skills">
        <div class="container">
            <h2>My Skills</h2>
            <div class="skills-grid">
                <div class="skills-info">
                    <h3>Skills Reflects Our Knowledge</h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>
                    <p><span class="highlight">10+</span> Years of Experience</p>
                </div>
                <div class="skills-list">
                    <div class="skill-item">
                        <div class="skill-header">
                            <p>UI/UX Design</p>
                            <p>90%</p>
                        </div>
                        <div class="progress-bar">
                            <div class="progress" style="width: 90%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-header">
                            <p>Web Development</p>
                            <p>80%</p>
                        </div>
                        <div class="progress-bar">
                            <div class="progress" style="width: 80%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-header">
                            <p>Branding</p>
                            <p>70%</p>
                        </div>
                        <div class="progress-bar">
                            <div class="progress" style="width: 70%;"></div>
                        </div>
                    </div>
                     <div class="skill-item">
                        <div class="skill-header">
                            <p>Photography</p>
                            <p>60%</p>
                        </div>
                        <div class="progress-bar">
                            <div class="progress" style="width: 60%;"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="services">
        <div class="container">
            <h2>My Services</h2>
            <div class="services-grid">
                <div class="service-card">
                    <h3>Web Development</h3>
                </div>
                <div class="service-card">
                    <h3>Graphic Design</h3>
                </div>
                <div class="service-card">
                    <h3>Digital Marketing</h3>
                </div>
                <div class="service-card">
                    <h3>Icon Design</h3>
                </div>
                <div class="service-card">
                    <h3>Photography</h3>
                </div>
                <div class="service-card">
                    <h3>Apps Development</h3>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2>Contact Me</h2>
            <h3>Have Any Project?</h3>
            <a href="mailto:email@example.com" class="btn">Let's Chat</a>
        </div>
    </section>

    <footer id="main-footer">
        <p>Created by LUMIQUIVER | © 2025 All Rights Reserved.</p>
    </footer>
