# SimpleDemoFlaskApp
A simple Flask API based web app for demo and tutorials of Flask fundamentals

Steps:

1. Create a repo in Github and clone it in your machine
2. Open a command prompt in admin mode and cd to the project directory (just cloned).
3. Create a virtual environment from your local Python installation and activate it. 
   Then install flask: pip install flask
4. cd to the root of project directory.
5. Create a python module & name it hello. The code is updated in the repo.
6. Go to command prompt and issue below commands:
   set FLASK_APP = hello
   set FLASK_DEBUG = True
7. Finally run your app by issuing below command in the command prompt:
   flask run
   It will deploy the app in your machine as localhost on port 5000
8. Then create a similar app in a module and name it app. This time instead of showing text directly, pass the same from a 
   template html using a helper render_template() from Flask package
9. Create two folders inside the root of the project diectory:
   templates/
   and static
   Inside static, create another folder and name it css to house style for your web app
10. Then inside template create index.html and inside static/css create style.css. The source code for 
    both of them are there inside this repo for reference.
11. Save all file and stip the server from the prompt by pressing CTRL+C.
12. Set another value to the environment variable, FLASK_APP like below:
    set FLASK_APP = app
    Then restart the server like before. This time the app would beloaded from a template html and 
    the stylesheet by the support of Jinja Template Engine.
13. After it, again stop the server and add a base.html inside the templates folder. This time
    add bootstrap, jQuery and other required libraries inside the same html.
14. Accordingly, in the next step replace the index.html content with code specific to Jinja template engine.
    Here we are extending the base html and thereby limiting code repetition 
15. Now restart the server and see the effect of this awesome change.
16. In next step, the SQLite database would be setup by leveraging the built-in database in the standard Python 
    library. For this create two files, namely schema.sql and init_db.py - one for creating a table inside 
    the database and another for creating some data inside the table by establishing a connecting between our app
    and the database using simple Python code.
17. Once these are created and saved, run the init_db.py from command prompy. It will create a database.db file
    If it's done, Voila ! You are all set to go further.
18. Now modify the app.py and index.html
19. Restart the server and hit the app, you will see the all the entries from the table 'posts' which were added by running the 
    script init_db.py 
20. To display one single entry, a new route and view function is added in the app.py module. Also another
    template is created for this kind of request.
21. Next we will develop the feature of creating a new post. For it, a new route and a view function is 
    added in our app.py module. Also in the base template one control is added for easy access to the functionality
    of creating new post.
22. Let's add the next obvious feature of editing an existing post. Like create, for this also add a new route
    and a view function to app module. Also add the edit link to navigate user to the corresponding post
    on the index page.
23. Finally add the delete functionality.