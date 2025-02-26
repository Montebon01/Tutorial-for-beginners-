# Tutorial-for-beginners-
This will provide tutorial for beginners 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About Me</a>
            <a href="gallery.html">Photo Gallery</a>
            <a href="community.html">Community</a>
        </nav>
    </header>
    <section>
        <h2>My Hobby</h2>
        <p>I love photography and traveling. Here are some of my favorite shots:</p>
        <img src="images/photo1.jpg" alt="Photo 1">
        <img src="images/photo2.jpg" alt="Photo 2">
    </section>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>About Me</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About Me</a>
            <a href="gallery.html">Photo Gallery</a>
            <a href="community.html">Community</a>
        </nav>
    </header>
    <section>
        <h2>Contact Me</h2>
        <form id="contactForm">
            <label for="name">Name:</label>
            <input type="text" id="name" required>
            
            <label for="email">Email:</label>
            <input type="email" id="email" required>
            
            <label for="message">Message:</label>
            <textarea id="message" required></textarea>
            
            <button type="submit">Send</button>
        </form>
        <h3>Follow me:</h3>
        <a href="https://facebook.com" target="_blank">Facebook</a> |
        <a href="https://instagram.com" target="_blank">Instagram</a>
    </section>
    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photo Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Photo Gallery</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About Me</a>
            <a href="gallery.html">Photo Gallery</a>
            <a href="community.html">Community</a>
        </nav>
    </header>
    <section>
        <h2>My Photos</h2>
        <div class="gallery">
            <img src="images/photo3.jpg" alt="Gallery Image 1">
            <img src="images/photo4.jpg" alt="Gallery Image 2">
            <img src="images/photo5.jpg" alt="Gallery Image 3">
        </div>
    </section>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
}

header {
    background: #333;
    color: white;
    padding: 15px;
    text-align: center;
}

nav a {
    color: white;
    text-decoration: none;
    margin: 0 10px;
}

nav a:hover {
    text-decoration: underline;
}

section {
    margin: 20px;
    padding: 20px;
    background: white;
    border-radius: 5px;
}

img {
    width: 100%;
    max-width: 300px;
    margin: 10px;
}

.gallery {
    display: flex;
    flex-wrap: wrap;
}

form {
    display: flex;
    flex-direction: column;
}

input, textarea {
    margin-bottom: 10px;
    padding: 8px;
    width: 100%;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    background: #28a745;
    color: white;
    padding: 10px;
    border: none;
    cursor: pointer;
}

button:hover {
    background: #218838;
}
document.getElementById("contactForm").addEventListener("submit", function(event) {
    event.preventDefault();
    let name = document.getElementById("name").value;
    let email = document.getElementById("email").value;
    let message = document.getElementById("message").value;

    if (name && email && message) {
        alert("Thank you for your message, " + name + "!");
        this.reset();
    } else {
        alert("Please fill out all fields.");
    }
});
