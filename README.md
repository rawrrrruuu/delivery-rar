<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>delivery from Natoy 💕</title>
  <style>
    body { 
      font-family: 'Comic Sans MS', cursive; 
      background: #FFE4E1; 
      text-align: center; 
      padding: 20px;
      overflow-x: hidden;
    }
    .box {
      background: white; 
      max-width: 400px; 
      margin: 30px auto; 
      padding: 30px; 
      border-radius: 20px; 
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      position: relative;
      min-height: 500px;
    }
    h1 { color: #FF69B4; font-size: 26px; }
    button {
      background: #FF69B4; 
      color: white; 
      border: none; 
      padding: 15px 30px; 
      border-radius: 50px; 
      font-size: 18px; 
      cursor: pointer;
      margin-top: 15px;
    }
    button:hover { background: #FF1493; }
    #house { font-size: 80px; margin: 10px 0; position: relative; }
    #girlfriend {
      font-size: 60px;
      position: absolute;
      top: 90px;
      left: 50%;
      transform: translateX(-50%);
      opacity: 0;
      transition: opacity 1s ease-in;
    }
    #girlfriend.show { opacity: 1; }
    #cart { 
      font-size: 45px; 
      position: absolute;
      left: -150px;
      top: 220px;
      transition: left 3s ease-in-out;
      white-space: nowrap;
    }
    #cart.move { left: 120px; }
    #knock { 
      font-size: 40px; 
      opacity: 0;
      transition: opacity 0.3s;
      margin: 10px 0;
    }
    #knock.show { 
      opacity: 1;
      animation: knock 0.5s 3; 
    }
    @keyframes knock {
      0%, 100% { transform: translateX(0); }
      50% { transform: translateX(5px); }
    }
    #loveMsg { 
      font-weight: bold; 
      color: #FF1493; 
      margin-top: 15px; 
      font-size: 22px;
      min-height: 60px;
      line-height: 1.4;
    }
    .hidden { display: none; }
    #kissHug { 
      font-size: 70px; 
      margin: 15px 0; 
      animation: pulse 1.2s infinite; 
    }
    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.15); }
    }
    .hearts {
      font-size: 30px;
      position: absolute;
      opacity: 0;
      animation: float 3s ease-in infinite;
    }
    #finalSection.show .hearts { opacity: 1; }
    @keyframes float {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(-80px); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="box">
    <h1>delivery from Natoy 💕</h1>
    
    <div id="house">
      🏠
      <div id="girlfriend">👩</div>
    </div>
    <div id="cart">👨🛒</div>
    <div id="knock">👊👊👊</div>
    
    <button id="deliverBtn" onclick="startDelivery()">Open delivery</button>
    
    <div id="finalSection" class="hidden">
      <div class="hearts" style="left: 20%;">💕</div>
      <div class="hearts" style="left: 80%; animation-delay: 0.5s;">💕</div>
      <div id="kissHug">😘🫂</div>
      <p id="loveMsg">I love you so much, baby<br>from Natoy 💕</p>
      <button onclick="reset()">Deliver ulit?</button>
    </div>
  </div>

  <script>
    function startDelivery() {
      document.getElementById('deliverBtn').classList.add('hidden');
      document.getElementById('cart').classList.add('move');
      
      setTimeout(() => {
        document.getElementById('knock').classList.add('show');
      }, 3000);
      
      setTimeout(() => {
        document.getElementById('knock').classList.remove('show');
        document.getElementById('girlfriend').classList.add('show');
      }, 5000);
      
      setTimeout(() => {
        document.getElementById('cart').innerText = '👨‍❤️‍👩';
        document.getElementById('finalSection').classList.remove('hidden');
        document.getElementById('finalSection').classList.add('show');
      }, 6500);
    }

    function reset() {
      document.getElementById('cart').classList.remove('move');
      document.getElementById('cart').innerText = '👨🛒';
      document.getElementById('girlfriend').classList.remove('show');
      document.getElementById('finalSection').classList.add('hidden');
      document.getElementById('finalSection').classList.remove('show');
      document.getElementById('deliverBtn').classList.remove('hidden');
    }
  </script>
</body>
</html>
