# Flexbox and Templating

In addition to the above-mentioned modes, **CSS3** provides another layout mode Flexible Box, commonly called as Flexbox.

Using this mode, you can easily create layouts for complex applications and web pages. Unlike floats, **Flexbox** _layout gives complete control over the direction, alignment, order, size of the boxes._

Features of **Flexbox** Following are the notable features of **Flexbox layout** :

- `Direction` − **You can arrange the items on a web page in any direction such as left to right, right to left, top to bottom, and bottom to top.**

- `Order` − **Using Flexbox, you can rearrange the order of the contents of a web page.**

- `Wrap` − **In case of inconsistent space for the contents of a web page (in single line), you can wrap them to multiple lines (both horizontally) and vertically.**

- `Alignment` − **Using Flexbox, you can align the contents of the webpage with respect to their container.**

- `Resize` − **Using Flexbox, you can increase or decrease the size of the items in the page to fit in available space.**

example:

```
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  ...
</div>
```

```
.container {
  display: flex;
}

.item {
  flex-grow: 1;
  height: 100px;
}

.item + .item {
  margin-left: 2%;
}
```

```
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.item {
  width: 32%;
  padding-bottom: 32%; /* Same as width, sets height */
  margin-bottom: 2%; /* (100-32*3)/2 */
  position: relative;
}
```
