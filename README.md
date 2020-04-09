# forked from dmulligan/docker-example-tomcat-mysql

added fixed version 8.0 for mysql and related jdbc driver
exposed port 3306 from mysql
tested on play-with-docker

A docker compose example project with a MySQL 8.0 and a Tomcat container linked together.

To run: 

	$ docker-compose up -d 
	
To stop:

	$ docker-compose down

Containers:
- MySQL: on startup, the container executes a simple database initialisation script `./db/mysql-init.sql`, which
  creates a database containing a single table which is populated with a few records.
- Tomcat: a simple web application, located within `./tomcat/webapps`, is deployed. The application contains some JSPs
  to test the database link between the Tomcat and the MySQL containers