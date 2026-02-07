<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Be My Valentine?</title>
  <style>
    body {
      height: 100vh;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      background: pink;
      font-family: Arial, sans-serif;
    }

    .container {
      text-align: center;
    }

    h1 {
      font-size: 2.5rem;
    }

    button {
      font-size: 1.2rem;
      padding: 10px 20px;
      margin: 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    #yes {
      background-color: #ff4d6d;
      color: white;
    }

    #no {
      position: absolute;
      background-color: #555;
      color: white;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Will you be my Valentine? 💕</h1>
    <button id="yes" onclick="yesClicked()">Yes 💖</button>
    <button id="no">No 💔</button>
  </div>

  <script>
    const noBtn = document.getElementById("no");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - noBtn.clientWidth);
      const y = Math.random() * (window.innerHeight - noBtn.clientHeight);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    });

    function yesClicked() {
      document.body.innerHTML = `
        <div style="text-align:center;">
          <h1>YAY!!! 💘🥰</h1>
          <p>I knew you’d say yes 😌</p>
        </div>
      `;
    }
  </script>

</body>
</html>
