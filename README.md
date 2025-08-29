<!-- Games Section -->
<section id="games" class="container mx-auto py-16 px-6">
  <h3 class="text-3xl font-semibold text-center mb-10">Available Content</h3>
  <div class="grid md:grid-cols-2 gap-6 justify-center">

    <!-- PS3 Mods Box -->
    <button onclick="openPS3Modal()" class="block bg-gray-900/70 rounded-2xl p-6 text-center shadow-lg hover:scale-105 transition">
      <h4 class="text-xl font-bold text-green-400 mb-2">PS3 Mods</h4>
      <p class="text-gray-300 mb-4">Click to view games</p>
      <span class="text-lg">👀 Look 👀</span>
    </button>

    <!-- Tools Box -->
    <button onclick="openToolsModal()" class="block bg-red-700/80 rounded-2xl p-6 text-center shadow-lg hover:scale-105 transition">
      <h4 class="text-xl font-bold text-white mb-2">Tools</h4>
      <p class="text-gray-200 mb-4">Click to view tools</p>
      <span class="text-lg">👀 Look 👀</span>
    </button>

  </div>
</section>

<!-- PS3 Modal -->
<div id="ps3Modal" class="fixed inset-0 bg-black/80 hidden items-center justify-center z-50">
  <div class="bg-gray-900 rounded-2xl p-8 max-w-lg w-full relative">
    <button onclick="closePS3Modal()" class="absolute top-3 right-3 text-gray-300 hover:text-red-500 text-2xl font-bold">&times;</button>
    <h3 class="text-2xl font-bold text-green-400 mb-6">PS3 Games</h3>
    <div class="grid gap-4">
      <div class="bg-gray-800 p-4 rounded-xl text-center hover:bg-gray-700 transition cursor-pointer">Skate 3</div>
      <div class="bg-gray-800 p-4 rounded-xl text-center hover:bg-gray-700 transition cursor-pointer">Black Ops 2</div>
      <div class="bg-gray-800 p-4 rounded-xl text-center hover:bg-gray-700 transition cursor-pointer">Black Ops 1</div>
      <div class="bg-gray-700 p-4 rounded-xl text-center text-gray-400 cursor-not-allowed">More Coming Soon...</div>
    </div>
  </div>
</div>

<!-- Tools Modal -->
<div id="toolsModal" class="fixed inset-0 bg-black/80 hidden items-center justify-center z-50">
  <div class="bg-red-800 rounded-2xl p-8 max-w-lg w-full relative">
    <button onclick="closeToolsModal()" class="absolute top-3 right-3 text-gray-100 hover:text-white text-2xl font-bold">&times;</button>
    <h3 class="text-2xl font-bold text-white mb-6">Tools</h3>
    <div class="grid gap-4">
      <div class="bg-red-700 p-4 rounded-xl text-center hover:bg-red-600 transition cursor-pointer">Tool 1</div>
      <div class="bg-red-700 p-4 rounded-xl text-center hover:bg-red-600 transition cursor-pointer">Tool 2</div>
      <div class="bg-red-700 p-4 rounded-xl text-center hover:bg-red-600 transition cursor-pointer">Tool 3</div>
      <div class="bg-red-600 p-4 rounded-xl text-center text-gray-200 cursor-not-allowed">More Coming Soon...</div>
    </div>
  </div>
</div>

<script>
  function openPS3Modal() {
    document.getElementById('ps3Modal').classList.remove('hidden');
  }
  function closePS3Modal() {
    document.getElementById('ps3Modal').classList.add('hidden');
  }

  function openToolsModal() {
    document.getElementById('toolsModal').classList.remove('hidden');
  }
  function closeToolsModal() {
    document.getElementById('toolsModal').classList.add('hidden');
  }
</script>
