# mnikolayenko.github.io

<html>
  <head>
    <style>
      #canvas {
        border: 1px solid black;
      }
    </style>
  </head>
  <body>
    <canvas id="canvas" width="500" height="500"></canvas>
    <br>
    <button id="export-png-btn">Export as PNG</button>
    <button id="export-pdf-btn">Export as PDF</button>

    <script>
      const canvas = document.getElementById("canvas");
      const context = canvas.getContext("2d");
      const exportPngBtn = document.getElementById("export-png-btn");
      const exportPdfBtn = document.getElementById("export-pdf-btn");

      let isDrawing = false;
      let x = 0;
      let y = 0;

      canvas.addEventListener("mousedown", event => {
        isDrawing = true;
        x = event.clientX;
        y = event.clientY;
      });

      canvas.addEventListener("mouseup", () => (isDrawing = false));

      canvas.addEventListener("mousemove", event => {
        if (isDrawing === false) {
          return;
        }

        const newX = event.clientX;
        const newY = event.clientY;

        context.beginPath();
        context.moveTo(x, y);
        context.lineTo(newX, newY);
        context.stroke();

        x = newX;
        y = newY;
      });

      exportPngBtn.addEventListener("click", () => {
        const dataURL = canvas.toDataURL("image/png");
        const link = document.createElement("a");
        link.download = "canvas.png";
        link.href = dataURL;
        link.click();
      });

      exportPdfBtn.addEventListener("click", () => {
        const imgData = canvas.toDataURL("image/png");
        const pdf = new jsPDF();
        pdf.addImage(imgData, "PNG", 0, 0);
        pdf.save("canvas.pdf");
      });
    </script>

    <!-- Include the jsPDF library -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/1.5.3/jspdf.min.js"></script>
  </body>
</html>


