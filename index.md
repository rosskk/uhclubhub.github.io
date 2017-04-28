# Table of contents

* [About UH Manoa Club Hub](#About-UH-Manoa-Club-Hub)
* [Installation](#installation)
* [Application design](#application-design)
  * [Directory structure](#directory-structure)
* [Development History](#development-history)
  * [Milestone 1](#milestone-1)
  * [Milestone 2](#milestone-2)
* [Galaxy Deployment](#galaxy-deployment)

# About UH Manoa Club Hub

UH Manoa Club Hub is a Meteor application Organizing Clubs for University of Hawaii at Manoa. When you come to the site, you'll come to a landing page:

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/landing-page.png "Landing Page")

From the landing page, you can easily access the login page, shown below, by clicking on the login button. Everyone with a UH account can login. 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/login-page.png "Login Page")

This web application is featured with three different users, the students, the club administrator and the website administrator. And different authorization goes to different users. When you log in as a student, you will go to your student homepage (shown below). On top of the page, it will list all the clubs, which you are in. It's then followed by the comming events of your clubs. 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/home-page.png "Home Page")

By clicking the "Browse Clubs" tab on the Menu of student homepage, you will go to club List page (shown below), which will contain all clubs available in University of Hawaii at Manoa. And this page is feaured with a interest search at the top of the page.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/club-listing-page.png "Browse Clubs Page")

If you login with a club administrator's account, you will go to the founder's admin page, shown below. This page is a channel where you can access all the clubs you created. And it will also allow you to create a new club by clicking on the card, with "+" sign in it.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/club-founder-admin.png "founder admin Page")
 
The following is the create club page. To create a club, you simply need to fill in all the required information and then click submit. 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/add-club-page.png "Create Club Page")

To modify the information of an existing club, you can click on the edit button on the bottom of the club card.And it will look like this: 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-club.png "Edit Club Page")

This page will show the events you've created, followed by your club info. To modify the events, you can simply click on the event card, then it will lead you modify event page. To create a event, you click at the card with "+" in it, and it will take you to a separate page which allow you to add more events.

The create event page and edit event page are both shown below:

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/create-event.png "Create Event Page")
  
![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-event.png "Edit Event Page")

To have a better control of the website, someone can log in with a site administrator login. this type of user can go the site admin page, shown below. And they will have the authority to hide or delete a club.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/site-admin.png "Site Admin Page")

# Installation

1. [Install Meteor](https://www.meteor.com/install).

1. clone [UH Manoa Club Hub](https://github.com/ics-software-engineering/meteor-application-template/archive/master.zip) project using git.
  
3. cd into the app/ directory and install libraries with:

```
> meteor npm install
```

4.  run the system with:

```
> meteor npm run start
```
If you successfully run it, you will see the following in your prompt.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/success.png "success screenshots")

And the application will appear at [http://localhost:3000](http://localhost:3000). 
# Application Design

## Directory structure

This App is designed with [meteor 1.4](https://guide.meteor.com/1.4-migration.html). And we also follow the Meteor 1.4 [Application Structure](https://guide.meteor.com/structure.html) guideline, for which we used an import/ directory in the app/ directory to hold our code. The structure of the app/ directory are shown below. 

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
 
# Development History

## Milestone 1

The goal of Milestone 1 was to create mockup HTML pages for the various pages that will be a part of UH Club Hub.

Milestone 1 consisted of 10 issues, and was managed via the [uhclubhub GitHub Project M1.](https://github.com/uhclubhub/uhclubhub/projects/1). 

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/issue-page.png "issue Page")

And we also use [projects](https://github.com/uhclubhub/uhclubhub/projects/1) feature on github to do the progress management.

![alt text](https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/project-page.png "Project Page")

So when ever we have an added issue, we will add it in the "Backlog" column, when we are working on a issue, we add it to the "In Progress" column, and when we are done, we close it and add it to the "Done" column. This keep our progress organized. By knowing what is done and who is working on what, it will be easier for the members to decide what to do first. 

The pages we created for this milestone includes:

* Landing Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/landing-page.png"/>
  
* Login Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/landing-page.png"/>

* Home Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/home-page.png"/>

* Create Club Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/add-club-page.png"/>

* Edit Club Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-club.png"/> 

* Create Event Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/create-event.png"/>
  
* Edit Event Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/edit-event.png"/>

## Milestone 2

Milestone 2 was started on April 13, 2017 and ends on April 25, 2017. The goal of Milestone 2 is to finish unfinished mockup pages and improve already existing ones, implement UH CAS authentication, and create the Collection for the Clubs. The Gitbub issue page of this mile stone is shown [here](https://github.com/uhclubhub/uhclubhub/issues?utf8=%E2%9C%93&q=milestone%3A%22M2%22). And it's progress is  being managed [here.](https://github.com/uhclubhub/uhclubhub/projects/2)

The mockup pages created includes:

* List Club Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/club-listing-page.png"/>

* Site admin Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/club-founder-admin.png"/>
  
* Club Admin Page

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/site-admin.png"/>  

* UH CAS Test Authentication

  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/uh-cas-authentication.png"/>
* Creation of Club collection
  
  <img width="500px" src="https://github.com/uhclubhub/uhclubhub.github.io/raw/master/images/browse-club-updated.png"/>
 
 In this issue, we 
  1. created the club collection in /imports/api/. 
  2. create an initialization file, club.js in /imports/startup/server/
  3. modified the browse-club-page.html and browse-club-page.js to link the content from collection, and allow the club in the database to show up iteratively.
  
## Milestone 3

Milestone 3 was started on April 27, 2017 and ends on May 9, 2017. The goal of Milestone 3 is to create the database for user profiles. Milestone 3's progress is being managed [here.](https://github.com/uhclubhub/uhclubhub/projects/3)

# Galaxy Deployment

The link to our galaxy deployment is [http://uhclubhub.meteorapp.com/](http://uhclubhub.meteorapp.com/)
