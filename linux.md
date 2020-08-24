# Day to Day Unix/Linux Command
<!-- topics-start -->
* [Checking for existing SSH keys](#)
* [Generating a new SSH key and adding it to the ssh agent](#)
* [Adding your SSH key to the ssh agent](#)
* [Adding a new SSH key to your GitHub account](#)

## Command line 
```
- ls (List)
- ls -R (will list all the files in the sub-directories as well)
- ls -a (will show the hidden files)
-ls -al (will list the files and directories with detailed information like the permissions, size, owner, etc.)
- pwd (Present working directory)
- cd (Change directory: to go straight to the home folder)
- cd- (with a hyphen) to move to your previous directory
- cd Desktop (Change directory to the Desktop)
- cd .. (One directory up (back))
- clear (Clear up the terminal)
- cd / (Change directory to the root directory of MAC)
- cd ~ (Change directory to the User directory)
- cd Desktop/test (Change directory to the test folder on the Desktop)
- open . (Folder will open)
- mkdir Test (Test Folder will create)
- cd Test (Change directory into Test Folder)
- touch index.html (Index.html file will created)
- open index.html (Index.html file will open)
- open -a "Sublime Text" (Open only Sublime editor)
- open -a "Sublime Text" Index.html (Index.html file will open with Sublime Text)
- mv index.html about.html (Rename the File)
- rm about.html (delete the file/Only works for file)
- rm -r Test (delete the Folder)
- say this is soooo cool
- echo (Print statement)
- zip, unzip (to Zip and Extract the file)
- Keyboard: Up arrow and Down arrow will bring up the entire history
- Keyboard: autofill what you are typing
- Keyboard: Ctrl + C (Terminate any command)
- Keyboard: Ctrl + Z (Pause any command)
- Keyboard: Ctrl+ S (Freeze Terminal)
- Keyboard: Ctrl + Q (Unfreeze Terminal)
```
### ou can run multiple commands in one single command by using the “;” to separate them. For example Command1; Command2; Command3. Or use && if you only want the next command to run when the first one is successful.

# Advanced Command
```
> cat(short for concatenate) is one of the most frequently used commands in Linux. It is used to list the contents of a file on the standard output (sdout). To run this command, type cat followed by the file’s name and its extension. For instance: cat file.txt.
> cp | Use the cp command to copy files from the current directory to a different directory. For instance, the command cp scenery.jpg /home/username/Pictures would create a copy of scenery.jpg (from your current directory) into the Pictures directory.
> mv | The primary use of the mv command is to move files, although it can also be used to rename files. For example: mv file.txt /home/username/Documents.
- grep | It lets you search through all the text in a given file. grep blue notepad.txt will search for the word blue in the notepad file.
- sudo | Short for “SuperUser Do”, this command enables you to perform tasks that require administrative or root permissions.
- head | The head command is used to view the first lines of any text file. For example, if you only want to show the first five lines, type head -n 5 filename.ext.
- tail | This one has a similar function to the head command, but instead of showing the first lines, the tail command will display the last ten lines of a text file. For example, tail -n filename.ext.
- diff | Short for difference, the diff command compares the contents of two files line by line. After analyzing the files, it will output the lines that do not match. Programmers often use this command when they need to make program alterations instead of rewriting the entire source code.

The simplest form of this command is diff file1.ext file2.ext
- chmod | chmod is another Linux command, used to change the read, write, and execute permissions of files and directories. i,e [chmod 754 myfile](https://www.computerhope.com/unix/uchmod.htm)
- chown | transfer the ownership of a file to the specified username
- kill | process identification number (PID) of the program you want to kill. i.e. kill [signal option] PID.
- ps ux | process identification number (PID) of the program 
-man | Manual Instruction of any command 

