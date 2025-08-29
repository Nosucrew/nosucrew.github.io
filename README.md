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
  background: url('https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/ChatGPT%20Image%2029%20aug%202025,%2013_23_10.png') no-repeat center center fixed;
  background-size: cover;
  color: white;
  position: relative;
}
body::after {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.3);
  z-index: -1;
}
#consentOverlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.95);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}
#consentOverlayContent {
  text-align: center;
  max-width: 400px;
  width: 100%;
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
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 10px;
  padding: 20px;
  justify-items: center;
  margin-top: 20px;
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
  background: rgba(30,60,114,0.3);
}
.box img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 5px;
}
.download-btn {
  padding: 6px;
  font-size: 13px;
  background-color: rgba(255,255,255,0.8);
  border: none;
  border-radius: 5px;
  cursor: pointer;
  text-align: center;
  text-decoration: none;
  color: black;
  display: block;
  margin-top: 5px;
}
.stars {
  position: absolute;
  width: 100%;
  height: 100%;
  pointer-events: none;
  background-image: radial-gradient(white 1px, transparent 1px);
  background-size: 5px 5px;
  opacity: 0.3;
}
</style>
</head>
<body>

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

<h1 style="text-align:center;">Skater Files Download</h1>
<div class="grid" id="grid"></div>

<script>
const checkbox = document.getElementById('consentCheckbox');
const proceedBtn = document.getElementById('proceedBtn');
const overlay = document.getElementById('consentOverlay');
const grid = document.getElementById('grid');

checkbox.addEventListener('change', () => {
  proceedBtn.disabled = !checkbox.checked;
});

proceedBtn.addEventListener('click', () => {
  overlay.style.display = 'none';
});

// First 5 images and their download links
const specialItems = [
  {img: 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/Epic%20Swag.jpg', zip: 'https://github.com/Nosucrew/nosucrew.github.io/blob/main/Epic-Swag-Red-Glow-White-Skin.rar'},
  {img: 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/Girls%20Love%20Me.png', zip: 'https://github.com/Nosucrew/nosucrew.github.io/blob/main/Girls-Love-Me-Green-Glow-Black-Skin.rar'},
  {img: 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/IMG-4297.jpg', zip: 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/ARIKA.zip'},
  {img: 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/Metallica.png', zip: 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/Metallica%20(1).zip'},
  {img: 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/rainbowlikeaboss.png', zip: 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/RainbowLikeABoss%20(2).zip'}
];

const stockImage = 'https://raw.githubusercontent.com/Nosucrew/nosucrew.github.io/main/soon.jpg';
const totalBoxes = 500;

for(let i=0; i<totalBoxes; i++){
  const box = document.createElement('div');
  box.className = 'box';

  const stars = document.createElement('div');
  stars.className = 'stars';
  box.appendChild(stars);

  const img = document.createElement('img');
  let zip = null;

  if(i < specialItems.length){
    img.src = specialItems[i].img;
    zip = specialItems[i].zip;
    img.alt = `Skater ${i+1}`;
  } else {
    img.src = stockImage;
    img.alt = `Skater ${i+1}`;
  }

  box.appendChild(img);

  const btn = document.createElement('a');
  btn.className = 'download-btn';
  if(zip){
    btn.href = zip;
    btn.target = '_blank';
    btn.innerText = 'Download';
  } else {
    btn.style.display = 'none';
  }
  box.appendChild(btn);

  grid.appendChild(box);
}
</script>

</body>
</html>
