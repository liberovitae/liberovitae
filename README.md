# liberovitae social connectivity platform


![logo](/logofull.svg)

[Demo/development site](https://dev.liberovitae.com)

A simple and modern community connectivity platform written with React/Material-UI/NodeJS/Apollo/GraphQL/Redis & Mongoose/MongoDB.


## Features 

* React (create-react-app, customize-cra) with Apollo Client
  * Queries, Mutations
* Node.js with Express and Apollo Server
  * Pagination
* MongoDB/Mongoose
  * entities: users, jobs, venues, companies, alerts, tasks
* Redis caching
  * entities: jobs, venues
* Authentication
  * powered by JWT and local storage
  * Sign Up, Sign In, Sign Out, Change password, Reset password
* Authorization
  * protected endpoint (e.g. verify valid session)
  * protected resolvers (e.g. e.g. session-based, role-based)
  * protected routes (e.g. session-based, role-based)
* UI/UX Features
    * Add items to saved list
    * Alerts/Notifications
      * Email alerts
      * Web push notifications
    * Dark/light themes


## Installation

    
Install & configure API
* `git clone git@github.com:liberovitae/api.git`  
* `cd api`
* `yarn install`
* Edit API `.env.*` files  
    
Install & configure UI/Frontend
* `git clone git@github.com:liberovitae/ui.git`  
* `cd liberovitae/ui`
* `yarn install`
* Edit UI `.env.*` files

Run API server

Use the environment variable `FAKE_DATA=1` to populate database with randomised/fake data. The process will exit upon completion. See `api/handlers/faker.js` for more details.


* `cd api`
* `NODE_ENV="development" yarn start`

Run UI/Frontend
* `cd ui`
* `NODE_ENV="development yarn start` 



#### .env files

Since this project is using MongoDB, you have to install it for your machine and get a database up and running. You find everything for the set up over here: [Setup MongoDB with Mongoose in Express Tutorial](https://www.robinwieruch.de/mongodb-express-setup-tutorial). After you have created a MongoDB database, you can fill out the environment variables in the *api/.env.\** & *ui/.env.\** files.

```
SECRET=asdlplplfwfwefwekwself.2342.dawasdq

DATABASE_URL=mongodb://localhost:27017/mydatabase
```

The `SECRET` is just a random string for your authentication. Keep all these information secure by adding the *.env* files to your *.gitignore* file. No third-party should have access to this information.


