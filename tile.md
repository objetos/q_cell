---
weight: 1
draft: false
---

# `TILE`

Static method for drawing cell tiles.

Used by [drawQuadrille]({{< ref "draw_quadrille" >}}).

# Example

{{< p5-global-iframe lib1="https://cdn.jsdelivr.net/gh/objetos/p5.quadrille.js/p5.quadrille.js" id="tile" width="130" height="130" >}}
`use strict`;
function setup() {
  createCanvas(105, 105);
}

function draw() {
  background('yellow');
  Quadrille.TILE( { graphics: this, outlineWeight: 9 } );
}
{{< /p5-global-iframe >}}

{{< details title="code" open=false >}}
```js
function setup() {
  createCanvas(105, 105);
}

function draw() {
  background('yellow');
  Quadrille.TILE( { graphics: this, outlineWeight: 9 } );
}
```
{{< /details >}}

# Syntax

> `Quadrille.TILE({graphics, [cellLength], [outline], [outlineWeight]})`

# Parameters

| parameter  | description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| graphics   | [p5.Graphics](https://p5js.org/reference/#/p5.Graphics): renderer target                    |
| cellLength | Number: edge length in pixels default is [Quadrille.CELL_LENGTH]({{< ref "cell_length" >}}) |
| outline       | [p5.Color](https://p5js.org/reference/#/p5.Color) representation: edge color default is [Quadrille.OUTLINE]({{< ref "outline" >}}) |
| outlineWeight | Number: edge weight default is [Quadrille.OUTLINE_WEIGHT]({{< ref "outline_weight" >}}). Use `0` to discard all edges |