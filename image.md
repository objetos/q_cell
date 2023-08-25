---
weight: 4
draft: false
---

# `IMAGE`

Static method for drawing cells that are [p5.Image](https://p5js.org/reference/#/p5.Image) or [p5.Graphics](https://p5js.org/reference/#/p5.Graphics) instances.

Used by [drawQuadrille]({{< ref "draw_quadrille" >}}) and [sample]({{< ref "sample" >}}).

# Example

{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" id="image" width="190" height="190" >}}
`use strict`;
let al;

function preload() {
  al = loadImage('../abraham_lincoln.jpg');
}

function setup() {
  createCanvas(165, 165);
}

function draw() {
  background('blue');
  Quadrille.IMAGE( { graphics: this, cell: al, cellLength: width } );
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
let al;

function preload() {
  al = loadImage('abraham_lincoln.jpg');
}

function setup() {
  createCanvas(165, 165);
}

function draw() {
  background('blue');
  Quadrille.IMAGE( { graphics: this, cell: al, cellLength: width } );
}
```
{{< /details >}}

# Syntax

> `Quadrille.IMAGE({graphics, cell, [cellLength]})`

# Parameters

| parameter  | description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| graphics   | [p5.Graphics](https://p5js.org/reference/#/p5.Graphics): renderer target                    |
| cell       | [p5.Color](https://p5js.org/reference/#/p5.Color): cell contents                            |
| cellLength | Number: edge length in pixels default is [Quadrille.CELL_LENGTH]({{< ref "cell_length" >}}) |