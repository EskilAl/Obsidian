- [[#What is Command Line interface?|What is Command Line interface?]]
- [[#What is a shell prompt?|What is a shell prompt?]]
- [[#Good to know before we move on...|Good to know before we move on...]]
- [[#What are the Options and Arguments to a command?|What are the Options and Arguments to a command?]]
- [[#Linux Directory Structure|Linux Directory Structure]]
- [[#Linux Commands|Linux Commands]]
	- [[#Linux Commands#PWD|PWD]]
	- [[#Linux Commands#CD|CD]]
		- [[#CD#cd (without any dot)|cd (without any dot)]]
		- [[#CD#cd . (with a single dot)|cd . (with a single dot)]]
		- [[#CD#cd .. (with two dots)|cd .. (with two dots)]]
	- [[#Linux Commands#IS (1/2)|IS (1/2)]]
- [[#File permission|File permission]]
- [[#Permission Attributes|Permission Attributes]]
	- [[#Permission Attributes#less|less]]
	- [[#Permission Attributes#cat|cat]]
- [[#How to manipulate files and directories|How to manipulate files and directories]]
	- [[#How to manipulate files and directories#touch|touch]]
	- [[#How to manipulate files and directories#mkdir|mkdir]]
	- [[#How to manipulate files and directories#cp|cp]]
	- [[#How to manipulate files and directories#mv|mv]]
	- [[#How to manipulate files and directories#rm|rm]]
- [[#Change out role in Linux|Change out role in Linux]]
- [[#sudo|sudo]]
- [[#su|su]]
- [[#How to get help|How to get help]]
- [[#summing up|summing up]]



## What is Command Line interface?

* command line interface (CLI) is a text-based-user-interface(UI) used to manage computer files and run programs.*
* Other names: propts, shells


## What is a shell prompt?

* A Shell prompt is a short text message shown on a CLI.
* It appears whenever the shell is ready to accept commands from a user
* $ means that your identity is a regular user.
* "#" means that you are either the root user or you have superuser privilege's.
* if you see the tilde symbol (~), it means that you are in your home directory.

## Good to know before we move on...

* To see command history, press up arrow.
* To position the cursor anywhere we want on a command line, press left or right arrow.
* To automatically complete a command or a filename use tab.
* How to clear our screens in CLI?
	* Use command 'clear'
	* This command will clear all the contents on the screen and leave only the shell prompt.
* Linux is case-sensitive.
	* Uppercases and lowercases are treated as different.
	* Abc.txt and abc.txt are treated as two different files.
	* John and john are treated as two different users.
	* documents and Documents are treated as two different folders.

## What are the Options and Arguments to a command?

* A Linux command is often followed by one or more options and further by one or more arguments.
	- Options modify the command's behavior
	- Arguments are the items upon which the command acts.

## Linux Directory Structure

* In Linux, all files and directories are organized in a single tree structure, regardless of the number of attached storage devices.
* The root directory is the topmost directory and it is denoted by a forward slash /.*
* At any given time, the directory you are standing in is called your current working directory.
* Each user account has his home directory.
	* E.g. "/home/bill" is bill's home directory
	* (by default.)
	* Any regular user can only write to his home directory.


## Linux Commands

### PWD

* We can use the Pwd command to know where we are in a Linux Directory tree.*
* NOTE Pwd ? print working directory.

### CD

* The cd command allows us to go to a particular directory by specifying the pathname of the directory.
* A pathname can be specified in two ways:
	1. Absolute pathname
		* Start from the rood directory
	 2. Relative pathname
		* Start from the current working directory
		* need two special notation "." and ".."
		* "."
#### cd (without any dot)
* always send a user back to his/her home directory.
* Example
	* if my username is kelly, my default home directory would be /home/kelly
	* no matter where I am, I can return to my home directory by just typing "cd".
#### cd . (with a single dot)
* always send a user from his/her current working directory to his/her current working directory.
* in other words, the user doesn't go anywhere.

#### cd .. (with two dots)
* Always send a user to the parent directory of his/her current directory.
	- what if we are already in the root directory?
	-  We will stay in the root directory because it is the topmost directory in a Linux directory tree.

### IS (1/2)
* We can list the content of the current working directory like this:
*ls
* We can also specify a directory to list:
*ls /usr
* Can this command list the contents of multiple directories?
*ls/usr /home /
* The ls command comes with many options.

## File permission
* Three types of users from the perspective of a file/directory:
	* Owner: The user who owns the file/directory.
	* Owner: group: A group of users who owns the file/directory.
	* World: Everyone else.

## Permission Attributes 
* r
	* Files - Allows a file to be opened and read.*
	* Directories - Allows a directory's contents to be listed if the execute attribute is also set.
* w
	* Files -Allows a file to be written to or truncated, however this attribute does not allow files to be renamed or deleted. the ability to delete or rename files is determined by directory attributes.
* x
	* Allows a file to be treated as a program and executed. program files written in scripting languages must be set as readable to be executed.

### less
* when we want to view text files page by page, we can use the less command
* syntax *less filename.* 

### cat
* we can use the cat command to
	- create a short text file
	- display the content of a short text file
	- to exit the cat command, press Control key and the d key at the same time.

## How to manipulate files and directories

### touch
- we can easily create an empty file using this command.
	*touch f1 <--- Create an empty file.
	ls -l
	cat f1 <-- prints out the empty file
### mkdir
- this command allows us to create one or more directories.
- syntax: *mkdir dir1* or *mkdir dir1 dir2 dir3*
	*mkdir Books* <-- Create

* what happened if the directory you want to create already exist?

### cp
- This command can be used to two different ways:
- the first way: *cp item1 item2*
- Note: *Both item 1 and item 2 can be a file ore a directory*.
- The execution result will be different depending on the file types of *item1* and *item2* and the existence of *item2*. 
	- You will have a chance to practice it in the lab.

* the Second way: *cp item... directory*
* it will copy multiple items (either files or directories) into a directory.
* However, the destination directory must pre-exist.

### mv
- the mv command performs both file moving and file renaming, depending on how it is used.
- the original files(s) will be deleted from their original directories.
- syntax: *mv item1 item2*
	- it will either move or rename item 1(witch can be a file or a directory) to item2 depending on if item1 and item2 are in the same directory 
	- it will move one or more items to a directory

![[Pasted image 20230904093144.png]]

- some useful options:

![[Pasted image 20230904093330.png]]
### rm 
- the rm command is used to remove/delete files or directories
- syntax *rm item...
* ![[Pasted image 20230904093405.png]]

![[Pasted image 20230904093428.png]]

## Change out role in Linux
- Why would we do it?
	- in some cases, we might need to take on the identity of another user, for examples:
		- when we want to gain superuser privliges to carry out some administrative tasks.
		- E.g. *create/delete a user account*.
	* when we want to test an account for a regular user.
* How do we do it?
 1. Log out and log back in as the alternative user.
 2. Use the sudo command.
 3. use the su command.


## sudo
- the sudo command allows a regular user to execute commands as another user (usually the superuser) in a control way.
- On skyHIgh, you don't need to type any password to use the sudo command for the user account *ubuntu*
	- However, if you use your own linux machine, you will be asked to enter your own password for using the sudo command
- what will happen if you type the following two commands?
	- less /etc/shadow
	- sudo less /etc/shadow
## su
- the su command enables us to start a shell session as another user.
- if no username is specified, the root user is assumed.
- in general, execute this command required the target user's password-
	- not your own password!
* to return to your original user account, just type *exit*.

## How to get help
- you can learn more about a command or get more help by the  following way:
	-  help commandName
	- man commandName
- But maybe the best way would be using google search.


## summing up 
- we have learned 
		- What command line interface is
		- shell prompt
		- Linux directory tree
		- File permission
		- Commands to navigate and explore file system
			- pwd, cd, ls, less, cat
		- Commands to manipulate files and directories
			- touch, mkdir, cp, mv, rm
		- sudo and su
		- How to get help
		- 
