#  Cinema application
![](front.jpg)

This application implements a service for buying cinema tickets. 

It uses popular frameworks as Spring and Hibernate, implements such principles as DI, SOLID and REST.

Using this application, you will be able to register users or also log into an already created 
account (using a login (which is email) and password). You can also manually add administrators to the 
database who will have additional advantages, and if desired, expand the list of roles. Also, users 
and administrators can be shown: cinema halls, available movie shows, movies, some specific movie show. 
Admins can add new cinemas and movies. Users can receive their orders and shopping carts, fulfill orders 
and add tickets for some movie sessions to the shopping cart. Using different endpoints.

# In this application you can find such endpoints by roles that have access to them:
- POST: /register - all
- GET: /cinema-halls - user/admin
- POST: /cinema-halls - admin
- GET: /movies - user/admin
- POST: /movies - admin
- GET: /movie-sessions/available - user/admin
- GET: /movie-sessions/{id} - user/admin
- POST: /movie-sessions - admin
- PUT: /movie-sessions/{id} - admin
- DELETE: /movie-sessions/{id} - admin
- GET: /orders - user
- POST: /orders/complete - user
- PUT: /shopping-carts/movie-sessions - user
- GET: /shopping-carts/by-user - user
- GET: /users/by-email - admin

# To launch and configure the application, you will need:
1. Install [MySQL](https://dev.mysql.com/downloads/) and [Apache Tomcat 9.0.54](https://tomcat.apache.org/download-90.cgi).
2. Fork this project to your GitHub repository
3. Clone this project, to your local machine
4. Create empty database.
5. Add up-to-date information(driver, URL, username, password) in ```db.properties``` in ```resources``` folder:
``` java
#MySQL properties

db.driver=YOUR_DRIVER
db.url=jdbc:YOUR DATABASE URL
db.user=YOUR USERNAME
db.password=YOUR PASSWORD
```
5. Add Tomcat to running configuration of your project and use / as your Tomcat application context.
6. Run project using previously configured Tomcat running configuration and login as admin (login: bob@gmail.com and password: 12345) or as default user (login: alice@gmail.com and password: 678910)

# Technologies
1. Java (JDK version 17)
2. Hibernate (version 5.4.27.Final)
3. Spring (Spring Core, Spring Web, Spring Security)
4. MySQL (version 8.0.22)
5. Tomcat (version 9.0.50), to run application locally
