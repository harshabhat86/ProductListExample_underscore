# ProductListExample_underscore


## How to use 
Download the files into a folder and start an http server, you can do `python -m SimpleHTTPServer` and open the url localhost:8000 in your browser (Or the port on which you have deployed. )

## Some other things.
index.html is the page that takes care of rendering the page.
The project structure looks as below.

-index.html
|
|-- css
|   |-- index.css
|
|-- js
|    |__ index.js
|    |
|    |__ products.module.js
|    |
|    |--data
|    |    |__ products.json
|    |
|    |__lib
|        |__underscore.min.js



`index.js` is the view layer javascript that takes care of the rendering and templating logic.
   This takes care of all the templating and rendering part and the business logic is strictly not done here (this is a view layer.)

`products.module.js` is the module that acts as a model for the loaded products.
`products.module.js` has the getters and setters, search logic, search filter generators, etc.
  In this module, there is no view logic.

Products are loaded when the DOM is loaded by making a `GET` call to the products.json file and loaded on the client as an array of objects in the module `products.module.js`.

