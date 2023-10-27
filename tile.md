---
weight: 1
draft: false
---

# `tile`

Static method for drawing cell tiles.

Used by [drawQuadrille]({{< ref "draw_quadrille" >}}).

# Example

{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" width="130" height="130" >}}
`use strict`;
function setup() {
  createCanvas(105, 105);
}

function draw() {
  background('yellow');
  Quadrille.tile( { graphics: this, outlineWeight: 9 } );
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
function setup() {
  createCanvas(105, 105);
}

function draw() {
  background('yellow');
  Quadrille.tile( { graphics: this, outlineWeight: 9 } );
}
```
{{< /details >}}

# Syntax

> `Quadrille.tile({graphics, [col], [row], [width], [height], [cellLength], [outline], [outlineWeight]})`

# Parameters

| parameter  | description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| graphics   | [p5.Graphics](https://p5js.org/reference/#/p5.Graphics): renderer target                    |
| col        | Number: cell col number [\[0..width\]]({{< ref "width" >}}) default is 0                    |
| row        | Number: cell row number [\[0..height\]]({{< ref "height" >}}) default is 0                  |
| width      | Number: total number of columns default is 1                                                |
| height     | Number: total number of rows default is 1                                                   |
| cellLength | Number: edge length in pixels default is [Quadrille.CELL_LENGTH]({{< ref "cell_length" >}}) |
| outline       | [p5.Color](https://p5js.org/reference/#/p5.Color) representation: edge color default is [Quadrille.OUTLINE]({{< ref "outline" >}}) |
| outlineWeight | Number: edge weight default is [Quadrille.OUTLINE_WEIGHT]({{< ref "outline_weight" >}}). Use `0` to discard all edges |