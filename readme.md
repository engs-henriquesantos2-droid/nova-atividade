# Aula de clonagem 
---------------------------------------------
# Aprendendo na nova aula, e observando.
 
## Subtitul<<<<<<<o
### NOVA ATIVIDADE 
# SLA, QUERIA UM SORVETE COM AMENDOIN 
# as vezes a vida prega peças para nos 
# Professor ensina bem, aula pratica 
# deu erro 
# Não da, amanha tem que trabalhar de novo, que vida triste, clt fudido 
# queria uma uva
# as vezes um ser é um ser 
# queria uma prova de matematica 
# nao da
# computador 
# informatica 4
# @
# @haydrec
# lan rouse 
# comida
# $ 
# <!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Calculadora Simples</title>
    <style>
        /* Estilo da Calculadora (CSS) */
        body { font-family: sans-serif; display: flex; justify-content: center; align-items: center; height: 100vh; background-color: #f4f4f4; }
        .calculadora { background-color: #333; padding: 20px; border-radius: 10px; box-shadow: 0px 10px 20px rgba(0,0,0,0.3); }
        #resultado { width: 100%; height: 50px; font-size: 24px; text-align: right; margin-bottom: 10px; padding: 10px; box-sizing: border-box; border: none; border-radius: 5px; }
        .botoes { display: grid; grid-template-columns: repeat(4, 1fr); gap: 10px; }
        button { padding: 20px; font-size: 18px; border: none; border-radius: 5px; cursor: pointer; transition: 0.2s; }
        button:hover { background-color: #ddd; }
        .operador { background-color: #f39c12; color: white; }
        .igual { background-color: #27ae60; color: white; grid-column: span 2; }
        .limpar { background-color: #c0392b; color: white; grid-column: span 2; }
    </style>
</head>
<body>

<div class="calculadora">
    <input type="text" id="resultado" disabled>
    <div class="botoes">
        <button class="limpar" onclick="limpar()">C</button>
        <button class="operador" onclick="inserir('/')">/</button>
        <button class="operador" onclick="inserir('*')">*</button>
        
        <button onclick="inserir('7')">7</button>
        <button onclick="inserir('8')">8</button>
        <button onclick="inserir('9')">9</button>
        <button class="operador" onclick="inserir('-')">-</button>
        
        <button onclick="inserir('4')">4</button>
        <button onclick="inserir('5')">5</button>
        <button onclick="inserir('6')">6</button>
        <button class="operador" onclick="inserir('+')">+</button>
        
        <button onclick="inserir('1')">1</button>
        <button onclick="inserir('2')">2</button>
        <button onclick="inserir('3')">3</button>
        <button onclick="inserir('0')">0</button>
        
        <button class="igual" onclick="calcular()">=</button>
        <button onclick="inserir('.')">.</button>
    </div>
</div>

<script>
    /* Lógica da Calculadora (JavaScript) */
    const visor = document.getElementById('resultado');

    function inserir(valor) {
        visor.value += valor;
    }

    function limpar() {
        visor.value = "";
    }

    function calcular() {
        try {
            // eval() processa a string matemática e retorna o resultado
            visor.value = eval(visor.value);
        } catch (e) {
            visor.value = "Erro";
        }
    }
</script>

</body>
</html>
