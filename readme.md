# Node js RESTful API

## What is API

API meaning Application Programming Interface, this also is a kind of "bridge", it let a piece of code comunicate with another.

## What is REST

REST meaning REpresentational State Transfer. The RESTful APIs are independent of the client server, they are composed of end-points and each end-point have his own http methods according of his logic, for example get, post, put, delete, and others. The client makes request to the end-point and the back-end server response with data.  

With RESTFul API we have a clearly separate architecture based in front-end and back-end. The back-end makes the processing of the data and the front-end renders them. 

## How the app works 

The application have his nucleus in the server and this server will call an express application. This express app will use some middleware to connect with de database, prevent cors errors, connect with the routes, catch errors and so on. 

When a request come to the app and if everything its ok, the request will be canalize to the respective route. In the respective route file it will be redirected to the respective controller according of the http request type, and in there, based on the object model, made the action on the database. 

![Alt text](explain.jpg?raw=true "Explain of the app")

### Middlewares
Middlewares have an important role in our Node - Express RESTful API, because basily our app is componed by middlewares. These are nothing just a kind of function with a minimun functionality with acces to the request's object , response's object  and the next middleware to be execute. This fuctions are called middlewares because are execute in the middle of the client request and the server response 

There are 5 kind of middleware:

* Application level:
    * They are middlewares that provides logic to the functionality of our app
* Router level:
* Built-in 
* Error handling
* Thirdparty 

### CORS
CORS meaning "Cross-Origin Resource Sharing", its a security mechanism by the browser and as the name indicates, it allows to share resources from different origins. And this is basily what our API does: share resources by requests from diferents origins. But, sometimes, if you dont indicate your "intention" of share resoures from diferents origins, it could create errors: CORS errors. You can handling CORS just with add some headers in the response


## API RESTful map

/

## Dependencies 

npm install --save express

npm install --save body-parser



* nodemon: 
    * re-start the server after save something in the project. It help us to  facilitate the development. Only for develpment propouses, not in production. 

* morgan:
    * Its a middleware who facilitate the logger of the http requests 

* body-parser:
    * Parse the body of the incoming request 

* Mongoose:
    * It facilitates the connection between Node.js and MongoDB.

For more, check packaje.json file

## Conclusions

* Espress apps are basically middlewares stacked
* We can prevent CORS errors just sending the correct headers in the response 


## Other things 

* "npm install --save" --> dependencys of the project
* "npm install --save-dev" --> dependencys of the project only in development 

## References 

https://academind.com/learn/node-js/building-a-restful-api-with/

https://www.youtube.com/watch?v=7YcW25PHnAA

https://expressjs.com/es/guide/using-middleware.html

