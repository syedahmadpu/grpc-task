# grpc-task

REQUIREMENTS:

To begin with, we will need to install the required library and dependencies, we will be using Flask-RESTful, an extension for Flask which enables rapid development of REST API with minimal setup. 
run the app using command 'python api.py'

Install one of these API testing tool:

1. Postman
2. Insomnia

this app was tested on insomnia.

IMPLEMENTATION:

We will be creating a RESTful API that is used to store users details, which will have CRUD (Create, Read, Update, Delete) functions, allowing us to create new user, get details of existing user, update details of existing user and delete existing user.

One of the good quality of a REST API is that it follows standard HTTP method to indicate the intended action to be performed.

1. The get method is used to retrieve a particular user details by specifying the name:


 - We will traverse through our users list to search for the user, if the name specified matched with one of the user in users list, we will return the user, along with 200 OK, else return a user not found message with 404 Not Found. Another characteristic of a well designed REST API is that it uses standard HTTP response status code to indicate whether a request is being processed successfully or not.

2. The post method is used to create a new user.

 - We will create a parser by using reqparse we imported earlier, add the age and occupation arguments to the parser, then store the parsed arguments in a variable, args (the arguments will come from request body in the form of form-data, JSON or XML). If a user with same name already exists, the API will return a message along with 400 Bad Request, else we will create the user by appending it to users list and return the user along with 201 Created.
 
3. The put method is used to update details of user, or create a new one if it is not existed yet.

 - If the user already exist, we will update his/her details with the parsed arguments and return the user along with 200 OK, else we will create and return the user along with 201 Created.
 
4.The delete method is used to delete user that is no longer relevant:

 - By specifying users as a variable in global scope, we update the users list using list comprehension to create a list without the name specified (simulating delete), then return a message along with 200 OK.

Note: 
<string:name> indicates that it is a variable part in the route which accepts any name. 


by. - Syed Ahmad Abbasi

M.C.A. Final Year

Pondicherry University
