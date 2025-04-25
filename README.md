<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Executores</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Orbitron', sans-serif;
      color: white;
      background: url('/mnt/data/faf91d45-6446-4b5a-b557-1cc2fae0bd9c.png') no-repeat center center fixed;
      background-size: cover;
      overflow-x: hidden;
      animation: backgroundMove 30s linear infinite;
    }

    @keyframes backgroundMove {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .overlay {
      background: linear-gradient(145deg, rgba(0,0,0,0.9), rgba(50,0,100,0.7));
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
    }

    .content {
      position: relative;
      z-index: 1;
      text-align: center;
      padding: 70px 20px;
      animation: fadeIn 2s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    h1 {
      font-size: 3em;
      text-shadow: 0 0 10px #00f0ff, 0 0 20px #ff00f0;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { text-shadow: 0 0 10px #00f0ff, 0 0 20px #ff00f0; }
      50% { text-shadow: 0 0 20px #00f0ff, 0 0 40px #ff00f0; }
    }

    .description {
      font-size: 1.3em;
      margin: 30px auto;
      background: rgba(0, 0, 0, 0.6);
      padding: 20px;
      border-radius: 15px;
      max-width: 700px;
      box-shadow: 0 0 20px rgba(255, 255, 255, 0.2);
    }

    .executors {
      display: flex;
      justify-content: center;
      gap: 30px;
      flex-wrap: wrap;
      margin-top: 40px;
    }

    .executor-card {
      background: rgba(255, 255, 255, 0.1);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 20px;
      padding: 25px;
      width: 220px;
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
      backdrop-filter: blur(8px);
      animation: floatCard 6s ease-in-out infinite;
    }

    .executor-card:hover {
      transform: scale(1.1);
      box-shadow: 0 0 30px #00f0ff;
    }

    @keyframes floatCard {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }

    .executor-card a {
      color: #00ffff;
      text-decoration: none;
      font-weight: bold;
    }

    .mini-panel {
      display: none;
      background: rgba(20, 20, 20, 0.95);
      position: fixed;
      top: 120px;
      left: 50%;
      transform: translateX(-50%);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 0 25px #00ffff;
      z-index: 100;
      color: white;
      min-width: 300px;
    }

    .mini-panel h3 {
      margin-top: 0;
      color: #00ffff;
    }

    .mini-panel ul {
      list-style: none;
      padding: 0;
    }

    .mini-panel li {
      padding: 10px 0;
      font-size: 1.1em;
    }
  </style>
</head>
<body>
  <div class="overlay"></div>
  <div class="content">
    <h1>Executores</h1>
    <p class="description">Faça sua escolha abaixo lembrando são todos atualizados e não nos responsabilizamos por nada</p>

    <div class="executors">
      <div class="executor-card" onclick="togglePanel()">Abrir Painel</div>
      <div class="executor-card">
        <a href="https://example.com/teste" target="_blank">Ir para Teste</a>
      </div>
    </div>
  </div>

  <div class="mini-panel" id="miniPanel">
    <h3>Executores</h3>
    <ul>
      <li>Xeno</li>
      <li><a href="https://example.com/teste" target="_blank">Teste</a></li>
    </ul>
  </div>

  <script>
    function togglePanel() {
      const panel = document.getElementById('miniPanel');
      panel.style.display = panel.style.display === 'block' ? 'none' : 'block';
    }
  </script>
</body>
</html>
