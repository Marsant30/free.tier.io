<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Disponibilidade ARM - Oracle Free Tier</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #111;
      color: #fff;
      padding: 20px;
    }
    h1 { color: #0f0; }
    .region {
      background: #222;
      padding: 10px;
      margin: 10px 0;
      border-left: 5px solid #0f0;
    }
    .unavailable {
      border-left-color: #f00;
    }
  </style>
</head>
<body>
  <h1>Disponibilidade ARM - Oracle Free Tier</h1>
  <p>Confira abaixo as regiões que <strong>geralmente</strong> estão com instâncias ARM disponíveis:</p>
  <div id="regions"></div>

  <script>
    const availableRegions = [
      { name: "South Korea Central", code: "icn" },
      { name: "Germany Central (Frankfurt)", code: "fra" },
      { name: "Japan East (Tokyo)", code: "nrt" },
      { name: "Brazil East (São Paulo)", code: "gru" },
      { name: "UK South (London)", code: "lhr" },
    ];

    const unavailableRegions = [
      { name: "US East (Ashburn)", code: "iad" },
      { name: "US West (Phoenix)", code: "phx" },
    ];

    const container = document.getElementById("regions");

    availableRegions.forEach(region => {
      const div = document.createElement("div");
      div.className = "region";
      div.innerHTML = `<strong>${region.name}</strong> - <em>Ampere geralmente disponível</em>`;
      container.appendChild(div);
    });

    unavailableRegions.forEach(region => {
      const div = document.createElement("div");
      div.className = "region unavailable";
      div.innerHTML = `<strong>${region.name}</strong> - <em>Ampere geralmente indisponível</em>`;
      container.appendChild(div);
    });
  </script>
</body>
</html>
