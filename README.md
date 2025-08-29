<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Mods Site</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Lightning effect */
    body {
      background: radial-gradient(circle, #7fff00 2px, transparent 3px), #8b0000;
      background-size: 60px 60px;
      animation: flicker 1.5s infinite alternate;
    }
    @keyframes flicker {
      0% { background-color: #8b0000; }
      100% { background-color: #b22222; }
    }
  </style>
</head>
<body class="text-gray-100 font-sans">

  <!-- Terms of Service Overlay -->
  <div id="tosOverlay" class="fixed inset-0 bg-black/90 flex flex-col items-center justify-center z-50">
    <h2 class="text-3xl font-bold mb-6">Welcome to My Mods Hub</h2>
    <button onclick="showTerms()" class="bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-xl text-white">View Terms of Service</button>

    <div id="tosContent" class="hidden bg-gray-900 mt-8 p-6 rounded-xl max-w-lg text-left">
      <h3 class="text-2xl font-semibold mb-4 text-blue-400">Terms of Service</h3>
      <ul class="list-disc pl-6 text-gray-300 space-y-2">
        <li>Use at your own risk.</li>
        <li>For educational purposes only.</li>
        <li>No responsibility for misuse.</li>
        <li>By proceeding, you agree to these terms.</li>
      </ul>
      <button onclick="acceptTerms()" class="mt-6 bg-green-600 hover:bg-green-700 px-6 py-3 rounded-xl text-white">Accept & Enter</button>
    </div>
  </div>

  <!-- Main Site (hidden until ToS accepted) -->
  <div id="siteContent" class="hidden">
    <!-- Navbar -->
    <nav class="bg-gray-900/80 backdrop-blur shadow-md p-4 sticky top-0 z-40">
      <div class="container mx-auto flex justify-between items-center">
        <h1 class="text-2xl font-bold text-green-400">My Mods</h1>
        <div class="space-x-4">
          <button onclick="toggleMenu()" class="hover:text-green-300">Games</button>
          <a href="#about" class="hover:text-green-300">About</a>
          <a href="#contact" class="hover:text-green-300">Contact</a>
        </div>
      </div>
    </nav>

    <!-- Dropdown Menu -->
    <div id="gameMenu" class="hidden bg-gray-800 text-center p-4">
      <p class="mb-2">Select a platform:</p>
      <button class="bg-green-600 hover:bg-green-700 px-4 py-2 rounded m-1">PS3</button>
      <button disabled class="bg-gray-600 px-4 py-2 rounded m-1">More Coming Soon...</button>
    </div>

    <!-- Hero Section -->
    <header class="text-center py-20">
      <h2 class="text-5xl font-bold mb-4 text-green-400 drop-shadow-lg">Welcome to My Mods Hub</h2>
      <p class="text-lg text-gray-200">Download my custom mods, tools, and resources.</p>
      <a href="#contact" class="mt-6 inline-block bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-xl shadow-lg">Contact Me</a>
    </header>

    <!-- About Section -->
    <section id="about" class="bg-gray-900/70 py-12 px-6 text-center">
      <h3 class="text-3xl font-semibold mb-4">About</h3>
      <p class="max-w-2xl mx-auto text-gray-300">This site is where I upload and share my mods. Everything here is free to download and use. I hope you enjoy playing with them as much as I enjoyed making them!</p>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="container mx-auto px-6 py-12 text-center">
      <h3 class="text-3xl font-semibold mb-4">Contact Me</h3>
      <p class="text-gray-300 mb-6">Got feedback or requests? Reach out!</p>
      <a href="mailto:nosucrew.info@gmail.com" class="bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-xl">Email Me</a>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900/80 text-center py-6 text-gray-400">
      <p>&copy; 2025 My Mods Site. All rights reserved.</p>
    </footer>
  </div>

  <script>
    function showTerms() {
      document.getElementById('tosContent').classList.remove('hidden');
    }
    function acceptTerms() {
      document.getElementById('tosOverlay').classList.add('hidden');
      document.getElementById('siteContent').classList.remove('hidden');
    }
    function toggleMenu() {
      const menu = document.getElementById('gameMenu');
      menu.classList.toggle('hidden');
    }
  </script>
</body>
</html>
