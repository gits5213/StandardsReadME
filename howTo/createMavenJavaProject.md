# How to create a Java Maven Selenium project?

<!-- topics-start -->
* [Create Java Maven Selenium Project](#Create-Java-Maven-Selenium-Project)
* [Import Project into Eclipse](#Import-Project-into-Eclipse)
* [Adding dependencies into pom-xml file](#Adding-dependencies-into-pom-xml-file)

### If you already don't have Java & Maven In your system, go ahead download and install and set up environment for windows and set up .bash_profile for MAC, Follow the seperate readme file.

## Create Java Maven Selenium Project
- Pre-requirement: Java & Maven work for the System.
- Open CMD/Terminal
- Change Directory (cd) as you wish to create a new project
- Copy and past below command on the CMD/Terminal

    > mvn archetype:generate -DgroupId=com.mycompany.app -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false

- Change ```com.mycompany.app``` to your company & project name i.e. ```com.ittci.boa```
- Change ```my-app ``` to your project name i.e. ```boa```
- Hit enter on the keyboard
- Vlidate: ```Build Success```
- Change Directory(cd) to project which is just created i.e. ```cd boa```
- Enter: ```mvn clean``` 
- Vlidate: ```Build Success```
- Enter: ```mvn compile```
- Vlidate: ```Build Success```
- If you using Eclipse as a IDE using below command otherwise not for compatible with Eclipse
- Enter: ```mvn eclipse:eclipse```
- Vlidate: ```Build Success```

## Import Project into Eclipse
- Open up your eclipse
- File > Import > General > Existing projects into Workspace > Next 
- Click on the Browse & Select the project from the System (which is you just created - boa)
- Click on Finish

## Adding dependencies into pom-xml file
- Open pom.xml file
- Inside dependencies add your Selenium, TestNG, ChromDriver dependency
- Navigate to [MVN Repository](https://mvnrepository.com/)
- Search for ```Selenium Java```|```Testng```| ```Selenium Chrome Driver```
- Click on the ```Selenium Java```|```Testng```| ```Selenium Chrome Driver``` > Click on the Highest ```Usages``` Version numer
- Copy & Past it into pom.xml file i.e.
    ```
    <dependencies>
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>3.141.59</version>
        </dependency>
        <dependency>
            <groupId>org.testng</groupId>
            <artifactId>testng</artifactId>
            <version>6.14.3</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-chrome-driver</artifactId>
            <version>3.141.59</version>
        </dependency>
    </dependencies>

    ```
    - NOTE: PAST It inside ```<dependencies>```
    - Now once you done that
    - Go back to CMD/Terminal & perform 3 maven command ```mvn clean, mvn compile & mvn eclipse:eclipse```
    - Vlidate: BUILD SUCCESS

    - Return to Eclipse and Refresh project 
    - Right click on the project > Click on the Refresh 
    - Vlidate: Referenced Library apears inside the project. and you are good to go.
    - Start create your packages and clases to do your test cases
    