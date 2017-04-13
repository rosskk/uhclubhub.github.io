# Table of contents

* [Installation](#installation)
* [Installation](#installation)
* [Application design](#application-design)
  * [Directory structure](#directory-structure)
  * [Naming conventions](#naming-conventions)
* [Development History](#development-history)
  * [Milestone 1](#milestone-1)
* [Galaxy Deployment](#galaxy-deployment)
# About UH Manoa Club Hub

UH Manoa Club Hub is a Meteor application Organizing Clubs in University of Hawaii community. When you come to the site, you'll come to a landing page:

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/landing-page.png "Landing Page")

From this the landing page, you can easily access the login page, shown below, by clicking on the login button. Everyone with a UH account can login. 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/login-page.png "Login Page")

After you login, you will go to your personal student homepage (shown below). On top of the page, it will list all the clubs, which you are in. It's then followed by the upcomming events of your clubs. Your homepage will also allow you to search for a club by clicking the "Club List" tab on the Menu. And you can search based on area of interests.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/home-page.png "Home Page")

If you want to create a club, you will need to request a separate login. With that login info, you can go to club-founder's admin page, which will give you the authority to create/modify clubs and create/modify events for the club you created. 

The create club page is shown below. You simply need to fill in all the required information and then click submit. 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/add-club-page.png "Create Club Page")

The following is modify club page. In this page will have the events you've created, followed by your club info. You can modify both your club info and the events through this page. To modify the events, you can simply click at the event card, then it will lead you modify event page. To create a event, you click at the card with "+" in it, and it will take you to a separate page which allow you to add more events.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-club.png "Edit Club Page")

The create event page and edit event page are shown below:

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/create-event.png "Create Event Page")
  
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-event.png "Edit Event Page")

# Installation

1. [install Meteor](https://www.meteor.com/install).

1. clone [UH Manoa Club Hub](https://github.com/ics-software-engineering/meteor-application-template/archive/master.zip) project using git.
  
3. cd into the app/ directory and install libraries with:

```
> meteor npm install
```

4.  run the system with:

```
> meteor npm run start
```

If all goes well, the application will appear at [http://localhost:3000](http://localhost:3000). If you have an account on the UH test CAS server, you can login.  

# Application Design

## Directory structure

The top-level directory structure contains:

```
app/        # holds the Meteor application sources
config/     # holds configuration files, such as, your database configuration file, settings.json
.gitignore  # don't commit IntelliJ project files, node_modules, and settings.production.json
```

This structure separates configuration files (such as the settings files) in the config/ directory from the actual Meteor application in the app/ directory.

The app/ directory has this top-level structure:

```
client/
  lib/           # holds Semantic UI files.
  head.html      # the <head>
  main.js        # import all the client-side html and js files. 

imports/
  api/           # Define collection processing code (client + server side)
    club/
    event/
  startup/       # Define code to run when system starts up (client-only, server-only)
    client/        
    server/ 
    both/
  ui/
    layouts/     # Layouts contain common elements to all pages (i.e. menubar and footer)
    pages/       # Pages are navigated to by FlowRouter routes.
    stylesheets/ # CSS customizations, if any.

node_modules/    # managed by Meteor

private/
  database/      # holds the JSON file used to initialize the database on startup.

public/          
  images/        # holds static images for landing page and predefined sample users.
  
server/
   main.js       # import all the server-side js files.
```
 
## Naming conventions

This system adopts the following naming conventions:

  * Files and directories are named in all lowercase, with words separated by hyphens. Example: accounts-config.js
  * "Global" Javascript variables (such as collections) are capitalized. Example: Club.
  * Other Javascript variables are camel-case. Example: collectionList.
  * Templates representing pages are capitalized, with words separated by underscores. Example: Home_Page. The files for this template are lower case, with hyphens rather than underscore. Example: home-page.html, home-page.js.
  * Routes to pages are named the same as their corresponding page. Example: Home_Page.

# Development History

## Milestone 1

The goal of Milestone 1 was to create mockup HTML pages for the various pages that will be a part of UH Club Hub.

Milestone 1 consisted of 10 issues, and was managed via the [uhclubhub GitHub Project M1](https://github.com/uhclubhub/uhclubhub/projects/1)

### Landing Page
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/landing-page.png "Landing Page")

### Login Page
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/login-page.png "Login Page")

### Home Page
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/home-page.png "Home Page")

### Create Club Page
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/add-club-page.png "Create Club Page")

### Create Event Page
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/create-event.png "Create Event Page")

### Edit Club Page
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-club.png "Edit Club Page")

### Edit Event Page
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-event.png "Edit Event Page")

# Galaxy Deployment

[http://uhclubhub.meteorapp.com/](http://uhclubhub.meteorapp.com/)
