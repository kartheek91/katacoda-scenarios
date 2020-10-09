# Commands in Ubuntu
We will learn some basic commands in order to get started with Linux environment.
### 1. echo: 
This command is used to display line of text/string that are passed as an argument.
```
kartheek@SAILS-DM87:~$ echo Sails Software Solutions
Sails Software Solutions
```
```
kartheek@SAILS-DM87:~$ echo $HOME
/home/kartheek
```
### 2. uname: 
This command displays the information about the system.
```
kartheek@SAILS-DM87:~$ uname
Linux
```
### 3. whoami: 
This command displays the username of the current user when this command is invoked.
```
kartheek@SAILS-DM87:~$ whoami
kartheek
```
### 4. man: 
This command is Used to show the manual of any command present in Linux.
```
kartheek@SAILS-DM87:~$ man echo
```
![Output of echo man](https://github.com/kartheek91/katacoda-scenarios/blob/main/linux-101/images/man.png)
### 4. ls: 
This command is Used to List Directory Contents, option  [a] = do not ignore entries starting with dot.

```
kartheek@SAILS-DM87:~$ ls
abc.txt  sample.txt  test
kartheek@SAILS-DM87:~$  
```
```
kartheek@SAILS-DM87:~$ ls -a
.              .bash_logout  .landscape   .oh-my-zsh  .sample.txt                .viminfo    abc.txt
..             .bashrc       .local       .p10k.zsh   .shell.pre-oh-my-zsh       .zshrc      sample.txt
.bash_history  .gem          .motd_shown  .profile    .sudo_as_admin_successful  .zshrc.swp  test
kartheek@SAILS-DM87:~$    
```
### 5. pwd: 
This command is Used to Print Working Directory.
```
kartheek@SAILS-DM87:~$ pwd
/home/kartheek
kartheek@SAILS-DM87:~$    
```

### 6. cd: Stands for Change Directory.
- To navigate into the root directory, use "cd /"
- To navigate to your home directory, use "cd" or "cd ~"
- To navigate up one directory level, use "cd .."
- To navigate to the previous directory (or back), use "cd -"
```
kartheek@SAILS-DM87:~$ cd test/
kartheek@SAILS-DM87:~/test$ pwd
/home/kartheek/test
```
```
kartheek@SAILS-DM87:~/test$ cd ..
kartheek@SAILS-DM87:~$ pwd
/home/kartheek
```
```
kartheek@SAILS-DM87:~$ cd -
/home/kartheek/test
```
```
kartheek@SAILS-DM87:~/test$ cd /
kartheek@SAILS-DM87:/$ pwd
/
kartheek@SAILS-DM87:/$    
```
### 7. mkdir: This command in Linux allows the user to create directories (also referred to as folders in some operating systems).

- How to create directories using mkdir?

```
kartheek@SAILS-DM87:~$ mkdir -v test
mkdir: created directory 'test'
kartheek@SAILS-DM87:~$ ls
abc.txt  sample.txt  test
kartheek@SAILS-DM87:~$                                                                                       
```
-  How to make sure parent directories (if non-existent) are created in process?

```
kartheek@SAILS-DM87:~$ "mkdir -p -v gsdd/medguides && touch gsdd/medguides/lasix.txt"
mkdir: created directory 'gsdd'
mkdir: created directory 'gsdd/medguides'
kartheek@SAILS-DM87:~$ cd gsdd/medguides/
kartheek@SAILS-DM87:~/gsdd/medguides$ ls
lasix.txt
kartheek@SAILS-DM87:~/gsdd/medguides$    
```