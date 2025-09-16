# Raj-Earth-Movers-and-Transporters
/project-root
│── index.html
│── css/
│    └── style.css
│── js/
│    └── script.js
│── images/   (your logos, favicon, etc.)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Raj Earth Movers and Transporters</title>
  <link rel="icon" href="images/favicon.ico" type="image/x-icon" />

  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Awesome for Icons -->
  <script src="https://kit.fontawesome.com/your-fontawesome-kit.js" crossorigin="anonymous"></script>

  <!-- Custom CSS -->
  <link rel="stylesheet" href="css/style.css" />
</head>
<body class="bg-gray-50 text-gray-800">
  <!-- Navbar -->
  <header class="fixed top-0 left-0 w-full bg-white shadow flex justify-between items-center px-8 py-4 z-10">
    <div class="flex items-center gap-3">
      <img id="logo" src="images/logo-light.png" alt="Raj Earth Movers Logo" class="h-12" />
      <h1 class="text-2xl font-bold text-orange-600">RAJ EARTH MOVERS</h1>
    </div>
    <nav class="space-x-6 font-medium">
      <a href="#services" class="hover:text-orange-500">Services</a>
      <a href="#about" class="hover:text-orange-500">About</a>
      <a href="#contact" class="hover:text-orange-500">Contact</a>
      <button id="toggleMode" class="ml-4 p-2 rounded-full bg-orange-600 text-white hover:bg-orange-700">
        <i class="fas fa-moon"></i>
      </button>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="flex flex-col md:flex-row items-center justify-between px-8 pt-28 pb-20 bg-gradient-to-r from-orange-500 to-orange-700 text-white">
    <div>
      <h2 class="text-4xl md:text-5xl font-bold mb-4">
        Reliable Earth Movers & Transporters
      </h2>
      <p class="text-lg mb-6">
        Trusted services with modern equipment and skilled operators.
      </p>
      <a href="#contact" class="bg-white text-orange-600 font-semibold px-6 py-3 rounded-lg shadow hover:bg-gray-100">
        Get a Quote
      </a>
    </div>
    <img src="images/logo-light.png" alt="Truck Logo" class="w-64 mt-10 md:mt-0" />
  </section>

  <!-- Services Section -->
  <section id="services" class="px-8 py-20 bg-gray-100">
    <h3 class="text-3xl font-bold text-center mb-10">Our Services</h3>
    <div class="grid md:grid-cols-3 gap-8">
      <div class="card shadow-lg rounded-2xl bg-white p-6 text-center">
        <i class="fas fa-truck text-orange-600 text-3xl"></i>
        <h4 class="font-semibold text-xl mt-4 mb-2">Earth Movers</h4>
        <p>Heavy-duty earth movers for all types of projects.</p>
      </div>
      <div class="card shadow-lg rounded-2xl bg-white p-6 text-center">
        <i class="fas fa-truck-loading text-orange-600 text-3xl"></i>
        <h4 class="font-semibold text-xl mt-4 mb-2">Transporters</h4>
        <p>Reliable goods & material transportation services.</p>
      </div>
      <div class="card shadow-lg rounded-2xl bg-white p-6 text-center">
        <i class="fas fa-cogs text-orange-600 text-3xl"></i>
        <h4 class="font-semibold text-xl mt-4 mb-2">Equipment Rental</h4>
        <p>Modern equipment available for rental.</p>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="px-8 py-20">
    <h3 class="text-3xl font-bold text-center mb-6">About Us</h3>
    <p class="max-w-3xl mx-auto text-center text-lg">
      Raj Earth Movers and Transporters has been serving the construction and logistics industry with excellence.
      We provide high-quality services, ensure timely delivery, and supply reliable equipment to meet client needs.
    </p>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="px-8 py-20 bg-gray-100">
    <h3 class="text-3xl font-bold text-center mb-10">Contact Us</h3>
    <div class="grid md:grid-cols-2 gap-10 max-w-5xl mx-auto">
      <form class="bg-white shadow-lg rounded-2xl p-6 space-y-4">
        <input type="text" placeholder="Your Name" class="w-full border rounded-lg p-3" required />
        <input type="email" placeholder="Your Email" class="w-full border rounded-lg p-3" required />
        <textarea placeholder="Your Message" rows="4" class="w-full border rounded-lg p-3" required></textarea>
        <button type="submit" class="bg-orange-600 hover:bg-orange-700 w-full text-white px-6 py-3 rounded-lg">
          Send Message
        </button>
      </form>
      <div class="space-y-6">
        <p class="flex items-center gap-3"><i class="fas fa-phone text-orange-600"></i> +91-9876543210</p>
        <p class="flex items-center gap-3"><i class="fas fa-envelope text-orange-600"></i> info@rajearthmovers.com</p>
        <p class="flex items-center gap-3"><i class="fas fa-map-marker-alt text-orange-600"></i> Mumbai, India</p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-orange-600 text-white text-center py-4 mt-10">
    © <span id="year"></span> Raj Earth Movers and Transporters. All rights reserved.
  </footer>

  <!-- Custom JS -->
  <script src="js/script.js"></script>
</body>
</html>
html {
  scroll-behavior: smooth;
}

.dark-mode {
  background-color: #111827;
  color: #f3f4f6;
}

.dark-mode .card {
  background-color: #1f2937;
}
document.addEventListener("DOMContentLoaded", () => {
  const toggleBtn = document.getElementById("toggleMode");
  const body = document.body;
  const logo = document.getElementById("logo");

  toggleBtn.addEventListener("click", () => {
    body.classList.toggle("dark-mode");
    if (body.classList.contains("dark-mode")) {
      logo.src = "images/logo-dark.png";
      toggleBtn.innerHTML = '<i class="fas fa-sun"></i>';
    } else {
      logo.src = "images/logo-light.png";
      toggleBtn.innerHTML = '<i class="fas fa-moon"></i>';
    }
  });

  document.getElementById("year").textContent = new Date().getFullYear();
});
