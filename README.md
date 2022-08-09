# Node-Interview-Day1

1. What is NPM?
Ans : Npm is stand for Node Package Manager.
It is the package manager for the Node JavaScript platform. It puts modules in place so that node can find them, and manages dependency conflicts intelligently. It is extremely configurable to support a wide variety of use cases. Most commonly, it is used to publish, discover, install, and develop node programs.
The NPM program is installed on your computer when you install Node.js. NPM is already ready to run on your computer!.

_________________________________________________________________________________________________________________________________________________________

2. What are the modules in Node.js?
In Node.js, Modules are the blocks of encapsulated code that communicates with an external application on the basis of their related functionality.
Modules can be a single file or a collection of multiples files/folders.
The reason programmers are heavily reliant on modules is because of their re-usability as well as the ability to break down a complex piece of code into manageable chunks.
Modules are of three types:

. Core Modules/Internal modules local Modules/Custom modules Third-party Modules

1.Core Modules: Node.js has many built-in modules that are part of the platform and comes with Node.js installation. These modules can be loaded into the program by using the require function.

2. The require() function will return a JavaScript type depending on what the particular module returns. ex:- http creates an HTTP server in Node.js.
Local Modules: Unlike built-in and external modules, local modules are created locally in your Node.js application. Let’s create a simple calculating module that calculates various operations. Another file can use its exported functionality using the require() function.

3.Third-party modules: Third-party modules are modules that are available online using the Node Package Manager(NPM). These modules can be installed in the project folder or globally. Some of the popular third-party modules are mongoose, express, angular, and react.

________________________________________________________________________________________________________________________________________________________

4. What is the purpose of the module.exports?
Module exports are the instruction that tells Node. js which bits of code (functions, objects, strings, etc.) to “export” from a given file so other files are allowed to access the exported code.

_________________________________________________________________________________________________________________________________________________________

5. Difference between default export and named export?

Named Export: (export)
With named exports, one can have multiple named exports per file. Then import the specific exports they want surrounded in braces. The name of imported module has to be the same as the name of the exported module.

example: import { MyComponent, MyComponent2 } from "./MyComponent";
         export const MyComponent = () => {}
         export const MyComponent2 = () => {}

Default Export: (export default)
One can have only one default export per file. When we import we have to specify a name and import like:

example: import MyDefaultComponent from "./MyDefaultExport";
         export default MyComponent;
         
_________________________________________________________________________________________________________________________________________________________

5. How do you import any module in Node.js
 1. Importing functions or modules enhances the reusability of code.

 2. Importing a Module: We need to import the module to use the functions defined in the imported module in another file. The result returned by require() is stored in a variable which is used to invoke the functions using the dot notation.
 
    const f = require('./func')
    
_________________________________________________________________________________________________________________________________________________________

6. What are the different types of HTTP requests?
   The set of common methods for HTTP/1.1 is defined below and this set can be expanded based on requirements. These method names are case sensitive and they must be used in uppercase.
   
 1. GET
The GET method is used to retrieve information from the given server using a given URI. Requests using GET should only retrieve data and should have no other effect on the data.

2. POST
A POST request is used to send data to the server, for example, customer information, file upload, etc. using HTML forms.

3. DELETE
Removes all current representations of the target resource given by a URI.

4. HEAD
Same as GET, but transfers the status line and header section only.

_________________________________________________________________________________________________________________________________________________________

7. Explain the concept of middleware in Node.js. Explain CORS
Ans : Express.js is a routing and Middleware framework for handling the different routing of the webpage and it works between the request and response cycle.

Middleware gets executed after the server receives the request and before the controller actions send the response.

Middleware has the access to the request object, responses object, and next, it can process the request before the server send a response. An Express-based application is a series of middleware function calls.

Middleware Chaining: Middleware can be chained from one to another, Hence creating a chain of functions that are executed in order. The last function sends the response back to the browser. So, before sending the response back to the browser the different middleware process the request.

The next() function in the express is responsible for calling the next middleware function if there is one.

app.get(path, (req, res, next) => {}, (req, res) => {})

CORS

CORS (Cross-Origin Resource Sharing) is a mechanism by which data or any other resource of a site could be shared intentionally to a third party website when there is a need. Generally, access to resources that are residing in a third party site is restricted by the browser clients for security purposes.

function httpGetAction(urlLink) { var xmlHttp = new XMLHttpRequest(); xmlHttp.open( "GET", urlLink, false ); xmlHttp.send(); return xmlHttp.responseText; }

npm i CORS

_________________________________________________________________________________________________________________________________________________________

8. What is Express. how it helps you to create a backend application
Express.js: Express is a small framework that sits on top of Node.js’s web server functionality to simplify its APIs and add helpful new features. It makes it easier to organize your application’s functionality with middle ware and routing. It adds helpful utilities to Node.js’s HTTP objects. It facilitates the rendering of dynamic HTTP objects.

More features than Node.js

It is used to build web-apps using approaches and principles of Node.js.

Routing is provided.

It requires less coding time.

Uses middleware for the arrangement of functions systematically server-side.

import by const express = require ("express")

_________________________________________________________________________________________________________________________________________________________

9. Explain min 5 status codes gets used in Backend development?

An HTTP status code is a message a website's server sends to the browser to indicate whether or not that request can be fulfilled. Status codes specs are set by the W3C. Status codes are embedded in the HTTP header of a page to tell the browser the result of its request.
102 PROCESSING Processing 200 OK OK 400 BAD_REQUEST Bad Request 401 UNAUTHORIZED Unauthorized 402 PAYMENT_REQUIRED Payment Required 403 FORBIDDEN Forbidden 404 NOT_FOUND Not Found 500 INTERNAL_SERVER_ERROR Internal Server Error 503 - Service Unavailable

_________________________________________________________________________________________________________________________________________________________

10. What is node.js ?
Node.js: Node.js is an open source and cross-platform runtime environment for executing JavaScript code outside of a browser. You need to remember that NodeJS is not a framework and it’s not a programming language. Most of the people are confused and understand it’s a framework or a programming language. We often use Node.js for building back-end services like APIs like Web App or Mobile App. It’s used in production by large companies such as Paypal, Uber, Netflix, Walmart and so on.

Node.js is a platform for building the i/o applications which are server-side event-driven and made using JavaScript.

It is used to build server-side, input-output, event-driven apps.

It is built on Google’s V8 engine.

C, C++, JavaScript can be used

Run-time platform or environment designed for server-side execution of JavaScript.

Routing is not provided.

No Middleware

_________________________________________________________________________________________________________________________________________________________

11. Difference between HTTP and HTTPS?

HTTPS stands for Hyper Text Transfer Protocol Secure. It is highly advanced and secure version of HTTP. It uses the port no. 443 for Data Communication.

HTTP also allows you to create a secure encrypted connection between the server and the browser. It offers the bi-directional security of Data.

HTTP lacks security mechanism to encrypt the data whereas HTTPS provides SSL or TLS Digital Certificate to secure the communication between server and client. HTTP operates at Application Layer whereas HTTPS operates at Transport Layer. HTTP by default operates on port 80 whereas HTTPS by default operates on port 443. HTTP transfers data in plain text while HTTPS transfers data in cipher text (encrypt text). HTTP is fast as compared to HTTPS because HTTPS consumes computation power to encrypt the communication channel.

HTTP It is hypertext transfer protocol. It is less secure as the data can be vulnerable to hackers. It uses port 80 by default. HTTP URLs begin with http:// It’s a good fit for websites designed for information consumption like blogs. HTTP does not scramble the data to be transmitted. HTTP website do not need SSL. Fast

HTTPS Vulnerable to hackers It Is highly secure as the data is encrypted before it is seen across a network. Slower than HTTP HTTPS requires SSL certificate. HTTPS scrambles the data before transmission. If the website needs to collect the private information such as credit card number, then it is a more secure protocol. HTTPs URLs begin with https:// It was use port 443 by default. It is designed to prevent hackers from accessing critical information. It is secure against such attacks. It is hypertext transfer protocol with secure. 

_________________________________________________________________________________________________________________________________________________________

12. What are JWT tokens?

Ans : JSON Web Token is a proposed Internet standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims. The tokens are signed either using a private secret or a public/private key.

In authentication, when the user successfully logs in using their credentials, a JSON Web Token will be returned and must be saved locally (typically in local or session storage, but cookies can also be used), instead of the traditional approach of creating a session in the server and returning a cookie. For unattended processes the client may also authenticate directly by generating and signing its own JWT with a pre-shared secret and pass it to a OAuth compliant service like so:

grant_type=urn:ietf:params:oauth:grant-type:jwt-bearer&assertion=eyJhb...






