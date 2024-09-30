<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>al1ghxtt.studio</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    <section class="hero">
        <h1>al1ghxtt</h1>
        <p>Editor & Motion Graphic Designer</p>
        <button>Explore Portfolio</button>
    </section>
    <section id="portfolio" class="portfolio">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <!-- Project thumbnails will be generated dynamically -->
        </div>
    </section>
    <section id="about" class="about">
        <h2>About</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </section>
    <section id="contact" class="contact">
        <h2>Contact</h2>
        <form>
            <input type="text" placeholder="Name">
            <input type="email" placeholder="Email">
            <textarea placeholder="Message"></textarea>
            <button>Send</button>
        </form>
    </section>
    <script src="script.js"></script>
</
```
[30/09, 12:11 pm] Meta AI: Converting the design concept into a real website requires writing HTML, CSS, and JavaScript code. Here's a basic implementation to get you started:


*HTML (index.html)*
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>al1ghxtt.studio</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    <section class="hero">
        <h1>al1ghxtt</h1>
        <p>Editor & Motion Graphic Designer</p>
        <button>Explore Portfolio</button>
    </section>
    <section id="portfolio" class="portfolio">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <!-- Project thumbnails will be generated dynamically -->
        </div>
    </section>
    <section id="about" class="about">
        <h2>About</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </section>
    <section id="contact" class="contact">
        <h2>Contact</h2>
        <form>
            <input type="text" placeholder="Name">
            <input type="email" placeholder="Email">
            <textarea placeholder="Message"></textarea>
            <button>Send</button>
        </form>
    </section>
    <script src="script.js"></script>
</body>
</html>
```


*CSS (styles.css)*
```
body {
    font-family: Montserrat, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #212121;
    color: #fff;
    padding: 1em;
    text-align: center;
}

.hero {
    background-image: linear-gradient(to bottom, #03A9F4, #FFC107);
    background-size: 100% 300px;
    background-position: 0% 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
}

.portfolio {
    padding: 2em;
}

.project-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1em;
}

.project-thumbnail {
    background-size: cover;
    background-position: center;
    height: 150px;
    transition: transform 0.3s ease;
}

.project-thumbnail:hover {
    transform: scale(1.1);
}

.about, .contact {
    padding: 2em;
}

.contact form {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.contact input, .contact textarea {
    width: 100%;
    padding: 1em;
    margin-bottom: 1em;
    border: none;
    border-radius: 0.5em;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
```


*JavaScript (script.js)*
```
// Generate project thumbnails dynamically
const projectThumbnails = [
    {
        title: "Epic Trailer",
        image: "epic-trailer.jpg",
        link: "#"
    },
    {
        title: "Motion Graphics Reel",
        image: "motion-graphics-reel.jpg",
        link: "#"
    },
    // Add more projects here...
];

const projectGrid = document.querySelector(".project-grid");

projectThumbnails.forEach((project) => {
    const thumbnail = document.createElement("div");
    thumbnail.classList.add("project-thumbnail");
    thumbnail.style.backgroundImage = `url(${project.image})`;
    thumbnail.innerHTML = `
        <h3>${project.title}</h3>
        <a href="${project.link}">View Project</a>
    `;
    projectGrid.appendChild(thumbnail);
});
