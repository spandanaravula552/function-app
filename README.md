Azure function app: azure function app is serverless managed service, where we can write functions into it in languages such as c, .NET, node.js, JavaScript, it provides integrate with visual studio to deploy the code, we can integrate it with app insights and azure monitor for monitoring purpose.

->when we define the function, we need to specify the trigger, like when the function should trigger HTTP Trigger: HTTP trigger means, the function will run, when it receives an HTTP request

there are two methods in http trigger, GET and POST GET means This is used to request the data

Post means: This is used to send data to update or create the resource, here we can pass the data in the body of the request.

One Scenario: the web application is hosted in azure web app in .NET language, it needs to a call a azure MySQL DB for some data, the function is there in node.js language b/w them, (function app can fetch the information from MySQL db and pass it onto azure web app) steps:

->

1. Creation of MySQL server in Azure.

once we create MySQL server, it will not create MySQL database for us, it done in case SQL only, in SQL when we create SQL database, behind SQL server gets create. ->so to login to MySQL server, we need to install azure data studio tool in local. Its a straight forward installation, its similar to VS code.

->once it's installed, launch it and go to extensions to install MySQL database.

->once extension installed, go to connections tab in studio, new connection and give the MySQL server details such as username, pad, server name. -> once server connected, click on 'new query" and write below query and execute it, it will create the table and fetches the data.

create database appdb;

use appdb;

create table course;

(

courseid int,

coursename varchar, );

ratings numeric

I

insert into course (courseid, coursename, ratings) values (1, "docker", 4.5); insert into course (courseid, coursename, ratings) values(1, "k8s", 4.5);

insert into course (courseid, coursename, ratings) values (1, "azure", 4.5);

select *from course;

