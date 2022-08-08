# Node-Interview-Day1

What is NPM?
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


