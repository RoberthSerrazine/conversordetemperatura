<!DOCTYPE html>
<html>
<head>
    <title>Conversor de Temperatura</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            padding: 20px;
        }

        h1 {
            color: #333;
        }

        input[type="number"] {
            padding: 10px;
            border: 1px solid #ccc;
            width: 200px;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            margin: 10px 0;
            border: none;
            cursor: pointer;
            width: 200px;
        }

        button:hover {
            opacity: 0.8;
        }

        #result {
            margin-top: 20px;
            font-size: 20px;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Conversor de Temperatura</h1>
    <input id="inputTemp" type="number" placeholder="Insira a temperatura">
    <button onclick="convertToCelsius()">Converter para Celsius</button>
    <button onclick="convertToFahrenheit()">Converter para Fahrenheit</button>
    <div id="result"></div>

    <script>
        function convertToCelsius() {
            var temp = document.getElementById('inputTemp').value;
            var celsius = (temp - 32) * 5/9;
            document.getElementById('result').innerHTML = temp + " Fahrenheit é " + celsius.toFixed(2) + " Celsius";
        }

        function convertToFahrenheit() {
            var temp = document.getElementById('inputTemp').value;
            var fahrenheit = (temp * 9/5) + 32;
            document.getElementById('result').innerHTML = temp + " Celsius é " + fahrenheit.toFixed(2) + " Fahrenheit";
        }
    </script>
</body>
</html>

