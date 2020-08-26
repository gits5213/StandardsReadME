# Set up Java & Maven for Windows

<!-- topics-start -->
* [What is a JDK](#What-is-a-JDK)
* [The installation process is very straight forward](#The-installation-process-is-very-straight-forward)
* [Download Maven](#Download-Maven)
* [Create & Set Up bash_profile for Java and Maven ](#Create-&-Set-Up-bash_profile-for-Java-and-Maven)
* [For Java](#For-Java)
* [For Maven](#For-Maven)

## Download JAVA
- [Download JAVA](https://www.oracle.com/java/technologies/javase-downloads.html)
- Click on JDK Download
- Click on JDK Version 
- Extract the Folder 
- double Click on it > Click > Click > Finish


## Download Mavaen
- [Download Maven](https://maven.apache.org/download.cgi) 
- Download "Binary zip archive" File
- Extract the file
- Press Windows key, type ```adva``` and clicks on the ```View advanced system settings```
- clicks on the ```Environment Variables```
- In ```System variables``` clicks ```New...``` button to add a new JAVA_HOME variable and point it to the JDK installed folder.
    - JAVA_HOME
    - C:\Program Files\Java\jdkxxxx
- In System variables, find & select ```PATH``` and then clicks ```edit...``` button 
- In old version of Windows, it will prompt dialog box to edit the values directly, append this ```%JAVA_HOME%\bin;``` to the end of the line. DO NOT Delete anything. 
- In latest Windows 10, it will prompt a dialog box, clicks on ```New button``` and add this 
    - ```%JAVA_HOME%\bin```
  ![images](/images/windows/add-JAVA-HOME-Windows.png)

- Validation: Open CMD Commnad prompt and Type 
    - ```java -version``` It will appear the version messages. 
