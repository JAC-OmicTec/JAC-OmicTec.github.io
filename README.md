<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OmicTec Institute</title>
    <meta name="description" content="OmicTec Institute - Building Africa's Next Generation of Bioinformatics, Data Science, and Tech Innovators.">
    <link rel="icon" type="image/png" href="https://i.imgur.com/wh0Nhy3.png">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #0A2342;
            --secondary-color: #FFD700;
            --accent: #03bfae;
            --accent-light: #e0f7fa;
            --text-dark: #222B45;
            --text-light: #fff;
            --bg-light: #F8F9FA;
            --card-bg: #fff;
            --shadow-light: 0 4px 24px rgba(10,35,66,0.07), 0 2px 4px rgba(0,0,0,0.04);
            --border-radius: 1rem;
            --transition-main: .2s cubic-bezier(.4,0,.2,1);
        }
        * { box-sizing: border-box; }
        body {
            margin: 0;
            font-family: 'Inter', Arial, sans-serif;
            background: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
            min-width: 0;
        }
        a { color: inherit; text-decoration: none; }
        /* HEADER */
        header {
            background: var(--primary-color);
            color: var(--text-light);
            box-shadow: var(--shadow-light);
        }
        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }
        .navbar {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 1rem 0;
        }
        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        .logo img {
            height: 48px;
            width: auto;
        }
        @media (max-width: 480px) {
            .logo img {
                height: 36px;
                max-width: 130px;
            }
        }
        .navlinks {
            display: flex;
            gap: 2rem;
            align-items: center;
        }
        .navlinks a {
            color: var(--text-light);
            font-weight: 600;
            font-size: 1rem;
            padding: .5rem .8rem;
            border-radius: .5rem;
            transition: background .2s;
        }
        .navlinks a:hover, .navlinks a.active {
            background: var(--accent);
            color: #fff;
        }
        .header-cta {
            background: var(--secondary-color);
            color: var(--primary-color);
            border-radius: .5rem;
            padding: .7rem 1.6rem;
            font-weight: 700;
            margin-left: 2rem;
            transition: background .2s;
        }
        .header-cta:hover {
            background: #ffd700cc;
        }
        /* HERO */
        .hero {
            background: linear-gradient(120deg, var(--primary-color) 65%, var(--accent) 100%);
            color: var(--text-light);
            padding: 4.5rem 0 3rem 0;
            text-align: center;
            position: relative;
        }
        .hero .container {
            position: relative;
            z-index: 1;
        }
        .hero h1 {
            font-size: 2.5rem;
            font-weight: 800;
            margin-bottom: 1rem;
            letter-spacing: -1px;
        }
        .hero p {
            font-size: 1.25rem;
            max-width: 600px;
            margin: 0 auto 2.2rem auto;
        }
        .hero .cta-btn {
            background: var(--secondary-color);
            color: var(--primary-color);
            padding: 1rem 2.3rem;
            font-size: 1.13rem;
            border-radius: .7rem;
            font-weight: 700;
            border: none;
            cursor: pointer;
            transition: box-shadow .2s, background .2s;
            box-shadow: 0 2px 12px 0 rgba(10,35,66,0.09);
        }
        .hero .cta-btn:hover { background: #e6c200; }
        .hero-logo {
            margin: 2.5rem auto 0 auto;
            display: flex;
            justify-content: center;
        }
        .hero-logo img {
            max-width: 220px;
            width: 100%;
            height: auto;
        }
        /* SECTION HEADINGS */
        section h2 {
            font-size: 2rem;
            font-weight: 800;
            color: var(--primary-color);
            margin-bottom: 1.2rem;
            text-align: center;
        }
        /* PROGRAMS */
        .programs {
            background: #fff;
            padding: 3.5rem 0 2.5rem 0;
        }
        .cards {
            display: flex;
            flex-wrap: wrap;
            gap: 1.7rem;
            justify-content: center;
            margin: 0;
            padding: 0;
        }
        .card {
            flex: 1 1 270px;
            max-width: 340px;
            background: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-light);
            padding: 2rem 1.3rem 1.5rem 1.3rem;
            display: flex;
            flex-direction: column;
            transition: box-shadow .2s, transform .2s;
            min-width: 240px;
            min-height: 320px;
        }
        .card:hover {
            box-shadow: 0 8px 28px rgba(10,35,66,0.17);
            transform: translateY(-7px) scale(1.02);
        }
        .card h3 {
            margin: .2rem 0 .7rem 0;
            font-size: 1.23rem;
            color: var(--primary-color);
            font-weight: 700;
        }
        .card p { font-size: 0.98rem; }
        .card .program-info {
            margin: 1.5rem 0 0 0;
            font-size: 0.95rem;
            color: #666;
        }
        .card .countdown {
            color: var(--accent);
            font-weight: 700;
            display: block;
            margin-top: .5rem;
        }
        .card .card-btn {
            margin-top: 1.2rem;
            padding: 0.7rem 1.4rem;
            font-weight: 700;
            border-radius: .4rem;
            background: var(--secondary-color);
            color: var(--primary-color);
            border: none;
            cursor: pointer;
            transition: background .2s;
            font-size: 1rem;
        }
        .card .card-btn[disabled], .card .btn-secondary {
            background: #e6e6e6;
            color: #888;
            cursor: not-allowed;
            pointer-events: none;
        }
        /* ABOUT */
        .about {
            padding: 3.5rem 0 2.5rem 0;
            background: var(--bg-light);
        }
        .about-content {
            max-width: 800px;
            margin: 0 auto;
            font-size: 1.08rem;
            color: #333;
            text-align: center;
        }
        /* FAQ */
        .faq-section {
            background: #fff;
            padding: 3.5rem 0 2.5rem 0;
        }
        .faq-list {
            max-width: 720px;
            margin: 2rem auto 0 auto;
        }
        .faq-item {
            border-bottom: 1px solid #eee;
            padding: 1rem 0;
        }
        .faq-question {
            cursor: pointer;
            font-weight: 700;
            color: var(--primary-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 1.04rem;
        }
        .faq-toggle { font-size: 1.25rem; margin-left: 1rem; }
        .faq-question.opened { color: var(--accent); }
        .faq-answer {
            display: none;
            color: #333;
            font-weight: 400;
            font-size: 0.97rem;
            padding: .7rem 0 0 0;
            max-width: 90%;
        }
        .faq-question.opened + .faq-answer {
            display: block;
        }
        /* CONTACT */
        .contact-section {
            padding: 3.5rem 0 2.5rem 0;
            background: var(--bg-light);
        }
        .contact-grid {
            max-width: 800px;
            margin: 0 auto;
            display: flex;
            gap: 3rem;
            flex-wrap: wrap;
            justify-content: center;
        }
        .contact-form-container {
            flex: 1 1 320px;
            min-width: 260px;
        }
        .contact-info-container {
            flex: 1 1 280px;
            min-width: 220px;
        }
        .contact-form-container form {
            background: #fff;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-light);
            padding: 1.4rem 1rem 1.1rem 1rem;
        }
        .form-group { margin-bottom: 1rem; }
        .contact-form-container label {
            font-size: .97rem;
            font-weight: 600;
            margin-bottom: .3rem;
            display: block;
        }
        .contact-form-container input,
        .contact-form-container textarea {
            width: 100%;
            padding: .7rem .9rem;
            border: 1px solid #bbb;
            border-radius: .4rem;
            font-family: inherit;
            font-size: 1rem;
            margin-bottom: .3rem;
            background: var(--bg-light);
        }
        .contact-form-container textarea { min-height: 85px; }
        .contact-form-container button {
            background: var(--secondary-color);
            color: var(--primary-color);
            padding: .8rem 1.6rem;
            font-weight: 700;
            border-radius: .4rem;
            border: none;
            cursor: pointer;
            transition: background .2s;
        }
        .contact-form-container button:hover { background: #e6c200; }
        .info-item { margin-bottom: 1.2rem; }
        .info-item strong { display: inline-block; min-width: 64px; }
        /* FOOTER */
        footer {
            background: var(--primary-color);
            color: var(--text-light);
            text-align: center;
            padding: 2.2rem 0 1.4rem 0;
        }
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }
        .social-icons { margin-top: 1.1rem; }
        .social-icons a {
            margin: 0 10px;
            display: inline-block;
        }
        .social-icons img {
            width: 28px;
            height: 28px;
            filter: invert(100%);
            transition: transform .2s;
        }
        .social-icons img:hover { transform: scale(1.1);}
        /* CHATBOT */
        .chatbot-toggle-btn {
            position: fixed;
            bottom: 22px;
            right: 22px;
            z-index: 1100;
            width: 56px;
            height: 56px;
            background-color: var(--accent);
            border-radius: 50%;
            box-shadow: 0 4px 16px rgba(0,0,0,0.16);
            display: flex;
            align-items: center;
            justify-content: center;
            border: none;
            cursor: pointer;
            transition: background .2s;
        }
        .chatbot-toggle-btn:hover { background-color: var(--primary-color);}
        .chatbot-toggle-btn svg {
            width: 30px;
            height: 30px;
            fill: #fff;
        }
        .chatbot-container {
            position: fixed;
            bottom: 88px;
            right: 22px;
            width: 320px;
            max-width: 95vw;
            max-height: 480px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.13);
            background-color: #fff;
            overflow: hidden;
            z-index: 1100;
            display: none;
            flex-direction: column;
        }
        .chatbot-container.active { display: flex; }
        .chat-header {
            background-color: var(--primary-color);
            color: #fff;
            padding: 12px 16px;
            text-align: center;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
            position: relative;
        }
        .chat-header #chatbot-close-btn {
            background: none;
            border: none;
            position: absolute;
            top: 8px;
            right: 14px;
            color: #fff;
            font-size: 1.5em;
            cursor: pointer;
            line-height: 1;
        }
        .chat-box { flex-grow: 1; padding: 10px; overflow-y: auto;}
        .user-message, .bot-message {
            margin: 5px 0;
            padding: 8px 12px;
            border-radius: 15px;
            max-width: 80%;
            word-wrap: break-word;
            font-size: .98rem;
        }
        .user-message { background-color: var(--accent); color: #fff; margin-left: auto; text-align: right;}
        .bot-message { background-color: #f1f1f1; color: #333; margin-right: auto;}
        .chat-input-container { display: flex; padding: 10px; border-top: 1px solid #ccc;}
        #user-input { flex-grow: 1; padding: 8px; border: 1px solid #ccc; border-radius: 5px; margin-right: 5px;}
        #send-btn { padding: 8px 12px; border: none; background-color: var(--accent); color: #fff; border-radius: 5px; cursor: pointer;}
        .loading-dots { display: inline-block; }
        .loading-dots span { display: inline-block; animation: loadingBlink 1s infinite; }
        .loading-dots span:nth-child(2) { animation-delay: 0.2s;}
        .loading-dots span:nth-child(3) { animation-delay: 0.4s;}
        @keyframes loadingBlink { 0%, 80%, 100% { opacity: 0;} 40% { opacity: 1;}}
        /* MEDIA QUERIES */
        @media (max-width: 1024px) {
            .container, .footer-content, .content-container, .faq-list { max-width: 96vw; }
            .navlinks { gap: 1.2rem; }
        }
        @media (max-width: 900px) {
            .cards { flex-direction: column; align-items: center; }
            .contact-grid { flex-direction: column; gap: 2rem; }
        }
        @media (max-width: 768px) {
            .header-container { flex-direction: column; gap: 16px; padding: 12px;}
            .navlinks { flex-direction: column; gap: 12px; align-items: center;}
            .hero-content h1 { font-size: 2.2rem;}
            .hero-content p { font-size: 1rem;}
            .faq-section { padding: 25px 5px;}
            .chatbot-container, .chatbot-toggle-btn { right: 10px; }
            .chatbot-container { width: 95vw; max-width: 380px; min-width: 0; }
        }
        @media (max-width: 480px) {
            .logo img { height: 36px; max-width: 130px; }
            .hero-content h1 { font-size: 1.2rem;}
            .hero { padding: 28px 2vw;}
            .content-section { padding: 25px 2vw;}
            .footer-content { padding: 0 2vw;}
            .faq-section { padding: 14px 1vw;}
            .chatbot-container, .chatbot-toggle-btn { right: 1vw; left: 1vw; }
            .chatbot-container { width: 98vw; max-width: 98vw;}
        }
    </style>
</head>
<body>
    <header>
        <div class="container navbar">
            <a href="#" class="logo">
                <img src="https://i.imgur.com/wh0Nhy3.png" alt="OmicTec Institute Logo">
            </a>
            <nav class="navlinks">
                <a href="#" class="active">Home</a>
                <a href="#about-us-section">About Us</a>
                <a href="#programs-section">Programs</a>
                <a href="#faq-section">FAQs</a>
                <a href="#contact-us-section">Contact</a>
                <a href="https://forms.gle/ZDhnjSiZXgnfVAoG7" class="header-cta">Register</a>
            </nav>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <h1>Build Your Future in Data &amp; Life Sciences at OmicTec Institute</h1>
            <p>
                Future-ready skills in Bioinformatics, Data Science, AI/ML, and Software Development—designed for Africa's next generation of innovators.
            </p>
            <a class="cta-btn" href="https://forms.gle/ZDhnjSiZXgnfVAoG7">Register Now</a>
            <div class="hero-logo">
                <img src="https://i.imgur.com/wh0Nhy3.png" alt="OmicTec Institute Logo">
            </div>
        </div>
    </section>

    <section class="about" id="about-us-section">
        <div class="container">
            <h2>About OmicTec Institute</h2>
            <div class="about-content">
                <p>
                    OmicTec Institute is on a mission to build a new generation of African innovators equipped with 21st-century skills in bioinformatics, artificial intelligence, software development, and data-driven research. As a youth-focused and future-facing educational hub, we bridge the gap between traditional academics and real-world application in health, research, and biotechnology.
                </p>
                <p>
                    Founded under JAC OmicTec Solutions Ltd, we democratize access to high-impact digital and life science skills—nurturing thinkers, researchers, and tech leaders. With hybrid and hands-on programs, our mentorship-driven learning prepares students and professionals for postgraduate research or competitive careers in biomedical tech.
                </p>
            </div>
        </div>
    </section>

    <section class="programs" id="programs-section">
        <div class="container">
            <h2>Our Programs</h2>
            <div class="cards">
                <div class="card" id="bioinformatics-card">
                    <h3>3-Months Bioinformatics Training</h3>
                    <p>
                        Learn Next-Generation Sequencing (NGS), variant calling, RNA-seq, and genome assembly. Hands-on skills for a career in genomics and precision medicine.
                    </p>
                    <div class="program-info">
                        <span><strong>Starts:</strong> September 3, 2025</span>
                        <span class="countdown" id="countdown-timer"></span>
                    </div>
                    <a href="https://forms.gle/ZDhnjSiZXgnfVAoG7" class="card-btn">Enroll Now</a>
                </div>
                <div class="card">
                    <h3>AI/ML for Life Sciences</h3>
                    <p>
                        Machine learning for genomics, drug discovery, and health research. From basics to advanced predictive models. Project-based, mentor-supported.
                    </p>
                    <button class="card-btn btn-secondary" disabled>Coming Soon</button>
                </div>
                <div class="card">
                    <h3>Data Science Bootcamp</h3>
                    <p>
                        Python, data wrangling, visualization, and statistical analysis for biotech and health. Real datasets, industry tools, practical challenges.
                    </p>
                    <button class="card-btn btn-secondary" disabled>Coming Soon</button>
                </div>
                <div class="card">
                    <h3>Software Development Immersive</h3>
                    <p>
                        Become a proficient developer: coding fundamentals, web apps, databases, teamwork, and real-world project experience.
                    </p>
                    <button class="card-btn btn-secondary" disabled>Coming Soon</button>
                </div>
                <div class="card">
                    <h3>Python Programming Essentials</h3>
                    <p>
                        Learn Python from scratch—data structures, scripting, and automation. Ideal for research and industry newcomers.
                    </p>
                    <button class="card-btn btn-secondary" disabled>Coming Soon</button>
                </div>
            </div>
        </div>
    </section>

    <section class="faq-section" id="faq-section">
        <div class="container">
            <h2>Frequently Asked Questions (FAQs)</h2>
            <div class="faq-list">
                <div class="faq-item">
                    <div class="faq-question">
                        <span>What is OmicTec Institute?</span>
                        <span class="faq-toggle">&#9654;</span>
                    </div>
                    <div class="faq-answer">
                        OmicTec Institute is an educational and research hub focused on training African youth in bioinformatics, AI/ML, software development, and data sciences for the 21st century.
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Who can participate in your programs?</span>
                        <span class="faq-toggle">&#9654;</span>
                    </div>
                    <div class="faq-answer">
                        Our programs are open to students, graduates, professionals, and anyone interested in building a career or research capacity in digital and life sciences.
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>How do I register for a program?</span>
                        <span class="faq-toggle">&#9654;</span>
                    </div>
                    <div class="faq-answer">
                        Click the "Register" button at the top or "Enroll Now" under available programs to access the registration form.
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Do you offer online or in-person classes?</span>
                        <span class="faq-toggle">&#9654;</span>
                    </div>
                    <div class="faq-answer">
                        We offer hybrid programs that combine online learning with practical, in-person sessions and mentorship.
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Are there scholarships or financial aid?</span>
                        <span class="faq-toggle">&#9654;</span>
                    </div>
                    <div class="faq-answer">
                        Yes, OmicTec Institute occasionally offers scholarships and financial aid for outstanding or disadvantaged candidates. Details will be announced on our website and social media.
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>How can I contact OmicTec Institute?</span>
                        <span class="faq-toggle">&#9654;</span>
                    </div>
                    <div class="faq-answer">
                        You can email us at jacomictecsolutions@gmail.com, call (+234) 912-487 5618, or visit 2 Akin Osiyemi Street, Allen Avenue, Lagos, Nigeria.
                    </div>
                </div>
                <div class="faq-item">
                    <div class="faq-question">
                        <span>Do you provide certificates after completion?</span>
                        <span class="faq-toggle">&#9654;</span>
                    </div>
                    <div class="faq-answer">
                        Yes, participants who successfully complete their programs and meet the requirements receive certificates of completion from OmicTec Institute.
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="contact-section" id="contact-us-section">
        <div class="container">
            <h2>Contact Us</h2>
            <div class="contact-grid">
                <div class="contact-form-container">
                    <form action="#" method="post" id="contact-form" autocomplete="off" novalidate>
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" name="name" required>
                            <small class="error-message" style="color: red; display: none;">Please enter your name.</small>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" name="email" required>
                            <small class="error-message" style="color: red; display: none;">Please enter a valid email.</small>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" name="subject" required>
                            <small class="error-message" style="color: red; display: none;">Please enter a subject.</small>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" name="message" rows="5" required></textarea>
                            <small class="error-message" style="color: red; display: none;">Please enter a message.</small>
                        </div>
                        <button type="submit" class="btn btn-primary">Send Message</button>
                        <div id="form-status" style="margin-top:10px;"></div>
                    </form>
                </div>
                <div class="contact-info-container">
                    <div class="info-item">
                        <strong>Email:</strong> <a href="mailto:jacomictecsolutions@gmail.com">jacomictecsolutions@gmail.com</a>
                    </div>
                    <div class="info-item">
                        <strong>Phone:</strong> <a href="tel:+2349124875618">(+234) 912-487 5618</a>
                    </div>
                    <div class="info-item">
                        <strong>Address:</strong><br>
                        2 Akin Osiyemi Street, Allen Avenue, Lagos, Nigeria.
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-content">
            <p>&copy; 2025 OmicTec Institute | Powered by JAC OmicTec Solutions Ltd</p>
            <div class="social-icons">
                <a href="https://twitter.com/OmicTec_Inst" target="_blank">
                    <img src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/twitter.svg" alt="Twitter">
                </a>
                <a href="https://linkedin.com/company/OmiTec-Institute" target="_blank">
                    <img src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/linkedin.svg" alt="LinkedIn">
                </a>
                <a href="mailto:jacomictecsolutions@gmail.com">
                    <img src="https://cdn.jsdelivr.net/npm/simple-icons@v5/icons/gmail.svg" alt="Email">
                </a>
            </div>
        </div>
    </footer>

    <!-- Chatbot Floating Button -->
    <button class="chatbot-toggle-btn" id="chatbot-toggle-btn" title="Chat with us!">
        <svg viewBox="0 0 24 24">
            <path d="M12 2C6.48 2 2 5.92 2 10.2c0 2.1 1.17 3.99 3.1 5.34-.14.54-.5 1.79-.56 2.04-.16.64.24.63.5.46.21-.14 1.6-1.07 2.26-1.49.88.17 1.8.27 2.7.27 5.52 0 10-3.92 10-8.2S17.52 2 12 2zm-3.5 7.5c.83 0 1.5.67 1.5 1.5S9.33 12.5 8.5 12.5 7 11.83 7 11s.67-1.5 1.5-1.5zm7 0c.83 0 1.5.67 1.5 1.5s-.67 1.5-1.5 1.5-1.5-.67-1.5-1.5.67-1.5 1.5-1.5zm-7.42 5.16c-.13.1-1.26.81-1.44.92.1-.41.27-1.01.32-1.21.05-.19-.03-.39-.19-.5C4.44 13.06 4 11.68 4 10.2 4 6.58 7.92 4 12 4s8 2.58 8 6.2-3.92 6.2-8 6.2c-.9 0-1.79-.09-2.66-.27-.16-.03-.32-.01-.44.08z"/>
        </svg>
    </button>
    <div class="chatbot-container" id="chatbot-container">
        <div class="chat-header">
            <h2>OmicTec Bot</h2>
            <button id="chatbot-close-btn" title="Close">&times;</button>
        </div>
        <div class="chat-box" id="chat-box">
            <div class="bot-message">Hello! How can I help you today?</div>
        </div>
        <div class="chat-input-container">
            <input type="text" id="user-input" placeholder="Type a message...">
            <button id="send-btn">Send</button>
        </div>
    </div>
    <script>
        // --- Chatbot Toggle Logic ---
        document.addEventListener('DOMContentLoaded', function() {
            const chatbotToggleBtn = document.getElementById('chatbot-toggle-btn');
            const chatbotContainer = document.getElementById('chatbot-container');
            const chatbotCloseBtn = document.getElementById('chatbot-close-btn');
            chatbotToggleBtn.addEventListener('click', function() {
                chatbotContainer.classList.toggle('active');
            });
            chatbotCloseBtn.addEventListener('click', function() {
                chatbotContainer.classList.remove('active');
            });
            document.addEventListener('keydown', function(e) {
                if (e.key === "Escape") chatbotContainer.classList.remove('active');
            });
        });

        // --------- COUNTDOWN ---------
        document.addEventListener('DOMContentLoaded', function() {
            const countDownDate = new Date("Sep 3, 2025 00:00:00").getTime();
            const countdownElement = document.getElementById("countdown-timer");
            const x = setInterval(function() {
                const now = new Date().getTime();
                const distance = countDownDate - now;
                const days = Math.floor(distance / (1000 * 60 * 60 * 24));
                const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((distance % (1000 * 60)) / 1000);
                countdownElement.innerHTML = days + "d " + hours + "h " + minutes + "m " + seconds + "s ";
                if (distance < 0) {
                    clearInterval(x);
                    countdownElement.innerHTML = "Program has started!";
                }
            }, 1000);
        });

        // --------- FAQ collapse/expand logic with animation ---------
        document.addEventListener('DOMContentLoaded', function() {
            document.querySelectorAll('.faq-question').forEach(function(q) {
                q.addEventListener('click', function() {
                    document.querySelectorAll('.faq-question.opened').forEach(openQ => {
                        if (openQ !== q) {
                            openQ.classList.remove('opened');
                            const ans = openQ.parentElement.querySelector('.faq-answer');
                            ans.style.display = 'none';
                            setTimeout(() => ans.style.maxHeight = '0', 10);
                        }
                    });
                    const answer = q.parentElement.querySelector('.faq-answer');
                    if (q.classList.contains('opened')) {
                        q.classList.remove('opened');
                        answer.style.opacity = 0;
                        setTimeout(() => {
                            answer.style.display = 'none';
                            answer.style.maxHeight = '0';
                        }, 400);
                    } else {
                        q.classList.add('opened');
                        answer.style.display = 'block';
                        setTimeout(() => {
                            answer.style.maxHeight = answer.scrollHeight + 'px';
                            answer.style.opacity = 1;
                        }, 10);
                    }
                });
            });
        });

        // --------- CHATBOT (OpenAI Integration, fallback to local bot) ---------
        document.addEventListener('DOMContentLoaded', function() {
            const chatBox = document.getElementById('chat-box');
            const userInput = document.getElementById('user-input');
            const sendBtn = document.getElementById('send-btn');
            sendBtn.addEventListener('click', sendMessage);
            userInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter') sendMessage();
            });
            function appendMessage(text, sender) {
                const div = document.createElement('div');
                div.classList.add(sender === 'user' ? 'user-message' : 'bot-message');
                div.textContent = text;
                chatBox.appendChild(div);
                chatBox.scrollTop = chatBox.scrollHeight;
            }
            function appendLoadingDots() {
                const div = document.createElement('div');
                div.className = "bot-message loading-dots";
                div.id = "loading-dots-id";
                div.innerHTML = "<span>.</span><span>.</span><span>.</span>";
                chatBox.appendChild(div);
                chatBox.scrollTop = chatBox.scrollHeight;
            }
            function removeLoadingDots() {
                const dots = document.getElementById("loading-dots-id");
                if (dots) dots.remove();
            }
            async function sendMessage() {
                const userText = userInput.value.trim();
                if (userText === '') return;
                appendMessage(userText, 'user');
                userInput.value = '';
                chatBox.scrollTop = chatBox.scrollHeight;
                appendLoadingDots();
                const OPENAI_API_KEY = "YOUR_OPENAI_API_KEY"; // <-- Replace with your key
                let responseText = "";
                if(OPENAI_API_KEY === "YOUR_OPENAI_API_KEY") {
                    removeLoadingDots();
                    responseText = getLocalBotResponse(userText);
                    appendMessage(responseText, 'bot');
                    return;
                }
                try {
                    const apiResponse = await fetch("https://api.openai.com/v1/chat/completions", {
                        method: "POST",
                        headers: {
                            "Content-Type": "application/json",
                            "Authorization": "Bearer " + OPENAI_API_KEY
                        },
                        body: JSON.stringify({
                            model: "gpt-3.5-turbo",
                            messages: [
                                {role: "system", content: "You are OmicTec Bot, a helpful assistant for OmicTec Institute's website visitors."},
                                {role: "user", content: userText}
                            ]
                        })
                    });
                    const data = await apiResponse.json();
                    removeLoadingDots();
                    if(data.choices && data.choices[0] && data.choices[0].message && data.choices[0].message.content) {
                        responseText = data.choices[0].message.content.trim();
                    } else if(data.error && data.error.message) {
                        responseText = "Sorry, there was a problem: " + data.error.message;
                    } else {
                        responseText = "Sorry, I couldn't understand your request.";
                    }
                } catch(e) {
                    removeLoadingDots();
                    responseText = "Sorry, I couldn't connect to the server. Please try again later.";
                }
                appendMessage(responseText, 'bot');
            }
            function getLocalBotResponse(input) {
                const lowerInput = input.toLowerCase();
                if (lowerInput.includes('hello') || lowerInput.includes('hi')) {
                    return "Hello! How can I assist you today?";
                } else if (lowerInput.includes('bye') || lowerInput.includes('goodbye')) {
                    return "Goodbye! Have a great day!";
                } else if (lowerInput.includes('thank you') || lowerInput.includes('thanks')) {
                    return "You're welcome! Feel free to ask if you have any more questions.";
                } else if (lowerInput.includes('about')) {
                    return "The OmicTec Institute is a leading research and educational center focusing on technology and applied sciences.";
                } else if (lowerInput.includes('mission')) {
                    return "Our mission is to innovate and educate in the fields of omics technologies, bioinformatics, and data science.";
                } else if (lowerInput.includes('history')) {
                    return "Founded in 20XX, the OmicTec Institute has been at the forefront of scientific discovery and technological innovation.";
                } else if (lowerInput.includes('contact')) {
                    return "You can reach us via email at jacomictecsolutions@gmail.com or call us at (+234) 912-487 5618. Our office hours are Monday to Friday, 9:00 AM - 5:00 PM.";
                } else if (lowerInput.includes('email')) {
                    return "Our email address is jacomictecsolutions@gmail.com.";
                } else if (lowerInput.includes('phone')) {
                    return "You can call us at (+234) 912-487 5618 during our business hours.";
                } else if (lowerInput.includes('address')) {
                    return "Our main office is located at 2 Akin Osiyemi Street, Allen Avenue, Lagos, Nigeria.";
                } else if (lowerInput.includes('programs') || lowerInput.includes('courses')) {
                    return "We offer various programs in bioinformatics, data analysis, software development, and more. Visit our Programs page for more details.";
                } else if (lowerInput.includes('software development')) {
                    return "The Software Development Immersive is a project-based program teaching modern programming, web development, and best practices for real-world applications. Coming soon!";
                } else if (lowerInput.includes('python')) {
                    return "Our Python Programming Essentials course covers Python basics, scripting, and automation for research and industry. Stay tuned!";
                } else if (lowerInput.includes('research')) {
                    return "We conduct cutting-edge research in genomics, proteomics, and computational biology. Check out our Research page to see our latest projects.";
                } else if (lowerInput.includes('bioinformatics')) {
                    return "The 3-months Bioinformatics training program starts on September 3, 2025. You can enroll now via the 'Register Now' button at the top of the page."
                } else {
                    return "I'm sorry, I'm not trained to answer that. Please contact us directly for more specific inquiries.";
                }
            }
        });

        // --------- CONTACT FORM VALIDATION ---------
        document.addEventListener('DOMContentLoaded', function() {
            const form = document.getElementById("contact-form");
            const status = document.getElementById("form-status");
            if(!form) return;
            form.addEventListener("submit", function(e){
                e.preventDefault();
                let valid = true;
                status.textContent = "";
                Array.from(form.querySelectorAll(".form-group")).forEach(group => {
                    const input = group.querySelector("input, textarea");
                    const error = group.querySelector(".error-message");
                    error.style.display = "none";
                    if(input.hasAttribute("required") && !input.value.trim()) {
                        error.style.display = "block";
                        valid = false;
                    }
                    if(input.type === "email" && input.value) {
                        const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                        if(!re.test(input.value)) {
                            error.textContent = "Please enter a valid email.";
                            error.style.display = "block";
                            valid = false;
                        }
                    }
                });
                if(!valid) return;
                status.style.color = "#007BFF";
                status.textContent = "Sending...";
                setTimeout(function(){
                    status.style.color = "green";
                    status.textContent = "Thank you! Your message has been sent.";
                    form.reset();
                }, 1500);
            });
        });
    </script>
</body>
</html>
