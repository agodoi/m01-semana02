# Prática de computação: desenvolvendo animações com código

## Objetivos

Foco em lógica de programação, especialmente em aplicação de operações lógicas e aritméticas para controle de personagem no jogo, incluindo animação da imagem com sprites e utilização de funções e laços de repetição para funcionamento do jogo como um todo.

## Assuntos relacionados
- Algoritmos para a solução de problemas de baixa complexidade
- Programação orientada a objetos

## Revisão da Semana 01
HTML --> linguagem estática para escrever documentos. Antigamente, a Internet era feita de páginas estáticas como a imagem a seguir:


<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m01-semana02/blob/main/imgs/088b90c_11088-1c3ely2.wvaxo2mx6r.png">
   <img alt="Boucing" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m01-semana02/blob/main/imgs/088b90c_11088-1c3ely2.wvaxo2mx6r.png)">
</picture>


Mas hoje, o HTML sozinho não atende a WEB moderna na maoria dos casos porque queremos páginas animadas, dinâmicas, validando e autenticando dados, acessando banco de dados e se atualizando sozinhas enquanto navegamos. Então surgiu o JavaScript (JS), além de outras linguagens que não serão foco nesse módulo: PHP e Java Server Page (JSP).

A ideia não é aposentar o HTML, porque não tem jeito de fazer isso porque ele é a base de qualquer documento, mas sim, turbinar o HTML com o JS.

Reforçando, que o JS roda predominantemente no lado do cliente (navegador) e não do servidor (computadores mantidos na nuvem).

Portanto, o JS é utilizado em páginas web para acrescentar características dinâmicas. Com isso, há, de maneira simples e eficiente, mais capacidade de interação com o usuário. O JavaScript acrescenta inúmeras possibilidades quando aplicado em conjunto com HTML e CSS na construção de sites para a Internet.

O JS possui:
* Funções
* Objetos
* Eventos
* Propriedades
* Métodos

Veja a figura a seguir para entender o que é cada item:


<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m01-semana02/blob/main/imgs/fig01.png">
   <img alt="Boucing" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m01-semana02/blob/main/imgs/fig01.png)">
</picture>

Outra característica importante é que suas variáveis assumem diferentes tipos de dados ao longo da programação. Em outras palavras, uma variável tipo INTEIRA pode assumir valores tipo FLOAT no meio do algoritmo.

Um exemplo básico de JS é esse a seguir:

```
<!DOCTYPE html>
<html>
	<head>
		<title> Introdução ao Java</title>
		<meta charset="UTF-8">
	<head>

	<body onload="iniciar()">
		<script type="text/javascript">
		function iniciar() {
			document.write("<h1>" + document.title + "</h1>");
			document.write("Olá pessoal!<br>");
		}
		</script>
	</body>
</html>
```

Adicionando um **método write** no **objeto document** para puxar o nome do navegador e sua versão.

```
<!DOCTYPE html>
<html>
	<head>
		<title> Introdução ao Java</title>
		<meta charset="UTF-8">
	<head>

	<body onload="iniciar()">
		<script type="text/javascript">
		function iniciar() {
			document.write("<h1>" + document.title + "</h1>");
			document.write("Olá pessoal!<br>");
			document.write("Você está usando o navegador " + navigator.appName + "na versão " + navigator.appVersion);
		}
		</script>
	</body>
</html>
```

Voltando à questão sobre o tipo de dado das variáveis, **onde em JS não se define que tipo de variável está sendo declarada**, segue um exemplo:

```
<!DOCTYPE html>
<html>
	<head>
		<title> Introdução ao Java</title>
		<meta charset="UTF-8">
	<head>

	<body onload="iniciar()">
		<script type="text/javascript">
		function iniciar() {
			document.write("<h1>" + document.title + "</h1>");
			document.write("Olá pessoal!<br>");
			document.write("Você está usando o navegador " + navigator.appName + " na versão " + navigator.appVersion);
			var x = "Oi, tudo bem?";
			document.write("<h1>Variáveis em JavaScript</h1>");
			document.write("X está guardando string: " + x + "<br>");
			x = 1 + 1;
			document.write("X está guardando inteiro: " + x + "<br>");
			x = 3.14;	
			document.write("X está guardando float: " + x + "<br>");
			
		}
		</script>
	</body>
</html>
```

A seguir, o mesmo código com cada linha comentada:

Aqui estão as linhas do código HTML/JavaScript com comentários explicativos:


```
<!DOCTYPE html>
<html>
	<head>
		<title> Introdução ao Java</title> <!-- Título da página -->
		<meta charset="UTF-8"> <!-- Meta tag para definir o conjunto de caracteres UTF-8 -->
	<head>

	<body onload="iniciar()"> //O evento 'onload' é acionado quando a página é carregada e chama a função 'iniciar()'
		<script type="text/javascript">
		function iniciar() { <!-- Declaração da função 'iniciar()' -->
			document.write("<h1>" + document.title + "</h1>"); <!-- Escreve o título da página em um cabeçalho h1 -->
			document.write("Olá pessoal!<br>"); <!-- Escreve uma mensagem -->
			document.write("Você está usando o navegador " + navigator.appName + " na versão " + navigator.appVersion); <!-- Escreve informações sobre o navegador -->
			x = "Oi, tudo bem?"; <!-- Declaração da variável 'x' como uma string -->
			document.write("<h1>Variáveis em JavaScript</h1>"); <!-- Escreve um cabeçalho h1 -->
			document.write("X está guardando string: " + x + "<br>" + "<br>"); <!-- Escreve o valor da variável 'x' -->
			x = 1 + 1; <!-- Atualiza o valor da variável 'x' para a soma de 1 + 1 -->
			document.write("X está guardando inteiro: " + x + "<br>"); <!-- Escreve o valor atualizado da variável 'x' -->
			x = 3.14; <!-- Atualiza o valor da variável 'x' para 3.14 -->
			document.write("X está guardando float: " + x + "<br>"); <!-- Escreve o valor atualizado da variável 'x' -->
			a=10; <!-- Declaração da variável 'a' com o valor 10 -->
			a += 2; <!-- Adiciona 2 ao valor da variável 'a' -->
			b = a ** 2 <!-- Calcula o quadrado do valor da variável 'a' e atribui a 'b' -->
			a > b <!-- Verifica se 'a' é maior que 'b', mas o resultado não é utilizado -->
			document.write("a = " + a + "<br>"); <!-- Escreve o valor atualizado da variável 'a' -->
			document.write("b = " + b + "<br>"); <!-- Escreve o valor da variável 'b' -->
			SOMA = soma(2,3); <!-- Chama a função 'soma()' com os valores 2 e 3 e atribui o resultado a 'SOMA' -->
			document.write("O resultado da soma = " + SOMA + "<br>"); <!-- Escreve o resultado da soma -->
		}

		function soma(a,b){ <!-- Declaração da função 'soma()' -->
			return a + b; <!-- Retorna a soma dos parâmetros 'a' e 'b' -->
		}
		</script>
	</body>
</html>
```

Espero que isso ajude a entender o código!


## Movimentos em Jogos

O movimento no jogo é na verdade uma enganação em nosso cérebro. O movimento ocorre a partir de imagens estáticas nas quais, se houver diferenças sultis na transição de uma para a outra, os nossos olhos vão **emendar** uma imagem na outra, parecendo que ela está se movimentando.

Existe um valor mínimo de imagens estáticas por segundo para que não percebamos o truque. A percepção do truque se assemelha à cintilação que é variação da tonalidade de luz sobre uma imagem. Veja tabela a seguir para entender melhor.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m01-semana02/blob/main/imgs/tabela-fps-jogoveio.png">
   <img alt="Boucing" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m01-semana02/blob/main/imgs/tabela-fps-jogoveio.png)">
</picture>

No seu projeto, usaremos bibliotecas em que você escolhe o FPS, mas nessa primeiro momento, isso não deve impactar na qualidade da sua solução.

Veja esse exemplo de como fazer animações em JS:

## Spritesheets

Em computação gráfica, um **spritesheets** ou **Atlas de Textura** é uma imagem que contém várias imagens menores, geralmente agrupadas para reduzir as dimensões gerais. Um atlas pode consistir em imagens de tamanho uniforme ou imagens de dimensões variadas.

No seu computador, usando o Visual Studio, crie um novo arquivo com o nome **index.html**. Dentro deste arquivo index.html , inclua o seguinte código:

```
<!DOCTYPE html>
<html>
    <head>
        <script src="//cdn.jsdelivr.net/npm/phaser@3.24.1/dist/phaser.min.js"></script>
    </head>
    <body>
        <div id="game"></div>
        <script>

            const phaserConfig = {
                type: Phaser.AUTO,
                parent: "game",
                width: 1280,
                height: 720,
                scene: {
                    init: initScene,
                    preload: preloadScene,
                    create: createScene,
                    update: updateScene
                }
            };

            const game = new Phaser.Game(phaserConfig);

            function initScene() {}
            function preloadScene() {}
            function createScene() {}
            function updateScene() {}

        </script>
    </body>
</html>
```
A marcação HTML e o código JavaScript acima criarão uma tela para renderizar o jogo. Como estamos usando **Phaser.AUTO**, talvez não estejamos usando uma tela, mas sim WebGL, mas vamos nos referir a ela como tela. O que é WebGL?

*WebGL é uma API em JavaScript, disponível a partir do novo elemento canvas da HTML5, que oferece suporte para renderização de gráficos 2D e gráficos 3D. Pode ser implementado em uma aplicação web sem a necessidade de plug-ins no navegador. A especificação foi lançada, sob versão 1.0, em 10 de fevereiro de 201.*
Se seu PC não estiver com o WebGL ativado, siga [esse tutorial](https://pt.wikihow.com/Ativar-o-WebGL) para ativá-lo.


No restante deste tutorial, passaremos nosso tempo nas funções preloadScenee createScene. No entanto, as funções initScenee updateSceneprovavelmente seriam usadas em um tutorial mais extenso.

## Funções

Uma função em JavaScript é um bloco de código reutilizável que executa uma tarefa específica. Ela é definida uma vez e pode ser chamada (ou invocada) múltiplas vezes, permitindo uma organização eficiente do código, modularidade e reutilização de lógica.

## Referência

[W3School](https://www.w3schools.com/js/js_functions.asp)

## Tipos de Funções

Existem dois tipos principais de funções em JavaScript: funções nomeadas e funções anônimas.

1. **Funções Nomeadas:**
   Uma função nomeada é declarada usando a palavra-chave `function` seguida pelo nome da função e, opcionalmente, uma lista de parâmetros entre parênteses. Aqui está a sintaxe básica:
   ```javascript
   function nomeDaFuncao(parametro1, parametro2) {
       // Corpo da função
   }
   ```

   Exemplo:
   ```javascript
   function soma(a, b) {
       return a + b;
   }
   ```

   Neste exemplo, a função `soma` aceita dois parâmetros (`a` e `b`) e retorna a soma desses dois valores quando invocada.

2. **Funções Anônimas:**
   Uma função anônima é uma função sem um nome associado e pode ser atribuída a uma variável ou passada como um argumento para outra função.
   ```javascript
   let nomeDaVariavel = function(parametro1, parametro2) {
       // Corpo da função
   };
   ```

   Exemplo:
   ```javascript
   let multiplica = function(x, y) {
       return x * y;
   };
   ```

   Neste exemplo, uma função anônima é atribuída à variável `multiplica`, que aceita dois parâmetros (`x` e `y`) e retorna o produto desses dois valores quando invocada.

Você deve estar perguntando o que é **let** no exemplo acima?

No JavaScript, `let` é uma palavra-chave padrão para declarar uma variável localmente em um escopo de bloco. Isso significa que a variável declarada com `let` está disponível apenas dentro do bloco em que foi declarada, incluindo blocos de função, blocos `if`, `for`, `while`, entre outros.

3. **Invocando uma Função:**
   Para chamar (ou invocar) uma função, você simplesmente usa o nome da função seguido por parênteses contendo quaisquer argumentos necessários.
   ```javascript
   let resultado = soma(2, 3); // resultado será 5
   ```

   ```javascript
   let resultadoMultiplicacao = multiplica(4, 5); // resultadoMultiplicacao será 20
   ```

   No primeiro exemplo, a função `soma` é chamada com os argumentos `2` e `3`, e retorna `5`. No segundo exemplo, a função `multiplica` é chamada com os argumentos `4` e `5`, e retorna `20`.

Esses são os conceitos básicos de funções em JavaScript. Elas são uma parte essencial da linguagem, permitindo que você escreva código modular e reutilizável, tornando seus programas mais organizados e fáceis de entender.

