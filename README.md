Programad by Marco

<!DOCTYPE html>
<html lang="pt-br">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Recado</title>
  <style>
    body {
      background-color: #ffcccc;
      text-align: center;
      font-family: Arial, sans-serif;
    }

    .container {
      padding: 20px;
    }

    h1 {
      color: #ff3366;
    }

    .heart {
      font-size: 50px;
      color: #ff3366;
      cursor: pointer;
    }

    #nao {
      font-size: 24px;
      color: #333;
      background-color: #ffcccc;
      border: none;
      cursor: pointer;
      position: absolute;
    }
  </style>
</head>

<body>
  <div class="container">
    <h1>Um Recadinho para o Leo!</h1>
    <p>Oii Gatinho, tudo bem?</p>
    <p>Quero dizer que depois do último encontro, tu me deixou louquinho por ti rsrs. 🤭🤭</p>
    <p>Clique no coração</p>
    <p class="heart" onclick="mostrarResposta()">❤️</p>
    <button id="nao" onmouseover="mudarPosicao()"></button>
    <p id="resposta" style="display: none;"></p>
  </div>
  <script>
    function mostrarResposta() {
      document.getElementById('resposta').style.display = 'block';
      document.getElementById('resposta').innerHTML = 'Soube me provocar direitinho. hehehe';
    }

    function mudarPosicao() {
      const buttonNao = document.getElementById('nao');
      const randomX = Math.floor(Math.random() * window.innerWidth);
      const randomY = Math.floor(Math.random() * window.innerHeight);
      buttonNao.style.left = `${randomX}px`;
      buttonNao.style.top = `${randomY}px`;
    }
  </script>
</body>

</html>
