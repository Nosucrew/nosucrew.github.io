<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nosucrew's Place</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Lightning background */
    body {
      background: radial-gradient(circle, #39ff14 2px, transparent 3px), #111;
      background-size: 60px 60px;
      animation: flicker 2s infinite alternate;
    }
    @keyframes flicker {
      0% { background-color: #1a0000; }
      100% { background-color: #330000; }
    }
    html {
      scroll-behavior: smooth;
    }
  </style>
</head>
<body class="text-gray-100 font-sans">

  <!-- Terms of Service Overlay -->
  <div id="tosOverlay" class="fixed inset-0 bg-black/90 flex flex-col items-center justify-center z-50">
    <h2 class="text-4xl font-bold mb-6 text-green-400 drop-shadow-lg">Welcome to Nosucrew's Place</h2>
    <button onclick="showTerms()" class="bg-blue-600 hover:bg-blue-700 px-6 py-3 rounded-xl text-white shadow-lg transition">View Terms of Service</button>

    <div id="tosContent" class="hidden bg-gray-900 mt-8 p-6 rounded-xl max-w-lg text-left shadow-lg animate-fade-in">
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
  <div id="siteContent" class="hidden">
    <!-- Navbar -->
    <nav class="bg-gray-900/80 backdrop-blur shadow-md p-4 sticky top-0 z-40">
      <div class="container mx-auto flex justify-between items-center">
        <h1 class="text-2xl font-bold text-green-400">Nosucrew's Place</h1>
        <div class="flex items-center space-x-6">
          <a href="#games" class="hover:text-green-300 transition">Games</a>
          <a href="#about" class="hover:text-green-300 transition">About</a>
          <a href="#contact" class="hover:text-green-300 transition">Contact</a>
          <!-- YouTube link -->
          <a href="https://www.youtube.com/@Nosucrew" target="_blank" class="bg-red-600 hover:bg-red-700 px-4 py-2 rounded-xl text-white shadow-md transition">YouTube</a>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <header class="text-center py-20 bg-gradient-to-b from-gray-800/70 to-transparent">
      <h2 class="text-5xl font-bold mb-4 text-green-400 drop-shadow-lg">Welcome to Nosucrew's Place</h2>
      <p class="text-lg text-gray-200">Mods, tools, and cool resources – made by Nosucrew.</p>
      <a href="#games" class="mt-6 inline-block bg-green-600 hover:bg-green-700 text-white px-6 py-3 rounded-xl shadow-lg transition">Explore Mods</a>
    </header>

    <!-- Games Section -->
    <section id="games" class="container mx-auto py-16 px-6">
      <h3 class="text-3xl font-semibold text-center mb-10">Available Mods</h3>
      <div class="grid md:grid-cols-3 gap-8">
        
        <!-- PS3 Card -->
        <div class="bg-gray-900/70 rounded-2xl p-6 text-center shadow-lg hover:scale-105 transition">
          <h4 class="text-xl font-bold text-green-400 mb-4">PS3 Mods</h4>
          <p class="text-gray-300 mb-4">Custom mod menus and tools for PS3.</p>
          <button class="bg-green-600 hover:bg-green-700 px-4 py-2 rounded-xl text-white shadow-md">Download</button>
        </div>

        <!-- Coming Soon -->
        <div class="bg-gray-800/70 rounded-2xl p-6 text-center shadow-lg opacity-60">
          <h4 class="text-xl font-bold text-gray-400 mb-4">More Platforms</h4>
          <p class="text-gray-400 mb-4">Mods for other platforms are coming soon.</p>
          <button disabled class="bg-gray-600 px-4 py-2 rounded-xl text-white">Coming Soon</button>
        </div>

      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="bg-gray-900/70 py-16 px-6 text-center">
      <h3 class="text-3xl font-semibold mb-6">About</h3>
      <p class="max-w-2xl mx-auto text-gray-300">Hey! I'm Nosucrew 👋 This is my spot to share mods, tools, and fun stuff I've built. Everything here is free to use – I just hope you enjoy playing with them as much as I enjoyed making them!</p>
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
  </script>
</body>
</html>

