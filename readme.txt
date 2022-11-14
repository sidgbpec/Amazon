This project can be used to automation a web application
Selenium API is being used for automation
Java and Javascript programming languages are being used
Page Object Model is being used with Page Factory
Log4j is being used for logging
TestNG is being used for unit testing framework
Maven is being used for dependency and build management
Extent report is being used for reporting
Bacially currently 3 packages are there: 
	a. config package to read config.properties like web application url
	b. pages package to create java classes for each page
	c. tests package to create test cases
4 folders are being used currently:
	a. Configurations: to store config files like config.properties
	b. Images: to store screenshots for actual result
	c. log: to store application and testlogs files
	d. target: to store Extent Spark report.
Selenium Grid is implemented for remote testing.
	start hub as follows: 
		download and store Selenium server standalone jar and all the driver executables in the same folder.
		open command prompt, navigate to above folder
		execute below command to start hub
			java -jar nameofseleniumserverstandalonejarfile hub
			note down the hub URL which is shown for hub at the end in command prompt and mention this 
			in hubURL in config.properties file inside Configurations folder
		execute below command to start node
			java -jar nameofseleniumstandaloneserverjarfile node --detect-drivers true
		launch hub URL in browser and make sure that nodes are being shown.
To run this project use one of the below methods: 
	1. right click on testng.xml and RunAs TestNG Suite.
	2. right click on pom.xml and click Run As and then click Maven test
	3. Open command prompt, navigate to directory of project where pom.xml is placed, type 
	command mvn test -Dtest=”AboutSection” and hit enter. You can also mention comma separated other test classes if any.
	4. right click on the project and select Run As TestNG test