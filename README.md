#Cybercat

Test automation framework

##System Requirements
- Git (http://git-scm.com/downloads)
- Java SE 7 (http://www.oracle.com/technetwork/java/javase/downloads/index.html)
- Maven  3.1.x (http://maven.apache.org/)
- Apache Ant 1.9.x (http://ant.apache.org/)


##Quick start

### Eclipse
- Install required software 
- Install Firefox
- Install Eclipse with maven & TestNG plugin 
- Run from commant line: git clone https://github.com/ubegun/Cybercat-sample.git
- Rename project folder
- edit pom.xml
- Remove .git from project folder
- Open Eclipse & import your existing maven project 
- Run SiteExploring.java as TestNG test 

### Command Line
- Run from commant line: git clone https://github.com/ubegun/Cybercat-sample.git
- Rename project folder
- edit pom.xml
- Remove .git from project folder
- execute: mvn clean compile test-compile antrun:run -X -Dconfig.properties=test.properties  -DfailIfNoTests=false -Dconfig.basicArtifactsDir=C:\Temp\Cybercat\Green
- execute: ant -f green.xml


##Helpful links 
https://www.facebook.com/af.cybercat - You can read last news & short notes about current project release

https://twitter.com/CyberCatAF - project timeline 

##What features are available in this project?

- functional feature boxing (BDD process)
- step-by-step video on tests execution 
- exception screenshots
- functional steps screenshots
- summary report on run tests
- short/detail execution logs
- any page objects may contain any subpage objects (called page fragments)
- any feature may contain another feature
- all functional objects are autowired on runtime 
- Feature version control
- compatible for running integration tests


##How does the project structure look like? 

```
core 
 | 
 `-> page objects , page fragments , integration services
      |     
      `-> feature steps
            |
            `-> test cases
```

##Cybercat maven repository configuration:

####pom.xml

```xml
...
<repositories>
    <repository>
        <id>Cybercat-mvn-repo</id>
        <url>https://raw.github.com/ubegun/Cybercat/mvn-repo/</url>
        <snapshots>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
        </snapshots>
    </repository>
</repositories>  
...
<dependency>
  <groupId>org.cybercat.autotest</groupId>
  <artifactId>cybercat-automation-core</artifactId>
  <version>0.5-SNAPSHOT</version>
</dependency>
...
```

## License
* [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
