<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Navbar</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
    }

    .navbar {
      background-color: #333;
      overflow: hidden;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 16px;
    }

    .navbar a {
      color: white;
      text-decoration: none;
      padding: 14px 20px;
      display: block;
    }

    .navbar a:hover {
      background-color: #575757;
    }

    .navbar .logo {
      font-size: 20px;
      font-weight: bold;
    }

    .navbar-links {
      display: flex;
    }

    .toggle-button {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }

    .toggle-button div {
      width: 25px;
      height: 3px;
      background-color: white;
      margin: 4px 0;
    }

    @media (max-width: 768px) {
      .navbar-links {
        display: none;
        flex-direction: column;
        width: 100%;
      }

      .navbar-links.active {
        display: flex;
      }

      .toggle-button {
        display: flex;
      }

      .navbar {
        flex-direction: column;
        align-items: flex-start;
      }
    }
  </style>
</head>
<body>

  <nav class="navbar">
    <div class="logo">MySite</div>
    <div class="toggle-button" onclick="toggleNavbar()">
      <div></div>
      <div></div>
      <div></div>
    </div>
    <div class="navbar-links" id="navbarLinks">
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Services</a>
      <a href="#">Contact</a>
    </div>
  </nav>

  <script>
    function toggleNavbar() {
      const navbarLinks = document.getElementById('navbarLinks');
      navbarLinks.classList.toggle('active');
    }
  </script>

</body>
</html>
# Netra
