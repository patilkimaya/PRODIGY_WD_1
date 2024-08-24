# PRODIGY_WD_1
1. RESPONSIVE LANDING PAGE
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="navbar" id="navbar">
        <ul>
            <li><a href="#home" class="nav-link">Home</a></li>
            <li><a href="#services" class="nav-link">Services</a></li>
            <li><a href="#about" class="nav-link">About</a></li>
            <li><a href="#contact" class="nav-link">Contact</a></li>
        </ul>
    </nav>

    <section id="home">
        <h1>Home Section</h1>
        <p>Content goes here...</p>
    </section>
    <section id="services">
        <h1>Services Section</h1>
        <p>Content goes here...</p>
    </section>
    <section id="about">
        <h1>About Section</h1>
        <p>Content goes here...</p>
    </section>
    <section id="contact">
        <h1>Contact Section</h1>
        <p>Content goes here...</p>
    </section>

    <script src="script.js"></script>
</body>
</html>


/* Basic Reset */
body, h1, p, ul, li {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Navigation Menu Styles */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: linear-gradient(135deg, #3498db, #8e44ad);
    padding: 10px 0;
    z-index: 1000;
    transition: background 0.3s ease;
}

.navbar ul {
    list-style-type: none;
    text-align: center;
}

.navbar li {
    display: inline;
    margin: 0 15px;
}

.navbar a {
    text-decoration: none;
    color: white;
    font-weight: bold;
    transition: color 0.3s ease;
}

/* Hover effect */
.navbar a:hover {
    color: #f39c12;
}

/* Change navbar color on scroll */
.navbar.scrolled {
    background: linear-gradient(135deg, #1abc9c, #e67e22);
}

section {
    padding: 60px 20px;
    min-height: 100vh;
}

section:nth-of-type(even) {
    background-color: #f2f2f2;
}

section:nth-of-type(odd) {
    background-color: #ffffff;
}


// Function to change navbar style on scroll
window.addEventListener('scroll', () => {
    const navbar = document.getElementById('navbar');
    if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});
