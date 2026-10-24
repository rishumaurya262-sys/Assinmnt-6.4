# Assignment 6.4 — Positioning Practice

## File 1: `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Positioning Practice</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <nav class="navbar">
        <h2>My Website</h2>
        <div>
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#services">Services</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>

    <section id="home" class="section">
        <h1>Welcome to My Website</h1>
        <p>This webpage demonstrates CSS positioning properties.</p>

        <div class="card">
            <span class="badge">New</span>
            <h2>Featured Card</h2>
            <p>This badge is positioned absolutely inside its relative parent card.</p>
        </div>
    </section>

    <section id="about" class="section">
        <h1>About Us</h1>
        <p>We create simple and useful web pages using HTML and CSS.</p>
    </section>

    <section id="services" class="section">
        <h1>Our Services</h1>
        <p>We provide web design, layout development, and styling practice.</p>
    </section>

    <section id="contact" class="section">
        <h1>Contact Us</h1>
        <p>Use the floating Help button for assistance.</p>
    </section>

    <a href="#contact" class="floating-button">Help</a>

</body>
</html>
```

## File 2: `style.css`

```css
* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 90px;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    color: #1e293b;
    background-color: #f1f5f9;
}

.navbar {
    position: sticky;
    top: 0;
    z-index: 1000;
    background-color: #1e3a8a;
    color: white;
    padding: 15px 25px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}

.navbar h2 {
    margin: 0;
}

.navbar a {
    color: white;
    text-decoration: none;
    margin-left: 15px;
}

.navbar a:hover {
    color: #bfdbfe;
}

.section {
    min-height: 100vh;
    padding: 50px 25px;
    text-align: center;
}

.section h1 {
    color: #1d4ed8;
}

.card {
    position: relative;
    max-width: 350px;
    margin: 40px auto;
    padding: 35px 20px;
    background-color: white;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.badge {
    position: absolute;
    top: 10px;
    right: 10px;
    z-index: 2;
    background-color: #dc2626;
    color: white;
    padding: 5px 12px;
    border-radius: 15px;
    font-size: 12px;
}

.floating-button {
    position: fixed;
    right: 20px;
    bottom: 20px;
    z-index: 1100;
    background-color: #16a34a;
    color: white;
    text-decoration: none;
    padding: 15px 20px;
    border-radius: 50px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.floating-button:hover {
    background-color: #15803d;
}

@media (max-width: 600px) {
    .navbar {
        gap: 10px;
    }

    .navbar a {
        margin-left: 0;
        margin-right: 10px;
    }

    .section {
        padding: 35px 15px;
    }
}
```

## Explanation

1. `position: sticky` keeps the navigation bar at the top while scrolling.
2. `position: fixed` keeps the Help button at the bottom-right of the screen.
3. `position: absolute` places the badge inside the card.
4. `position: relative` makes the card the positioning parent for the badge.
5. `z-index` controls the stacking order of the navbar, badge, and floating button.
6.