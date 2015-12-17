# Camel Restlet and JDBC Example

### Introduction
An example which shows how to expose CRUD operations with REST interface and JDBC implementation


### Build

You will need to compile this example first:

	mvn install
	
### Run

To run the example type
Run the application using XML-DSL:

	mvn jetty:run

### Run Java-DS
To run with Java-DSL use: 
	
	mvn jetty:run -Dimpl=java-dsl

### Run XML-REST-DSL
To run with XML-REST-DSL use: 

	mvn jetty:run -Dimpl=xml-rest-dsl

### Check
To create an person, make a http POST request with firstName and lastName parameters:

	curl -d "firstName=test&lastName=person" http://localhost:8080/rs/persons/

To update an existing person, make a http PUT request with firstName and lastName parameters:

	curl -X PUT -d "firstName=updated&lastName=person" http://localhost:8080/rs/persons/2

To retrieve an existing person, make a http GET request with the personId as part of the url:

	curl -X GET  http://localhost:8080/rs/persons/1

To delete an existing person, make a http DELETE request with the personId as part of the url:

	curl -X DELETE  http://localhost:8080/rs/persons/1

To retrieve all the existing persons, make a http GET request to persons url:

	curl -X GET  http://localhost:8080/rs/persons

### Forum, Help, etc 

If you hit an problems please let us know on the Camel Forums <http://camel.apache.org/discussion-forums.html>

Please help us make Apache Camel better - we appreciate any feedback you may
have.  Enjoy!

