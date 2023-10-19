---
weight: 5
draft: false
---

# `STRING`

Static method for drawing cells that are filled with colors.

Used by [drawQuadrille]({{< ref "draw_quadrille" >}}) and [sample](https://objetos.github.io/p5.quadrille.js/docs/visual_computing/sample/).

# Example

{{< p5-global-iframe lib1="/p5.quadrille.js/docs/libs/p5.quadrille.js" width="205" height="230" >}}
`use strict`;
let string;

function setup() {
  createCanvas(180, 180);
  string = createInput('hola');
}

function draw() {
  background('tomato');
  Quadrille.STRING({ graphics: this, value: string.value(), cellLength: width, textZoom: 0.65 });
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
let string;

function setup() {
  createCanvas(180, 180);
  string = createInput('hola');
}

function draw() {
  background('tomato');
  Quadrille.STRING({ graphics: this, value: string.value(),
                     cellLength: width, textZoom: 0.65 });
}
```
{{< /details >}}

# Syntax

> `Quadrille.STRING({graphics, value, [cellLength], [textColor], [textZoom]})`

# Parameters

| parameter  | description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| graphics   | [p5.Graphics](https://p5js.org/reference/#/p5.Graphics): renderer target                    |
| value      | [p5.Color](https://p5js.org/reference/#/p5.Color): cell contents                            |
| cellLength | Number: edge length in pixels default is [Quadrille.CELL_LENGTH]({{< ref "cell_length" >}}) |
| textColor     | [p5.Color](https://p5js.org/reference/#/p5.Color) representation: text color default is [Quadrille.TEXT_COLOR]({{< ref "text_color" >}}) |
| textZoom      | Number:: text zoom level default is [Quadrille.TEXT_ZOOM]({{< ref "text_zoom" >}})       |
