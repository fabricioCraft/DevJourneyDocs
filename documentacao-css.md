# Sumário
- [Representando cores com CSS](#representando-cores-com-css)
- [Harmonia de cores](#harmonia-de-cores)
    - [Círculo Cromático](#círculo-cromático)
        - [Cores Primárias](#cores-primárias)
        - [Cores Secundárias](#cores-secundárias)
        - [Cores Terciárias](#cores-terciárias)
    - [Cores Complementares](#cores-complementares)
    - [Cores Análogas](#cores-análogas)
        - [Cores Análogas Relacionadas](#cores-análogas-relacionadas)
    - [Cores Triádicas](#cores-triádias)
    - [Cores Quadráticas](#cores-qudráticas)
    - [Cores Tetrádicas](#cores-tetrádicas)
    - [Monocromia](#monocromia)


## Representando cores com CSS

 Exitem 3 formas de fazer a representação de cores em CSS:

 - Representando-as pelos nomes das cores

 ```html
 <h2 style="background-color: blue; color: white;">Exemplo de Cores</h2>
 ```

 - Representando-as por códigos hexadecimais, onde o tom mais baixo é 0 que
 significa tons mais escuros e o tom mais forte é 255 que significa tons mais claros.

 **A denominação RGB vem de: R(Red), G(Green) e B(Blue). Quanto mais baixo, mais escuro é a cor, quanto mais alto, mais claro é a cor**

 ```html
  <h2 style="background-color: rgb(0, 0, 255); color: rgb(255, 255, 255);">Exemplo de Cores</h2>
 ```

 - Representando-as por HSL
    - H(Hue ou Matriz) - Define a cor do objeto. No modelo HSL, o matiz é representado por um ângulo de 0 a 360 graus, onde 0 e 360 correspondem ao vermelho, 120 ao verde e 240 ao azul.

    - S(Saturation) - Define a intensidade da cor. Quanto maior a saturação, mais vibrante e intensa será a cor. No modelo HSL, a saturação é representada por um valor de 0 a 100%, onde 0% corresponde a uma cor completamente desaturada (tons de cinza) e 100% a uma cor totalmente saturada (corestão vibrantes).

    - L(Luminosity) - Define a claridade da cor.No modelo HSL, a luminosidade é representada por um valor de 0 a 100%, onde 0% corresponde ao preto absoluto e 100% ao branco absoluto. Valores intermediários representam diferentes níveis de luminosidade, permitindo criar uma ampla gama de tons e nuances de uma mesma cor.

```html
<h2 style="background-color: hsla(0, 100%, 50%, 0.928); color: hsl(0, 0, 100);">Exemplo de Cores</h2>
```
## Harmonia de cores

Uma paleta de cores tem de 3 à 5 cores.

### Círculo Cromático

Ao fazer um corte central no círculo, entre o vermelho-arroxeado e o amarelo-esverdeado, do lado esquerdo estão as cores frias e do lado direito as cores quentes

#### Cores primárias

- Amarelo
- Vermelho
- Azul

Estão simétricas no círculo cromático e formam um triângulo, formando uma harmonia.

#### Cores Secundárias

- Laranja
- Violeta
- Verde

#### Cores Terciárias

Mistura das cores primárias e secundárias. Elas são de tons pastéis e formam um hexágono no círculo cromático.

### Cores Complementares

Ao escolher as cores para compor um site, depois de escolher uma cor, a cor que mais combina com a cor escolhida está exatamente na sua oposição.

### Cores Análogas

São cores que não tem muito contraste uma com a outra, mas ainda assim são perceptives. Elas se sencontram ao lado uma da outra, ou seja, são cores vizinhas.

#### Cores Análogas Relacionadas

```html

<img href="./images/cores-analogas-relacionadas.png" alt="cores análogas relacionadas">
```
### Cores Triádias

Combinação de três cores que estão igualmente espaçadas no círculo cromático, formando um triângulo equilátero.

```html
<img href= "./images/cores-triadicas.webp" alt="cores triadicas">
```

### Cores Qudráticas

É uma harmonia semelhante à harmonia de cores triádicas, exceto que neste esquema harmónico existem quatro cores, todas equidistantes no círculo cromático.

```html
<img href ="./images/cores-quadraticas.webp" alt="cores quadraticas">
```

### Cores Tetrádicas

Esquema de cores que se caracteriza por uma paelte de quatro cores uniformemente distribuídas no círculo cromático, formando dois pares de cores complementares.

Para obter as cores tetrádicas, é necessário traçar um retângulo comprido no centro do círculo cromático.

```html
<img href="./images/cores-tetradicas.png" alt="cores tetradicas">
```

### Monocromia

Trabalha somente com uma cor com a mudança de duas características, luminosidade e saturação.







