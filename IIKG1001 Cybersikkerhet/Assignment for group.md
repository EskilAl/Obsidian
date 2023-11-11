In this assignment, each group is required to perform a series of tasks one by one and show the corresponding results to two pre-determined TAs.

In this assignment, you will need to demonstrate your practical skills in

·       network configuration

·       VM creation

·       user and group management

·       file permissions and access control

·       file ownership management

·       User identity management and authentication

·       searching keywords from a file

·       Secure password implementation

·       File editing

·       symmetric key generation and management

·       asymmetric key pair generation and management

·       file encryption and decryption for data security

·       securing ftp services

·       transferring files in a secure way

·       troubleshooting

**When and where**:  It will be announced soon on blackboard.

**Rules:**

·       Two TAs will assess your group assessment. They will randomly choose one member from your group to perform a task. Make sure that all of you are familiar with the solutions to all the tasks, and able to explain the commands and the results to the TAs.

·       Each group will have at most 30 minutes to perform and show all the tasks.

·       There are a series of tasks. Each task is worth some points. If your group can successfully obtain 60 points out of 100 points, your group assignment is approved, meaning that all members in your group are allowed to take the exam in December.

·       You can bring a note with you, but the note cannot contain the complete solution to any task. If you cannot clearly explain the solutions to the TAs, you might lose some points. You are allowed to help your group members during the assessment, e.g., you can give them a hint, rather than taking over the task assigned to them.

**What you need to do way before the demo day**:

·      Make sure you have one ubuntu VM (called “server”) on one network on SkyHiGH.

·      Make sure you have another Ubuntu VM (called “uclient”) on another network on SkyHiGH.

**Tasks:**

1.      (3 points) Show the TAs that the “server” VM and the “uclient” VM are indeed on two different networks on SkyHiGh.

	"points at the network topologhy"

2.      (5 points) Create a user account called “John” on the “uclient” VM with only one command. Note the account must meet the following two requirements:

·       John has a default home directory called “John” under the /home directory.

·       John should use “/bin/bash” as his default login shell.

	sudo useradd -m -d /home/John -s /bin/bash John
- `-m`: This option creates the user's home directory if it does not exist.
- `-d /home/John`: Specifies the home directory for the user as "/home/John."
- `-s /bin/bash`: Sets the default login shell for the user as "/bin/bash."
- `John`: Specifies the username.


3.      (3 points) Show that the user account “John” is successfully created by searching this account name from the /etc/passwd file.

`go cd .. and then navigate to etc/ cat the passwd file and see the user there `

4.      (2 points) Show that the default home directory for John is successfully created and show the detailed information of this directory in a long format using the ls command.

`Navigate to the home directory, you can also just login and then  us ls -la or you can use ls -ld /home/John`

5.      (3 points) Create a secure password for John using the passwd command.

`passwd John type a safe password that is hard to hack, like 10 letters lover uper case, §§§§!!! makrings and stuff`

6.      (6 points) On the “uclient” VM, change your identity from “ubuntu” to “John” and to use John’s environment. After that, show John’s current working directory and John’s uid to the TAs.

`to change user you can just type su John, prob have to type the password you just made, so remember it.`

7.      (10 points) Keep your identify as John. Create a RSA key pair for John using OpenSSL.

`ssh-keygen, and rsa is default it is saved under home/.ssh`

8.      (2 points) Show the TAs where the key pair can be found.

`it can be found under home/.ssh`

9.      (2 points) Switch to the “server” VM. Show the private IP address of the “server” VM using the ip command.

`use ip a`

10.  (2 points) Show the floating IP address of the “server” VM via the SkyHiGh dashboard.

`point to floating ip adddress on the server`

11.  (2 points) Create a directory called “sftp” under the root directory on the “server” VM.

`just go to the directory and do mkdir sftp`

12.  (4 points) Create a group called “sftpGroup” on the “server” VM using the groupadd command, and then show the TAs that the group is indeed created by searching the group name from the /etc/group file.

`navigate to the etc file and find the group file.`

13.  (4 points) Make sure you stay on the “server ” VM now. Transfer the group ownership of the “/sftp” directory to group “sftpGroup” but keep the user owner the same. After that, show the TAs that the sftpGroup group indeed owns the “/sftp” directory by showing the long format of the “/sftp” directory.

`sudo chown :sftpGroup /sftp`

14.  (4 points) Keep staying on the “server” VM. Create a user account called “John”, assign the “/sftp” directory to be his home directory, and assign “sftpGroup” to be John’s primary group. Please use only one command to finish this task.

```bash
sudo useradd -m -d /sftp -g sftpGroup John
`````

15.  (5 points) Keep staying on the “server” VM. Add the following lines to the end of the /etc/ssh/sshd_config file using nano. Please show the TAs how you do it.

       _Match group sftpGroup_

        _ChrootDirectory /sftp_

        _PermitTunnel no_

        _X11Forwarding no_

       _AllowTcpForwarding no_

       _ForceCommand internal-sftp_

       _PasswordAuthentication yes_

After that, you should execute command “sudo service ssh restart” to restart the ssh service.

16.  (8 points) Now use the terminal on the “uclient” VM and use user account “John” to connect to the sftp service on the “server” VM.

````bash
sftp John@<server-IP-address>
````

17.  (10 points) Make sure you stay on the “uclient” VM now and terminate the sftp connection that was created in the previous task. After that, switch your identity to John and then create a symmetric key with 128 bits using OpenSSL. Please name the key “sym.key”.

````bash
sudo su - John
openssl rand -out sym.key 16
````

18.  (8 points) Keep being John on the “uclient” VM. Make a text file and use the symmetric key to encrypt the file. Show the contents of the file before and after encryption.

```bash
echo "This is a sample text file." > plaintext.txt
```

`cat plaintext.txt

`openssl enc -aes-128-cbc -in plaintext.txt -out ciphertext.enc -kfile sym.key
`
`cat ciphertext.enc
`


19.  (10 points) Stay on the “uclient” VM. Use John’s account to upload both “sym.key” and the previously encrypted file to the sftp server. Please tell the TAs where the key and the file will be uploaded to, and who can see them. If you couldn’t upload the key and the file, try to make them work and explain to the TAs how you solve the problem.

20.  (7 points) Switch to the “server” VM and use user account “ubuntu”. Try to decrypt the encrypted file uploaded by John using John’s symmetric key. Please show the decrypted file contents to the TAs.