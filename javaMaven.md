# Set up Java & Maven for Mac & Windows

<!-- topics-start -->
* [What is a JDK](#What-is-a-JDK)
* [The installation process is very straight forward](#The-installation-process-is-very-straight-forward)
* [Download Maven](#Download-Maven)
* [Create & Set Up bash_profile for Java and Maven ](#Create-&-Set-Up-bash_profile-for-Java-and-Maven)
* [For Java](#For-Java)
* [For Maven](#For-Maven)

## Installing Java SE Development Kit on Mac
## What is a JDK?
-   The Java SE Development Kit, or JDK, is an extended subset of tools that allow for developing applications for the Java programming language.

### The installation process is very straight forward:
- Navigate to the [Java SE Downloads page](https://www.oracle.com/java/technologies/javase-downloads.html)
- Choose the JDK Download
- Download the appropiate JDK version based on the Operating System.
- Continue > Click > Click > Finish

### Download Maven
- Navigate to [Maven website](https://maven.apache.org/download.cgi)
- Click on First zipfile or 2nd zipfile and download
- Then extract the zipfolder
- Move extracted folder to Application folder ```mv apache-maven-xxxx /Application```

### Create & Set Up bash_profile for Java and Maven 
- Start up Terminal
- Type ```cd ~/``` to go to your home folder
- Type ```touch .bash_profile``` to create your new file.
- Open .bash_profile
```
open .bash_profile
```

### For Java 
- Validate JDK Version: From Laptop –> ```Shift + Command + G ``` then enter ```/Library/Java/JavaVirtualMachines/jdkXXXXXX ```
- Add ```export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdkXXXX/Contents/Home```
- Add ```export JAVA_HOME```
- Validate > java --version
- Validate > which java

### For Maven
- Add ```export M2_HOME=/usr/local/apache-maven/apache-maven-XXXXX```
- Add ```export M2_HOME```

- Add ```export PATH=${PATH}:${JAVA_HOME}/bin:${M2_HOME}/bin```
- Add ```export PATH```
- Validate > mvn --versioon
- Validate > which mvn

- Save & Close .bash_profile
- Open .bash_profile with editor like: vi/neno```> vi ~/.bash_profile```
- Press ESC + E (edit)
- Shift + : wq --> Press enter (Save & Quit)
- ```> source ~/.bash_profile```
- Validate > echo $JAVA_HOME
- Validate > echo $M2_HOME
