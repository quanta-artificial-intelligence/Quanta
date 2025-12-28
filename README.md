<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Quanta</title>

<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">

<style>
/* === RESET === */
* {
    box-sizing: border-box;
}

/* === BACKGROUND GLOBAL === */
html, body {
    margin: 0;
    padding: 0;
    font-family: 'Roboto', sans-serif;

    background-image:
        linear-gradient(rgba(20, 10, 40, 0.75), rgba(20, 10, 40, 0.75)),
        url("https://images.unsplash.com/photo-1725654730257-236397b73557?fm=jpg&q=60&w=3000&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1yZWxhdGVkfDl8fHxlbnwwfHx8fHw=");

    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;

    color: white;
    overflow-x: hidden;
    scroll-behavior: smooth;
}

/* === INTRO FULLSCREEN === */
.intro {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.intro h1 {
    font-size: 70px;
    margin-bottom: 30px;
}

/* NAV DANS INTRO */
.intro-nav a {
    background: #ffdd57;
    color: #333;
    padding: 12px 24px;
    border-radius: 5px;
    font-size: 20px;
    text-decoration: none;
    margin: 0 10px;
    display: inline-block;
    transition: background 0.3s, transform 0.3s;
}

.intro-nav a:hover {
    background: #ffc107;
    transform: scale(1.08);
}

/* === HERO === */
.hero {
    padding: 120px 20px;
    text-align: center;
}

.hero h1 {
    font-size: 45px;
}

.hero p {
    font-size: 25px;
}

.btn {
    background: #ffdd57;
    padding: 12px 24px;
    border-radius: 5px;
    border: none;
    font-size: 20px;
    cursor: pointer;
}

.btn a {
    color: #333;
    text-decoration: none;
}

.btn:hover {
    transform: scale(1.08);
}

/* === FEATURES === */
.features {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 80px 20px;
}

.feature {
    background: linear-gradient(to right, #8a4abb, white, #8a4abb);
    color: black;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    margin: 20px;
    padding: 30px;
    flex: 0 1 calc(30% - 40px);
    text-align: center;
}

/* === FOOTER === */
footer {
    padding: 30px;
    text-align: center;
}

/* === REVEAL ON SCROLL === */
.reveal {
    opacity: 0;
    transform: translateY(40px);
    filter: blur(2px);
    transition: all 0.6s cubic-bezier(0.22,1,0.36,1);
}

.reveal.active {
    opacity: 1;
    transform: translateY(0);
    filter: blur(0);
}

/* === GRADIENT TEXT === */
.rainbow {
    background: linear-gradient(to right, #c77dff, white, #c77dff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.rainbow2 {
    background: linear-gradient(to right, white, #c77dff, white);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* === RESPONSIVE === */
@media (max-width: 768px) {
    .intro h1 {
        font-size: 45px;
    }
    .feature {
        flex: 0 1 calc(45% - 40px);
    }
}

@media (max-width: 480px) {
    .feature {
        flex: 0 1 100%;
    }
    .intro-nav a {
        display: block;
        margin: 10px 0;
    }
}
</style>
</head>

<body>

<!-- INTRO -->
<section class="intro">
    <h1 class="reveal active">
        Quanta <span class="rainbow">Programmation</span>
    </h1>

    <div class="intro-nav reveal active">
        <a href="#features">Fonctionnalités</a>
        <a href="#contact">Contact</a>
    </div>
</section>

<!-- HERO -->
<section class="hero reveal">
    <h1>Bienvenue dans l'univers de <span class="rainbow2">Quanta</span></h1>
    <p>Une application qui révolutionne votre manière de coder.</p>
    <button class="btn">
        <a href="https://quanta-a602a5ca.base44.app/dashboard">Découvrir l'application 🚀</a>
    </button>
</section>

<!-- FEATURES -->
<section id="features" class="features">
    <div class="feature reveal">
        <h3>Facilité d'utilisation</h3>
        <p>Une interface intuitive pour tous les utilisateurs.</p>
    </div>
    <div class="feature reveal">
        <h3>Performance</h3>
        <p>Une expérience fluide et rapide.</p>
    </div>
    <div class="feature reveal">
        <h3>Accessibilité</h3>
        <p>Disponible sur toutes vos plateformes.</p>
    </div>
</section>

<!-- FOOTER -->
<footer id="contact" class="reveal">
    <p>&copy; 2025 Quanta. Tous droits réservés.</p>
</footer>

<script>
function revealOnScroll() {
    const reveals = document.querySelectorAll('.reveal');
    const windowHeight = window.innerHeight;

    reveals.forEach((el, index) => {
        const top = el.getBoundingClientRect().top;
        if (top < windowHeight - 100) {
            setTimeout(() => {
                el.classList.add('active');
            }, index * 120);
        }
    });
}

window.addEventListener('scroll', revealOnScroll);
window.addEventListener('load', revealOnScroll);
</script>

</body>
</html>
