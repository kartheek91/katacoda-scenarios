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