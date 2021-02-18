# NODE.JS

A common task for a web server can be to open a file on the server and return the content to the client.

Here is how PHP or ASP handles a file request:

1. Sends the task to the computer's file system.
2. Waits while the file system opens and reads the file.
3. Returns the content to the client.
4. Ready to handle the next request.
5. Here is how Node.js handles a file request:

_Sends the task to the computer's file system._
_Ready to handle the next request._
_When the file system has opened and read the file, the server returns the content to the client._
**Node.js** eliminates the waiting, and simply continues with the next request.

**Node.js** runs single-threaded, non-blocking, asynchronously programming, which is very memory efficient.

Once you have downloaded and installed **Node.js** on your computer, let's try to display "Hello World" in a web browser.

Create a Node.js file named "myfirst.js", and add the following code:

```
onst express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})

```
