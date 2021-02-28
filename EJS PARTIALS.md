# EJS PARTIALS

In real life we generally have more than one template. Moreover, if we create a website with several pages, it usually happens that a number of them are of the same design. The template systems should consider this aspect. Unfortunately, `ejs` doesn’t deal very well with this task. That’s why we are going to install a different templating system named `ejs-locals`

This is almost the same as ejs, but with a number of essential opportunities, such as `layout`, `block`, `partials`.

Install the module:

`npm i ejs-locals`

We’ve used the directive app.engine to inform Express that _“files with this extension need to be handled by the template engine require(`'ejs-locals`') instead of standard `ejs`.”_

Once more we draw your attention to the fact that there are many great temlating systems in `Node.js`. Here we use ejs just because it really resembles **HTML** and requires minimum time for studying.

`Layout` is some formatting that we insert into a separate file and specify, where we should insert body( `<%-body -%>`).

**example:**

```
<!DOCTYPE html>
<html lang="en">
<head>
    <%- include('../partials/head'); %>
</head>
<body class="container">

<header>
    <%- include('../partials/header'); %>
</header>

<main>
<div class="row">
    <div class="col-sm-8">
        <div class="jumbotron">
            <h1>This is great</h1>
            <p>Welcome to templating using EJS</p>
        </div>
    </div>

    <div class="col-sm-4">
        <div class="well">
            <h3>Look I'm A Sidebar!</h3>
        </div>
    </div>

</div>
</main>

<footer>
    <%- include('../partials/footer'); %>
</footer>

</body>
</html>
```
