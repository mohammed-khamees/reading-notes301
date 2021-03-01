# SENDING FORM DATA

The `action` _attribute_ defines where the data gets sent. Its value must be a valid `relative` or `absolute` URL. If this _attribute_ isn't provided, the data will be sent to the URL of the page containing the `form` — the current page.

In this example, the data is sent to an absolute _URL_ — `https://example.com`:

`<form action="https://example.com">`

Here, we use a `relative` URL — the data is sent to a different URL on the same origin:

`<form action="/somewhere_else">`

The `names` and `values` of the non-file form controls are sent to the server as name=value pairs joined with ampersands. The `action` value should be a file on the server that can handle the incoming data, including ensuring server-side validation. The server then responds, generally handling the data and loading the URL defined by the action attribute, causing a new page load (or a refresh of the existing page, if the action points to the same page).

How the data is sent depends on the `method` attribute.

The `method` attribute defines how data is sent. The **HTTP protocol** provides several ways to perform a request; **HTML** form data can be transmitted via a number of different methods, the most common being the `GET` method and the `POST` method

To understand the difference between those two methods, let's step back and examine how HTTP works. Each time you want to reach a resource on the Web, the browser sends a request to a **URL**. An **HTTP request** consists of two parts:

- a header that contains a set of global metadata about the browser's capabilities
- a body that can contain information necessary for the server to process the specific request.
