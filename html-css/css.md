# CSS

CSS significa Cascading Style Sheets.

Utilizado em conjunto com as outras linguagens HTML e JS, conferindo um conjunto de estilos como propriedades de cada elemento desejado na página HTML.

## TERMOS COMUNS EM CSS

- SELETOR

Seleciona qual elemento (s) está sofrendo alteração em seu estilo.

Pode sofrer especificações, identificando elementos específicos elementos específicos (id, nomes, classes).

- PROPRIEDADES

Estilos adicionados ao elemento selecionado 

- VALOR

Comportamento da propriedade

```css
|--> SELETOR
p {
	|--> PROPRIEDADE
	color : orange;
	font-size : 12px;
				  |-->VALOR
}
```

## REFINANDO OS SELETORES

- TYPE

Seleção por tipo do elemento

```css
div {...}
Todo elemento com tag <div>
```

- CLASSE

Selecionamos elementos a partir de sua classe

```css
div.suaclasse { ... }
.suaclase { ... }
```

Exemplo 1: elementos com tag <div> e classe "suaclasse".

Exemplo 2: elementos de qualquer tag, com classe "suaclasse".

OBS .: podemos determinam um objeto no HTML com várias classes, de modo a modularizar a escolha de estilo:

```html
<a class="btn btn-danger">...</a>
<a class="btn btn-success">...</a>
```

Neste caso, temos uma classe comum (btn), na qual a fonte de tamanho 16 pixels será padrão. Depois temos 2 especificações de modo a individualizar as outras 2 "sub-classes"

```css
.btn {
  font-size: 16px;
}
.btn-danger {
  background: red;
}
.btn-success {
  background: green;
}
```

- ID

Selecionamos, especificamente, um elemento a partir do seu ID.

```css
div#seuID { ... }
#seuID { ... }
```

Exemplo 1: elemento com tag <div> e id "seuID".

Exemplo 2:  elemento de qualquer tag, com id "seuID".

## REFERENCIANDO O CSS NO HTML

Dentro do HTML

```html
<head>
	<link rel="stylesheet" href="main.css">
</head>
```