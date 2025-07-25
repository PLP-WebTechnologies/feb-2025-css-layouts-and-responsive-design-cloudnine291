index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Web Layout</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header>
    <nav class="navbar">
      <div class="logo">MySite</div>
      <ul class="nav-links">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="grid-container">
    <section class="main-content">
      <h1>Welcome</h1>
      <p>This is a responsive layout built with Flexbox and CSS Grid. Resize the window to see the layout adjust for different screen sizes.</p>
    </section>
    <aside class="sidebar">
      <h2>Sidebar</h2>
      <p>Useful links or extra info can go here.</p>
    </aside>
  </main>

  <footer>
    <p>&copy; 2025 MySite. All rights reserved.</p>
  </footer>
</body>
</html>




styles.css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background: #f4f4f4;
  color: #333;
}

header {
  background: #333;
  color: #fff;
  padding: 1rem 0;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 1rem;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links a {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #f0a500;
}

.grid-container {
  display: grid;
  grid-template-columns: 3fr 1fr;
  gap: 2rem;
  max-width: 1100px;
  margin: 2rem auto;
  padding: 0 1rem;
}

.main-content,
.sidebar {
  background: #fff;
  padding: 1.5rem;
  border-radius: 5px;
}

footer {
  text-align: center;
  padding: 1rem;
  background: #333;
  color: #fff;
  margin-top: 2rem;
}

/* Responsive Layout */

@media (max-width: 900px) {
  .grid-container {
    grid-template-columns: 1fr;
  }

  .nav-links {
    flex-direction: column;
    gap: 0.75rem;
    align-items: flex-end;
  }
}

@media (max-width: 600px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .logo {
    margin-bottom: 0.5rem;
  }

  .nav-links {
    align-items: flex-start;
  }
}

