# mnikolayenko.github.io

<html>
<head>
  <title>Пример интерактивных элементов</title>
</head>
<body>
  <h1>Интерактивные элементы</h1>

  <!-- Пример 1: Кнопка с обработчиком события -->
  <button id="myButton">Нажми меня!</button>

  <!-- Пример 2: Поле ввода с динамическим обновлением -->
  <input type="text" id="myInput">
  <p id="output"></p>

  <!-- Пример 3: Вращающийся квадрат -->
  <div id="mySquare"></div>

  <script>
    // Пример 1: Кнопка с обработчиком события
    var button = document.getElementById('myButton');
    button.addEventListener('click', function() {
      alert('Вы нажали на кнопку!');
    });

    // Пример 2: Поле ввода с динамическим обновлением
    var input = document.getElementById('myInput');
    var output = document.getElementById('output');
    input.addEventListener('input', function() {
      output.innerText = input.value;
    });

    // Пример 3: Вращающийся квадрат
    var square = document.getElementById('mySquare');
    var rotation = 0;
    setInterval(function() {
      rotation += 1;
      square.style.transform = 'rotate(' + rotation + 'deg)';
    }, 10);
  </script>
</body>
</html>