
# Recap - File Access Control

![[Pasted image 20230917205328.png]]
**File mode:** it shows file permission attributes for three types of users.

Three types of users from the perspective of a file/directory:
- **Owner**--The user who owns the file/directory:
- **Owner group** - A group of users who own the file/directory
- **World** -- Everyone else

![[Pasted image 20230917205354.png]]

# chmod - Change file mode 

- This command is used to change the **file mode (permission)** of a file/directory.
- Who can execute this command?
	1. **File/directory owner**
	2. **Superuser**
		- A superuser is **a user** who has **all permissions** to perform administrative tasks. He is **not** necessary to be the root user.
		- The **root user** is  <font color="red">a superuser  </font> and <font color ="red"> the main superuser </font>
- This command changes file mode based on two ways:
	1. **Symbolic representation (or called Symbolic mode)**
	2. **Octal number representation (or called Numeric mode)**

# chmod based on Symbolic Representation 

![[Pasted image 20230917210251.png]]
![[Pasted image 20230917210309.png]]

# chmode based on octal Number Representation
- Octal is a base-8 number system. It uses the digits from 0 to 7.
- How do we translate a file mode to an octal number?
	- Each type of permission has a specific octal value:
	- We need to sum up total octal values of the file mode.
![[Pasted image 20230917210556.png]]
- By using **three octal digits**, we can set the **file mode** for **the file owner**, **group**, and **the world**.

- Examples: ![[Pasted image 20230917210700.png]]

# command "id"
- This command prints information about an account.
	- Syntax: `id[-options][userName]`
	- Superuser privileges are **NOT** required to run this command.

![[Pasted image 20230917210838.png]]

# chown - Change file ownership
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

# The /etc/passwd file
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

# Commands related to User Management
- useradd
- usermod
- userdel
	- <font color="brown"> Note: Superusers privliges are required to run these commands. </font>


