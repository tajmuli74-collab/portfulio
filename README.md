<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tajmul Islam | WordPress Web Designer</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-bg: #0f172a;
            --accent-blue: #3b82f6;
            --glass-bg: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 255, 255, 0.1);
            --text-main: #f8fafc;
            --text-dim: #94a3b8;
            --transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #020617 0%, #0f172a 50%, #1e293b 100%);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* --- Global Components --- */
        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .section {
            padding: 100px 0;
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .section.appear {
            opacity: 1;
            transform: translateY(0);
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 3rem;
            text-align: center;
            background: linear-gradient(to right, #fff, var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* --- Navbar --- */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.5rem 0;
            z-index: 1000;
            transition: var(--transition);
            backdrop-filter: blur(10px);
        }

        nav.scrolled {
            background: rgba(15, 23, 42, 0.9);
            padding: 1rem 0;
            border-bottom: 1px solid var(--glass-border);
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-weight: 800;
            font-size: 1.5rem;
            color: var(--accent-blue);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dim);
            font-weight: 500;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--accent-blue);
        }

        /* --- Hero Section --- */
        #hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            opacity: 1;
            transform: none;
        }

        .hero-content h1 {
            font-size: clamp(3rem, 8vw, 5rem);
            font-weight: 800;
            margin-bottom: 1rem;
        }

        .hero-content p {
            font-size: 1.25rem;
            color: var(--text-dim);
            margin-bottom: 2rem;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: var(--accent-blue);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: var(--transition);
            box-shadow: 0 10px 20px rgba(59, 130, 246, 0.3);
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(59, 130, 246, 0.5);
        }

        /* --- Glassmorphism Cards (Services & Portfolio) --- */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .card {
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
            backdrop-filter: blur(12px);
            padding: 2rem;
            border-radius: 20px;
            transition: var(--transition);
        }

        .card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            border-color: var(--accent-blue);
        }

        .card i {
            font-size: 2.5rem;
            color: var(--accent-blue);
            margin-bottom: 1.5rem;
        }

        .portfolio-img {
            width: 100%;
            height: 200px;
            background: #1e293b;
            border-radius: 12px;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-dim);
        }

        /* --- Contact --- */
        .contact-container {
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }

        .social-links {
            margin-top: 2rem;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
        }

        .social-links a {
            font-size: 1.5rem;
            color: var(--text-main);
            transition: var(--transition);
        }

        .social-links a:hover {
            color: var(--accent-blue);
            transform: scale(1.2);
        }

        /* --- Mobile Styles --- */
        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero-content h1 { font-size: 2.5rem; }
            .section { padding: 60px 0; }
        }
    </style>
</head>
<body>

    <nav id="navbar">
        <div class="container nav-content">
            <a href="#" class="logo">TAJMUL.</a>
            <ul class="nav-links">
                <li><a href="#hero">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Work</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <section id="hero" class="container">
        <div class="hero-content">
            <h1>Tajmul Islam</h1>
            <p>WordPress Web Designer</p>
            <p style="margin-top: -15px; font-weight: 300;">"I build fast, modern and high-converting websites."</p>
            <a href="#portfolio" class="btn">View My Work</a>
        </div>
    </section>

    <section id="about" class="section container">
        <h2>About Me</h2>
        <div class="card" style="max-width: 800px; margin: 0 auto; text-align: center;">
            <p>I am a passionate WordPress expert dedicated to crafting digital experiences that are not only visually stunning but also technically superior. With a focus on user experience and conversion optimization, I help businesses transform their online presence into a powerful growth engine.</p>
        </div>
    </section>

    <section id="services" class="section container">
        <h2>
