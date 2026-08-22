
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Personal portfolio of Gelou Menchavez">
    <title>Gelou Menchavez | IT Student</title>

    <style>
        /* =========================
           CSS VARIABLES
        ========================== */
        :root {
            --bg: #060b16;
            --bg-light: #0d1628;
            --card: #101b2d;
            --blue: #2563eb;
            --light-blue: #38bdf8;
            --white: #f8fafc;
            --gray: #94a3b8;
            --border: rgba(148, 163, 184, 0.15);
            --gradient: linear-gradient(135deg, #2563eb, #38bdf8);
        }

        /* =========================
           RESET
        ========================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: var(--bg);
            color: var(--white);
            line-height: 1.7;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        ul {
            list-style: none;
        }

        .container {
            width: 90%;
            max-width: 1150px;
            margin: auto;
        }

        section {
            padding: 100px 0;
        }

        /* =========================
           NAVIGATION
        ========================== */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(6, 11, 22, 0.9);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border);
        }

        nav {
            height: 75px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.7rem;
            font-weight: bold;
        }

        .logo span {
            color: var(--light-blue);
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            color: #cbd5e1;
            font-size: 0.9rem;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: var(--light-blue);
        }

        /* =========================
           HERO
        ========================== */
        #home {
            min-height: 100vh;
            display: flex;
            align-items: center;
            background:
                radial-gradient(
                    circle at 80% 30%,
                    rgba(37, 99, 235, 0.2),
                    transparent 35%
                );
        }

        .hero {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            align-items: center;
            gap: 60px;
        }

        .tag {
            color: var(--light-blue);
            font-size: 0.8rem;
            font-weight: bold;
            letter-spacing: 3px;
            margin-bottom: 15px;
        }

        .hero h1 {
            font-size: clamp(3rem, 7vw, 5rem);
            line-height: 1.05;
            margin-bottom: 15px;
        }

        .hero h1 span {
            display: block;
            background: var(--gradient);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero h2 {
            color: #cbd5e1;
            font-weight: normal;
            margin-bottom: 20px;
        }

        .hero p {
            color: var(--gray);
            max-width: 600px;
            margin-bottom: 30px;
        }

        .buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 13px 24px;
            border-radius: 8px;
            font-weight: bold;
            transition: 0.3s;
        }

        .btn-primary {
            background: var(--gradient);
            color: white;
        }

        .btn-outline {
            border: 1px solid var(--border);
            color: white;
        }

        .btn:hover {
            transform: translateY(-4px);
        }

        .btn-primary:hover {
            box-shadow: 0 15px 35px rgba(37, 99, 235, 0.3);
        }

        .btn-outline:hover {
            border-color: var(--light-blue);
            color: var(--light-blue);
        }

        /* =========================
           PROFILE PLACEHOLDER
        ========================== */
        .profile-area {
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        .profile {
            width: 300px;
            height: 370px;
            border-radius: 150px 150px 25px 25px;
            background: var(--gradient);
            padding: 8px;
            animation: float 4s ease-in-out infinite;
        }

        .profile-inner {
            width: 100%;
            height: 100%;
            background: #101a2c;
            border-radius: 145px 145px 20px 20px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .profile-circle {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: var(--gradient);
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .profile-inner p {
            color: var(--gray);
        }

        /* =========================
           SECTION TITLES
        ========================== */
        .section-title {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 60px;
        }

        .section-title small {
            color: var(--light-blue);
            letter-spacing: 3px;
            font-weight: bold;
        }

        .section-title h2 {
            font-size: 2.8rem;
            margin: 10px 0;
        }

        .section-title h2 span {
            color: var(--light-blue);
        }

        .section-title p {
            color: var(--gray);
        }

        /* =========================
           ABOUT
        ========================== */
        #about {
            background: var(--bg-light);
        }

        .about {
            display: grid;
            grid-template-columns: 0.8fr 1.2fr;
            gap: 70px;
            align-items: center;
        }

        .about-box {
            height: 300px;
            border-radius: 25px;
            background: linear-gradient(
                145deg,
                rgba(37, 99, 235, 0.2),
                var(--card)
            );
            border: 1px solid var(--border);
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .about-box strong {
            font-size: 6rem;
            color: var(--light-blue);
        }

        .about-box span {
            color: var(--gray);
        }

        .about-content h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
        }

        .about-content p {
            color: var(--gray);
            margin-bottom: 15px;
        }

        .details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 25px;
        }

        .detail {
            padding: 15px;
            background: rgba(255,255,255,0.03);
            border: 1px solid var(--border);
            border-radius: 10px;
        }

        .detail small {
            color: var(--gray);
            display: block;
        }

        /* =========================
           SKILLS
        ========================== */
        .skills {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .skill-card {
            padding: 30px;
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 15px;
            transition: 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-8px);
            border-color: var(--light-blue);
            box-shadow: 0 15px 40px rgba(0,0,0,0.25);
        }

        .skill-icon {
            width: 55px;
            height: 55px;
            border-radius: 12px;
            background: rgba(37,99,235,0.15);
            color: var(--light-blue);
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .skill-card p {
            color: var(--gray);
            font-size: 0.9rem;
            margin-top: 10px;
        }

        /* =========================
           PROJECTS
        ========================== */
        #projects {
            background: var(--bg-light);
        }

        .projects {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project {
            background: var(--card);
            border: 1px solid var(--border);
            border-radius: 15px;
            overflow: hidden;
            transition: 0.3s;
        }

        .project:hover {
            transform: translateY(-10px);
            border-color: var(--light-blue);
        }

        .project-image {
            height: 190px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 3rem;
            background: var(--gradient);
        }

        .project-content {
            padding: 25px;
        }

        .project-content h3 {
            margin-bottom: 10px;
        }

        .project-content p {
            color: var(--gray);
            font-size: 0.9rem;
        }

        .tags {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .tags span {
            background: rgba(56,189,248,0.08);
            color: var(--light-blue);
            padding: 5px 9px;
            border-radius: 5px;
            font-size: 0.7rem;
        }

        /* =========================
           EDUCATION
        ========================== */
        .education {
            max-width: 800px;
            margin: auto;
        }

        .education-card {
            padding: 35px;
            border-radius: 18px;
            background: var(--card);
            border: 1px solid var(--border);
            display: flex;
            gap: 25px;
            transition: 0.3s;
        }

        .education-card:hover {
            transform: translateX(8px);
            border-color: var(--light-blue);
        }

        .education-icon {
            width: 65px;
            height: 65px;
            min-width: 65px;
            border-radius: 50%;
            background: var(--gradient);
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
        }

        .education-card h3 {
            font-size: 1.5rem;
        }

        .education-card h4 {
            color: var(--light-blue);
            font-weight: normal;
            margin: 5px 0 15px;
        }

        .education-card p {
            color: var(--gray);
        }

        /* =========================
           CONTACT
        ========================== */
        #contact {
            background: var(--bg-light);
        }

        .contact {
            display: grid;
            grid-template-columns: 0.8fr 1.2fr;
            gap: 60px;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 15px;
        }

        .contact-info > p {
            color: var(--gray);
            margin-bottom: 30px;
        }

        .contact-item {
            margin-bottom: 20px;
        }

        .contact-item small {
            color: var(--gray);
            display: block;
        }

        .contact-form {
            background: var(--card);
            padding: 30px;
            border-radius: 18px;
            border: 1px solid var(--border);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-size: 0.85rem;
            color: #cbd5e1;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 13px 15px;
            background: rgba(255,255,255,0.03);
            color: white;
            border: 1px solid var(--border);
            border-radius: 8px;
            outline: none;
            transition: 0.3s;
        }

        .form-group textarea {
            resize: vertical;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            border-color: var(--light-blue);
            box-shadow: 0 0 0 3px rgba(56,189,248,0.08);
        }

        .send-btn {
            border: none;
            cursor: pointer;
        }

        /* =========================
           FOOTER
        ========================== */
        footer {
            padding: 30px 0;
            text-align: center;
            border-top: 1px solid var(--border);
        }

        footer p {
            color: var(--gray);
            font-size: 0.85rem;
        }

        /* =========================
           ANIMATION
        ========================== */
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }

            50% {
                transform: translateY(-15px);
            }
        }

        /* =========================
           TABLET
        ========================== */
        @media (max-width: 900px) {
            .hero,
            .about,
            .contact {
                grid-template-columns: 1fr;
            }

            .hero {
                text-align: center;
            }

            .hero p {
                margin-left: auto;
                margin-right: auto;
            }

            .buttons {
                justify-content: center;
            }

            .profile-area {
                order: -1;
            }

            .skills,
            .projects {
                grid-template-columns: repeat(2, 1fr);
            }

            .about-box {
                max-width: 400px;
                margin: auto;
            }
        }

        /* =========================
           MOBILE
        ========================== */
        @media (max-width: 650px) {
            section {
                padding: 75px 0;
            }

            .nav-links {
                display: none;
            }

            nav {
                justify-content: center;
            }

            .hero h1 {
                font-size: 3rem;
            }

            .profile {
                width: 240px;
                height: 300px;
            }

            .skills,
            .projects {
                grid-template-columns: 1fr;
            }

            .details {
                grid-template-columns: 1fr;
            }

            .education-card {
                flex-direction: column;
            }

            .education-icon {
                align-self: flex-start;
            }

            .buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
                text-align: center;
            }

            .section-title h2 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>

<body>

    <!-- =========================
         NAVIGATION
    ========================== -->
    <header>
        <div class="container">
            <nav>
                <a href="#home" class="logo">
                    <span>G</span>M.
                </a>

                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#education">Education</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>


    <!-- =========================
         HOME
    ========================== -->
    <section id="home">
        <div class="container hero">

            <div>
                <div class="tag">WELCOME TO MY PORTFOLIO</div>

                <h1>
                    Gelou
                    <span>Menchavez</span>
                </h1>

                <h2>Information Technology Student</h2>

                <p>
                    Hello! I'm Gelou Menchavez, a 2nd year Information Technology
                    student passionate about programming, web development,
                    databases, and learning new technologies.
                </p>

                <div class="buttons">
                    <a href="#projects" class="btn btn-primary">
                        View My Projects
                    </a>

                    <a href="#contact" class="btn btn-outline">
                        Contact Me
                    </a>
                </div>
            </div>


            <div class="profile-area">
                <div class="profile">
                    <div class="profile-inner">

                        <!-- PROFILE PICTURE PLACEHOLDER -->
                        <div class="profile-circle">
                            GM
                        </div>

                        <p>Profile Picture</p>

                    </div>
                </div>
            </div>

        </div>
    </section>


    <!-- =========================
         ABOUT
    ========================== -->
    <section id="about">
        <div class="container">

            <div class="section-title">
                <small>ABOUT ME</small>
                <h2>Get To Know <span>Me</span></h2>
                <p>
                    A short introduction about myself and my journey as an IT student.
                </p>
            </div>

            <div class="about">

                <div class="about-box">
                    <strong>02</strong>
                    <span>YEAR STUDENT</span>
                    <span>Information Technology</span>
                </div>

                <div class="about-content">

                    <h3>Learning, Building, and Growing</h3>

                    <p>
                        I'm Gelou Menchavez, a 2nd year Information Technology
                        student who is interested in technology and software
                        development.
                    </p>

                    <p>
                        I am currently learning programming, web development,
                        databases, and other IT skills. I enjoy creating projects
                        that allow me to practice what I learn in school and
                        improve my problem-solving skills.
                    </p>

                    <p>
                        My goal is to continue improving my technical skills,
                        gain more experience, and become a capable IT professional
                        in the future.
                    </p>

                    <div class="details">

                        <div class="detail">
                            <small>Name</small>
                            <strong>Gelou Menchavez</strong>
                        </div>

                        <div class="detail">
                            <small>Course</small>
                            <strong>Information Technology</strong>
                        </div>

                        <div class="detail">
                            <small>Year Level</small>
                            <strong>2nd Year Student</strong>
                        </div>

                        <div class="detail">
                            <small>Focus</small>
                            <strong>Web & Software Development</strong>
                        </div>

                    </div>
                </div>

            </div>
        </div>
    </section>


    <!-- =========================
         SKILLS
    ========================== -->
    <section id="skills">
        <div class="container">

            <div class="section-title">
                <small>MY SKILLS</small>
                <h2>What I <span>Know</span></h2>
                <p>
                    Some of the technologies and IT concepts I am currently learning.
                </p>
            </div>

            <div class="skills">

                <div class="skill-card">
                    <div class="skill-icon">&lt;/&gt;</div>
                    <h3>HTML</h3>
                    <p>
                        Creating structured and semantic web pages using HTML5.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">#</div>
                    <h3>CSS</h3>
                    <p>
                        Designing responsive and attractive websites using CSS3.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">C#</div>
                    <h3>C#</h3>
                    <p>
                        Learning programming concepts and application development
                        using C#.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">DB</div>
                    <h3>Database</h3>
                    <p>
                        Learning database organization, records, and CRUD operations.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">WEB</div>
                    <h3>Web Development</h3>
                    <p>
                        Building responsive and user-friendly websites.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">{ }</div>
                    <h3>Basic Programming</h3>
                    <p>
                        Understanding variables, conditions, loops, functions,
                        and programming logic.
                    </p>
                </div>

            </div>
        </div>
    </section>


    <!-- =========================
         PROJECTS
    ========================== -->
    <section id="projects">
        <div class="container">

            <div class="section-title">
                <small>MY PROJECTS</small>
                <h2>Featured <span>Projects</span></h2>
                <p>
                    Projects I have worked on while learning Information Technology.
                </p>
            </div>

            <div class="projects">

                <div class="project">

                    <div class="project-image">
                        🏨
                    </div>

                    <div class="project-content">
                        <h3>Hotel Management System</h3>

                        <p>
                            A system designed to manage hotel information,
                            room reservations, customer records, and basic
                            hotel operations.
                        </p>

                        <div class="tags">
                            <span>C#</span>
                            <span>Database</span>
                            <span>CRUD</span>
                        </div>
                    </div>

                </div>


                <div class="project">

                    <div class="project-image">
                        { }
                    </div>

                    <div class="project-content">
                        <h3>CRUD System</h3>

                        <p>
                            A basic Create, Read, Update, and Delete system
                            created to practice database management and
                            programming logic.
                        </p>

                        <div class="tags">
                            <span>C#</span>
                            <span>Database</span>
                            <span>CRUD</span>
                        </div>
                    </div>

                </div>


                <div class="project">

                    <div class="project-image">
                        &lt;/&gt;
                    </div>

                    <div class="project-content">
                        <h3>Personal Website</h3>

                        <p>
                            A responsive portfolio website created to showcase
                            my skills, projects, education, and experience
                            as an IT student.
                        </p>

                        <div class="tags">
                            <span>HTML</span>
                            <span>CSS</span>
                            <span>Responsive</span>
                        </div>
                    </div>

                </div>

            </div>
        </div>
    </section>


    <!-- =========================
         EDUCATION
    ========================== -->
    <section id="education">
        <div class="container">

            <div class="section-title">
                <small>MY EDUCATION</small>
                <h2>Educational <span>Journey</span></h2>
                <p>
                    My current academic journey in Information Technology.
                </p>
            </div>

            <div class="education">

                <div class="education-card">

                    <div class="education-icon">
                        🎓
                    </div>

                    <div>
                        <h3>Information Technology</h3>

                        <h4>2nd Year Student</h4>

                        <p>
                            Currently studying Information Technology while
                            developing knowledge and skills in programming,
                            web development, databases, and other areas
                            of technology.
                        </p>
                    </div>

                </div>

            </div>
        </div>
    </section>


    <!-- =========================
         CONTACT
    ========================== -->
    <section id="contact">
        <div class="container">

            <div class="section-title">
                <small>CONTACT ME</small>
                <h2>Let's <span>Connect</span></h2>
                <p>
                    Feel free to send me a message.
                </p>
            </div>

            <div class="contact">

                <div class="contact-info">

                    <h3>Get In Touch</h3>

                    <p>
                        If you want to ask a question, discuss a project,
                        or simply connect with me, you can use the form.
                    </p>

                    <div class="contact-item">
                        <small>Name</small>
                        <strong>Gelou Menchavez</strong>
                    </div>

                    <div class="contact-item">
                        <small>Email</small>
                        <strong>gelou.menchavez@email.com</strong>
                    </div>

                    <div class="contact-item">
                        <small>Course</small>
                        <strong>Information Technology</strong>
                    </div>

                </div>


                <form class="contact-form" action="#" method="post">

                    <div class="form-group">
                        <label for="name">Name</label>

                        <input
                            type="text"
                            id="name"
                            name="name"
                            placeholder="Enter your name"
                            required
                        >
                    </div>

                    <div class="form-group">
                        <label for="email">Email</label>

                        <input
                            type="email"
                            id="email"
                            name="email"
                            placeholder="Enter your email"
                            required
                        >
                    </div>

                    <div class="form-group">
                        <label for="message">Message</label>

                        <textarea
                            id="message"
                            name="message"
                            rows="6"
                            placeholder="Write your message..."
                            required
                        ></textarea>
                    </div>

                    <button type="submit" class="btn btn-primary send-btn">
                        Send Message →
                    </button>

                </form>

            </div>
        </div>
    </section>


    <!-- =========================
         FOOTER
    ========================== -->
    <footer>
        <div class="container">
            <p>
                © 2026 Gelou Menchavez. All Rights Reserved.
            </p>
        </div>
    </footer>

</body>
</html>
```

