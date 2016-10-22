##Maven tutorial :

Maven can manage a project's build, reporting and documentation from a central piece of information

		1) Maven manages Dependencies
		2) Build Jar or war 
		3) install the application locally - Tomcat or Jetty
		4) Add new dependencies to a project
		5) Run Unit Tests

Maven uses configuration file to build project 

pom.xml ( Project Object Model) is core configuration file for project 

It is a single configuration file that contains the majority of information required to build a project
it content :
         
         1) Name of project
         2) Version 
         3) Packaging
         4) Dependencies
         5) Plugins information


Every maven build goes through following phases:

		1)  Validate: validate the project is correct and all necessary information is available
		2)  Compile: compile the source code of the project
		3)  Test: test the compiled source code using a suitable unit testing framework
		4)  Package: take the compiled code and package it in its distributable format, such as a JAR.
		5)	Integration-test: process and deploy the package if necessary into an environment where integration tests can be run
		6)	Verify: run any checks to verify the package is valid and meets quality criteria
		7)	Install: install the package into the local repository, for use as a dependency in other projects locally
		8)	Deploy: done in an integration or release environment, copies the final package to the remote repository for sharing with other developers and projects.

##Every build having below directory structure: 

        my-app
        |-- pom.xml
        `-- src
           |-- main
           |   `-- java
           |       `-- com
           |           `-- mycompany
           |               `-- app
           |                   `-- App.java
           `-- test
               `-- java
                   `-- com
                       `-- mycompany
                           `-- app
                               `-- AppTest.java

##Build Project command:
	
    mvn package 

Maven clean :

 cleans up artifacts created by prior builds
 
 maven site: generates site documentation for this project

 mvn test - run unit tests