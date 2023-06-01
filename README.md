<html>

<head>
  <title>Calculator</title>
  <style>
    .calculator {
      width: 50%;
      margin-left: 25%;
      margin-top: 10%;
      border: 5px solid #ccc;
      padding: 10px;
      background-color: rgb(187, 118, 172);
      color: black;
      padding: 2%;
    }

    .calculator input[type="button"] {
      width: 45px;
      height: 45px;
      margin: 2px;
    }

    .calculator input[type="text"] {
      width: 34%;
      margin-bottom: 10px;
    }

    .button {
      box-shadow: 0 8px 16px 0 rgba(4, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
      background-color: rgb(203, 121, 121);
      padding-top: 2%;
    }
  </style>
</head>

<body bgcolor="wheat">
  <div class="calculator" align="center">
    <h1 align="center">Calculator</h1>
    <div class="button">
      <input type="text" id="display" readonly><br>
      <input type="button" value="1" onclick="addToDisplay('1')">
      <input type="button" value="2" onclick="addToDisplay('2')">
      <input type="button" value="3" onclick="addToDisplay('3')">
      <input type="button" value="+" onclick="addToDisplay('+')">
      <input type="button" value="-" onclick="addToDisplay('-')"><br>
      <input type="button" value="4" onclick="addToDisplay('4')">
      <input type="button" value="5" onclick="addToDisplay('5')">
      <input type="button" value="6" onclick="addToDisplay('6')">
      <input type="button" value="*" onclick="addToDisplay('*')">
      <input type="button" value="/" onclick="addToDisplay('/')"><br>
      <input type="button" value="7" onclick="addToDisplay('7')">
      <input type="button" value="8" onclick="addToDisplay('8')">
      <input type="button" value="9" onclick="addToDisplay('9')">
      <input type="button" value="C" onclick="clearDisplay()">
      <input type="button" value="=" onclick="calculate()"><br>
      <input type="button" value="0" onclick="addToDisplay('0')">
      <input type="button" value="." onclick="addToDisplay('.')">
    </div>
  </div>

  <script>
    function addToDisplay(value) {
      document.getElementById("display").value += value;
    }

    function clearDisplay() {
      document.getElementById("display").value = "";
    }

    function calculate() {
      var expression = document.getElementById("display").value;
      var result = eval(expression);
      document.getElementById("display").value = result;
    }
  </script>
</body>

</html>
