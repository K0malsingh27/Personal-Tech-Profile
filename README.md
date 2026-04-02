<!DOCTYPE html>
<html lang="en">
<head>
    <title>Komal Singh | Personal Tech Profile</title>
    <style>
        body {
            font-family: Arial;
            margin: 0;
            background: linear-gradient(to right, #74ebd5, #ACB6E5);
        }

        header {
            text-align: center;
            padding: 60px 20px;
            color: white;
        }

        .typing {
            border-right: 3px solid white;
            white-space: nowrap;
            overflow: hidden;
            margin: auto;
            width: fit-content;
            animation: typing 3s steps(20, end) forwards, blink 0.7s infinite;
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 220px; }
        }

        @keyframes blink {
            50% { border-color: transparent; }
        }

        nav {
            text-align: center;
            background: #333;
            padding: 10px;
        }

        nav a {
            color: white;
            margin: 10px;
            text-decoration: none;
            font-weight: bold;
        }

        section {
            background: white;
            margin: 20px;
            padding: 20px;
            border-radius: 12px;
            opacity: 0;
            transform: translateY(50px);
            transition: 0.6s;
        }

        section.show {
            opacity: 1;
            transform: translateY(0);
        }

        .card {
            text-align: center;
            transition: 0.3s;
        }

        .card:hover {
            box-shadow: 0 0 20px #4CAF50;
            transform: scale(1.05);
        }

        .skill {
            margin: 10px 0;
            text-align: left;
        }

        .bar {
            height: 10px;
            background: #ddd;
            border-radius: 5px;
        }

        .fill {
            height: 10px;
            background: #4CAF50;
            width: 0;
            border-radius: 5px;
            animation: fillBar 2s forwards;
        }

        .java { width: 80%; }
        .cpp { width: 70%; }
        .html { width: 85%; }

        @keyframes fillBar {
            from { width: 0; }
        }

    </style>
</head>
<body>

<header>
    <h1 class="typing">Komal Singh</h1>
    <p>Personal Tech Profile | Aspiring Web Developer</p>
</header>

<nav>
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#education">Education</a>
    <a href="#interest">Interest</a>
    <a href="#contact">Contact</a>
</nav>

<section id="about" class="card">
    <h2>About Me</h2>
    <p>I am Komal Singh, a B.Tech student passionate about web development and programming.</p>
    <p>I enjoy learning Java, C++, and HTML and creating creative projects.</p>
</section>

<section id="skills" class="card">
    <h2>Skills</h2>

    <div class="skill">
        <p>Java</p>
        <div class="bar"><div class="fill java"></div></div>
    </div>

    <div class="skill">
        <p>C++</p>
        <div class="bar"><div class="fill cpp"></div></div>
    </div>

    <div class="skill">
        <p>HTML</p>
        <div class="bar"><div class="fill html"></div></div>
    </div>

</section>

<section id="education" class="card">
    <h2>Education</h2>
    <p>School: C.M.A Higher Secondary School (Satna)</p>
    <p>Board: CBSE</p>
    <p>B.Tech: Oriental College of Technology (2024–2028) (Bhopal)</p>
</section>

<section id="interest" class="card">
    <h2>Interest</h2>
    <p>Stone Painting 🎨</p>
    <p>Music 🎵</p>
</section>

<section id="contact" class="card">
    <h2>Contact</h2>
    <p>Email: singhkomal0229@gmail.com</p>
    <p>Phone: 7974512140</p>
</section>

<script>
    const sections = document.querySelectorAll("section");

    window.addEventListener("scroll", () => {
        sections.forEach(sec => {
            const top = sec.getBoundingClientRect().top;
            if(top < window.innerHeight - 100){
                sec.classList.add("show");
            }
        });
    });
</script>

</body>
</html>
