<html>
<head>
  <title>Simple Calculator</title>
  <link rel="stylesheet" href="external.css">
  <script>let displayValue = '';

    function appendToDisplay(value) {
      displayValue += value;
      document.getElementById('display').value = displayValue;
    }
    
    function calculate() {
      try {
        displayValue = eval(displayValue).toString();
        document.getElementById('display').value = displayValue;
      } catch (error) {
        displayValue = '';
        document.getElementById('display').value = 'Error';
      }
    }
    
    function clearDisplay() {
      displayValue = '';
      document.getElementById('display').value = displayValue;
    }
    </script>

</head>
<body>
  <div class="calculator">
    <input type="text" id="display" readonly>
    <div class="buttons">
      <button onclick="clearDisplay()">C</button> 
      <button onclick="appendToDisplay('/')">/</button><br> 
      <button onclick="appendToDisplay('*')">*</button>
      <button onclick="appendToDisplay('7')">7</button>
      <button onclick="appendToDisplay('8')">8</button>
      <button onclick="appendToDisplay('9')">9</button><br>
      <button onclick="appendToDisplay('-')">-</button>
      <button onclick="appendToDisplay('5')">5</button>
      <button onclick="appendToDisplay('4')">4</button>
      <button onclick="appendToDisplay('6')">6</button><br>
      <button onclick="appendToDisplay('+')">+</button>
      <button onclick="appendToDisplay('1')">1</button>
      <button onclick="appendToDisplay('2')">2</button>
      <button onclick="appendToDisplay('3')">3</button><br>
      <button onclick="calculate()">=</button>
      <button onclick="appendToDisplay('0')">0</button>
      <button onclick="appendToDisplay('.')">.</button>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>





**CSS CODE:**
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.calculator {
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 10px;
}

input {
  width: 200px;
  padding: 10px;
  font-size: 24px;
  text-align: right;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 5px;
  margin-top: 10px;
}

button {
  padding: 15px;
  font-size: 18px;
  background-color: #eee;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #ddd;
}

