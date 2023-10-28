# nareshh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
        }

        .calculator {
            width: 300px;
            margin: 0 auto;
            background-color: #fff;
            border: 1px solid #ccc;
            border-radius: 5px;
            padding: 10px;
        }

        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            font-size: 18px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }

        .button-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 5px;
        }

        .button {
            padding: 10px;
            text-align: center;
            font-size: 18px;
            cursor: pointer;
            border: 1px solid #ccc;
            border-radius: 3px;
            background-color: #f2f2f2;
        }

        .button:hover {
            background-color: #ddd;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="result" readonly>
        <div class="button-container">
            <div class="button" onclick="clearResult()">C</div>
            <div class="button" onclick="appendToResult('7')">7</div>
            <div class="button" onclick="appendToResult('8')">8</div>
            <div class="button" onclick="appendToResult('9')">9</div>
            <div class="button" onclick="appendToResult('4')">4</div>
            <div class="button" onclick="appendToResult('5')">5</div>
            <div class="button" onclick="appendToResult('6')">6</div>
            <div class="button" onclick="appendToResult('1')">1</div>
            <div class="button" onclick="appendToResult('2')">2</div>
            <div class="button" onclick="appendToResult('3')">3</div>
            <div class="button" onclick="appendToResult('0')">0</div>
            <div class="button" onclick="appendToResult('+')">+</div>
            <div class="button" onclick="appendToResult('-')">-</div>
            <div class="button" onclick="appendToResult('*')">*</div>
            <div class="button" onclick="appendToResult('/')">/</div>
            <div class="button" onclick="calculateResult()">=</div>
        </div>
    </div>

    <script>
        function appendToResult(value) {
            document.getElementById("result").value += value;
        }

        function clearResult() {
            document.getElementById("result").value = "";
        }

        function calculateResult() {
            try {
                document.getElementById("result").value = eval(document.getElementById("result").value);
            } catch (error) {
                document.getElementById("result").value = "Error";
            }
        }
    </script>
</body>
</html>
