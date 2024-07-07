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
        minha primeira impressão era que isso ia ser muito dificil mas não achei muito legal, aprendi um pouco de html com o chat GPT e com uns videos do youtube,então acredito que ainda tenho muita coisa para aprender, tanto com meu pai,tanto com o chatGPT.Abaixo está uma calculadora basica que fiz com ajuda do chat gpt, pedi ajuda a ele, e me disse passo a passo como fazer uma calculadora basica..</p>
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
    .calculator input[type="button"] {
        width: 50px;
        height: 50px;
        font-size: 20px;
        margin: 5px;
        cursor: pointer;
    }
    .calculator input[type="text"] {
        width: 100%;
        margin-bottom: 10px;
        padding: 10px;
        box-sizing: border-box;
        font-size: 24px;
        text-align: right;
    }
</style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <br>
        <input type="button" value="7" onclick="addToDisplay('7')">
        <input type="button" value="8" onclick="addToDisplay('8')">
        <input type="button" value="9" onclick="addToDisplay('9')">
        <input type="button" value="+" onclick="addToDisplay('+')">
        <br>
        <input type="button" value="4" onclick="addToDisplay('4')">
        <input type="button" value="5" onclick="addToDisplay('5')">
        <input type="button" value="6" onclick="addToDisplay('6')">
        <input type="button" value="-" onclick="addToDisplay('-')">
        <br>
        <input type="button" value="1" onclick="addToDisplay('1')">
        <input type="button" value="2" onclick="addToDisplay('2')">
        <input type="button" value="3" onclick="addToDisplay('3')">
        <input type="button" value="*" onclick="addToDisplay('*')">
        <br>
        <input type="button" value="0" onclick="addToDisplay('0')">
        <input type="button" value="C" onclick="clearDisplay()">
        <input type="button" value="=" onclick="calculate()">
        <input type="button" value="/" onclick="addToDisplay('/')">
    </div>

    <script>
        // Função para adicionar valores ao display
        function addToDisplay(value) {
            // Verificar se o display está desativado e ativá-lo
            let display = document.getElementById('display');
            if (display.disabled) {
                display.disabled = false;
            }
            // Adicionar valor ao display
            display.value += value;
        }

        // Função para limpar o display
        function clearDisplay() {
            let display = document.getElementById('display');
            display.value = '';
        }

        // Função para calcular a expressão no display
        function calculate() {
            let display = document.getElementById('display');
            try {
                // Calcular a expressão e exibir o resultado
                display.value = eval(display.value);
            } catch(error) {
                // Exibir erro em caso de expressão inválida
                display.value = 'Error';
            }
        }
    </script>
</body>
</html>


