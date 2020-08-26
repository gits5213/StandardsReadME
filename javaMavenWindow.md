# Set up Java & Maven for Windows

<!-- topics-start -->
* [Download JAVA](#Download-JAVA)
* [JAVA Vlidation](#JAVA-Vlidation)
* [Download Mavaen](#Download-Mavaen)
* [Maven Vlidation](#Maven-Vlidation)

## Download JAVA
- [Download JAVA](https://www.oracle.com/java/technologies/javase-downloads.html)
- Click on JDK Download
- Click on JDK Version 
- Extract the Folder 
- double Click on it > Click > Click > Finish
- Press Windows key, type ```adva``` and clicks on the ```View advanced system settings```
- clicks on the ```Environment Variables```
- In ```System variables``` clicks ```New...``` button to add a new JAVA_HOME variable and point it to the JDK installed folder.
    - JAVA_HOME
    - C:\Program Files\Java\jdkxxxx
- In System variables, find & select ```PATH``` and then clicks ```edit...``` button 
- In old version of Windows, it will prompt dialog box to edit the values directly, append this ```%JAVA_HOME%\bin;``` to the end of the line. DO NOT Delete anything. 
- In latest Windows 10, it will prompt a dialog box, clicks on ```New button``` and add this 
    - ```%JAVA_HOME%\bin```

## JAVA Vlidation
- Press Windows key, type ```cmd``` and clicks on the ```Command Promt```
- Validation: Enter 
    - ```java -version``` It will appear the version messages. 

## Download Mavaen
- [Download Maven](https://maven.apache.org/download.cgi) 
- Download "Binary zip archive" File
- Extract the file
- Press Windows key, type ```adva``` and clicks on the ```View advanced system settings```
- clicks on the ```Environment Variables```
- In System Properties dialog, select ```Advanced tab``` and clicks on the ```Environment Variables...``` button.
- In ```Environment variables``` dialog, System variables, Clicks on the ```New...``` button and add a 
    - ```MAVEN_HOME``` 
    -  ```C:\Download\apache-maven-xxx```
- In system variables, find & Select ```PATH``` clicks on the ```Edit...``` button. In “Edit environment variable” dialog, clicks on the ```New button``` and add this 
    - ```%MAVEN_HOME%\bin```

## Maven Vlidation
- Press Windows key, type ```cmd``` and clicks on the ```Command Promt```
- Validation: Enter 
    - ```mvn -version``` It will appear the version messages. 
