# TIPOGRAFIA

**TIPOGRAFIA vs FONT**

A *typeface* is what we see. It is the artistic impression of how text looks, feels, and reads.

A *font* is a file that contains a typeface. Using a font on a computer allows the computer to access the typeface.

### FONT PROPERTIES

***Color***

```css
html {
	color : #effeea
}
```

***Font-Family***   

```css
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
```

***Font-Size***

```css
body {
  font-size: 14px;
}
```

***Font Style***

italic, oblique, and inherit

```css
.special {
  font-style: italic;
}
```

***Font Variant***

```css
.firm {
  font-variant: small-caps;
}
```

***Font Weight***

The numeric values 100, 200, 300, 400, 500, 600, 700, 800, and 900

```css
.daring {
  font-weight: bold;
}
```

***Line Height***

Distância entre duas linhas

O padrão é colocar 1.5 vezes o tamanho da fonte: 1.5 ou 150%

```css
body {
  line-height: 1.5;
}
```

### APLICANDO PROPRIEDADES DO TEXTO

***Text Align***

Utilizamos a propriedade text-align para alinhar o texto em uma página.

A propriedade aceita os valores: left, right, center, justify e inherit.

```css
p {
  text-align: center;
}
```

***Text Decoration***

A propriedade text-decoration permite fazer uma decoração do texto, com os seguintes valores: none, underline, overline, line-through e inherit.

```css
.note {
  text-decoration: underline;
}
```

Podemos colocar várias decorações ao mesmo tempo, separando os valores com vírgula.

***Text Indent***

A propriedade text-indent é usada para a indentação da primeira linha do texto.

```css
p {
  text-indent: 20px;
}
```

***Text Shadow***

text-shadow adiciona sombra ou multiplas sombras ao texto.

Recebe com parâmetro 4 argumentos.

sombra horizontal, sombra vertical, espalhamento da sombra e cor da sombra.

```css
p {
  text-shadow: 3px 6px 2px rgba(0, 0, 0, .3);
}
```

OBS ***Box Shadow***

A propriedade box-shadow cria uma caixa ao redor do objeto, criando uma sombra.

***Text Transform***

text-transform property accepts five values: none, capitalize, uppercase, lowercase, and inherit.

```css
p {
  text-transform: uppercase;
}
```

***Letter Spacing***

Propriedade letter-spacing para ajustar os espaços entre as letras

```css
p {
  letter-spacing: -.5em;
}
```

***Word Spacing***

word-spacing altera o espaço entre palavras

```css
p {
  word-spacing: .25em;
}
```