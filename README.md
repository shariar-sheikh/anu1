<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Welcome Anu!</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      height: 100vh;
      background: linear-gradient(135deg, #fce3ec, #ffe1f2);
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      overflow: hidden;
    }

    .welcome {
      font-size: 2rem;
      color: #ff5e78;
      margin-bottom: 50px;
      animation: fadeIn 2s ease-in-out forwards;
    }

    .circle-btn {
      width: 150px;
      height: 150px;
      background: #ff5e78;
      color: white;
      border: none;
      border-radius: 50%;
      font-size: 1.2rem;
      cursor: pointer;
      box-shadow: 0 10px 20px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
      animation: bounce 2s infinite;
    }

    .circle-btn:hover {
      transform: scale(1.1);
    }

    .message {
      display: none;
      margin-top: 30px;
      font-size: 1.5rem;
      color: #6b2f2f;
      animation: popIn 1s forwards;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes popIn {
      0% { transform: scale(0.5); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
  </style>
</head>
<body>

  <div class="welcome">স্বাগতম, আনু! 👋</div>

  <button class="circle-btn" onclick="showMessage()">Tap Here</button>

  <div id="message" class="message">✨ তুই একটা brilliant student, Anu! ✨</div>

  <script>
    function showMessage() {
      const btn = document.querySelector('.circle-btn');
      const msg = document.getElementById('message');

      btn.style.display = 'none';
      msg.style.display = 'block';
    }
  </script>

</body>
</html>
