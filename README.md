# Lab1Linux

1.	Create a user account with the following attribute

• username: xxxx

• Fullname/comment: xxx xxx

• Password: xxxxx
```
useradd adam
sudo usermod -c "adam mohammed" adam
sudo passwd adam
```
2.	Create a user account with the following attribute

• Username: baduser

• Full name/comment: Bad User

• Password: baduser
```
useradd baduser
sudo usermod -c "Bad User" baduser
sudo passwd baduser
```
3.	Create a supplementary (Secondary) group called pgroup with group ID of 30000
```
 sudo groupadd -g 30000 pgroup
```
4.	Create a supplementary group called badgroup
```
 sudo groupadd -g badgroup
```
5.	Add xxx user to the pgroup group as a supplementary group
```
usermod -g pgroup mona
```
7.	Modify the password of xxx's account to password
```
sudo passwd xxx
```
7.	Modify xxx's account so the password expires after 30 days
```
sudo chage -M 30 mona
```
8.	Lock bad user account so he can't log in
```
sudo usermod --lock baduser
```
9.	Delete bad user account
```
userdel baduser
```
10.	Delete the supplementary group called badgroup.

11.	Create a folder called myteam in your home directory and change its permissions to read only for the owner.
```
chmod ogu-rwx myteam
chmod u+r myteam

```
12.	Log out and log in by another user
```
exit
```
```
su - mona
```
13.	Try to access (by cd command) the folder (myteam)

```
output:wont access
```
14.	Using the command Line

Change the permissions of oldpasswd file to give owner read and write permissions and for group write and execute and execute only for the others (using chmod in 2 different ways)

change your default permissions to be as above.
```
touch oldpasswd
```
```
chmod u=rw,g=wx,o=x oldpasswd
```
or 
```
chmod go-r,go+x oldpasswd
```
15.	What is the maximum permission a file can have, by default when it is just created? And what is that for directory.
```
-rw-r--r--
```
```
drwxr-xr-x 
```
16.	Change your default permissions to be no permission to everyone then create a directory and a file to verify.

17.	What are the minimum permission needed for:

Copy a directory (permission for source directory and permissions for target parent directory)

Copy a file (permission for source file and and permission for target parent directory)

Delete a file
```
222
```
Change to a directory
```
111
```
List a directory content (ls command)
```
444
```
View a file content (more/cat command)
```
444
```
Modify a file content
```
222
```
18.	Create a file with permission 444. Try to edit in it and to remove it? Note what happened.
that is in vim
```
E45: 'readonly' option is set (add ! to override)       
```
```
[No write since last change]
```
remove it :
```
rm test5
```

19.	What is the difference between the “x” permission for a file and for a directory?

20.	Using vi write your CV in the file mycv. Your CV should include your name, age, school, college, experience,...
```
vim mycv
```
21.	Open mycv file using vi command then: Without using arrows state how to:

Show all lines numbers
```
:set number
```
Search for word age
```
/age
```
Step to line 5 (assuming that you are in line 1 and file is more than 5 lines).
```
5G

```
Delete the line you are on and line 5.
```
:.,5 d
```



22.	List the available shells in your system.
```
cat etc/shells
```
23.	List the environment variables in your current shell.
```
env
```
24.	List all of the environment variables for the bash shell.
```
env
```
25.	What are the commands that list the value of a specific variable?
```
echo $varname
```
26.	Display your current shell name.
```
echo $SHELL
```
27.	State the initialization files of: sh, ksh, bash.

28.	Edit in your profile to display date at login and change your prompt permanently.
```
vim ~./bashrc
echo"Last Login: $(date)"
```

29.	Execute the following command :

echo \ then press enter

What is the purpose of \ ?

Notice the prompt ”>” what is that? and how can you change it from “>” to “:”. (Search PS1, PS2, ...)

30.	Create a Bash shell alias named ls for the “ls –l” command
```
vim ~.\bashrc
alias ls='ls -l'
source ~.\bashrc
```




