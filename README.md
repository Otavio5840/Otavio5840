<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Página</title>
    <meta name="description" content="Minha primeira página HTML">
    <meta name="author" content="Otávio">
</head>
<body>
    <h1>Minha Primeira Página</h1>
    <p>Meu nome é Otávio e esta é minha primeira página HTML, gosto de estudar coisas novas,acho que não conheço ninguém com 11 anos que já se aventura por ai aprendendo essas coisas.
        minha primeira impressão era que isso ia ser muito dificil mas não achei muito legal, aprendi um pouco de html com o chat GPT e com uns videos do youtube,então acredito que ainda tenho muita coisa para aprender, tanto com meu pai,tanto com o chatGPT.Abaixo esta uma calculadora basica.</p>
</body>
</html>

---->
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Calculadora Básica</title>
<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
    }
    .calculator {
        width: 300px;
        margin: 50px auto;
        border: 1px solid #ccc;
        padding: 10px;
        border-radius: 5px;
        background-color: #f3f3f3;
    }
    .calculator input {
        width: 100%;
        margin-bottom: 10px;
        padding: 10px;
        box-sizing: border-box;
        font-size: 18px;
    }
    .calculator button {
        width: 48%;
        padding: 10px;
        font-size: 18px;
        margin-top: 5px;
        cursor: pointer;
    }
</style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <button onclick="addToDisplay('7')">7</button>
        <button onclick="addToDisplay('8')">8</button>
        <button onclick="addToDisplay('9')">9</button>
        <button onclick="addToDisplay('+')">+</button>
        <button onclick="addToDisplay('4')">4</button>
        <button onclick="addToDisplay('5')">5</button>
        <button onclick="addToDisplay('6')">6</button>
        <button onclick="addToDisplay('-')">-</button>
        <button onclick="addToDisplay('1')">1</button>
        <button onclick="addToDisplay('2')">2</button>
        <button onclick="addToDisplay('3')">3</button>
        <button onclick="addToDisplay('*')">*</button>
        <button onclick="addToDisplay('0')">0</button>
        <button onclick="clearDisplay()">C</button>
        <button onclick="calculate()">=</button>
        <button onclick="addToDisplay('/')">/</button>
    </div>

    <script>
        function addToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            let display = document.getElementById('display');
            try {
                display.value = eval(display.value);
            } catch(error) {
                display.value = 'Error';
            }
        }
    </script>
</body>
</html>
