# codingwalle
this project for class
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>About Us | CodingWale</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #f5f7fb;
            color: #1f2937;
        }

        /* Navbar */
        .navbar {
            background: #111827;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            color: #38bdf8;
            font-size: 28px;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            gap: 25px;
            list-style: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 16px;
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: #38bdf8;
        }

        /* Hero */
        .hero {
            background: linear-gradient(135deg, #0f172a, #0369a1);
            color: white;
            text-align: center;
            padding: 90px 20px;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 15px;
        }

        .hero h1 span {
            color: #38bdf8;
        }

        .hero p {
            max-width: 750px;
            margin: auto;
            font-size: 18px;
            line-height: 1.7;
        }

        /* About */
        .about {
            padding: 70px 8%;
            text-align: center;
        }

        .about h2 {
            font-size: 36px;
            margin-bottom: 20px;
        }

        .about > p {
            max-width: 850px;
            margin: auto;
            line-height: 1.8;
            color: #64748b;
            font-size: 17px;
        }

        /* Cards */
        .cards {
            margin-top: 50px;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .card {
            background: white;
            padding: 35px 25px;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
            transition: 0.3s;
        }

        .card:hover {
            transform: translateY(-8px);
        }

        .card .icon {
            font-size: 42px;
            margin-bottom: 15px;
        }

        .card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: #0284c7;
        }

        .card p {
            color: #64748b;
            line-height: 1.7;
        }

        /* Why CodingWale */
        .why {
            background: #e0f2fe;
            padding: 70px 8%;
            text-align: center;
        }

        .why h2 {
            font-size: 36px;
            margin-bottom: 35px;
        }

        .why-list {
            max-width: 800px;
            margin: auto;
            display: grid;
            gap: 18px;
        }

        .why-item {
            background: white;
            padding: 20px;
            border-radius: 10px;
            text-align: left;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.06);
        }

        .why-item strong {
            color: #0284c7;
        }

        /* Footer */
        footer {
            background: #111827;
            color: white;
            text-align: center;
            padding: 25px;
        }

        /* Responsive */
        @media (max-width: 768px) {

            .navbar {
                flex-direction: column;
                gap: 15px;
            }

            .nav-links {
                gap: 12px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero h1 {
                font-size: 36px;
            }

            .cards {
                grid-template-columns: 1fr;
            }

            .about h2,
            .why h2 {
                font-size: 30px;
            }
        }
    </style>
</head>

<body>

    <!-- Navigation -->
    <header class="navbar">

        <div class="logo">
            CodingWale
        </div>

        <ul class="nav-links">
            <li>
                <a href="index.html">Home</a>
            </li>

            <li>
                <a href="about.html">About</a>
            </li>

            <li>
                <a href="courses.html">Courses</a>
            </li>

            <li>
                <a href="reviews.html">Reviews</a>
            </li>

            <li>
                <a href="contact.html">Contact</a>
            </li>
        </ul>

    </header>


    <!-- Hero Section -->
    <section class="hero">

        <h1>
            About <span>CodingWale</span>
        </h1>

        <p>
            CodingWale is a learning platform created to make
            programming and technology simple, practical and accessible
            for every student.
        </p>

    </section>


    <!-- About Section -->
    <section class="about">

        <h2>Who We Are</h2>

        <p>
            CodingWale is an educational platform designed for students,
            beginners and technology enthusiasts who want to learn coding
            and modern technologies. Our goal is to provide simple,
            practical and easy-to-understand learning resources that help
            students build real-world skills.
        </p>


        <div class="cards">

            <!-- Mission -->
            <div class="card">

                <div class="icon">🎯</div>

                <h3>Our Mission</h3>

                <p>
                    Our mission is to make programming easy to understand
                    and help students develop strong technical skills
                    through practical learning.
                </p>

            </div>


            <!-- Vision -->
            <div class="card">

                <div class="icon">🚀</div>

                <h3>Our Vision</h3>

                <p>
                    We aim to build a strong coding community where
                    students can learn, practice and create innovative
                    technology projects.
                </p>

            </div>


            <!-- Learning -->
            <div class="card">

                <div class="icon">💻</div>

                <h3>Practical Learning</h3>

                <p>
                    We believe in learning by doing. Our courses and
                    resources focus on practical projects and real-world
                    programming concepts.
                </p>

            </div>

        </div>

    </section>


    <!-- Why CodingWale -->
    <section class="why">

        <h2>Why Choose CodingWale?</h2>

        <div class="why-list">

            <div class="why-item">
                ✅ <strong>Beginner Friendly:</strong>
                Learn programming from the basics.
            </div>

            <div class="why-item">
                ✅ <strong>Practical Projects:</strong>
                Build projects while learning.
            </div>

            <div class="why-item">
                ✅ <strong>Modern Technologies:</strong>
                Learn technologies used in today's industry.
            </div>

            <div class="why-item">
                ✅ <strong>Easy Learning:</strong>
                Simple explanations designed for students.
            </div>

        </div>

    </section>


    <!-- Footer -->
    <footer>

        <p>
            © 2026 CodingWale. All Rights Reserved.
        </p>

    </footer>

</body>
</html>
