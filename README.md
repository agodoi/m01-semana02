# Prática de computação: desenvolvendo animações com código

## Objetivos

Foco em lógica de programação, especialmente em aplicação de operações lógicas e aritméticas para controle de personagem no jogo, incluindo animação da imagem com sprites e utilização de funções e laços de repetição para funcionamento do jogo como um todo.

## Assuntos relacionados
- Algoritmos para a solução de problemas de baixa complexidade
- Programação orientada a objetos

## Revisão da Semana 01
HTML --> linguagem estática para escrever documentos. Antigamente, a Internet era feita de páginas estáticas como a imagem a seguir:

https://github.com/agodoi/m01-semana02/blob/main/imgs/088b90c_11088-1c3ely2.wvaxo2mx6r.png

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

https://github.com/agodoi/m01-semana02/blob/main/imgs/fig01.png

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

## Spritesheets

Em computação gráfica, um **spritesheets** ou **Atlas de Textura** é uma imagem que contém várias imagens menores, geralmente agrupadas para reduzir as dimensões gerais. Um atlas pode consistir em imagens de tamanho uniforme ou imagens de dimensões variadas
