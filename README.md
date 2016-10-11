1)Jenkins is used to CI (continuous integration ), which written in JAVA

2) Jenkins earlier known as Hudson 

3) Jenkins can be build other languages also like Ruby on Rail, python,php, .net etc build 


###Continuous Integration : 

Automate development process like code compile, execute some test ( Test driven approach or Behaviour Driven Approach ), perform quality check & make report etc

###Continuous Deployment :

it is fully automate process, every successful build automatically deploy on production environment 


###Continuous Delivery:

The notion of Continuous Delivery is a slight variation on the idea of Continuous Deployment that takes
into account these considerations. With Continuous Delivery, any and every successful build that has
passed all the relevant automated tests and quality gates can potentially be deployed into production
via a fully automated one-click process, and be in the hands of the end-user within minutes. However,
the process is not automatic: it is the business, rather than IT, that decides the best time to deliver the
latest changes. 


### Jenkins Installation 

Jenkin can be install with application server like tomcat,jboss etc OR standalone 

****Jenkin standalone****

		$ java -jar jenkins.war

By Default jenkins will run on the 8080 If this doesn’t suit your environment, you can specify the
port manually, using the --httpPort option

		$ java -jar jenkins.war --httpPort=8081
		
**** Jenkins with apache***

		$ java -jar jenkins.war --httpPort=8081 --ajp13Port=8010 --prefix=jenkins

using AJP apache module & proxy server we can call on URL like http://myserver.myorg.com/jenkins. 
		

		
### Jenkins home directory 

**1)jenkins**      	: The default Jenkins home directory (may be .hudson in older installations) is .jenkins

**2)fingerprints**  : This directory is used by Jenkins to keep track of artifact fingerprints

**3)jobs**			:  This directory contains configuration details about the build jobs that Jenkins manages, as well as the artifacts and data resulting from
				   these builds.    
				   
**4)plugins**		: This directory contains any plugins that you have installed. Plugins allow you to extend Jenkins by adding extra feature. Note that,
				  with the exception of the Jenkins core plugins (subversion, cvs,ssh-slaves, maven, and scid-ad), plugins are not stored with the
                  jenkins executable, or in the expanded web application directory.This means that you can update your Jenkins executable and not
				  have to reinstall all your plugins.
				  
**5)updates**      : This is an internal directory used by Jenkins to store information about available plugin updates

**6)userContent**  : You can use this directory to place your own custom content onto your Jenkins server.You can access files in this directory at http://myserver/hudson/userContent (if you are running Jenkins on an
				 application server) or http://myserver/userContent (if you are running in stand-alone mode).
				 
**7)users**		 : If you are using the native Jenkins user database, user accounts will be stored in this directory.

**8)war**        : This directory contains the expanded web application. When you start Jenkins as a stand-alone application, it will extract the web
				  application into this directory.
				  
### Build Jobs 

1)Job builds build which nothing but complied version of code & also perform some unit test & quality check
2)Each jobs has two subdirectories:
  
   1) build directory which content build.xml & other files which help to configure jobs
   2) workspace directory where jenkins builds your projects,it contains the source code jenkins checks out 

**Build Job Type**

1) Free Style Software project : Freestyle build jobs are general-purpose build jobs, which provides a maximum of flexibility

2) Maven project               : Generally used to build java application using Maven OR ant

3) Monitoring an external jobs : used to monitor on non interactive process such crontab

4) Multi Configuration jobs    : you run the same build job in many different configurations. This powerful feature can be useful for testing an
                                 application in many different environments, with different databases, or even on different build machines

								 
### Advance project options 

1)Quiet period					:Mainly used to even developer having habit to commit some changes frequently to avoid conflict 

2)Block build when upstream     : Mainly used in inter-dependent project, keep child project on hold until parent project build ready 				project building finished 

3)Use custom workspace          : used to use custom workspace 


### Build Triggers

• Start a build job once another build job has completed
• Kick off builds at periodical intervals
• Poll the SCM for changes

### Jenkins authorization

1) Matrix based 

2) Project based 

3) Role based

### Unit testing on source
1) code coverage

2) other maven test & verfiy

### Code Quality in build process
1)Checkstyle

2)PMD also comes with CPD, a robust open source detector of duplicated and near-duplicated code

3)FindBugs
