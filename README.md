
log in to heroku login-i

Deploying to Heroku
to create a connection between Git and Heroku to push our changes using Git and update the application at any given time

Create a new app in Heroku (remember app name must be unique!)

Login to heroku in CLI by typing heroku login

Check the apps by typing heroku apps into CLI (we should see our heroku app listed)

Then create a new git repository using git init

Add files to repository with git add . then git commit -m   

Then associate heroku application as remote master branch with $ heroku git:remote -a task-manager-flask-mongo-td

Then we want to push to Heroku with $ git push heroku master

Push will fail because we don’t have our requirements.txt file in place. This will contain a list of the applications that are required for Heroku to run the application

To create the requirements.txt file type pip3 freeze —local > requirements.txt in the CLI

Then git add . , git commit -m, and git push heroku master

Then need to create a procfile which is an instruction to Heroku as to which file is used as our entry point at the application, which file we use to call the application to get it up and running

Specify that using echo web Python - echo web: python app.py > Procfile 

Then git add . , git commit -m, and git push heroku master

We then want to run our application by sending a command to Heroku heroku ps:scale web=1

Set IP and PORT on Heroku so server instance on Heroku will know how to run our Flask application

In settings on Heroku, config vars - IP 0.0.0.0 and PORT 5000

Then open app

install pip3 install flask-pymongo 

install pip3 install dnspython

