# EJS

**EJS** or **Embedded Javascript Templating** is a templating engine used by Node.js. Template engine helps to create an **HTML** template with minimal code. Also, it can inject data into HTML template at the client side and produce the final **HTML**. **EJS** is a simple templating language which is used to generate HTML markup with plain JavaScript. It also helps to embed JavaScript to **HTML** pages. To begin with, using EJS as templating engine we need to install EJS using given command: `npm install ejs --save`

The default behavior of EJS is that it looks into the ‘views’ folder for the templates to render. So, let’s make a ‘views’ folder in our main node project folder and make a file named `“home.ejs”` which is to be served on some desired request in our node project. The content of this page is:

```
<!DOCTYPE html>
<html>

<head>
    <title>Home Page</title>

    <style type="text/css" media="screen">
        body {
            background-color: skyblue;
            text-decoration-color: white;
            font-size:7em;
        }
    </style>
</head>

<body>
    <center>This is our home page.</center>
</body>

</html>
```

**Now, we will render this page on a certain request by the user as:**

```
app.get('/', (req, res)=>{

// The render method takes the name of the HTML
// page to be rendered as input
// This page should be in the views folder
// in the root directory.
res.render('home');

});

```

**Now, the page home.ejs will be displayed on requesting localhost. To add dynamic content this render method takes a second parameter which is an object. This is done as:**

```
app.get('/', (req, res)=>{

// The render method takes the name of the HTML
// page to be rendered as input.
// This page should be in views folder in
// the root directory.
// We can pass multiple properties and values
// as an object, here we are passing the only name
res.render('home', {name:'Akashdeep'});

});

var server = app.listen(4000, function(){
    console.log('listining to port 4000')
});

```

**Now, We will embed name to HTML page as:**

```
<!DOCTYPE html>
<html>
<head>
    <title>Home Page</title>
    <style type="text/css" media="screen">
        body {
            background-color: skyblue;
            text-decoration-color: white;
            font-size:7em;
        }
    </style>
</head>
<body>
    <center>
        This is our home page.<br/>
        Welcome <%=name%>, to our home page.
    </center>
</body>
</html>

```

**It is used to embed dynamic content to the page and is used to embed normal JavaScript. Now embedding normal JavaScript:**

```
app.get('/', (req, res)=>{

// The render method takes the name of the html
// page to be rendered as input.
// This page should be in views folder
// in the root directory.
var data = {name:'Akashdeep',
    hobbies:['playing football', 'playing chess', 'cycling']}

res.render('home', {data:data});
});

var server = app.listen(4000, function() {
    console.log('listining to port 4000')
});


```

**The final HTML content:**

```
<!DOCTYPE html>
<html>
<head>
    <title>Home Page</title>
    <style type="text/css" media="screen">
        body {
            background-color: skyblue;
            text-decoration-color: white;
            font-size:5em;
        }
    </style>
</head>

<body>
    Hobbies of <%=data.name%> are:<br/>

    <ul>
        <% data.hobbies.forEach((item)=>{%>
        <li><%=item%></li>
        <%});%>
    </ul>
</body>

</html>

```
