# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.


What is the purpose of a backend?

```bash
To handle requests from clients (frontend), and send back the appropriate response and data.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```bash
The controller sends parsed requests to the model layer to process business logic and interact with databases.
```

Which layer in the MVC pattern communicates with the model?

```bash
The controller layer.
```

Why don't we use views in our interpretation of the MVC pattern?

```bash
The view layer is old school, and alters the styling (CSS) of web pages - these days we can alter styling directly in the DOM using jQuery.
```

What does C.R.U.D stand for?

```bash
Create, Read, Update, Destroy
```

In which part of the MVC pattern can we find C.R.U.D actions?

```bash
In the routing.
```
List at least 5 standard actions that C.R.U.D corresponds to?

```bash
index, create, show, update, destroy
```

A user action fires a `GET` request for `person/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```bash
- The web server receives the GET request from the client
- The request is routed to a dispatcher, which selects the appropriate controller to send the GET request to
- The People controller parses the request into output that the People model can interpret
- The model sees that the GET request is for person1 only, and reads the database for that entry, and returns the data to the controller for person1
- The controller receives the person1 data from the people model, and sends it back to the client
```

What is the command to generate a new rails-api app?

```bash
rails-api new <api_name>
```

What is the command to start an instance of a rails server?

```bash
rails s
```

What are the commands to drop, create and migrate a database? (3 bullet points)

```bash
- db:drop
- db:create
- db:migrate
```

What is the command to scaffold a pet with a name and an age?

```bash
rails-api g scaffold pet name:string age:integer
```

List two advantages of using serializers? (2 bullet points)

```bash
- Can keep acess to certain api requests restricted, so hackers cant hack your shit
- Can access attributes with semantic plurals - i.e., if a serializer is generated on person data, you can search for has_many :people
```
