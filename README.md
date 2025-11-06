# Tradertarun-<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Colour Trading Recovery Plan</title>
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #141E30, #243B55);
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .container {
      background: rgba(255,255,255,0.1);
      padding: 30px 40px;
      border-radius: 15px;
      text-align: center;
      width: 90%;
      max-width: 400px;
      box-shadow: 0 0 20px rgba(0,0,0,0.3);
      backdrop-filter: blur(10px);
    }
    h1 {
      font-size: 22px;
      margin-bottom: 20px;
    }
    .question {
      display: none;
      flex-direction: column;
    }
    .question.active {
      display: flex;
    }
    input {
      padding: 10px;
      margin-top: 10px;
      border: none;
      border-radius: 8px;
      outline: none;
    }
    button {
      margin-top: 20px;
      padding: 12px;
      border: none;
      border-radius: 8px;
      background: #00C9FF;
      color: #000;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #92FE9D;
    }
    .telegram {
      display: none;
    }
    a.telegram-btn {
      background: #0088cc;
      color: #fff;
      padding: 14px 25px;
      border-radius: 8px;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }
    a.telegram-btn:hover {
      background: #00aced;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>🎯 Colour Trading Recovery Plan</h1>

    <div class="question active" id="q1">
      <label>1️⃣ Aapka Naam Kya Hai?</label>
      <input type="text" id="name" placeholder="Apna naam likhiye..." required>
      <button onclick="nextQuestion(1)">Next</button>
    </div>

    <div class="question" id="q2">
      <label>2️⃣ Aapka Colour Trading Mein Kitna Loss Hua?</label>
      <input type="text" id="loss" placeholder="₹ Loss Amount likhiye..." required>
      <button onclick="nextQuestion(2)">Next</button>
    </div>

    <div class="question" id="q3">
      <label>3️⃣ Loss Recover Karne Ke Liye Aap Kitna Deposit Karoge?</label>
      <input type="text" id="deposit" placeholder="₹ Deposit Amount likhiye..." required>
      <button onclick="showTelegram()">Submit</button>
    </div>

    <div class="telegram" id="telegram">
      <h2>✅ Dhanyavaad, <span id="userName"></span>!</h2>
      <p>Apka Recovery Plan Ready Hai 💸</p>
      <a href="https://t.me/YOUR_CHANNEL_LINK" target="_blank" class="telegram-btn">Join Telegram Channel</a>
    </div>
  </div>

  <script>
    function nextQuestion(num) {
      document.getElementById(`q${num}`).classList.remove('active');
      document.getElementById(`q${num+1}`).classList.add('active');
    }

    function showTelegram() {
      const name = document.getElementById('name').value;
      document.getElementById('q3').classList.remove('active');
      document.getElementById('telegram').style.display = 'block';
      document.getElementById('userName').innerText = name;
    }
  </script>

</body>
</html>
