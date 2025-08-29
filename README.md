<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Mods Site</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-900 text-gray-100 font-sans">
  <!-- Navbar -->
  <nav class="bg-gray-800 shadow-md p-4 sticky top-0 z-50">
    <div class="container mx-auto flex justify-between items-center">
      <h1 class="text-2xl font-bold text-indigo-400">My Mods</h1>
      <div class="space-x-4">
        <a href="#mods" class="hover:text-indigo-300">Mods</a>
        <a href="#about" class="hover:text-indigo-300">About</a>
        <a href="#contact" class="hover:text-indigo-300">Contact</a>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <header class="text-center py-16 bg-gradient-to-b from-indigo-700 to-gray-900">
    <h2 class="text-4xl font-bold mb-4">Welcome to My Mods Hub</h2>
    <p class="text-lg text-gray-300">Download my custom mods, tools, and resources.</p>
    <a href="#mods" class="mt-6 inline-block bg-indigo-500 hover:bg-indigo-600 text-white px-6 py-3 rounded-xl shadow-lg">Browse Mods</a>
  </header>

  <!-- Mods Grid -->
  <section id="mods" class="container mx-auto px-6 py-12">
    <h3 class="text-3xl font-semibold mb-8 text-center">Available Mods</h3>
    <div class="grid md:grid-cols-3 gap-8">
      <!-- Example mod card -->
      <div class="bg-gray-800 rounded-2xl shadow-lg overflow-hidden hover:scale-105 transition">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/70/Video-Game-Controller-Icon.png/512px-Video-Game-Controller-Icon.png" alt="Mod Screenshot" class="w-full h-48 object-contain bg-gray-900">
        <div class="p-4">
          <h4 class="text-xl font-bold mb-2">Cool Mod #1</h4>
          <p class="text-gray-400 text-sm mb-4">This mod adds awesome new features and improves gameplay.</p>
          <a href="#" class="bg-indigo-500 hover:bg-indigo-600 text-white px-4 py-2 rounded-lg">Download</a>
        </div>
      </div>

      <!-- Duplicate and edit this block for more mods -->
      <div class="bg-gray-800 rounded-2xl shadow-lg overflow-hidden hover:scale-105 transition">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/20/Gamepad_icon.svg/512px-Gamepad_icon.svg.png" alt="Mod Screenshot" class="w-full h-48 object-contain bg-gray-900">
        <div class="p-4">
          <h4 class="text-xl font-bold mb-2">Cool Mod #2</h4>
          <p class="text-gray-400 text-sm mb-4">Another mod description goes here.</p>
          <a href="#" class="bg-indigo-500 hover:bg-indigo-600 text-white px-4 py-2 rounded-lg">Download</a>
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="bg-gray-800 py-12 px-6 text-center">
    <h3 class="text-3xl font-semibold mb-4">About</h3>
    <p class="max-w-2xl mx-auto text-gray-300">This site is where I upload and share my mods. Everything here is free to download and use. I hope you enjoy playing with them as much as I enjoyed making them!</p>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="container mx-auto px-6 py-12 text-center">
    <h3 class="text-3xl font-semibold mb-4">Contact Me</h3>
    <p class="text-gray-300 mb-6">Got feedback or requests? Reach out!</p>
    <a href="mailto:your@email.com" class="bg-indigo-500 hover:bg-indigo-600 text-white px-6 py-3 rounded-xl">Email Me</a>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-800 text-center py-6 text-gray-400">
    <p>&copy; 2025 My Mods Site. All rights reserved.</p>
  </footer>
</body>
</html>
