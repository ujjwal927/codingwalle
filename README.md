# codingwalle
this project for class
<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <meta name="description"
          content="Explore CodingWalle courses in Web Development, Programming, AI, Database and Cyber Security.">

    <title>CodingWalle | Courses</title>


    <style>

        /* =====================================================
           CODINGWALLE COURSES PAGE
        ===================================================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: "Segoe UI", Arial, sans-serif;
            background: #050810;
            color: #ffffff;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }


        /* =====================================================
           BACKGROUND
        ===================================================== */

        body::before {
            content: "";

            position: fixed;

            width: 500px;
            height: 500px;

            top: -200px;
            left: -200px;

            background: #00e5ff;

            filter: blur(180px);

            opacity: .055;

            z-index: -1;
        }

        body::after {
            content: "";

            position: fixed;

            width: 500px;
            height: 500px;

            right: -220px;
            bottom: -200px;

            background: #7c4dff;

            filter: blur(180px);

            opacity: .07;

            z-index: -1;
        }


        /* =====================================================
           NAVBAR
        ===================================================== */

        header {
            position: sticky;

            top: 0;

            z-index: 1000;

            background:
                rgba(5, 8, 16, .88);

            backdrop-filter: blur(18px);

            border-bottom:
                1px solid #192438;
        }


        .navbar {
            max-width: 1250px;

            margin: auto;

            padding: 15px 25px;

            display: flex;

            align-items: center;

            justify-content: space-between;
        }


        .logo {
            display: flex;

            align-items: center;

            gap: 10px;

            font-size: 24px;

            font-weight: 800;
        }


        .logo-icon {
            width: 40px;
            height: 40px;

            display: flex;

            align-items: center;
            justify-content: center;

            border-radius: 10px;

            background:
                linear-gradient(
                    135deg,
                    #00e5ff,
                    #7c4dff
                );

            color: #050810;

            font-weight: 900;
        }


        .logo span {
            background:
                linear-gradient(
                    90deg,
                    #00e5ff,
                    #a970ff
                );

            -webkit-background-clip: text;

            color: transparent;
        }


        .nav-links {
            display: flex;

            gap: 24px;
        }


        .nav-links a {
            color: #919db2;

            font-size: 14px;

            font-weight: 600;

            transition: .3s;
        }


        .nav-links a:hover,
        .nav-links .active {
            color: #00e5ff;
        }


        .nav-button {
            padding: 11px 18px;

            border-radius: 9px;

            background:
                linear-gradient(
                    135deg,
                    #00e5ff,
                    #7c4dff
                );

            font-size: 13px;

            font-weight: 800;
        }


        /* =====================================================
           HERO
        ===================================================== */

        .hero {
            max-width: 1200px;

            margin: auto;

            padding:
                90px 25px 65px;

            text-align: center;
        }


        .hero-label {
            color: #00e5ff;

            font-size: 12px;

            font-weight: 900;

            letter-spacing: 2px;

            margin-bottom: 18px;
        }


        .hero h1 {
            font-size:
                clamp(45px, 6vw, 70px);

            line-height: 1;

            letter-spacing: -3px;

            margin-bottom: 22px;
        }


        .hero h1 span {
            background:
                linear-gradient(
                    90deg,
                    #00e5ff,
                    #8b5cf6
                );

            -webkit-background-clip: text;

            color: transparent;
        }


        .hero p {
            max-width: 720px;

            margin: auto;

            color: #7e8ba0;

            font-size: 16px;

            line-height: 1.8;
        }


        /* =====================================================
           SEARCH
        ===================================================== */

        .search-area {
            max-width: 850px;

            margin:
                0 auto 60px;

            padding: 0 25px;
        }


        .search-box {
            display: flex;

            align-items: center;

            gap: 12px;

            padding: 6px 8px 6px 18px;

            background: #0a101c;

            border:
                1px solid #26344b;

            border-radius: 12px;

            transition: .3s;
        }


        .search-box:focus-within {
            border-color: #00e5ff;

            box-shadow:
                0 0 25px
                rgba(0,229,255,.07);
        }


        .search-icon {
            font-size: 18px;

            color: #66758c;
        }


        .search-box input {
            width: 100%;

            border: none;
            outline: none;

            background: transparent;

            color: white;

            font-size: 14px;
        }


        .search-box input::placeholder {
            color: #56647a;
        }


        .search-button {
            border: none;

            padding: 12px 20px;

            border-radius: 8px;

            background:
                linear-gradient(
                    135deg,
                    #00e5ff,
                    #7c4dff
                );

            color: #050810;

            font-weight: 800;

            cursor: pointer;
        }


        /* =====================================================
           FILTERS
        ===================================================== */

        .filters {
            max-width: 1200px;

            margin: auto;

            padding:
                0 25px 55px;

            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 10px;
        }


        .filter {
            padding:
                10px 17px;

            border:
                1px solid #26344b;

            border-radius: 30px;

            color: #8793a7;

            background: #090f1a;

            font-size: 12px;

            font-weight: 700;

            transition: .3s;

            cursor: pointer;
        }


        .filter:hover,
        .filter.active {
            color: #00e5ff;

            border-color: #00e5ff;

            background:
                rgba(0,229,255,.05);
        }


        /* =====================================================
           MAIN SECTION
        ===================================================== */

        .section {
            max-width: 1200px;

            margin: auto;

            padding:
                0 25px 100px;
        }


        .branch-heading {
            display: flex;

            align-items: end;

            justify-content: space-between;

            margin:
                55px 0 25px;
        }


        .branch-label {
            color: #00e5ff;

            font-size: 11px;

            font-weight: 900;

            letter-spacing: 2px;
        }


        .branch-heading h2 {
            font-size: 32px;

            margin-top: 5px;
        }


        .branch-heading p {
            color: #69768b;

            font-size: 13px;
        }


        /* =====================================================
           COURSE GRID
        ===================================================== */

        .course-grid {
            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 18px;
        }


        .course {
            background: #0a101c;

            border:
                1px solid #1c293d;

            border-radius: 16px;

            overflow: hidden;

            transition: .35s;

            display: flex;

            flex-direction: column;
        }


        .course:hover {
            transform:
                translateY(-7px);

            border-color:
                #00e5ff;

            box-shadow:
                0 18px 50px
                rgba(0,0,0,.3);
        }


        .course-top {
            height: 145px;

            display: flex;

            align-items: center;

            justify-content: center;

            font-size: 48px;

            background:
                linear-gradient(
                    135deg,
                    rgba(0,229,255,.06),
                    rgba(124,77,255,.10)
                );

            border-bottom:
                1px solid #1b273a;
        }


        .course-content {
            padding: 23px;

            display: flex;

            flex-direction: column;

            flex: 1;
        }


        .course-tag {
            color: #00e5ff;

            font-size: 10px;

            font-weight: 900;

            letter-spacing: 1.5px;

            margin-bottom: 7px;
        }


        .course h3 {
            font-size: 20px;

            margin-bottom: 9px;
        }


        .course-description {
            color: #748198;

            font-size: 13px;

            line-height: 1.7;

            margin-bottom: 20px;
        }


        .course-meta {
            display: flex;

            gap: 15px;

            flex-wrap: wrap;

            padding-bottom: 17px;

            border-bottom:
                1px solid #1c2739;

            color: #66748a;

            font-size: 11px;
        }


        .course-bottom {
            display: flex;

            align-items: center;

            justify-content: space-between;

            margin-top: 17px;
        }


        .level {
            color: #9ba7b9;

            font-size: 11px;
        }


        .learn-btn {
            color: #00e5ff;

            font-size: 12px;

            font-weight: 900;

            transition: .3s;
        }


        .learn-btn:hover {
            color: white;

            transform:
                translateX(4px);
        }


        /* =====================================================
           BRANCH CARD
        ===================================================== */

        .branch-intro {
            margin-top: 85px;

            padding: 35px;

            border:
                1px solid #202e44;

            border-radius: 17px;

            background:
                linear-gradient(
                    135deg,
                    rgba(0,229,255,.035),
                    rgba(124,77,255,.06)
                );
        }


        .branch-intro h2 {
            font-size: 30px;

            margin-bottom: 8px;
        }


        .branch-intro p {
            color: #748198;

            font-size: 14px;

            max-width: 750px;
        }


        /* =====================================================
           CTA
        ===================================================== */

        .cta {
            max-width: 1100px;

            margin:
                0 auto 100px;

            padding:
                70px 25px;

            text-align: center;

            border:
                1px solid #26344b;

            border-radius: 20px;

            background:
                linear-gradient(
                    135deg,
                    rgba(0,229,255,.06),
                    rgba(124,77,255,.10)
                );
        }


        .cta-label {
            color: #00e5ff;

            font-size: 11px;

            font-weight: 900;

            letter-spacing: 2px;
        }


        .cta h2 {
            font-size:
                clamp(32px,5vw,50px);

            margin:
                10px 0 12px;
        }


        .cta p {
            color: #748198;

            margin-bottom: 28px;
        }


        .cta-btn {
            display: inline-block;

            padding:
                14px 23px;

            border-radius: 9px;

            background:
                linear-gradient(
                    135deg,
                    #00e5ff,
                    #7c4dff
                );

            font-weight: 900;

            color: #050810;

            transition: .3s;
        }


        .cta-btn:hover {
            transform:
                translateY(-4px);

            box-shadow:
                0 15px 35px
                rgba(0,229,255,.18);
        }


        /* =====================================================
           FOOTER
        ===================================================== */

        footer {
            border-top:
                1px solid #182337;

            padding:
                50px 25px 25px;

            text-align: center;
        }


        .footer-logo {
            font-size: 24px;

            font-weight: 800;

            margin-bottom: 10px;
        }


        .footer-logo span {
            color: #00e5ff;
        }


        .footer-text {
            color: #657289;

            margin-bottom: 25px;
        }


        .footer-links {
            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 25px;

            margin-bottom: 30px;
        }


        .footer-links a {
            color: #7d899d;

            font-size: 13px;

            transition: .3s;
        }


        .footer-links a:hover {
            color: #00e5ff;
        }


        .copyright {
            border-top:
                1px solid #182337;

            padding-top: 20px;

            color: #4f5c70;

            font-size: 12px;
        }


        /* =====================================================
           RESPONSIVE
        ===================================================== */

        @media(max-width:950px) {

            .nav-links {
                display: none;
            }

            .course-grid {
                grid-template-columns:
                    repeat(2,1fr);
            }

        }


        @media(max-width:600px) {

            .navbar {
                padding:
                    12px 15px;
            }

            .logo {
                font-size: 19px;
            }

            .logo-icon {
                width: 34px;
                height: 34px;
            }

            .nav-button {
                padding:
                    9px 12px;

                font-size: 11px;
            }

            .hero {
                padding:
                    70px 18px 50px;
            }

            .hero h1 {
                font-size: 45px;

                letter-spacing: -2px;
            }

            .search-area {
                padding:
                    0 18px;
            }

            .search-box {
                padding-left: 13px;
            }

            .search-button {
                padding:
                    11px 14px;
            }

            .filters {
                padding:
                    0 18px 40px;
            }

            .section {
                padding:
                    0 18px 70px;
            }

            .course-grid {
                grid-template-columns: 1fr;
            }

            .branch-heading {
                display: block;
            }

            .branch-heading p {
                margin-top: 5px;
            }

            .branch-intro {
                margin-top: 60px;

                padding: 25px;
            }

            .cta {
                margin:
                    0 15px 70px;

                padding:
                    50px 20px;
            }

        }

    </style>

</head>


<body>


<!-- =====================================================
     NAVBAR
===================================================== -->

<header>

    <nav class="navbar">


        <a href="index.html"
           class="logo">

            <div class="logo-icon">
                &lt;/&gt;
            </div>

            <span>
                CodingWalle
            </span>

        </a>


        <div class="nav-links">

            <a href="index.html">
                Index
            </a>

            <a href="home.html">
                Home
            </a>

            <a href="about.html">
                About
            </a>

            <a href="courses.html"
               class="active">
                Courses
            </a>

            <a href="reviews.html">
                Reviews
            </a>

            <a href="contact.html">
                Contact
            </a>

        </div>


        <a href="#all-courses"
           class="nav-button">

            Browse Courses →

        </a>


    </nav>

</header>



<!-- =====================================================
     HERO
===================================================== -->

<section class="hero">


    <div class="hero-label">
        CODINGWALLE LEARNING HUB
    </div>


    <h1>

        Learn.
        <span>Code. Build.</span>

    </h1>


    <p>

        Explore structured coding courses across five
        technology branches. Start from the basics,
        practice your skills and build real projects.

    </p>


</section>



<!-- =====================================================
     SEARCH
===================================================== -->

<div class="search-area">

    <div class="search-box">

        <span class="search-icon">
            🔍
        </span>


        <input
            type="text"
            placeholder="Search HTML, Python, JavaScript, AI, SQL..."
            aria-label="Search courses"
        >


        <button
            class="search-button">

            Search

        </button>

    </div>

</div>



<!-- =====================================================
     FILTERS
===================================================== -->

<div class="filters">

    <a href="#all-courses"
       class="filter active">

        All Courses

    </a>


    <a href="#web"
       class="filter">

        Web Development

    </a>


    <a href="#programming"
       class="filter">

        Programming

    </a>


    <a href="#ai"
       class="filter">

        AI & Data

    </a>


    <a href="#database"
       class="filter">

        Database & Backend

    </a>


    <a href="#security"
       class="filter">

        Cyber Security

    </a>

</div>



<!-- =====================================================
     COURSES
===================================================== -->

<main id="all-courses">


<!-- =====================================================
     BRANCH 01
     WEB DEVELOPMENT
===================================================== -->

<section class="section"
         id="web">


    <div class="branch-heading">


        <div>

            <div class="branch-label">
                BRANCH 01
            </div>

            <h2>
                Web Development
            </h2>

        </div>


        <p>
            Build modern websites & web apps
        </p>


    </div>



    <div class="course-grid">


        <!-- HTML -->

        <article class="course">


            <div class="course-top">
                🌐
            </div>


            <div class="course-content">


                <div class="course-tag">
                    WEB DEVELOPMENT
                </div>


                <h3>
                    HTML Fundamentals
                </h3>


                <p class="course-description">

                    Learn the structure of websites,
                    semantic HTML, forms, tables,
                    links and modern HTML elements.

                </p>


                <div class="course-meta">

                    <span>
                        📚 20+ Lessons
                    </span>

                    <span>
                        💻 Projects
                    </span>

                </div>


                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>


                    <a href="#"
                       class="learn-btn">

                        Learn More →

                    </a>

                </div>


            </div>

        </article>



        <!-- CSS -->

        <article class="course">


            <div class="course-top">
                🎨
            </div>


            <div class="course-content">


                <div class="course-tag">
                    WEB DEVELOPMENT
                </div>


                <h3>
                    CSS Mastery
                </h3>


                <p class="course-description">

                    Master layouts, Flexbox, Grid,
                    responsive design, animations
                    and modern UI styling.

                </p>


                <div class="course-meta">

                    <span>
                        📚 25+ Lessons
                    </span>

                    <span>
                        🎨 UI Projects
                    </span>

                </div>


                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>


                    <a href="#"
                       class="learn-btn">

                        Learn More →

                    </a>

                </div>


            </div>

        </article>



        <!-- JavaScript -->

        <article class="course">


            <div class="course-top">
                ⚡
            </div>


            <div class="course-content">


                <div class="course-tag">
                    WEB DEVELOPMENT
                </div>


                <h3>
                    JavaScript
                </h3>


                <p class="course-description">

                    Learn variables, functions, DOM,
                    events, arrays, objects and
                    interactive web development.

                </p>


                <div class="course-meta">

                    <span>
                        📚 30+ Lessons
                    </span>

                    <span>
                        ⚙️ Projects
                    </span>

                </div>


                <div class="course-bottom">

                    <span class="level">
                        Beginner → Intermediate
                    </span>


                    <a href="#"
                       class="learn-btn">

                        Learn More →

                    </a>

                </div>


            </div>

        </article>



        <!-- React -->

        <article class="course">


            <div class="course-top">
                ⚛️
            </div>


            <div class="course-content">


                <div class="course-tag">
                    WEB DEVELOPMENT
                </div>


                <h3>
                    React
                </h3>


                <p class="course-description">

                    Build component-based modern
                    web interfaces with React.

                </p>


                <div class="course-meta">

                    <span>
                        📚 25+ Lessons
                    </span>

                    <span>
                        ⚛️ Projects
                    </span>

                </div>


                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>


                    <a href="#"
                       class="learn-btn">

                        Learn More →

                    </a>

                </div>


            </div>

        </article>



        <!-- Node -->

        <article class="course">


            <div class="course-top">
                🟢
            </div>


            <div class="course-content">


                <div class="course-tag">
                    WEB DEVELOPMENT
                </div>


                <h3>
                    Node.js
                </h3>


                <p class="course-description">

                    Learn server-side JavaScript,
                    APIs and backend fundamentals.

                </p>


                <div class="course-meta">

                    <span>
                        📚 25+ Lessons
                    </span>

                    <span>
                        🔌 API Projects
                    </span>

                </div>


                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>


                    <a href="#"
                       class="learn-btn">

                        Learn More →

                    </a>

                </div>


            </div>

        </article>



        <!-- Web Projects -->

        <article class="course">


            <div class="course-top">
                🚀
            </div>


            <div class="course-content">


                <div class="course-tag">
                    WEB DEVELOPMENT
                </div>


                <h3>
                    Web Projects
                </h3>


                <p class="course-description">

                    Apply your knowledge by building
                    responsive websites and practical
                    web applications.

                </p>


                <div class="course-meta">

                    <span>
                        🛠️ 10+ Projects
                    </span>

                    <span>
                        🚀 Portfolio
                    </span>

                </div>


                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>


                    <a href="#"
                       class="learn-btn">

                        Learn More →

                    </a>

                </div>


            </div>

        </article>


    </div>


</section>



<!-- =====================================================
     BRANCH 02
     PROGRAMMING
===================================================== -->

<section class="section"
         id="programming">


    <div class="branch-heading">

        <div>

            <div class="branch-label">
                BRANCH 02
            </div>

            <h2>
                Programming
            </h2>

        </div>


        <p>
            Build strong coding fundamentals
        </p>

    </div>



    <div class="course-grid">


        <article class="course">

            <div class="course-top">
                🔵
            </div>

            <div class="course-content">

                <div class="course-tag">
                    PROGRAMMING
                </div>

                <h3>
                    C Programming
                </h3>

                <p class="course-description">

                    Learn programming logic,
                    variables, loops, functions,
                    arrays and pointers.

                </p>

                <div class="course-meta">

                    <span>
                        📚 30+ Lessons
                    </span>

                    <span>
                        💻 Practice
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                🔷
            </div>

            <div class="course-content">

                <div class="course-tag">
                    PROGRAMMING
                </div>

                <h3>
                    C++ Programming
                </h3>

                <p class="course-description">

                    Learn object-oriented programming,
                    classes, inheritance and STL.

                </p>

                <div class="course-meta">

                    <span>
                        📚 30+ Lessons
                    </span>

                    <span>
                        🧩 OOP
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                🐍
            </div>

            <div class="course-content">

                <div class="course-tag">
                    PROGRAMMING
                </div>

                <h3>
                    Python
                </h3>

                <p class="course-description">

                    Learn Python syntax, data structures,
                    functions, modules and practical coding.

                </p>

                <div class="course-meta">

                    <span>
                        📚 35+ Lessons
                    </span>

                    <span>
                        🐍 Projects
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                ☕
            </div>

            <div class="course-content">

                <div class="course-tag">
                    PROGRAMMING
                </div>

                <h3>
                    Java
                </h3>

                <p class="course-description">

                    Understand Java programming,
                    OOP concepts and application development.

                </p>

                <div class="course-meta">

                    <span>
                        📚 30+ Lessons
                    </span>

                    <span>
                        ☕ OOP
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>

    </div>

</section>



<!-- =====================================================
     BRANCH 03
     AI & DATA SCIENCE
===================================================== -->

<section class="section"
         id="ai">


    <div class="branch-heading">

        <div>

            <div class="branch-label">
                BRANCH 03
            </div>

            <h2>
                AI & Data Science
            </h2>

        </div>

        <p>
            Explore data and intelligent systems
        </p>

    </div>



    <div class="course-grid">


        <article class="course">

            <div class="course-top">
                🤖
            </div>

            <div class="course-content">

                <div class="course-tag">
                    ARTIFICIAL INTELLIGENCE
                </div>

                <h3>
                    AI Fundamentals
                </h3>

                <p class="course-description">

                    Understand artificial intelligence,
                    machine learning and modern AI concepts.

                </p>

                <div class="course-meta">

                    <span>
                        📚 20+ Lessons
                    </span>

                    <span>
                        🤖 AI
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                📊
            </div>

            <div class="course-content">

                <div class="course-tag">
                    DATA SCIENCE
                </div>

                <h3>
                    Data Science
                </h3>

                <p class="course-description">

                    Learn how to work with data,
                    visualize information and discover patterns.

                </p>

                <div class="course-meta">

                    <span>
                        📚 25+ Lessons
                    </span>

                    <span>
                        📊 Data
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                🧠
            </div>

            <div class="course-content">

                <div class="course-tag">
                    MACHINE LEARNING
                </div>

                <h3>
                    Machine Learning
                </h3>

                <p class="course-description">

                    Explore machine learning concepts,
                    algorithms and model building.

                </p>

                <div class="course-meta">

                    <span>
                        📚 30+ Lessons
                    </span>

                    <span>
                        🧠 ML
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>

    </div>

</section>



<!-- =====================================================
     BRANCH 04
     DATABASE & BACKEND
===================================================== -->

<section class="section"
         id="database">


    <div class="branch-heading">

        <div>

            <div class="branch-label">
                BRANCH 04
            </div>

            <h2>
                Database & Backend
            </h2>

        </div>

        <p>
            Understand servers, APIs and data
        </p>

    </div>



    <div class="course-grid">


        <article class="course">

            <div class="course-top">
                🗄️
            </div>

            <div class="course-content">

                <div class="course-tag">
                    DATABASE
                </div>

                <h3>
                    SQL Fundamentals
                </h3>

                <p class="course-description">

                    Learn databases, tables, queries,
                    joins and SQL fundamentals.

                </p>

                <div class="course-meta">

                    <span>
                        📚 25+ Lessons
                    </span>

                    <span>
                        🗄️ SQL
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                🍃
            </div>

            <div class="course-content">

                <div class="course-tag">
                    DATABASE
                </div>

                <h3>
                    MongoDB
                </h3>

                <p class="course-description">

                    Explore NoSQL databases,
                    documents, collections and MongoDB.

                </p>

                <div class="course-meta">

                    <span>
                        📚 20+ Lessons
                    </span>

                    <span>
                        🍃 NoSQL
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                🔌
            </div>

            <div class="course-content">

                <div class="course-tag">
                    BACKEND
                </div>

                <h3>
                    REST APIs
                </h3>

                <p class="course-description">

                    Understand APIs, HTTP methods,
                    requests, responses and backend communication.

                </p>

                <div class="course-meta">

                    <span>
                        📚 18+ Lessons
                    </span>

                    <span>
                        🔌 API
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Intermediate
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>

    </div>

</section>



<!-- =====================================================
     BRANCH 05
     CYBER SECURITY
===================================================== -->

<section class="section"
         id="security">


    <div class="branch-heading">

        <div>

            <div class="branch-label">
                BRANCH 05
            </div>

            <h2>
                Cyber Security
            </h2>

        </div>

        <p>
            Learn the fundamentals of digital security
        </p>

    </div>



    <div class="course-grid">


        <article class="course">

            <div class="course-top">
                🛡️
            </div>

            <div class="course-content">

                <div class="course-tag">
                    CYBER SECURITY
                </div>

                <h3>
                    Cyber Security Basics
                </h3>

                <p class="course-description">

                    Learn core cybersecurity concepts,
                    threats, security principles and safe computing.

                </p>

                <div class="course-meta">

                    <span>
                        📚 20+ Lessons
                    </span>

                    <span>
                        🛡️ Security
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                🐧
            </div>

            <div class="course-content">

                <div class="course-tag">
                    CYBER SECURITY
                </div>

                <h3>
                    Linux Fundamentals
                </h3>

                <p class="course-description">

                    Learn Linux commands, files,
                    permissions and basic system concepts.

                </p>

                <div class="course-meta">

                    <span>
                        📚 25+ Lessons
                    </span>

                    <span>
                        🐧 Linux
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>



        <article class="course">

            <div class="course-top">
                🌐
            </div>

            <div class="course-content">

                <div class="course-tag">
                    CYBER SECURITY
                </div>

                <h3>
                    Networking Basics
                </h3>

                <p class="course-description">

                    Understand networks, protocols,
                    IP addresses and essential networking concepts.

                </p>

                <div class="course-meta">

                    <span>
                        📚 22+ Lessons
                    </span>

                    <span>
                        🌐 Networking
                    </span>

                </div>

                <div class="course-bottom">

                    <span class="level">
                        Beginner
                    </span>

                    <a href="#" class="learn-btn">
                        Learn More →
                    </a>

                </div>

            </div>

        </article>

    </div>

</section>


</main>



<!-- =====================================================
     CTA
===================================================== -->

<section class="cta">


    <div class="cta-label">
        YOUR CODING JOURNEY STARTS HERE
    </div>


    <h2>
        Ready To Start Learning?
    </h2>


    <p>

        Choose a branch, pick a course and start
        building your skills today.

    </p>


    <a href="contact.html"
       class="cta-btn">

        Join CodingWalle →

    </a>


</section>



<!-- =====================================================
     FOOTER
===================================================== -->

<footer>


    <div class="footer-logo">

        <span>&lt;/&gt;</span>
        CodingWalle

    </div>


    <p class="footer-text">

        Learn. Code. Build. Become.

    </p>


    <div class="footer-links">

        <a href="index.html">
            Index
        </a>

        <a href="home.html">
            Home
        </a>

        <a href="about.html">
            About
        </a>

        <a href="courses.html">
            Courses
        </a>

        <a href="reviews.html">
            Reviews
        </a>

        <a href="contact.html">
            Contact
        </a>

    </div>


    <div class="copyright">

        © 2026 CodingWalle.
        All Rights Reserved.

    </div>


</footer>


<!-- =====================================================
     SIMPLE SEARCH FUNCTION
===================================================== -->

<script>

    const searchInput =
        document.querySelector(".search-box input");

    const searchButton =
        document.querySelector(".search-button");

    const courses =
        document.querySelectorAll(".course");


    function searchCourses() {

        const search =
            searchInput.value
            .toLowerCase()
            .trim();


        courses.forEach(course => {

            const text =
                course.innerText.toLowerCase();


            if (text.includes(search)) {

                course.style.display = "flex";

            } else {

                course.style.display = "none";

            }

        });

    }


    searchButton.addEventListener(
        "click",
        searchCourses
    );


    searchInput.addEventListener(
        "keyup",
        function(event) {

            if (event.key === "Enter") {

                searchCourses();

            }

        }
    );

</script>


</body>

</html>
