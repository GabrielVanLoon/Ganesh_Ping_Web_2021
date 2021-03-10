# DATA & TABLES

Tables são usadas para facilitar a estruturação de dados, melhorando a interação do usuário com informações fornecidas pela página.

### CRIANDO UMA TABELA

Tabelas são feitas de dados, contidos em linhas e colunas.

Uma tabela possui, no mínimo, os seguintes elementos:

***< table > , < tr >*** (table row) e ***< td >*** (table data).

Para estruturar tabelas mais formais e adicionar valores semânticos, utilizamos tambem o elemento ***< th >*** (table header) assim como outros elementos adicionais.

***TABLE***

Utilizamos o elemento ***< table >*** para iniciar uma tabela na página em HTML. Significa que os dados serão apresentados de maneira tabular.

```html
<table>
...
</table>
```

***TABLE ROW***

Após definida e criada a tabela, podemos adicionar o elemento ***< tr >.***

Uma tabela pode conter inúmeros table rows.

```html
<table>
  <tr>
    ...
  </tr>
  <tr>
    ...
  </tr>
</table>
```

***TABLE DATA***

Após definida a tabela e adicionada as linhas desta (com o elemento **tr**), utilizamos o ***< td >*** para acrescentar células de dados.

Listando multiplos elementos table data um apos o outro, criará colunas dentro de cada table row.

```html
<table>
  <tr>
    <td>Don&#8217;t Make Me Think by Steve Krug</td>
    <td>In Stock</td>
    <td>1</td>
    <td>$30.02</td>
  </tr>
  <tr>
    <td>A Project Guide to UX Design by Russ Unger &#38; Carolyn Chandler</td>
    <td>In Stock</td>
    <td>2</td>
    <td>$52.94 ($26.47 &#215; 2)</td>
  </tr>
  <tr>
    <td>Introducing HTML5 by Bruce Lawson &#38; Remy Sharp</td>
    <td>Out of Stock</td>
    <td>1</td>
    <td>$22.23</td>
  </tr>
  <tr>
    <td>Bulletproof Web Design by Dan Cederholm</td>
    <td>In Stock</td>
    <td>1</td>
    <td>$30.17</td>
  </tr>
</table>
```

![Screenshot_from_2020-08-12_13-48-18.png](./Data&Tables/Screenshot_from_2020-08-12_13-48-18.png)

***TABLE HEADER***

Para designar um cabeçalho para cada coluna ou linha da célula, o elemento ***< th >,*** table header, deve ser adicionado.

O elemento **th** funciona de uma forma bem semelhante ao elemento **td,** mas dessa vez fornecendo valor semântico ao dado adicionado.

***Scope attribute***

Table headers devem ser utilizados entre colunas e linhas.

O atributo *scope* ajuda a identificar exatamente qual contexto da tabela aquele header esta referenciando.

O atributo scope pode receber os valores: col, row, colgroup e rowgroup.

A utilização de table headers e do atributo scope ajudam screen readers e tecnologias de assistência.

```html
<table>
  <tr>
    <th scope="col">Item</th>
    <th scope="col">Availability</th>
    <th scope="col">Qty</th>
    <th scope="col">Price</th>
  </tr>
  <tr>
    <td>Don&#8217;t Make Me Think by Steve Krug</td>
    <td>In Stock</td>
    <td>1</td>
    <td>$30.02</td>
  </tr>
  <tr>
    <td>A Project Guide to UX Design by Russ Unger &#38; Carolyn Chandler</td>
    <td>In Stock</td>
    <td>2</td>
    <td>$52.94 ($26.47 &#215; 2)</td>
  </tr>
  <tr>
    <td>Introducing HTML5 by Bruce Lawson &#38; Remy Sharp</td>
    <td>Out of Stock</td>
    <td>1</td>
    <td>$22.23</td>
  </tr>
  <tr>
    <td>Bulletproof Web Design by Dan Cederholm</td>
    <td>In Stock</td>
    <td>1</td>
    <td>$30.17</td>
  </tr>
</table>
```

![Screenshot_from_2020-08-12_13-54-50.png](./Data&Tables/Screenshot_from_2020-08-12_13-54-50.png)

***ATRIBUTO HEADERS***

O atributo headers é bem semelhante ao atributo scope.

Por padrão, scope pode ser utilizado apenas em elementos < th >.

No caso em que uma célula, tanto <td\> quanto <th\>, deve ser associada a diferente header, o atributo headers é utilizado.

O valor do atributo headers em um elemento <td\> ou <th\> deve relacionar ao valor do atributo *id* do elemento th que aquela célula de dado pertence.

### TABLE STRUCTURE

<caption\> , <thead\> , <tbody\> e <tfoot\>

***TABLE CAPTION***

O elemento <caption\> providencia uma descrição ou título para a tabela.

O elemento deve vir imediatamente apos a abertura da tag <table\>.

```html
<table>
  <caption>Design and Front-End Development Books</caption>
  ...
</table>
```

![Screenshot_from_2020-08-12_14-01-26.png](./Data&Tables/Screenshot_from_2020-08-12_14-01-26.png)

***TABLE HEAD, BODY & FOOT***

O conteúdo de uma tabela pode ser quebrado em diferentes grupos, incluindo head, body e foot, sendo respectivamente definidos pelos elementos ***< thead >, < tbody >** e **< tfoot >.***

 ***< thead >***

Envolve as linhas relacionadas ao headings da tabela para denotar o cabeçalho da tabela.

```html
 <thead>
    <tr>
      <th scope="col">Item</th>
      <th scope="col">Availability</th>
      <th scope="col">Qty</th>
      <th scope="col">Price</th>
    </tr>
  </thead>
```

***< tbody >***

Deve conter os dados que correspondem aos dados gerais da tabela.

```html
<tbody>
    <tr>
      <td>Don&#8217;t Make Me Think by Steve Krug</td>
      <td>In Stock</td>
      <td>1</td>
      <td>$30.02</td>
    </tr>
    ...
  </tbody>
```

***< tfoot >***

Originalmente, deveria vir logo após ao < thead >, no entanto, a partir do HTML5, o tfoot pode ser acrescentado para envolver elementos da tabela que são extras, que ultrapassam o counteúdo da tabela.

```html
  <tfoot>
    <tr>
      <td>Subtotal</td>
      <td></td>
      <td></td>
      <td>$135.36</td>
    </tr>
    <tr>
      <td>Tax</td>
      <td></td>
      <td></td>
      <td>$13.54</td>
    </tr>
    <tr>
      <td>Total</td>
      <td></td>
      <td></td>
      <td>$148.90</td>
    </tr>
  </tfoot>
```

EXEMPLO COMPLETO:

```html
<table>
  <caption>Design and Front-End Development Books</caption>
  <thead>
    <tr>
      <th scope="col">Item</th>
      <th scope="col">Availability</th>
      <th scope="col">Qty</th>
      <th scope="col">Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Don&#8217;t Make Me Think by Steve Krug</td>
      <td>In Stock</td>
      <td>1</td>
      <td>$30.02</td>
    </tr>
    ...
  </tbody>
  <tfoot>
    <tr>
      <td>Subtotal</td>
      <td></td>
      <td></td>
      <td>$135.36</td>
    </tr>
    <tr>
      <td>Tax</td>
      <td></td>
      <td></td>
      <td>$13.54</td>
    </tr>
    <tr>
      <td>Total</td>
      <td></td>
      <td></td>
      <td>$148.90</td>
    </tr>
  </tfoot>
</table>
```

![Screenshot_from_2020-08-12_14-14-49.png](./Data&Tables/Screenshot_from_2020-08-12_14-14-49.png)

### COMBINANDO MULTIPLAS CÉLULAS

Comumente é necessário que algumas célula seja combinada à outra sem quebrar o layout da linha e da coluna.

Para isso, podemos utilizar os atributos ***colspan*** e ***rowspan***.

Estes atributos podem ser acrescentados ao elementos ***<td>*** e ***<th>.***

colspan: expande uma única célula em múltiplas colunas dentro da tabela.

rowspan: expande uma única célula em múltiplas linhas.

Os atributos aceitam valores inteiros que indicam o número de células para expansão, sendo 1 o padrão.

```html
<th scope="col" colspan="2">Item</th>
```

### TABLE BORDERS

Duas propriedades dentro da estilização CSS são muito relevantes para a estilização de tabelas: ***border-collapse*** e ***border-spacing.***

***BORDER COLLAPSE PROPERTY***

A propriedade border-collapse determina o modelo de borda.

Existem 3 valores: collapse, separate e inherit.

Por padrão, o valor de border-collapse é separate, ou seja, cada borda será acumulada uma proxima à outra.

O valor collapse condensa as bordas em uma única, sendo a borda da célula, a borda primária.

```css
table {
  border-collapse: collapse;
}
th,
td {
  border: 1px solid #cecfd5;
  padding: 10px 15px;
}
```

![Screenshot_from_2020-08-12_14-24-16.png](./Data&Tables/Screenshot_from_2020-08-12_14-24-16.png)

***BORDER SPACING PROPERTY***

Border-spacing determina qual o tamnho aparece entre as bordas, nos casos de border-collapse igual à separate.

```css
table {
  border-collapse: separate;
  border-spacing: 4px;
}
table,
th,
td {
  border: 1px solid #cecfd5;
}
th,
td {
  padding: 10px 15px;
}
```

![Screenshot_from_2020-08-12_14-26-33.png](./Data&Tables/Screenshot_from_2020-08-12_14-26-33.png)

OBS:

Funciona apenas com border-collapse setado para separate.

Aceita dois valores numéricos, o primeiro correspondente ao espaço horizontal de espaçamento, enquanto o segundo corresponde ao espaçamento vertical.

### ADICIONANDO BORDAS NAS LINHAS

Dentro de uma tabela, não podemos acrescentar bordas à elementos ***<tr\>,*** sendo necessário outra estratégia para acrescentar bordas nas linhas.

Colocamos border-collapse setado para collapse.

Adicioanamos uma bottom border para cada table cell, sendo ela <th\> ou <td\>.

Podemos selecionar a borda da última linha da tabela utilizando a pseudo classe ***:last-chield*** para selecionar o último elemento <tr\> e selecionar todos os <td\> elementos daquela linha.

```css
table {
  border-collapse: collapse;
}
th,
td {
  border-bottom: 1px solid #cecfd5;
  padding: 10px 15px;
}
tfoot tr:last-child td {
  border-bottom: 0;
}
```

![Screenshot_from_2020-08-12_14-35-17.png](./Data&Tables/Screenshot_from_2020-08-12_14-35-17.png)

### TABLE STRIPING

Alternando a colaração do background de tabelas.

Uma forma de fazer isto, é acrescentar um atributo classe em um ou outro elemento <tr\> e setar sua coloração de fundo para elementos desta classe.

Outra forma de fazer é utilizar a pseudo-clase ***:nth-child***, com um elemento par ou impar para selecionar um ou outro elemento <tr\>.

```css
table {
  border-collapse: separate;
  border-spacing: 0;
}
th,
td {
  padding: 10px 15px;
}
thead {
  background: #395870;
  color: #fff;
}
tbody tr:nth-child(even) {
  background: #f0f0f2;
}
td {
  border-bottom: 1px solid #cecfd5;
  border-right: 1px solid #cecfd5;
}
td:first-child {
  border-left: 1px solid #cecfd5;
}
```

![Screenshot_from_2020-08-12_14-38-25.png](./Data&Tables/Screenshot_from_2020-08-12_14-38-25.png)

### ALINHAMENTO DE TEXTO

O alinhamento horizontal é feito a partir da prorpiedade ***text-align*** no CSS.

Para alinhar um texto verticalmente, utilizamos a propriedade ***vertical-align***. Aceita vários valores, sendo os mais populares: top, middle e bottom.

### Exemplo completo de uma tabela

HTML

```css
<table>
  <thead>
    <tr>
      <th scope="col" colspan="2">Item</th>
      <th scope="col">Qty</th>
      <th scope="col">Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <strong class="book-title">Don&#8217;t Make Me Think</strong>
        <span class="text-offset">by Steve Krug</span>
      </td>
      <td class="item-stock">In Stock</td>
      <td class="item-qty">1</td>
      <td class="item-price">$30.02</td>
    </tr>
    <tr>
      <td>
        <strong class="book-title">A Project Guide to UX Design</strong>
        <span class="text-offset">by Russ Unger &#38; Carolyn Chandler</span>
      </td>
      <td class="item-stock">In Stock</td>
      <td class="item-qty">2</td>
      <td class="item-price">$52.94 <span class="text-offset item-multiple">$26.47 &#215; 2</span></td>
    </tr>
    <tr>
      <td>
        <strong class="book-title">Introducing HTML5</strong>
        <span class="text-offset">by Bruce Lawson &#38; Remy Sharp</span>
      </td>
      <td class="item-stock">Out of Stock</td>
      <td class="item-qty">1</td>
      <td class="item-price">$22.23</td>
    </tr>
    <tr>
      <td>
        <strong class="book-title">Bulletproof Web Design</strong>
        <span class="text-offset">by Dan Cederholm</span>
      </td>
      <td class="item-stock">In Stock</td>
      <td class="item-qty">1</td>
      <td class="item-price">$30.17</td>
    </tr>
  </tbody>
  <tfoot>
    <tr class="text-offset">
      <td colspan="3">Subtotal</td>
      <td>$135.36</td>
    </tr>
    <tr class="text-offset">
      <td colspan="3">Tax</td>
      <td>$13.54</td>
    </tr>
    <tr>
      <td colspan="3">Total</td>
      <td>$148.90</td>
    </tr>
  </tfoot>
</table>
```

CSS

```css
table {
  border-collapse: separate;
  border-spacing: 0;
  color: #4a4a4d;
  font: 14px/1.4 "Helvetica Neue", Helvetica, Arial, sans-serif;
}
th,
td {
  padding: 10px 15px;
  vertical-align: middle;
}
thead {
  background: #395870;
  background: linear-gradient(#49708f, #293f50);
  color: #fff;
  font-size: 11px;
  text-transform: uppercase;
}
th:first-child {
  border-top-left-radius: 5px;
  text-align: left;
}
th:last-child {
  border-top-right-radius: 5px;
}
tbody tr:nth-child(even) {
  background: #f0f0f2;
}
td {
  border-bottom: 1px solid #cecfd5;
  border-right: 1px solid #cecfd5;
}
td:first-child {
  border-left: 1px solid #cecfd5;
}
.book-title {
  color: #395870;
  display: block;
}
.text-offset {
  color: #7c7c80;
  font-size: 12px;
}
.item-stock,
.item-qty {
  text-align: center;
}
.item-price {
  text-align: right;
}
.item-multiple {
  display: block;
}
tfoot {
  text-align: right;
}
tfoot tr:last-child {
  background: #f0f0f2;
  color: #395870;
  font-weight: bold;
}
tfoot tr:last-child td:first-child {
  border-bottom-left-radius: 5px;
}
tfoot tr:last-child td:last-child {
  border-bottom-right-radius: 5px;
}
```

![Screenshot_from_2020-08-12_14-45-26.png](./Data&Tables/Screenshot_from_2020-08-12_14-45-26.png)