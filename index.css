<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }

        .calculator {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }

        #display {
            width: 100%;
            height: 50px;
            text-align: right;
            padding: 10px;
            border: none;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
            font-size: 2em;
            background-color: #f9f9f9;
            box-shadow: inset 0px 0px 5px rgba(0, 0, 0, 0.1);
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
        }

        .btn {
            padding: 20px;
            font-size: 1.5em;
            border: 1px solid #ddd;
            background-color: #f0f0f0;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .btn:hover {
            background-color: #e0e0e0;
        }

        .equal {
            grid-column: span 4;
            background-color: #ff9500;
            color: white;
        }

        .equal:hover {
            background-color: #e08900;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <div class="buttons">
            <button class="btn" onclick="appendNumber('1')">1</button>
            <button class="btn" onclick="appendNumber('2')">2</button>
            <button class="btn" onclick="appendNumber('3')">3</button>
            <button class="btn" onclick="setOperation('+')">+</button>
            <button class="btn" onclick="appendNumber('4')">4</button>
            <button class="btn" onclick="appendNumber('5')">5</button>
            <button class="btn" onclick="appendNumber('6')">6</button>
            <button class="btn" onclick="setOperation('-')">-</button>
            <button class="btn" onclick="appendNumber('7')">7</button>
            <button class="btn" onclick="appendNumber('8')">8</button>
            <button class="btn" onclick="appendNumber('9')">9</button>
            <button class="btn" onclick="setOperation('*')">*</button>
            <button class="btn" onclick="appendNumber('0')">0</button>
            <button class="btn" onclick="appendNumber('.')">.</button>
            <button class="btn" onclick="clearDisplay()">C</button>
            <button class="btn" onclick="setOperation('/')">/</button>
            <button class="btn equal" onclick="calculate()">=</button>
        </div>
    </div>
    <script>
        let display = document.getElementById('display');
        let currentOperation = null;
        let firstOperand = null;
        let shouldResetDisplay = false;

        function appendNumber(number) {
            if (shouldResetDisplay) {
                display.value = '';
                shouldResetDisplay = false;
            }
            display.value += number;
        }

        function clearDisplay() {
            display.value = '';
            currentOperation = null;
            firstOperand = null;
        }

        function setOperation(operation) {
            if (currentOperation !== null) calculate();
            firstOperand = parseFloat(display.value);
            currentOperation = operation;
            shouldResetDisplay = true;
        }

        function calculate() {
            if (currentOperation === null) return;
            let secondOperand = parseFloat(display.value);
            switch (currentOperation) {
                case '+':
                    display.value = firstOperand + secondOperand;
                    break;
                case '-':
                    display.value = firstOperand - secondOperand;
                    break;
                case '*':
                    display.value = firstOperand * secondOperand;
                    break;
                case '/':
                    display.value = firstOperand / secondOperand;
                    break;
            }
            currentOperation = null;
            firstOperand = null;
        }
    </script>
</body>
</html>
