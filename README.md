<html>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            background-color: #f8f8f8;
            color: #333;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
            text-align: center;
        }
        input, .result {
            margin: 10px;
            font-size: 18px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            width: 80%;
        }
        .label {
            font-size: 20px;
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="label">Salaire du candidat</div>
        <input type="number" id="inputNumber" placeholder="Entrez un nombre">
        <div class="result" id="annualPrice">Prix annuel: </div>
        <div class="result" id="monthlyPrice">Prix mensuel: </div>
    </div>

    <script>
        document.getElementById('inputNumber').addEventListener('input', function(e) {
            var inputValue = e.target.value;
            var annualPrice = inputValue * 0.17;
            var monthlyPrice = annualPrice / 12;
            document.getElementById('annualPrice').textContent = 'Prix annuel: ' + annualPrice.toFixed(2);
            document.getElementById('monthlyPrice').textContent = 'Prix mensuel: ' + monthlyPrice.toFixed(2);
        });
    </script>
</body>
</html>
