# Unit 14 Sequelize Homework: Reverse Engineering Code

Reverse engineer the starter code provided and create a tutorial for the code.

In the `Develop` folder, there is starter code for a project. Begin inspecting the code to get an understanding of each file's responsibility. Then, in a Google Doc, write a tutorial explaining *every* file and its purpose. If one file is dependant on other files, be sure to let the user know.

At the end of the tutorial, add instructions for how you could now add changes to this project.

Following the [common templates for user stories](https://en.wikipedia.org/wiki/User_story#Common_templates), we can frame this challenge as follows:

```
AS A developer

I WANT a walk-through of the codebase

SO THAT I can use it as a starting point for a new project
```

## Business Context

When joining a new team, you will be expected to inspect a lot of code that you have never seen before. Rather than having a team member explain every line for you, you will dissect the code by yourself, saving any questions for a member of your team.

## Acceptance Criteria

```md
GIVEN a Node.js application using Sequelize and Passport
WHEN I follow the walkthrough
THEN I understand the codebase
```
- - -

## CODE EXPLAINED 


CONFIG

MIDDLEWARE

isAuthenticated.js:
restricts routes that user is not allowed to visit if not logged in. if user is logged in, it continues with request 

config.json: connection configuration to connect to server 

passport.js: contains javascript logic that tells passport we want to log in with an email address and password

MODELS

index.js: connects to database and imports users log in data 

user.js: requires "bcrypt" for password hashing. this makes our database secure even if compromised. Here we have JS that defines what is stored on our database 

ROUTES

api-routes.js: contains routes for signing in, logging out and getting users specific data to be displayed client side

html-routes.js: routes that check whether user is signed in, whether user already has account etc and sends them tio the correct html page

package.json: contains all package info, node modules used, version info etc 

server.js: requires packages, sets up PORT, creates express and middleware, creates routes and syncs database / logs message in terminal on successful connection to server
