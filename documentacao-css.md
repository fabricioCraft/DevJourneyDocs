# Sumário
- [Represando cores com CSS](#representando-cores-com-css)

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
