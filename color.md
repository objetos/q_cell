---
weight: 3
draft: false
---

# `COLOR`

Static method for drawing cells that are colors.

Used by [drawQuadrille]({{< ref "draw_quadrille" >}}) and [sample]({{< ref "sample" >}}).

# Example

{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" width="190" height="225" >}}
`use strict`;
let color;

function setup() {
  createCanvas(165, 165);
  color = createColorPicker('magenta');
}

function draw() {
  background('blue');
  Quadrille.COLOR( { graphics: this, cell: color.value(), cellLength: width } );
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
let color;

function setup() {
  createCanvas(165, 165);
  color = createColorPicker('magenta');
}

function draw() {
  background('blue');
  Quadrille.COLOR({graphics: this, cell: color.value(), cellLength: width});
}
```
{{< /details >}}

# Syntax

> `Quadrille.COLOR({graphics, cell, [cellLength]})`

# Parameters

| parameter  | description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| graphics   | [p5.Graphics](https://p5js.org/reference/#/p5.Graphics): renderer target                    |
| cell       | [p5.Color](https://p5js.org/reference/#/p5.Color): cell contents                            |
| cellLength | Number: edge length in pixels default is [Quadrille.CELL_LENGTH]({{< ref "cell_length" >}}) |