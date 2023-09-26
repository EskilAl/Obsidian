- [[#Recap - File Access Control|Recap - File Access Control]]
- [[#chmod - Change file mode|chmod - Change file mode]]
- [[#chmod based on Symbolic Representation|chmod based on Symbolic Representation]]
- [[#chmode based on octal Number Representation|chmode based on octal Number Representation]]
- [[#command "id"|command "id"]]
- [[#chown - Change file ownership|chown - Change file ownership]]
- [[#The /etc/passwd file|The /etc/passwd file]]
- [[#Commands related to User Management|Commands related to User Management]]
	- [[#Commands related to User Management#useradd|useradd]]
	- [[#Commands related to User Management#usermod|usermod]]
	- [[#Commands related to User Management#userdel|userdel]]
- [[#Summing up|Summing up]]

## Recap - File Access Control

![[Pasted image 20230917205328.png]]
**File mode:** it shows file permission attributes for three types of users.

Three types of users from the perspective of a file/directory:
- **Owner**--The user who owns the file/directory:
- **Owner group** - A group of users who own the file/directory
- **World** -- Everyone else

![[Pasted image 20230917205354.png]]

## chmod - Change file mode 

- This command is used to change the **file mode (permission)** of a file/directory.
- Who can execute this command?
	1. **File/directory owner**
	2. **Superuser**
		- A superuser is **a user** who has **all permissions** to perform administrative tasks. He is **not** necessary to be the root user.
		- The **root user** is  <font color="red">a superuser  </font> and <font color ="red"> the main superuser </font>
- This command changes file mode based on two ways:
	1. **Symbolic representation (or called Symbolic mode)**
	2. **Octal number representation (or called Numeric mode)**

## chmod based on Symbolic Representation 

![[Pasted image 20230917210251.png]]
![[Pasted image 20230917210309.png]]

## chmode based on octal Number Representation
- Octal is a base-8 number system. It uses the digits from 0 to 7.
- How do we translate a file mode to an octal number?
	- Each type of permission has a specific octal value:
	- We need to sum up total octal values of the file mode.
![[Pasted image 20230917210556.png]]
- By using **three octal digits**, we can set the **file mode** for **the file owner**, **group**, and **the world**.

- Examples: 
  ![[Pasted image 20230917210700.png]]

## command "id"
- This command prints information about an account.
	- Syntax: `id[-options][userName]`
	- Superuser privileges are **NOT** required to run this command.

![[Pasted image 20230917210838.png]]

## chown - Change file ownership
- This command is used to **change** the owner and group owner of a file or a directory.
- Syntax:
	- <font color="red"> chown [new_owner][:[new_group]] file...</font>
	- <font color="red"> chown [new_owner][:[new_group]] directory...</font>
- **Superuser privileges** are required to run this command.
- is a regular user able to change the ownership of his/her file using this command?

![[Pasted image 20230917211324.png]]
* ***Complete commands:**
	* `sudo chown bob f1.txt`
	* `sudo cown bob:users f1.txt`
	* `sudo chown :admins f1.txt`
	* `sudo chown bob: f1.txt`

## The /etc/passwd file
- This file contains information for all accounts on a Linux system.
- The /etc/passwd file is a text file and it is **world-readable.**

![[Pasted image 20230917212113.png]]

- **Each record** represents **one account**, and it consists of 7 fields separated by <font color="yellow"> colons (:) </font>
	1. Username or account name
	2. The password field.
		- `x` denotes the password is **encrypted** and saved in the `/etc/shadow` file.
	3. uid
	4. Primary gid (More group info is stored in the **/etc/group file)
	5. A commentary field to describe an account, such as full name, contact info.
	6. Home directory 
	7. the default login shell that is assigned to the account.

## Commands related to User Management
- useradd
- usermod
- userdel
	- <font color="brown"> Note: Superusers privliges are required to run these commands. </font>

### useradd 
- This command is ues to create a new account and modify default information for the account.
- syntax: <font color="red"> useradd [-options] NewAccountName </font>
- Example: 
![[Pasted image 20230917215003.png]]

- Some commonly used options:
	- Option `m`:
		- With this option, **a default home directory** will be created.
![[Pasted image 20230917215250.png]]
- options `md`
	- To **Specify a different home directory** for the new account.
![[Pasted image 20230917215402.png]]

- Option `g`:
	- Specify **an existing group** to be the new account's **primary group**.
	- Both **gid** and **group name** are accepted.
![[Pasted image 20230917215528.png]]

- Option `G`:
	- Add the new account to **multiple existing groups**.
	- Each **group name** or **GID** is separated from the next by **a comma,** with no intervening space.
![[Pasted image 20230917215719.png]]

- Option `s`:
	- By default, login shell for every new account is "<font color="red">/bin/sh.</font>".
		- Which is defined by **variable "SHELL"** in the **"/etc/default/useradd"** file.
	- With options `s`, we can change **the login shell** for the new account.
	- Example: <font color="brown"> sudo useradd -s/bin/bash john</font>

### usermod
- This command is used to **change any attributes** associated with an **existing account**.
- Syntax: <font color="red"> usermod [options] ExistingUserName </font>
- Some commonly used options:
	- Option `g`:
		- Change the specified account's **primary group**
		![[Pasted image 20230917220419.png]]
		
	- Option `G`: 
		- Add the specified account to **more existing groups.**
		![[Pasted image 20230917220514.png]]
		
- Option <font color="red"> -G " "</font>
	- Remove the account from all groups except his primary group
![[Pasted image 20230917220651.png]]

How do we remove an account from a particular group?
<font color="yellow"> sudo gpasswd -d userName groupName </font>
![[Pasted image 20230917220746.png]]

![[Pasted image 20230917220801.png]]

- Option `md`:
	- Change the specified account's **home directory**.
![[Pasted image 20230917220848.png]]

- Option `l` (the lower case of L):
	- Change the specified account's **username**.
	- Syntax: sudo usermod <font color="yellow"> -l newName oldName </font>
- ![[Pasted image 20230917221025.png]]

- Option `s`:
	- Change the **login shell** for an existing account.
	- E.g., <font color="brown"> sudo usermod -s /bin/bash olaf </font>

### userdel 
- This command is used to <font color="red"> delete </font> an existing account.
- Syntax : <font color="red"> userdel [options] userName </font>
- if no options is specified, the account will be **removed**, but the associated **home directory will be kept**. 
	- E.g., <font color="brown"> sudo userdel olaf </font>
	- Use case: if that gome directory is **worth** to keep.
- Option `r`:
	- the account's **home directory** will be **removed** as well.
	- E.g.,  <font color="brown"> sudo userdel -r olaf </font>
- Option `f`:
	- it **forces** the removal of the specified account and its home directory, even if the account is still logged in.
	- This option is **dangerous** and mat leave your system in an **inconsistent** state.

## Summing up
- Linux commands related to access control and user management
	- chmod
		- Symbolic representation
		- Octal number representation
	- id
	- chown
	- useradd
	- usermod
	- userdel



