###Jenkins interview Questions

**1)Explain how you can move or copy Jenkins from one server to another?**

Answer:
1)Slide a job from one installation of Jenkins to another by copying the related job directory

2)Make a copy of an already existing job by making clone of a job directory by a different name

3)Renaming an existing job by renaming a directory.

**2)Mention what are the commands you can use to start Jenkins manually?**

Answer:
(Jenkins_url)/restart: Forces a restart without waiting for builds to complete

(Jenkin_url)/safeRestart: Allows all running builds to complete

**3)  Explain how you can deploy a custom build of a core plugin? **

Answer:

1)Stop Jenkins

2)Copy the custom JPI file to $JENKINS_HOME/plugins

3)Remove the previously expanded plugin directory

4)Create an empty file called <plugin>.jpi.pinned - e.g. maven-plugin.jpi.pinned

5)Start Jenkins

**4) What you do to make sure that your project build doesn’t break in Jenkins ?**

Answer:

1)I make sure that I perform successful clean install on my local machine with all unit tests.

2)Then I make sure that I check in all code changes.

3)Then I do a Synchronize with repository to make sure that all required config and POM changes and any difference is checked into the repository.


**5)  What you do when you see a broken build for your project in Jenkins ?**

Answer:

1)I will open the console output for the build and will try to see if any file changes were missed.

2)If not able to find the issue that way, Will clean and update my local workspace to replicate the problem on my local and will try to solve it.



**6)  How do you trigger builds on remote servers ? **

Answer
[ master-slave concept]


**7) How do you change base directory of checkout in Jenkins?**

Answer:

custom workspace

**8) Is there a way to reset all (or just disable the security settings) from the command line without a user/password as I have managed to completely lock myself out of Jenkins?**

Answer:
The simplest solution is to completely disable security - change true to false in /var/lib/jenkins/config.xml file.

	<useSecurity>true</useSecurity>
		
Then just restart Jenkins, go to admin panel and set everything once again.
