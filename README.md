<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Classificador de Nível de Herói</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #1e1e2f;
      color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    h1 {
      color: #ffd700;
    }
    input {
      padding: 10px;
      margin: 5px 0;
      border-radius: 5px;
      border: none;
      width: 250px;
      font-size: 16px;
    }
    button {
      padding: 10px 20px;
      margin-top: 10px;
      font-size: 16px;
      background-color: #ffd700;
      color: #1e1e2f;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background-color: #ffbf00;
    }
    #resultado {
      margin-top: 20px;
      font-size: 20px;
      color: #00ffcc;
      text-align: center;
    }
  </style>
</head>
<body>

  <h1>Classificador de Nível de Herói</h1>

  <input type="text" id="nomeHeroi" placeholder="Digite o nome do herói">
  <input type="number" id="xpHeroi" placeholder="Digite a XP do herói">
  <button onclick="classificarHeroi()">Classificar Herói</button>

  <div id="resultado"></div>

  <script>
    function classificarHeroi() {
      // Pegar valores do input
      let nome = document.getElementById("nomeHeroi").value;
      let xp = parseInt(document.getElementById("xpHeroi").value);
      let nivel = "";

      // Estrutura de decisão
      if (xp < 1000) {
        nivel = "Ferro";
      } else if (xp >= 1001 && xp <= 2000) {
        nivel = "Bronze";
      } else if (xp >= 2001 && xp <= 5000) {
        nivel = "Prata";
      } else if (xp >= 5001 && xp <= 7000) {
        nivel = "Ouro";
      } else if (xp >= 7001 && xp <= 8000) {
        nivel = "Platina";
      } else if (xp >= 8001 && xp <= 9000) {
        nivel = "Ascendente";
      } else if (xp >= 9001 && xp <= 10000) {
        nivel = "Imortal";
      } else {
        nivel = "Radiante";
      }

      // Exibir resultado
      document.getElementById("resultado").innerText = 
        `O Herói de nome ${nome} está no nível de ${nivel}`;
    }
  </script>

</body>
</html>
