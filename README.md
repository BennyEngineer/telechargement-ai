<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Connexion IA...</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #000;
      color: #027da8;
      font-family: 'Courier New', Courier, monospace;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    #terminal {
      width: 90%;
      max-width: 700px;
      background-color: #000;
      border: 2px solid #027da8;
      padding: 30px;
      box-shadow: 0 0 15px #027da8;
      font-size: 1rem;
      white-space: pre-line;
      overflow: hidden;
    }
  </style>
</head>
<body>
  <div id="terminal">Connexion à l'intelligence système...</div>

  <script>
    const terminal = document.getElementById("terminal");
    const lines = [
      "Analyse biométrique...",
      "Authentification réussie.",
      "Initialisation du protocole de téléchargement...",
      "Redirection sécurisée vers la page de téléchargement en cours...",
      "Merci de faire confiance à software store."
    ];

    let lineIndex = 0;
    let charIndex = 0;
    let baseDelay = 40;

    function typeLine(callback) {
      if (lineIndex < lines.length) {
        const currentLine = lines[lineIndex];
        if (charIndex < currentLine.length) {
          terminal.innerHTML += currentLine.charAt(charIndex);
          charIndex++;
          setTimeout(() => typeLine(callback), baseDelay);
        } else {
          terminal.innerHTML += "\n";
          lineIndex++;
          charIndex = 0;
          setTimeout(() => typeLine(callback), 400);
        }
      } else {
        callback();
      }
    }

    function measureConnectionSpeed(callback) {
      const img = new Image();
      const startTime = new Date().getTime();
      const cacheBuster = "?nn=" + startTime;
      img.src = "https://via.placeholder.com/100" + cacheBuster;
      img.onload = () => {
        const duration = new Date().getTime() - startTime;
        const speedFactor = Math.min(Math.max(duration / 100, 1), 6);
        baseDelay = 30 * speedFactor;
        callback();
      };
      img.onerror = () => {
        baseDelay = 50;
        callback();
      };
    }

    measureConnectionSpeed(() => {
      typeLine(() => {
        setTimeout(() => {
          window.location.href = "https://sites.google.com/view/softwarstor/cat%C3%A9gories/logiciels/cao-dao/archicad/tarchicad"; // Remplace avec ton lien
        }, 1000);
      });
    });
  </script>
</body>
</html>
