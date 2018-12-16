# API
API: 
Application Programming Interface is a set of software components that interact with one another. It provides a set of functions, variables, and object classes for the creation of an application, operating system or any other thing. 
Ajax is to make an asynchronous HTTP request. Data can be sent using the HTTP POST method and received using the HTTP GET method. 
Let’s take a look and make a GET request. 
To make an HTTP call in Ajax, you need to initialize a new XMLHttpRequest () method, specify the URL endpoint and HTTP method (in this case GET). Finally, we use the open () method to tie the HTTP method and URL endpoint together and call the send () method to fire off the request.
To make an HTTP call in Ajax, you need to initialize a new XMLHttpRequest () method, specify the URL endpoint and HTTP method (in this case GET). Finally, we use the open () method to tie the HTTP method and URL endpoint together and call the send () method to fire off the request.
const Http = new XMLHttpRequest();
const url=’';
Http.open("GET", url);
Http.send();
Http.onreadystatechange=(e)=>{
console.log(Http.responseText)
}
If you view your browser console, it will return an Array of data in JSON format. But how would we know if the request is done
The onreadystatechange property has two methods, ready State and status which allow us to check the state of our request.
By doing this we will get an error like 
Access to XMLHttpRequest at 'file://in.api load.compost' from origin 'null' has been blocked by CORS policy: Cross origin requests are only supported for protocol schemes: http, data, chrome, chrome-extensios.

To remove this error we have to install the CORS plugin to perform the operations.



