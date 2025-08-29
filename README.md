<!DOCTYPE html>
<html lang="nl">
<head>
<meta charset="UTF-8">
<title>Skater Downloads</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background: black;
    color: white;
  }

  /* Consent Overlay */
  #consentOverlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.95);
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 9999;
  }

  #consentOverlayContent {
    max-width: 400px;
    text-align: center;
  }

  #consentOverlayContent label {
    display: block;
    margin: 15px 0;
    font-size: 16px;
    cursor: pointer;
  }

  #consentOverlayContent button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    background-color: #1e3c72;
    color: white;
  }

  h1 {
    text-align: center;
    margin-top: 20px;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 15px;
    margin: 20px;
    justify-items: center;
  }

  .box {
    position: relative;
    width: 200px;
    height: 240px;
    border-radius: 10px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 5px;
    cursor: pointer;
    animation: galaxy 12s infinite alternate ease-in-out;
  }

  .box img {
    width: 100%;
    height: 160px;
    object-fit: cover;
    border-radius: 5px;
  }

  .download-btn {
    background-color: rgba(255,255,255,0.8);
    border: none;
    border-radius: 5px;
    padding: 6px;
    font-size: 13px;
    cursor: pointer;
    text-align: center;
  }

  @keyframes galaxy {
    0% { background: linear-gradient(135deg, #1e3c72, #2a5298); }
    25% { background: linear-gradient(135deg, #1e3c72, #00ffcc); }
    50% { background: linear-gradient(135deg, #1e3c72, #ff00ff); }
    75% { background: linear-gradient(135deg, #1e3c72, #00ffff); }
    100% { background: linear-gradient(135deg, #1e3c72, #2a5298); }
  }

  .stars {
    position: absolute;
    width: 100%;
    height: 100%;
    pointer-events: none;
    background-image: radial-gradient(white 1px, transparent 1px);
    background-size: 5px 5px;
    opacity: 0.5;
  }
</style>
</head>
<body>

<!-- Consent Overlay -->
<div id="consentOverlay">
  <div id="consentOverlayContent">
    <h2>Disclaimer & Terms</h2>
    <p>Some content may be sensitive, offensive, or disturbing to some viewers.</p>
    <label>
      <input type="checkbox" id="consentCheckbox" style="margin-right:5px;">
      I have read and accept the terms
    </label>
    <button id="proceedBtn" disabled>Proceed</button>
  </div>
</div>

<h1>Skater Files Download</h1>
<div class="grid" id="grid"></div>

<script>
const checkbox = document.getElementById('consentCheckbox');
const proceedBtn = document.getElementById('proceedBtn');
const overlay = document.getElementById('consentOverlay');
const grid = document.getElementById('grid');

// Enable proceed button only if checkbox is checked
checkbox.addEventListener('change', () => {
  proceedBtn.disabled = !checkbox.checked;
});

// Hide overlay on proceed
proceedBtn.addEventListener('click', () => {
  overlay.style.display = 'none';
});

// GitHub raw image links (5 images)
const skaterImages = [
  'https://raw.githubusercontent.com/Nosucrew/skaters.github.io/main/Epic%20Swag.jpg',
  'https://raw.githubusercontent.com/Nosucrew/skaters.github.io/main/Girls%20Love%20Me.png',
  'https://raw.githubusercontent.com/Nosucrew/skaters.github.io/main/IMG-4297.jpg',
  'https://raw.githubusercontent.com/Nosucrew/skaters.github.io/main/Metallica.png',
  'https://raw.githubusercontent.com/Nosucrew/skaters.github.io/main/rainbowlikeaboss.png'
];

// Create 5 big boxes
for(let i = 0; i < skaterImages.length; i++){
  const box = document.createElement('div');
  box.className = 'box';

  const stars = document.createElement('div');
  stars.className = 'stars';
  box.appendChild(stars);

  const img = document.createElement('img');
  img.src = skaterImages[i];
  img.alt = `Skater ${i + 1}`;
  box.appendChild(img);

  const btn = document.createElement('button');
  btn.className = 'download-btn';
  btn.innerText = 'Download';
  btn.onclick = () => {
    alert(`Downloading Skater ${i + 1} file...`);
  };
  box.appendChild(btn);

  grid.appendChild(box);
}
</script>

</body>
</html>
