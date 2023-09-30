# gradle-tutorial
Everything related to understanding of gradle. This repo is used to learn about Gradle and Git repo creation in local and pushing it to Github.

Gradle has 3 main thigns:   
- What app to build?   
- what dependency to include/use to build and dependency management system?  
- Additional actions to take (tasks)?  

**gradlew** uses a downloaded version of gradle instead of a locally installed gradle. This helps every developer running this project to build it with same gradle version in their local machines

*Hierarchy:*   
Project ->  Build script -> Tasks  & plugins

gradlew tasks
plugins help with adding new common tasks that many generally use

Important things about groovy used by Gradle:   
	1. Parenthesis after method are optional unless there are no arguments in which case they are required   
       - So id 'java' and id('java') both are same   
	2. Everything is a class and method and the start is org.gradle.api.Project class [https://docs.gradle.org/current/javadoc/org/gradle/api/Project.html]   
	3. {} brackets are closure like lambda expressions that you pass to a method as argument   
	4. Some methods take Map as argument  
		- Like `attributes('Main-class':'com.example.tutorial.GradleTutorial')`  
		- Again above line is same as attributes 'Main-class':'com.example.tutorial.GradleTutorial'  
		- ap is created without having to use new keyword here  

Started the project creation by running `gradle init`. Chosen options it has given.
Then updated build.gradle file with required tasks for the present simple java project
Then added testing with junit5
This also list all Gradle tasks programatically written in build.gradle
Explored tasks creation, println and groovy syntax i.e. parenthesis, closures

**To push to git:**
- Created a new repo with same name as project name on github.com
- In local ran `git init`
- configured git in local with username, email and above created repo url`git remote add origin <REMOTE_URL>`
- Created personal token
- Then committed the files and pushed `git push origin master`


References:
https://www.youtube.com/watch?v=-dtcEMLNmn0

