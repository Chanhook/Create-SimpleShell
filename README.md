# Create-SimpleShell
OS Design 2nd HW 
17102045 Kim Chanhyeok

# Create a Shell Interface Using Java


# 1 Project Description
Create a shell interface using Java. And verify that given commands such as 
'ls','ps','cat','cd',and 'history' are executed correctly.

# 2 Initial Settings
### Compile SimpleShell.java
`$ javac SimpleShell.java` Then, there is SimpleShell.class in same directory.

### Run the SimpleShell.class
`$ java SimpleShell` Then, you can see `jsh> ` on the terminal.

# 3 Functional Description
### cd
*`cd`
    *Current directory change to /home/user/ 
    *Absolute path is working

*`cd /home`
    *Current directory change to /home

*`cd user`
    *Current directory change to sub directory folder named user when current directory is home
    *Relative path is working

*`cd <any existing folder>` or `cd ./<any existing folder>`
    *Current directory change to input directory

*`cd fakeDirectory`
    *Print error message that `The specified path could not be found.`

### History
*`history`
    *Print all history of commands

*`history <number>`
    *Print the number of recently commands
     
*`history !!`
    *Run the previous command in the history
	
*`history !<number>`
    *Run the <number> index command in the history

### Other Shell command
*`ls`
    *Shows a list of directories and files in a particular directory
    
*`pwd` 
    *Command that displays the absolute path to which directory path you are currently in

*`cat`
    *Print the contents of the file

# 4 Error and exception handling
1. `cat <not exist file or directory>`
    *`No such that file or directory`

2. `cd fakeDirectory` Error message for invalid path
    *`The specified path could not be found.`

3. `history !!` When there is no element in history
    *`bash: !!: event not found`

4. `history !<ith>` When there is no element in history ith index
    *`bash: !<ith>: event not found` 

5. `history <number>` When number exceeds size of history
    *print all of history elements

6. When any command not exist is inputted
    *`<command>: command not found`
