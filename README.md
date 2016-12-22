# Rails Commands Quiz

Fork, clone, and write your answers directly in this file. Then submit a pull request.

### Question 1

I want to start a new Rails project/app called `BunnyApp`. What command should I type in the terminal?

```

rails new BunnyApp

or if you want to use Postgres instead:

rails new BunnyApp -d postgresql

```


### Question 2

I want to create a new model called `Bunny`, with the following attributes: name (string), color (string), and age (integer). What command(s) should I type in the terminal and/or Sublime? (In your answer, create both a migration and the model file.)


```

inside the new BunnyApp folder:
rails g model bunny name:string color:string age:integer

```

### Question 3

What does the command in Question 2 do, exactly? What files are created, where are they located, and what does the database look like at this time? Explain.


```

It will create a new model in the app/model folder called bunny.rb and it
will create a migration file to update the database with the new model
information (name, age, color). It will also create some test files. The database will not be changed until you do a migration on it (rake db:migrate)

```



### Question 4

I want to create a database and make it reflect the new model I created in Question 2. What command(s) should I type in the terminal?

```

rake db:drop db:create db:migrate

and if appropriate rake db:seed

rake db:drop is optional (i.e. not needed if new database)

```

### Question 5

I want to look at the actual database that has been created. What command should I type in the terminal?

```

you could enter either 'psql' or 'rails c' to view info contained within it.

```


### Question 6

I want to see a list of all the URLs available in my app, along with the HTTP requests and controllers associated with them. What command should I type in the terminal?

```

rails routes

```


### Question 7

What line should I add to `config/routes.rb` to create a complete set of RESTful routes for a "bunnies" resource?

```

resources :bunnies

```


### Question 8

According to standard Rails conventions, what directory and filename would the BunniesController be located in, starting from the root of the project?


```

app/controllers

```

### Question 9

According to standard Rails conventions, what directory and filename would the "show" view for bunnies be located in, starting from the root of the project?


```

app/views/bunnies

```

### Question 10

I have worked on my app and finally want to see it in action. What command should I type in the terminal, and where should I navigate to in my browser?

```

start the rails server with:
rails s

and navigate your browser (assuming you set up the root route) to:
localhost:3000

```
