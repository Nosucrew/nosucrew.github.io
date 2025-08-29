<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nosucrew's Place</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/lucide@latest"></script>
  <style>
    /* Thunderstorm background */
    body {
      margin: 0;
      padding: 0;
      background: #0b0c10;
      overflow-x: hidden;
      position: relative;
    }

    .lightning {
      position: absolute;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: transparent;
      pointer-events: none;
      animation: thunder 4s infinite;
    }

    @keyframes thunder {
      0%, 95%, 100% { background: transparent; }
      96% { background: rgba(255,255,255,0.3); }
      97% { background: transparent; }
      98% { background: rgba(255,255,255,0.5); }
      99% { background: transparent; }
    }
  </style>
</head>
<body class="text-gray-100 font-sans relative">

  <div class="lightning"></div>

  <!-- Terms of Service Overlay -->
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
    <nav class="bg-gray-900/80 backdrop-blur shadow-md p-4 sticky top-0 z-40">
      <div class="container mx-auto flex justify-between items-center">
        <h1 class="text-2xl font-bold text-green-400 flex items-center space-x-2">
          Nosucrew's Place
          <!-- YouTube Icon -->
          <a href="https://www.youtube.com/@Nosucrew" target="_blank" class="text-red-600 hover:text-red-700 transition">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="lucide lucide-youtube"><path d="M22.54 6.42a2.8 2.8 0 0 0-1.97-1.97C18.35 4 12 4 12 4s-6.35 0-8.57.45a2.8 2.8 0 0 0-1.97 1.97A29.73 29.73 0 0 0 1 12a29.73 29.73 0 0 0 .46 5.58 2.8 2.8 0 0 0 1.97 1.97C5.65 20 12 20 12 20s6.35 0 8.57-.45a2.8 2.8 0 0 0 1.97-1.97A29.73 29.73 0 0 0 23 12a29.73 29.73 0 0 0-.46-5.58ZM10 15V9l5 3-5 3Z"></path></svg>
          </a>
        </h1>
        <div class="hidden md:flex space-x-6">
          <button onclick="toggleMenu()" class="hover:text-green-300 transition">Games</button>
          <a href="#about" class="hover:text-green-300 transition">About</a>
          <a href="#contact" class="hover:text-green-300 transition">Contact</a>
        </div>
      </div>
    </nav>

    <!-- Dropdown Modal -->
    <div id="gameMenu" class="hidden fixed inset-0 bg-black/70 backdrop-blur flex items-center justify-center z-50">
      <div class="bg-gray-900 rounded-2xl p-8 max-w-md w-full text-center space-y-4 shadow-lg">
        <h3 class="text-2xl font-bold text-green-400 mb-4">PS3 Mods</h3>
        <ul class="text-gray-300 space-y-2">
          <li>Skate 3</li>
          <li>Black Ops 2</li>
          <li>Black Ops 1</li>
          <li>More Coming Soon...</li>
        </ul>
        <button onclick="closeMenu()" class="mt-6 bg-red-600 hover:bg-red-700 px-6 py-3 rounded-xl text-white shadow-lg transition">Close</button>
      </div>
    </div>

    <!-- Hero Section -->
    <header class="text-center py-20 bg-gradient-to-b from-gray-800/70 to-transparent">
      <h2 class="text-5xl font-bold mb-4 text-green-400 drop-shadow-lg">Welcome to Nosucrew's Place</h2>
      <p class="text-lg text-gray-200">Download and explore mods, tools, and game resources shared here.</p>
      <button onclick="toggleMenu()" class="mt-6 inline-block bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-xl shadow-lg transition">Explore PS3 Mods</button>
    </header>

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

  <script>
    function showTerms() {
      document.getElementById('tosContent').classList.remove('hidden');
    }
    function acceptTerms() {
      document.getElementById('tosOverlay').classList.add('hidden');
      document.getElementById('siteContent').classList.remove('hidden');
    }
    function toggleMenu() {
      document.getElementById('gameMenu').classList.toggle('hidden');
    }
    function closeMenu() {
      document.getElementById('gameMenu').classList.add('hidden');
    }
  </script>
</body>
</html>

