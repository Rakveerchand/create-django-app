[![CodeQL](https://github.com/imagineai/create-django-app/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/imagineai/create-django-app/actions/workflows/codeql-analysis.yml) [![codecov](https://codecov.io/gh/imagineai/create-django-app/branch/master/graph/badge.svg?token=5IK4BJB4I3)](https://codecov.io/gh/imagineai/create-django-app) [![test across OS, package managers and Python versions](https://github.com/imagineai/create-django-app/actions/workflows/test_envs.yml/badge.svg)](https://github.com/imagineai/create-django-app/actions/workflows/test_envs.yml) 

<h1> Create Django App </h1>

Easy **one-line command** to create a Django app with all the **dependencies auto-installed**, and **built-in support for**:
- package managers (**pipenv, poetry**)
- web servers (**dev, gunicorn, uwsgi**)
- connecting to different databases (**MySQL, PostgreSQL, SQLite3**)
- data model creation
- CRUD API creation (**REST, GraphQL**)
- unit tests and test coverage reporting
- autogenerated test factories (**FactoryBoy**)
- linting and code formatting (**autopep8, isort**)
- autogenerated API documentation (**Swagger, ReDoc**)

<br/>

<h2> Overview </h2>

- To create your new Django app, run the following command in your terminal:
```
npm install -g imagine && imagine create -f django -n myapp 
```
(If you don't have npm installed, you'll need to [install this first](https://docs.npmjs.com/cli/v7/commands/npm-install).)
<br/>
- You should see this:

```
$ npm install -g imagine && imagine create -f django -n myapp 

changed 214 packages, and audited 215 packages in 5s

found 0 vulnerabilities
32 files written
You have successfully created a new project!
Now you can run "cd myapp && imagine run" to install the dependencies and open a web server running at
http://127.0.0.1:8000/
```
<br/>
- Run `cd myapp && imagine run` to run your new Django app, and open http://127.0.0.1:8000/ to see that the install worked successfully.

- Congrats! Your Django app is up and running!

- Now that you've created your new app, check out the `myapp.im` in your app directory - using this you can: 
  - easily change your app settings such as django server, package manager, API format, database etc.
  - auto-generate code for data models, CRUD APIs etc using our simple config spec. 

- Continue reading to learn more, or check out www.imagine.ai.

</br>
<h2> Learn more </h2>

<h3> Easy to create </h3>

- Our one-line command allows your to get started with your Django app immediately, without worrying about installing dependencies - we use commonly used dependencies to help you get started with your app, so you can focusing on writing business logic. 


- Our default settings when we create your django app are as follows: 
  - Server:                 dev
  - Package manager:        pipenv
  - Django models layout:   single-file
  - Project directory name: microservice
  - API format:             REST
  - Database:               sqlite
  - Database name:          myapp-db

- These aren't the exact settings you want? No sweat, you can always change the settings as per your preferences - read on to see how to do this.

<br/>

<h3> Easy to customize </h3>

- If you want to change any of the above defaults for your app, its a piece of cake.

- Go to the myapp.im file in your directory, your should see the basic default settings here:

</br>

```
settings

app:
    # your application name
    name: myapp
    # choose one: [django, node]
    framework: django

django:
    # choose one: [pipenv, poetry]
    package-manager: pipenv
    # choose one: [gunicorn, uwsgi, dev]
    server: dev

    layout:
        # choose one: [single-file, separate-files]
        models: single-file
        # name of the project settings directory:
        project-dir: microservice

api:
    # choose one: [rest, graphql]
    format: rest

end settings

# database <database type: [sqlite, mysql, posgresql]> <database name>
database sqlite myapp-db 

```
  
- You can replace the default settings with your preferences (based on the options allowed), and then run `imagine compile myapp.im` in your terminal. Your app and will be updated with the new settings.


<br/>

<h3> Easy to add app functionality </h3>

- Not only can you change your app settings easily, you can also generated production-ready code using the `myapp.im` file. 


- Use Imagine's simple syntax to add [data models](www.imagine.ai/docs/model) and [CRUD APIs](www.imagine.ai/docs/api) to your Django app. 


- Run `imagine compile myapp.im` to see the generated code.

- PS - all our generated code has:
  - unit tests and test coverage reporting
  - autogenerated test factories (using FactoryBoy)
  - linting and code formatting (you can select autopep8 or isort)
  - autogenerated API documentation (using Swagger and ReDoc)

- Enjoy!

