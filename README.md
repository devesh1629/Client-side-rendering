This project is created using this article
https://javascript.plainenglish.io/back-to-basics-client-side-rendering-a-react-app-using-express-js-c828e3664b88

Express().static

To serve our react app, we will use the built-inexpress().static middleware from Express.js. An Express.js application is basically a series of middleware and routing functions. Middleware functions tell Express.js what to do with incoming requests. Whether to transform the request data, sending back response, or passing it to the next middleware. The express().static middleware instructs express to serve static files from a specified directory.

We use Node’s path module to get the path to our public directory where our bundled react app (in a JavaScript file called bundle.js) and its corresponding html (index.html) is situated. Using the public directory path, we instruct express to statically serve the files in the said directory.

We have successfully served our react app using express.js back end. The way our react app is rendered in this project is through the client side (thus the name ‘client-side rendering’). When requests come to the home route, we instruct express().static to send back the index.html file along with the JavaScript and css files that the html file requires. Our index.html file only contains an empty div element with the id ‘root’ inside the body tag. The actual rendering of the page UI is done by the JavaScript file, bundle.js, where all our react code resides. This is why it is called ‘client-side rendering’, the UI rendering process is done in the client side by the client’s browser after the JavaScript files have been successfully sent to and downloaded by the client browser. 