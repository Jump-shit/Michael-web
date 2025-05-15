# Michael-web

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>You all my son</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #f9b9d3;
      color: #d6324a;
      font-family: "Comic Sans MS", "Segoe UI", cursive;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
      position: relative;
    }

    h1 {
      font-size: 2.5rem;
      text-align: center;
      z-index: 1;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: rgb(217, 91, 112);
      transform: rotate(45deg);
      animation: fall 5s linear infinite;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: pink;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes fall {
      0% {
        top: -10%;
        opacity: 1;
      }
      100% {
        top: 110%;
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>儿子们你们好，你们都是我儿子<br>💗</h1>

  <script>
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (3 + Math.random() * 2) + "s";
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 5000);
    }

    setInterval(createHeart, 200);
  </script>
</body>
</html>
