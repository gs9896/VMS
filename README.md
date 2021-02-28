# Visitor Management System (VMS)
## (Project by Bangmetric LLC)
## Team :
### Project Manager : Gundeep Singh (DevOps Specialist)
### Team Leader : Neeraj Kumar
### Gurdeep Singh
### Front End Team : Anuj Kumar Singh, Aayush Kumar Roy
## Purpose of Project :
* A visitor management system provides you to track your visitors in and out of your Organisation. In a world full of people, you would want to know who wants to meet you and when.
* VMS helps you track all those people wanting to come into your organisation and provides you a control whom to allow and when to allow.
* No more unncessary crowd will be at your workplace and everyone who enters is recorded and valid.

## Technology Used :
### Front End :
* HTML 
* CSS 
* Bootstrap
* View.JS
* Font awesome
* Jquery

### Back End :
* Django Rest framework (DRF)
* Python
* PostgreSQL

## Project Schedule :
* We here used the agile methodology in the development of Visitor Management System.
* The Agile software development methodology is one of the simplest and effective processes to turn a vision for a business need into software solutions. Agile is a term used to describe software development approaches that employ continual planning, learning, improvement, team collaboration, evolutionary development, and early delivery. It encourages flexible responses to change.
![image](https://user-images.githubusercontent.com/54369528/109427241-7b83be00-7a17-11eb-9e20-b32235fd51b2.png)

* The agile software development emphasizes on four core values.

1. Individual and team interactions over processes and tools
2. Working software over comprehensive documentation
3. Customer collaboration over contract negotiation
4. Responding to change over following a plan

* It took two sprints of two weeks( including backend development, front end development, integration, and testing) each in this project.

![image](https://user-images.githubusercontent.com/54369528/109428654-ef28c980-7a1d-11eb-9cb2-263a444f191a.png)


## Flow Chart :
### User booking appointment outside premises :
![image](https://user-images.githubusercontent.com/54369528/109418006-123a8580-79ec-11eb-9af5-91a51d9cf32b.png)

Here in this flow it is described how visitor can book thier appointment using VMS application without even going to meeting site.
* Visitor will first see VMS landing page there they have to click on BOOK APPOINTMENT.
* After that they see a Visit form where the  user have to fill details like Full Name, Phone Number, Email, Host and the Purpose of visit.
* On click to Proceed user will see a thank you page and receives mail for appointment verification.
* Then user needs to verify their appointment via link received in mail.
* After Appointment verification user will receive check in/out token which they have to use on visit to site.
* On premise visitor have to use the token received via mail earlier to check-in and after entering the token user check-in time will be noted and image will also be captured at that time.
* Afer meeting with particular host user have to use check out token to exit and the check-out time will be recorded and thankyou for your visit message will be received.


### Visitor on premises : 
![image](https://user-images.githubusercontent.com/54369528/109418027-254d5580-79ec-11eb-83bb-2ca0ee9d6f4c.png)

Here in this flow it is described how visitor entering premises can check-in using VMS application.
* Visitor first of all will view Check-in/out page.
* There visitor have to click on NEW VISITOR and he/she will be redirected to visit form.
* At visit form user have to enter their details, host they want to meet and the purpose of the meeting.
* On click to proceed user will be redirected to click image and save details.
* After that visitor details and check in time will be recorded and receives mail regarding check out token.
* Host will also get a mail for their meeting with Visitor.
* After that user can enter premises.
* Now at the time of check out user have to use the token received via mail and can successfully check-out from the building.

### Admin Portal :
![image](https://user-images.githubusercontent.com/54369528/109418039-3eee9d00-79ec-11eb-8746-a7919c636f31.png)

Here in this flow Admin portal is described and the features admin can use.
* First of all Admin needs to login to the portal.
* Admin enters the credentials and validation occurs, if credentials are valid admin will see portal.
* There at admin portal admin can see visitor's table regarding visitor's check in/out and other records, can add new host to VMS, can download Records CSV, opens the visitor's portal.
* To see visitor's records admin have to click on Visit table.
* To add new host admin clicks on ADD HOST and after that fill form regarding host name, host designation, phone number, email and click on ADD HOST. New host will be added to the database.
* To download CSV of Visitor's records admin have to click on CSV and CSV file be downloaded and saved on local system.
* Admin also have to open Visitors landing page at reception for visitors check in/out.

## Database schema :
### Complete VMS database schema :

![image](https://user-images.githubusercontent.com/54369528/109427137-f4364a80-7a16-11eb-8eb8-0921d73f59bb.png)

### Visitor's -> Visit database schema :
* Visitors to Visit database is ( one to many relationship )
* As single user can be mapped to multiple appointments so single vistor database has many relations with visits.

![image](https://user-images.githubusercontent.com/54369528/109417939-bf60ce00-79eb-11eb-80e6-155d45ba0558.png)

### Visitor -> Host database schema :
* Visitor to Host database is ( many to many relationship )
* A single visitor can book many hosts and multiple visitors can book a single host.
* So many visitor can have appointment with many hosts so many to many relationship holds here with Visitor to Host database schema.

![image](https://user-images.githubusercontent.com/54369528/109417931-b53ecf80-79eb-11eb-87f7-7bd69fd85250.png)

### Visits -> Host database schema :
* Visit to Appointment verification token is ( one to one relationship )
* A single visit will generate a single verification token and a single verfication token can verfiy a single visit.
* So Visit to Host database is one to one relationship.

![image](https://user-images.githubusercontent.com/54369528/109417920-a0623c00-79eb-11eb-98ac-a414c3de9dfe.png)


