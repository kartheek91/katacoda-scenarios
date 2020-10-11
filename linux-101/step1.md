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
kartheek@SAILS-DM87:~$ mkdir -p -v gsdd/medguides && touch gsdd/medguides/lasix.txt
mkdir: created directory 'gsdd'
mkdir: created directory 'gsdd/medguides'
kartheek@SAILS-DM87:~$ cd gsdd/medguides/
kartheek@SAILS-DM87:~/gsdd/medguides$ ls
lasix.txt
kartheek@SAILS-DM87:~/gsdd/medguides$    
```
### 8. rmdir: It is a command-line utility for deleting empty directories. It is useful when you want to delete a directory only if it is empty, without needing to check whether the directory is empty or not.
```
kartheek@SAILS-DM87:~$ mkdir -p -v test && touch /home/kartheek/test/sample.txt
mkdir: created directory 'test'
kartheek@SAILS-DM87:~$ cd test/
kartheek@SAILS-DM87:~/test$ ls
sample.txt
kartheek@SAILS-DM87:~/test$ cd ../
kartheek@SAILS-DM87:~$ rmdir test/
rmdir: failed to remove 'test/': Directory not empty
```
In the above example directpry is not empty as it contains "sample.txt" file. rmdir command only works when you want to delete a directory only if it is empty.

```
kartheek@SAILS-DM87:~$ cd test/
kartheek@SAILS-DM87:~/test$ rm sample.txt
kartheek@SAILS-DM87:~/test$ cd ../
kartheek@SAILS-DM87:~$ rmdir -v test/
rmdir: removing directory, 'test/'
kartheek@SAILS-DM87:~$ ls
abc.txt  gsdd  sample.txt
kartheek@SAILS-DM87:~$ 
```
### 9.File creation in ubuntu:
### touch: If the file name specified as an argument doesn’t exist touch will create a new file.
```
kartheek@SAILS-DM87:~$ touch file1.txt
kartheek@SAILS-DM87:~$ ls
file1.txt  gsdd
kartheek@SAILS-DM87:~$ touch file2.txt file3.txt
kartheek@SAILS-DM87:~$ ls
file1.txt  file2.txt  file3.txt  gsdd
kartheek@SAILS-DM87:~$  
```

### 10.touch: If the file name specified as an argument doesn’t exist touch will create a new file.
```
kartheek@SAILS-DM87:~$ touch file1.txt
kartheek@SAILS-DM87:~$ ls
file1.txt  gsdd
kartheek@SAILS-DM87:~$ touch file2.txt file3.txt
kartheek@SAILS-DM87:~$ ls
file1.txt  file2.txt  file3.txt  gsdd
kartheek@SAILS-DM87:~$  
```