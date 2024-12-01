# my-frontend
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Investment Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 50%;
            margin: 50px auto;
            padding: 20px;
            background-color: #f4f4f4;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        input, button {
            margin: 10px 0;
            display: block;
            width: 100%;
            padding: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Investment Calculator</h1>
        <p>Enter your investment details:</p>
        <input type="number" id="investment" placeholder="Investment Amount">
        <input type="number" id="rate" placeholder="Interest Rate (%)">
        <button onclick="calculate()">Calculate</button>
        <p id="result"></p>
    </div>
    <script>
        function calculate() {
            const investment = document.getElementById('investment').value;
            const rate = document.getElementById('rate').value;
            const futureValue = investment * (1 + rate / 100);
            document.getElementById('result').innerText = `Future Value: $${futureValue.toFixed(2)}`;
        }
    </script>
</body>
</html>
