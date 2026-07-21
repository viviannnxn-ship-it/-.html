html_content = '''<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday P’Kao ✨</title>
  <link href="https://fonts.googleapis.com/css2?family=Mitr:wght@300;400;500;600&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      font-family: 'Mitr', sans-serif;
      user-select: none;
      -webkit-tap-highlight-color: transparent;
    }

    body {
      margin: 0;
      padding: 0;
      background-color: #f7eedd;
      background-image: radial-gradient(#e4d1f9 1.5px, transparent 1.5px), radial-gradient(#fcd5ce 1.5px, #f7eedd 1.5px);
      background-size: 60px 60px;
      background-position: 0 0, 30px 30px;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      color: #6c5ce7;
      overflow-x: hidden;
    }

    .container {
      width: 90%;
      max-width: 430px;
      background: rgba(255, 255, 255, 0.88);
      backdrop-filter: blur(12px);
      border-radius: 35px;
      padding: 30px 22px;
      box-shadow: 0 15px 35px rgba(184, 169, 202, 0.25);
      border: 3px solid #ffffff;
      text-align: center;
      position: relative;
      transition: all 0.5s ease;
    }

    .screen {
      display: none;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      animation: fadeIn 0.4s ease-in-out;
    }

    .screen.active {
      display: flex;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(12px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h2 {
      color: #6c5ce7;
      font-size: 1.35rem;
      margin-bottom: 15px;
      font-weight: 500;
    }

    .meme-img {
      width: 120px;
      height: 120px;
      object-fit: cover;
      border-radius: 22px;
      margin-bottom: 15px;
      border: 3px solid #fcd5ce;
      box-shadow: 0 6px 15px rgba(0,0,0,0.06);
    }

    .pin-input {
      width: 80%;
      padding: 12px;
      border: 2px solid #e4d1f9;
      border-radius: 18px;
      text-align: center;
      font-size: 1.3rem;
      letter-spacing: 6px;
      outline: none;
      color: #6c5ce7;
      background: #fff;
      margin-bottom: 12px;
      box-shadow: inset 0 2px 4px rgba(0,0,0,0.03);
    }

    .btn {
      background: #fcd5ce;
      color: #5d4037;
      border: none;
      padding: 12px 20px;
      border-radius: 22px;
      font-size: 1rem;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.2s ease;
      margin: 6px 0;
      box-shadow: 0 4px 12px rgba(252, 213, 206, 0.4);
      width: 100%;
      max-width: 260px;
    }

    .btn:hover, .btn:active {
      background: #f8edeb;
      transform: translateY(-2px);
      box-shadow: 0 6px 16px rgba(252, 213, 206, 0.6);
    }

    .toast-msg {
      color: #e63946;
      font-size: 0.92rem;
      min-height: 26px;
      margin-top: 6px;
      font-weight: 400;
    }

    .interactive-item {
      font-size: 80px;
      cursor: pointer;
      transition: transform 0.25s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      margin: 15px 0;
    }

    .interactive-item:active {
      transform: scale(0.92);
    }

    .cake-container {
      width: 220px;
      height: 200px;
      cursor: pointer;
      margin: 10px 0;
      position: relative;
      transition: transform 0.2s ease;
    }

    .cake-container:active {
      transform: scale(0.96);
    }

    .candle-flame {
      animation: flicker 0.6s infinite alternate ease-in-out;
      transform-origin: center bottom;
    }

    @keyframes flicker {
      0% { transform: scale(1) rotate(-2deg); opacity: 0.95; }
      100% { transform: scale(1.15) rotate(2deg); opacity: 1; }
    }

    .polaroid-frame {
      background: white;
      padding: 12px 12px 35px 12px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.08);
      border-radius: 6px;
      margin: 10px 0;
      width: 190px;
      position: relative;
      border: 1px solid #f1f2f6;
      animation: popIn 0.5s ease-out;
    }

    @keyframes popIn {
      0% { opacity: 0; transform: scale(0.8) translateY(20px); }
      100% { opacity: 1; transform: scale(1) translateY(0); }
    }

    .polaroid-frame img {
      width: 100%;
      height: 145px;
      object-fit: cover;
      border-radius: 4px;
    }

    .sticker {
      position: absolute;
      font-size: 22px;
    }

    .letter-box {
      background: #fffdf9;
      border: 2px dashed #fcd5ce;
      border-radius: 20px;
      padding: 18px;
      margin-top: 15px;
      font-size: 0.92rem;
      line-height: 1.7;
      color: #555;
      text-align: left;
      display: none;
      max-height: 210px;
      overflow-y: auto;
      box-shadow: 0 4px 15px rgba(0,0,0,0.03);
    }

    .dreamcore-bg {
      background: #11052C !important;
      border-color: #d6a419 !important;
      box-shadow: 0 0 40px rgba(180, 100, 255, 0.4) !important;
      overflow: hidden;
    }

    .time-tunnel {
      position: relative;
      width: 220px;
      height: 220px;
      margin: 15px 0;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .vortex-ring {
      position: absolute;
      border-radius: 50%;
      border: 2px dashed rgba(255, 255, 255, 0.4);
      animation: rotateVortex 10s linear infinite;
    }

    .vortex-ring:nth-child(1) {
      width: 210px;
      height: 210px;
      border-color: #fcd5ce;
      animation-duration: 8s;
    }

    .vortex-ring:nth-child(2) {
      width: 160px;
      height: 160px;
      border-color: #e4d1f9;
      animation-duration: 6s;
      animation-direction: reverse;
    }

    .vortex-ring:nth-child(3) {
      width: 110px;
      height: 110px;
      border-color: #a8edea;
      animation-duration: 4s;
    }

    .vortex-center {
      width: 60px;
      height: 60px;
      background: radial-gradient(circle, #fff 0%, #d8b4fe 70%, #11052C 100%);
      border-radius: 50%;
      box-shadow: 0 0 30px #e4d1f9;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 28px;
      animation: pulseVortex 2s ease-in-out infinite alternate;
    }

    @keyframes rotateVortex {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    @keyframes pulseVortex {
      0% { transform: scale(0.9); box-shadow: 0 0 15px #e4d1f9; }
      100% { transform: scale(1.15); box-shadow: 0 0 35px #a8edea; }
    }

    .floating-time-icons {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }

    .time-icon {
      position: absolute;
      font-size: 20px;
      animation: floatAround 5s ease-in-out infinite alternate;
    }

    @keyframes floatAround {
      0% { transform: translate(0, 0) rotate(0deg); }
      100% { transform: translate(15px, -15px) rotate(20deg); }
    }

    .balloon-container {
      position: relative;
      height: 250px;
      width: 100%;
      overflow: hidden;
      border-radius: 22px;
      background: rgba(255,255,255,0.6);
      margin: 12px 0;
      border: 1px solid #e4d1f9;
    }

    .balloon {
      position: absolute;
      width: 42px;
      height: 52px;
      border-radius: 50% 50% 50% 50% / 40% 40% 60% 60%;
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 12px;
      animation: floatUp 6.5s linear infinite;
      box-shadow: inset -4px -4px 10px rgba(0,0,0,0.08);
      transition: transform 0.1s;
    }

    @keyframes floatUp {
      0% { bottom: -60px; }
      100% { bottom: 270px; }
    }
  </style>
</head>
<body>

<div class="container" id="mainContainer">

  <div class="screen active" id="screenPin">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHp1a3Fqbm42ZmRsdWZ3YzFqZms0eGRyeXdqM3YwZzBhOHJibDFiZCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Cmr1OMJ2FN0B2/giphy.gif" class="meme-img" alt="meme">
    <h2>ใส่รหัส PIN เพื่อเข้าสู่งาน ✨</h2>
    <input type="password" maxlength="6" id="pinInput" class="pin-input" placeholder="••••••">
    <button class="btn" onclick="checkPin()">ยืนยัน</button>
    <div class="toast-msg" id="pinMsg"></div>
  </div>

  <div class="screen" id="screenQ1">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMnRybjl0cGZhd3ZwOHptMzB2MW41dWRmdXZ4bnEzMGQ5N3EwcDFjdyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/MDJ9IbxxvDUQM/giphy.gif" class="meme-img" alt="meme">
    <h2>“วันนี้วันที่เท่าไร” 🤔</h2>
    <button class="btn" onclick="checkQ1(22)">22</button>
    <button class="btn" onclick="checkQ1(21)">21</button>
    <button class="btn" onclick="checkQ1(0)">ไม่รู้อะ</button>
    <div class="toast-msg" id="q1Msg"></div>
  </div>

  <div class="screen" id="screenQ2">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbnFlOXJmdG5reWlsbW5hcm9sbDVmbW81ZWR6M2UxbzBicnQ3OTh1eiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/mlvseq9yvZhba/giphy.gif" class="meme-img" alt="meme">
    <h2>“แล้ววันนี้คือวันอะไรเอ่ยย” 💖</h2>
    <button class="btn" onclick="checkQ2(1)">ไม่รู้จำไม่ได้</button>
    <button class="btn" onclick="checkQ2(2)">วันอังคาร</button>
    <button class="btn" onclick="checkQ2(3)">วันเกิดไง</button>
    <div class="toast-msg" id="q2Msg"></div>
  </div>

  <div class="screen" id="screenGift">
    <h2>แกะของขวัญกันหน่อยย 🎁</h2>
    <div class="interactive-item" id="giftBox" onclick="clickGift()">🎁</div>
    <div style="font-size: 1.05rem; color: #7d639b;" id="giftText">แตะที่กล่องเพื่อเปิด!</div>
  </div>

  <div class="screen" id="screenCake">
    <h2>“เรามาอธิษฐานแล้วทานเค้กกันเถอะ” 🕯️✨</h2>
    
    <div class="cake-container" onclick="eatCakeSVG()">
      <svg width="220" height="200" viewBox="0 0 220 200" id="cakeSvg">
        <defs>
          <mask id="cakeBiteMask">
            <rect x="0" y="0" width="220" height="200" fill="white" />
            <circle id="bite1" cx="170" cy="90" r="28" fill="black" opacity="0" />
            <circle id="bite2" cx="50" cy="115" r="32" fill="black" opacity="0" />
            <circle id="bite3" cx="110" cy="130" r="55" fill="black" opacity="0" />
          </mask>
        </defs>

        <ellipse cx="110" cy="175" rx="95" ry="20" fill="#E2E8F0" stroke="#CBD5E1" stroke-width="3"/>
        <ellipse cx="110" cy="172" rx="85" ry="16" fill="#FFFFFF"/>

        <g mask="url(#cakeBiteMask)">
          <path d="M 35 110 Q 110 135 185 110 L 185 160 Q 110 185 35 160 Z" fill="#FDE2E4" stroke="#FB6F92" stroke-width="2"/>
          <path d="M 35 135 Q 110 155 185 135 L 185 142 Q 110 162 35 142 Z" fill="#FFB5A7"/>
          <ellipse cx="110" cy="110" rx="75" ry="25" fill="#FFF0F5" stroke="#FB6F92" stroke-width="2"/>
          <path d="M 35 110 Q 50 130 60 115 Q 75 135 90 118 Q 110 138 125 116 Q 145 135 160 115 Q 175 130 185 110 Q 110 135 35 110 Z" fill="#FF8FA3"/>
          <circle cx="80" cy="102" r="8" fill="#FF4D6D"/>
          <circle cx="110" cy="98" r="9" fill="#FF4D6D"/>
          <circle cx="140" cy="102" r="8" fill="#FF4D6D"/>
        </g>

        <g id="candleGroup">
          <rect x="106" y="65" width="8" height="30" rx="3" fill="#A8E6CF" stroke="#56AB91" stroke-width="1.5"/>
          <line x1="110" y1="65" x2="110" y2="58" stroke="#333" stroke-width="2"/>
          <g id="flame" class="candle-flame">
            <path d="M 110 40 Q 118 50 110 58 Q 102 50 110 40 Z" fill="#FFD166"/>
            <path d="M 110 45 Q 114 51 110 56 Q 106 51 110 45 Z" fill="#EF476F"/>
          </g>
        </g>

        <g id="crumbsGroup" opacity="0">
          <circle cx="185" cy="100" r="3" fill="#FF8FA3"/>
          <circle cx="192" cy="115" r="2" fill="#FDE2E4"/>
          <circle cx="40" cy="125" r="3.5" fill="#FF8FA3"/>
          <circle cx="32" cy="135" r="2" fill="#FDE2E4"/>
        </g>
      </svg>
    </div>

    <div style="font-size: 1.05rem; color: #7d639b; font-weight: 500;" id="cakeText">แตะที่เค้กเพื่อกิน (3 คำ) 😋</div>
  </div>

  <div class="screen" id="screenMenu">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaTJjcHRybTVwcnl2a3BxcWRudTdhbzR4cnBhbHpxNGp0aWpmbnkwaCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/GeimqsH0TLDt4tScGw/giphy.gif" class="meme-img" style="width: 95px; height: 95px;">
    <h2>เลือกกิจกรรมได้เลยเจ้าซ่า 🎈</h2>
    <button class="btn" onclick="goTo('screenPhoto')">📷 ห้องถ่ายรูป</button>
    <button class="btn" onclick="goTo('screenBalloon'); startBalloonGame();">🎈 ลูกโป่งเสี่ยงทาย</button>
    <button class="btn" onclick="goTo('screenTime')">⌛️ ห้องย้อนเวลา</button>
  </div>

  <div class="screen" id="screenPhoto">
    <h2>📷 Polaroid Camera</h2>
    <p style="font-size: 0.85rem; color: #777; margin-bottom: 10px;">เลือกอัปโหลด 3 รูปเพื่อเข้ากรอบรูปสวยๆ</p>
    <input type="file" id="fileInput" multiple accept="image/*" style="display:none" onchange="handleFiles(this.files)">
    <button class="btn" onclick="document.getElementById('fileInput').click()">📁 เลือก 3 รูปภาพ</button>
    
    <div id="countdown" style="font-size: 1.6rem; font-weight: 600; margin: 8px; color: #e63946;"></div>

    <div id="photoArea" style="display:none; flex-direction: column; align-items: center; width: 100%;">
      <button class="btn" style="background:#b8e994; color: #2b580c;" onclick="triggerCamera()">📸 กดถ่ายรูป!</button>
    </div>

    <div id="polaroidDisplay" style="display:flex; flex-direction:column; align-items:center;"></div>

    <div class="letter-box" id="letterBox">
      <b>💌 Happy birthday to P’Kao</b><br><br>
      <span id="typedLetter"></span>
    </div>

    <button class="btn" id="btnBackPhoto" style="display:none; margin-top:15px;" onclick="goTo('screenMenu')">🏠 กลับหน้ากิจกรรม</button>
  </div>

  <div class="screen" id="screenBalloon">
    <h2>🎈 จิ้มลูกโป่งหาคำอวยพร!</h2>
    <div class="toast-msg" id="balloonMsg">หาให้เจอครบ 4 พรนะ!</div>
    <div class="balloon-container" id="balloonBox"></div>
    <button class="btn" id="btnBackBalloon" style="display:none;" onclick="goTo('screenMenu')">🏠 กลับหน้ากิจกรรม</button>
  </div>

  <div class="screen" id="screenTime">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNmhwb3E2bWRyYTY3ZWN5YzE4ZzFsdXNsbHJjc3BwdmVxbTFndnU3MyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/bC9czlgCMM4cjOHKxt/giphy.gif" class="meme-img" alt="meme">
    <h2>ชอบหรือเปล่า ❓❓</h2>
    <button class="btn" onclick="checkQTime(1)">ชอบ</button>
    <button class="btn" onclick="checkQTime(2)">ไม่ชอบ</button>
    <div class="toast-msg" id="timeMsg"></div>
  </div>

  <div class="screen" id="screenDreamcore">
    <h2 style="color: #fcd5ce; text-shadow: 0 0 12px rgba(252, 213, 206, 0.6); margin-bottom: 5px;">⌛️ ห้วงเวลาแห่งความทรงจำ... 🌀</h2>
    <p style="color: #e4d1f9; font-size: 0.85rem; margin-bottom: 10px;">Time Travel Vortex</p>

    <div class="time-tunnel">
      <div class="vortex-ring"></div>
      <div class="vortex-ring"></div>
      <div class="vortex-ring"></div>
      <div class="vortex-center">⏳</div>
      <div class="floating-time-icons">
        <span class="time-icon" style="top: 10%; left: 15%;">✨</span>
        <span class="time-icon" style="top: 20%; right: 15%;">🕰️</span>
        <span class="time-icon" style="bottom: 15%; left: 20%;">⭐</span>
        <span class="time-icon" style="bottom: 20%; right: 20%;">💫</span>
      </div>
    </div>

    <button class="btn" style="background:#fff; color:#333; font-weight: 600; margin-top: 15px;" onclick="resetAll()">🌀 ย้อนเวลากลับไปหน้า PIN</button>
  </div>

</div>

<script>
  function goTo(screenId) {
    document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
    document.getElementById(screenId).classList.add('active');
    
    const container = document.getElementById('mainContainer');
    if(screenId === 'screenDreamcore') {
      container.classList.add('dreamcore-bg');
    } else {
      container.classList.remove('dreamcore-bg');
    }
  }

  function checkPin() {
    const pin = document.getElementById('pinInput').value;
    const msg = document.getElementById('pinMsg');
    if (pin === '210744') {
      msg.innerText = '';
      goTo('screenQ1');
    } else {
      msg.innerText = 'ใกล้แล้วลองใหม่นะคะ 🥺';
    }
  }

  function checkQ1(ans) {
    const msg = document.getElementById('q1Msg');
    if (ans === 21) {
      msg.innerText = '';
      goTo('screenQ2');
    } else {
      msg.innerText = 'อาจจะยังน้าา 🤪';
    }
  }

  function checkQ2(ans) {
    const msg = document.getElementById('q2Msg');
    if (ans === 3) {
      msg.innerText = '';
      goTo('screenGift');
    } else if (ans === 1) {
      msg.innerText = 'ผิดนะค้าบบ 😜';
    } else if (ans === 2) {
      msg.innerText = 'เดี๋ยวตีมือ ตอบใหม่เลย ✋💥';
    }
  }

  let giftClicks = 0;
  function clickGift() {
    giftClicks++;
    const text = document.getElementById('giftText');
    const box = document.getElementById('giftBox');
    
    if (giftClicks === 1) {
      text.innerText = 'กดอีกสิ 🥺';
      box.style.transform = 'scale(1.2) rotate(-5deg)';
    } else if (giftClicks === 2) {
      text.innerText = 'ใกล้แล้วว ✨';
      box.style.transform = 'scale(1.35) rotate(5deg)';
    } else if (giftClicks >= 3) {
      text.innerText = 'เปิดแล้ววว 🎉';
      box.style.transform = 'scale(1.5)';
      setTimeout(() => goTo('screenCake'), 700);
    }
  }

  let cakeBitesCount = 0;
  function eatCakeSVG() {
    cakeBitesCount++;
    const text = document.getElementById('cakeText');
    const bite1 = document.getElementById('bite1');
    const bite2 = document.getElementById('bite2');
    const bite3 = document.getElementById('bite3');
    const flame = document.getElementById('flame');
    const crumbs = document.getElementById('crumbsGroup');

    if (cakeBitesCount === 1) {
      bite1.setAttribute('opacity', '1');
      crumbs.setAttribute('opacity', '1');
      flame.style.display = 'none';
      text.innerText = 'ง่ำ! คำแรกอร่อยมากๆ ✨';
    } else if (cakeBitesCount === 2) {
      bite2.setAttribute('opacity', '1');
      text.innerText = 'อีกคำใหญ่ๆ ง่ำๆๆ! 😋';
    } else if (cakeBitesCount >= 3) {
      bite3.setAttribute('opacity', '1');
      document.getElementById('candleGroup').style.display = 'none';
      text.innerText = 'หมดแล้วว อร่อยมากๆ เลย! ❤️';
      setTimeout(() => goTo('screenMenu'), 1200);
    }
  }

  let selectedImages = [];
  function handleFiles(files) {
    if(files.length !== 3) {
      alert('กรุณาเลือกให้ครบ 3 รูปพอดีน้า');
      return;
    }
    selectedImages = [];
    for(let i=0; i<3; i++) {
      selectedImages.push(URL.createObjectURL(files[i]));
    }
    document.getElementById('photoArea').style.display = 'flex';
  }

  function triggerCamera() {
    let count = 3;
    const cd = document.getElementById('countdown');
    cd.innerText = count;
    const timer = setInterval(() => {
      count--;
      if(count > 0) {
        cd.innerText = count;
      } else {
        clearInterval(timer);
        cd.innerText = '📸 CHEESE!';
        setTimeout(renderPolaroids, 500);
      }
    }, 1000);
  }

  function renderPolaroids() {
    document.getElementById('countdown').innerText = '';
    document.getElementById('photoArea').style.display = 'none';
    const display = document.getElementById('polaroidDisplay');
    display.innerHTML = '';

    const stickers = ['🎀', '✨', '🧁', '💖', '🧸'];

    selectedImages.forEach((src, idx) => {
      const frame = document.createElement('div');
      frame.className = 'polaroid-frame';
      frame.innerHTML = `<img src="${src}">
        <span class="sticker" style="top:-8px; right:-8px;">${stickers[idx]}</span>`;
      display.appendChild(frame);
    });

    const letter = document.getElementById('letterBox');
    letter.style.display = 'block';
    const text = "วันนี้วันเกิดแล้ว วันนี้ก็ขอให้เป็นวันที่ดีและสดใสนะคะ ยิ้มเย้อๆ มีความสุขกับการใช้ชีวิตให้มากๆ พรไหนที่ว่าเจ๋งๆขอยกให้พี่นะคะ ท้ายนี้อยากจะขอให้พี่เดินไปในเส้นทางที่ดี และพบเจอแต่ความสุข ขอให้เจอแต่คนใจดี นี่อาจจะไม่ใช่พรที่ดีเหมือนคนอื่นๆ แต่ตั้งใจสร้างเพื่อพี่เลยนะคะ 💕";
    let i = 0;
    document.getElementById('typedLetter').innerText = '';
    
    function typeWriter() {
      if (i < text.length) {
        document.getElementById('typedLetter').innerText += text.charAt(i);
        i++;
        setTimeout(typeWriter, 40);
      } else {
        document.getElementById('btnBackPhoto').style.display = 'inline-block';
      }
    }
    typeWriter();
  }

  let foundWishes = 0;
  const wishes = [
    "1.ขอให้ยิ้มเยอะๆ 😊", 
    "2.ขอให้มีความสุขมากๆ 💖", 
    "3.ขอให้คนบนโลกใจดีกับเธอ 🌍", 
    "4.ขอให้เธอมีชีวิตอยู่ไปนานๆ 🌟"
  ];

  function startBalloonGame() {
    foundWishes = 0;
    document.getElementById('balloonMsg').innerText = "หาคำอวยพรให้เจอครบ 4 ข้อนะ!";
    document.getElementById('btnBackBalloon').style.display = 'none';
    const box = document.getElementById('balloonBox');
    box.innerHTML = '';

    let balloonData = Array(20).fill(null);
    for(let i=0; i<4; i++) {
      balloonData[i] = wishes[i];
    }
    balloonData.sort(() => Math.random() - 0.5);

    balloonData.forEach((wish, idx) => {
      const b = document.createElement('div');
      b.className = 'balloon';
      b.style.left = (idx % 5 * 18 + 5) + '%';
      b.style.animationDelay = (Math.random() * 3) + 's';
      b.style.backgroundColor = ['#fcd5ce','#f8edeb','#e4d1f9','#d8e2dc'][idx % 4];
      b.innerText = '🎈';
      
      b.onclick = () => {
        if(b.style.visibility === 'hidden') return;
        b.style.visibility = 'hidden';
        if(wish) {
          foundWishes++;
          alert('✨ คุณเจอพรข้อที่: ' + wish);
          if(foundWishes === 4) {
            document.getElementById('balloonMsg').innerText = "เก่งมาก ขอให้พรเหล่านั้นเป็นจริงนะ 🎉";
            document.getElementById('btnBackBalloon').style.display = 'inline-block';
          }
        }
      };
      box.appendChild(b);
    });
  }

  function checkQTime(ans) {
    const msg = document.getElementById('timeMsg');
    if (ans === 1) {
      msg.innerText = '';
      goTo('screenDreamcore');
    } else {
      msg.innerText = 'เห้ยยตอบใหม่เดี๋ยวต่อย 🥊💥';
    }
  }

  function resetAll() {
    document.getElementById('pinInput').value = '';
    giftClicks = 0;
    cakeBitesCount = 0;
    document.getElementById('giftBox').innerText = '🎁';
    document.getElementById('giftBox').style.transform = 'scale(1)';
    document.getElementById('giftText').innerText = 'แตะที่กล่องเพื่อเปิด!';
    
    document.getElementById('bite1').setAttribute('opacity', '0');
    document.getElementById('bite2').setAttribute('opacity', '0');
    document.getElementById('bite3').setAttribute('opacity', '0');
    document.getElementById('candleGroup').style.display = 'block';
    document.getElementById('flame').style.display = 'block';
    document.getElementById('crumbsGroup').setAttribute('opacity', '0');
    document.getElementById('cakeText').innerText = 'แตะที่เค้กเพื่อกิน (3 คำ) 😋';
    
    goTo('screenPin');
  }
</script>

</body>
</html>
'''

with open("hbd_p_kao.html", "w", encoding="utf-8") as f:
    f.write(html_content)

print("FILE_CREATED")
