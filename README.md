<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>С Днем Рождения!</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom, #ffecd2, #fcb69f);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .card {
      text-align: center;
      background: white;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }
    h1 {
      color: #ff6f61;
      font-size: 3em;
    }
    p {
      font-size: 1.2em;
      color: #333;
    }
    .balloons {
      animation: float 3s infinite;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>С Днем Рождения!</h1>
    <p>Желаем счастья, здоровья и успехов!</p>
    <div class="balloons">
      🎈🎈🎈
    </div>
  </div>
</body>
</html>
