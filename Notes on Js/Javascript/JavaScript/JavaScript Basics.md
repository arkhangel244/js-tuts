- JavaScript is a dynamic,weakly typed language which is compiled at runtime.
- JavaScript is interpreted on the fly, i.e. its not compiled previously and it happens only when its executed. 
- Dynamic interpreted programming languages are known for their flexibility and ease of use, where variable types are checked during runtime, not before. Though keep this in mind it leads to lots of errors but the decision was made 
- Weakly typed programming languages allows for implicit conversions between data types, meaning that the compiler or interpreter will automatically try to convert a value from one type to another when needed, rather than throwing an error. It also assumes datatypes automatically.
- JavaScript helps us to add dynamic behaviour into Web-pages.
- It uses a single thread for executing the program.


### How do web-pages work

Below is an image of how websites work
![[browser_work.png]]

In the following image you can see that when a user uses a client browser for on his or her desktop the client needs to generate request to a server in order to load a web-page. The request sent by the client is processed at the server and the server then sends the requested page(i.e the contents in HTML and CSS). 
Now let's look into how a basic HTML and CSS works.

## HTML

[[HTML]] or Hyper Text Markup Language is the language of the web. They have got a few defined blocks used to make up a web-page. They all have given properties with a given view that stays same throughout browser engines. 

## CSS

[[CSS]] or Cascading Style Sheets are used to change the basic properties of the HTML blocks so it changes and becomes more aesthetically pleasing and can produce a signature content based on a website.



So as we can see both of these are not programmable. They are static and cannot be changed. So JavaScript came up on the client side in order to put some life/dynamic behaviour into the pages. JavaScript processes the contents of the static page and can change the properties of the elements in the web-page. 

![[jsengine.png]]

This is a snapshot provides us a look into how JavaScript works along with HTML-CSS to give life to our web pages. At first our code is downloaded by our browser then the JavaScript engine (depends on the browser we are using like V8 or Spider
Monkey) looks for *js* codes. Once the code is found the engine compiles and interprets to machine code and then executes it on a single thread. For this reason there are a few caveats that comes with JavaScript which we will look into later. 

JavaScript runs on a huge variety of hosted environment the main being a ==Browser Environment==, browser side environment is a restricted environment where it is used to send dynamic request change properties and fetch data for the website on the go. The browser environment is constricted only to the browser and is sand-boxed. It can't use the file-systems on the computer as it would definitely pose security risks. 
On the other hand there is also ==Server Side Environment==, this environment runs a true programming language, i.e. the JavaScript engine runs directly on the Operating system and thus can use the whole power of system, though it runs on a single thread it can be used to builds servers. We will look into it in Node.js part later and how it can be used to make servers.  