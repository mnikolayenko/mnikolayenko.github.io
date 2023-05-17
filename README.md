# mnikolayenko.github.io

<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Mermaid Gantt Diagram Generator</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/mermaid@8.11.2/dist/mermaid.min.css" />
    <script src="https://cdn.jsdelivr.net/npm/mermaid@8.11.2/dist/mermaid.min.js"></script>
    <script>
      // Initialize mermaid
      mermaid.initialize({
        startOnLoad: true,
      });

      // Function to generate the diagram
      function generateDiagram() {
        // Get the input values
        const title = document.getElementById("title").value;
        const dateFormat = document.getElementById("dateFormat").value;
        const sections = document.getElementById("sections").value;

        // Generate the mermaid code
        const code = `gantt
          title ${title}
          dateFormat ${dateFormat}

          ${sections}
        `;

        // Render the diagram
        const container = document.getElementById("diagram");
        container.innerHTML = "";
        mermaid.render("diagram", code, (svgCode) => {
          container.innerHTML = svgCode;
        });
      }
    </script>
  </head>
  <body>
    <h1>Mermaid Gantt Diagram Generator</h1>

    <label for="title">Diagram Title:</label>
    <input type="text" id="title" placeholder="Enter the diagram title" />

    <label for="dateFormat">Date Format:</label>
    <input type="text" id="dateFormat" placeholder="Enter the date format (e.g. YYYY-MM-DD)" />

    <label for="sections">Diagram Sections:</label>
    <textarea id="sections" placeholder="Enter the diagram sections in mermaid syntax"></textarea>

    <button onclick="generateDiagram()">Generate Diagram</button>

    <div id="diagram"></div>
  </body>
</html>

