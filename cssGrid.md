# CSS GRID

The structure of the `grid`, like how many `rows` and `columns` it has and their sizing, is controlled by properties applied to the **grid container**. Placement of grid items is determined by CSS properties applied to the child elements inside the grid container.

A grid container is defined by setting the `display` to `grid` or `inline-grid` on an element. This creates a `grid` formatting context for its content, which are laid out into a grid. The `grid` formatting context only applies to child elements and does not extend to grandchild elements and beyond.

example:

```
.grid {
  display: grid;
  grid-template-columns: 150px 150px;
  grid-template-rows: 150px 150px;
  grid-auto-columns: 50px 75px;
  grid-auto-flow: column;
}

.item {
  grid-column: 8;
}
```
