
# JMETER TESTS  

![architecture](src/main/resources/architecture.png)
  
This project contains a framework for testing the performance of applications.  
## Getting Started  
    
### Prerequisites  
  
* [Maven](https://maven.apache.org/) - Dependency Management  
* [Java](https://www.java.com/download/) - Dependency Management  
  
## Running the tests  
the tests are inside src/test /jmeter all tests expect a series of parameters through maven. they are in the pom.xml and you can add more there if needed 
  
#### default.jmx  
the .jmx should receive the following parameters:  

* threads   
* rampup   
* loop   
  
read the jmeter documentation for more info about these values.  if you need to use third files, you can put them on /test/jmeter/, like the audio700.mp3 demo file.
  
the maven task to run the test is verify. ex:  
  
mvn clean verify -Dthreads=1 -Dloop=1 -Drampup=10  -Djmeterscript=x.jmx

## Reporting
after the test run, you can find an html report inside the target folder.

## Built With  
* [Maven](https://maven.apache.org/) - Dependency Management  
* [Jmeter Maven Plugin](https://github.com/jmeter-maven-plugin/jmeter-maven-plugin) - Jmeter handler  
  
## Authors  
ramiro andrés cruz