# mnikolayenko.github.io

<!DOCTYPE html>
<html>
<head>
  <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
</head>
<body>
  <div class="mermaid">
    graph LR
      A["Element A" config={"color": "red", "size": "10px"}]
      B["Element B" config={"color": "blue", "size": "12px"}]
      A --> B
  </div>

  <script>
    mermaid.initialize({ startOnLoad: true, theme: "default" });

    mermaid.render("graph", document.getElementsByClassName("mermaid")[0].innerHTML, function (svgCode) {
      document.getElementsByClassName("mermaid")[0].innerHTML = svgCode;
    });
  </script>
</body>
</html>
