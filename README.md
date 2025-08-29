<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nosucrew's Place</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #0b0c10;
      overflow-x: hidden;
      font-family: sans-serif;
      color: #f0f0f0;
      position: relative;
    }

    /* Falling lightning */
    .bolt {
      position: absolute;
      width: 2px;
      height: 20px;
      background: white;
      opacity: 0.8;
      top: -20px;
      animation: fall linear forwards;
    }

    @keyframes fall {
      to {
        top: 100%;
        transform: scaleY(0.1);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <div id="tosOverlay" class="fixed inset-0 bg-black/90 flex flex-col items-center justify-center z-50">
    <h2 class="text-4xl font-bold mb-6 text-green-400 drop-shadow-lg">Welcome to Nosucrew's Place</h2>
    <button onclick="showTerms()" class="bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-xl text-white shadow-lg transition">View Terms of Service</button>

    <div id="tosContent" class="hidden bg-gray-900 mt-8 p-6 rounded-xl max-w-lg text-left shadow-lg">
      <h3 class="text-2xl font-semibold mb-4 text-blue-400">Terms of Service</h3>
      <ul class="list-disc pl-6 text-gray-300 space-y-2">
        <li>Use at your own risk.</li>
        <li>For educational purposes only.</li>
        <li>No responsibility for misuse.</li>
        <li>By proceeding, you agree to these terms.</li>
      </ul>
      <button onclick="acceptTerms()" class="mt-6 bg-green-600 hover:bg-green-700 px-6 py-3 rounded-xl text-white shadow-lg transition">Accept & Enter</button>
    </div>
  </div>

  <!-- Main Site -->
  <div id="siteContent" class="hidden relative z-10">

    <!-- Navbar -->
    <nav class="bg-gray-900/80 backdrop-blur shadow-md p-4 sticky top-0 z-40 flex justify-between items-center">
      <h1 class="text-2xl font-bold text-green-400 flex items-center space-x-2">
        Nosucrew's Place
        <a href="https://www.youtube.com/@Nosucrew" target="_blank" class="text-red-600 hover:text-red-700 transition">
          👁️‍🗨️
        </a>
      </h1>
      <div class="hidden md:flex space-x-6">
        <a href="#games" class="hover:text-green-300 transition">Games</a>
        <a href="#about" class="hover:text-green-300 transition">About</a>
        <a href="#contact" class="hover:text-green-300 transition">Contact</a>
      </div>
    </nav>

    <!-- Hero Section -->
    <header class="text-center py-20 bg-gradient-to-b from-gray-800/70 to-transparent">
      <h2 class="text-5xl font-bold mb-4 text-green-400 drop-shadow-lg">Welcome to Nosucrew's Place</h2>
      <p class="text-lg text-gray-200">Explore mods, tools, and resources for games.</p>
    </header>

    <!-- Games Section -->
    <section id="games" class="container mx-auto py-16 px-6">
      <h3 class="text-3xl font-semibold text-center mb-10">Available Content</h3>
      <div class="grid md:grid-cols-2 gap-6 justify-center">

        <!-- PS3 Mods Box -->
        <a href="ps3.html" class="block bg-gray-900/70 rounded-2xl p-6 text-center shadow-lg hover:scale-105 transition">
          <h4 class="text-xl font-bold text-green-400 mb-2">PS3 Mods</h4>
          <p class="text-gray-300 mb-4">Click to view games</p>
          <span class="text-lg">👀 Look 👀</span>
        </a>

        <!-- Tools Box -->
        <a href="tools.html" class="block bg-red-700/80 rounded-2xl p-6 text-center shadow-lg hover:scale-105 transition">
          <h4 class="text-xl font-bold text-white mb-2">Tools</h4>
          <p class="text-gray-200 mb-4">Click to view tools</p>
          <span class="text-lg">👀 Look 👀</span>
        </a>

      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="bg-gray-900/70 py-16 px-6 text-center">
      <h3 class="text-3xl font-semibold mb-6">About</h3>
      <p class="max-w-2xl mx-auto text-gray-300">
        Hey! I'm Nosucrew 👋 This is my place to share mods, tools, and resources for games. Everything here is free to use – enjoy exploring and playing with them!
      </p>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="container mx-auto px-6 py-16 text-center">
      <h3 class="text-3xl font-semibold mb-6">Contact Me</h3>
      <p class="text-gray-300 mb-6">Got feedback or requests? Reach out!</p>
      <a href="mailto:nosucrew.info@gmail.com" class="bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-xl shadow-lg transition">Email Me</a>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900/80 text-center py-6 text-gray-400">
      <p>&copy; 2025 Nosucrew's Place. All rights reserved.</p>
    </footer>

  </div>

  <!-- Lightning JS -->
  <script>
    function spawnBolt() {
      const bolt = document.createElement('div');
      bolt.classList.add('bolt');
      bolt.style.left = Math.random() * window.innerWidth + 'px';
      bolt.style.height = 20 + Math.random() * 30 + 'px';
      bolt.style.animationDuration = (1 + Math.random()*1.5) + 's';
      document.body.appendChild(bolt);
      bolt.addEventListener('animationend', () => bolt.remove());
    }

    setInterval(spawnBolt, 300); // spawn bolts every 0.3s

    function showTerms() {
      document.getElementById('tosContent').classList.remove('hidden');
    }
    function acceptTerms() {
      document.getElementById('tosOverlay').classList.add('hidden');
      document.getElementById('siteContent').classList.remove('hidden');
    }
  </script>

</body>
</html>
