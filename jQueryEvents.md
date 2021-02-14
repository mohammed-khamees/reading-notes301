# jQuery, Events, and The DOM

**jQuery** _is a JavaScript file you include in your pages._

Once included, it makes it faster and easier to write cross-browser JavaScript, based on two steps:

1. Using **CSS-style** se lectors to collect one or more nodes from the DOM tree.
2. Using **jQuery's** built-in methods to work with the elements in that selection.

jQuery's **CSS-style selector syntax** _makes it easier to select elements to work with_. It also has methods that
make it easier to traverse the DOM. jQuery makes it easier to handle events because the
event methods work across all browsers. jQuery offers methods that make it quick and simple to
achieve a range of tasks that JavaScript programmers commonly need to perform.

examples:

```
<p>This is a paragraph selected by a jQuery method.</p>
<p>This is also a paragraph selected by a jQuery method.</p>

$("p").addClass("selected")
```

```
<ul class="wishList">My Wish List</ul>

$("ul.wishList").append("<li>New blender</li>");
```
