<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>9Cálculo de Função Exponencial</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        input, button {
            padding: 10px;
            margin: 5px;
        }
        .result {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Cálculo de f(x) = e^x</h1>
    <label for="valorX">Insira o valor de x:</label>
    <input type="number" id="valorX" placeholder="Digite o valor de x" step="0.01" />
    <button onclick="calcularExponencial()">Calcular e^x</button>
    <div class="result">
        <p><strong>Resultado:</strong> <span id="resultado"></span></p>
    </div>
    <script>
        function calcularExponencial() {
            const x = parseFloat(document.getElementById('valorX').value);
            if (isNaN(x)) {
                alert("Por favor, insira um valor válido para x.");
                return;
            }
            const resultado = Math.exp(x);
            document.getElementById('resultado').textContent = `f(${x}) = e^${x} ≈ ${resultado.toFixed(6)}`;
        }
    </script>
</body>
</html>
 
