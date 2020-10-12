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
### 9.1 touch: If the file name specified as an argument doesn’t exist touch will create a new file.
```
kartheek@SAILS-DM87:~$ touch file1.txt
kartheek@SAILS-DM87:~$ ls
file1.txt  gsdd
kartheek@SAILS-DM87:~$ touch file2.txt file3.txt
kartheek@SAILS-DM87:~$ ls
file1.txt  file2.txt  file3.txt  gsdd
kartheek@SAILS-DM87:~$  
```

### 9.2 Redirection allows you to capture the output from a command and send it as input to another command or file. There are two ways to redirect output to a file. The > operator will overwrite an existing file, while the >> operator will append the output to the file.
```
kartheek@SAILS-DM87:~$ echo "Hello from Redirection" > redirection_file.txt
kartheek@SAILS-DM87:~$ cat redirection_file.txt
Hello from Redirection
kartheek@SAILS-DM87:~$ echo "Hello from Redirection1" > redirection_file.txt
kartheek@SAILS-DM87:~$ cat redirection_file.txt
Hello from Redirection1
```

### In the above mentioned snippet we created a file with sample text i.e "Hello from Redirection" and with  redirection operator ">" .

```
kartheek@SAILS-DM87:~$ echo "Hello from Redirection Operator >>" >> redirection_file.txt
kartheek@SAILS-DM87:~$ cat redirection_file.txt
Hello from Redirection1
Hello from Redirection Operator >>
```

### In the above mentioned snippet we append output to the file "redirection_file.txt".

### 9.3 Creating a File using Heredoc : Here document or Heredoc is a type of redirection that allows you to pass multiple lines of input to a command.
```
kartheek@SAILS-DM87:~$ cat << END
> Hi All hope you are able to follow this session.
> Thank You all for this oppurtunity.
> END
Hi All hope you are able to follow this session.
Thank You all for this oppurtunity.
kartheek@SAILS-DM87:~$
```
### 10.File copy in ubuntu:
### 10.1 Copy file to target directory: We created two directories called source and destination and we will try to copy file from source -> destination.
```
kartheek@SAILS-DM87:~$ cp source/sampl1.txt  /home/kartheek/destination/
kartheek@SAILS-DM87:~$ ls /home/kartheek/destination/
sampl1.txt
kartheek@SAILS-DM87:~$     
```
### 10.2 Copy multiple files at the same time
```
kartheek@SAILS-DM87:~$ ls
clear.save  destination  file1.txt  file2.txt  file3.txt  gsdd  redirection_file.txt  source
kartheek@SAILS-DM87:~$ cp source/sampl1.txt  source/sampl2.txt  /home/kartheek/destination/
kartheek@SAILS-DM87:~$ ls /home/kartheek/destination/
sampl1.txt  sampl2.txt
kartheek@SAILS-DM87:~$    
```
### 10.3 Copying a directory or folder (-r or -R)
```
kartheek@SAILS-DM87:~$ ls
clear.save  destination  file1.txt  file2.txt  file3.txt  gsdd  redirection_file.txt  source
kartheek@SAILS-DM87:~$ cp gsdd/ /home/kartheek/source/
cp: -r not specified; omitting directory 'gsdd/'
```
```
kartheek@SAILS-DM87:~$ cp -R gsdd/ /home/kartheek/source/
kartheek@SAILS-DM87:~$ ls -l /home/kartheek/source/
total 0
drwxr-xr-x 1 kartheek kartheek 4096 Oct 12 19:01 gsdd
-rw-r--r-- 1 kartheek kartheek   19 Oct 12 18:44 sampl1.txt
-rw-r--r-- 1 kartheek kartheek    0 Oct 12 18:39 sampl2.txt
kartheek@SAILS-DM87:~$    
```
### 10.4 Copy only when source file is newer than the target file (-u)
```
kartheek@SAILS-DM87:~$ cd source/
kartheek@SAILS-DM87:~/source$ cat <<END >> sampl1.txt
> Lasix is the generic drug
> END
```
```
kartheek@SAILS-DM87:~/source$ cp -v -u sampl1.txt /home/kartheek/destination/
'sampl1.txt' -> '/home/kartheek/destination/sampl1.txt'
kartheek@SAILS-DM87:~/source$  
```
```
kartheek@SAILS-DM87:~/source$ cp -v -u sampl1.txt /home/kartheek/destination/
kartheek@SAILS-DM87:~/source$ 
```
### 11.Ln Command: A symbolic link, also known as a symlink or soft link, is a special type of file that points to another file or directory.

### Now we will create Symlink to a file: We have sample file in this location "/home/kartheek/source/gsdd/medguides/generic_medguides/brand_medguides/brand_drugs" and we will create Symlink.

```
kartheek@SAILS-DM87:~$ ln -s /home/kartheek/source/gsdd/medguides/generic_medguides/brand_medguides/brand_drugs/brand_drugs.txt  brand
```
### Now we will check whether Symlink for the mentioned file is created or not.

```
kartheek@SAILS-DM87:~$ ls -l brand
lrwxrwxrwx 1 kartheek kartheek 98 Oct 12 20:10 brand -> /home/kartheek/source/gsdd/medguides/generic_medguides/brand_medguides/brand_drugs/brand_drugs.txt
kartheek@SAILS-DM87:~$  
```
```
kartheek@SAILS-DM87:~$ ls
brand  destination  file1.txt  file2.txt  file3.txt  gsdd  redirection_file.txt  source
kartheek@SAILS-DM87:~$ cat brand
This is sample file
Symbolic link works fine
kartheek@SAILS-DM87:~$
```
### In order to delete the Symlink we need to used this command

```
kartheek@SAILS-DM87:~$ ls
brand  destination  file1.txt  file2.txt  file3.txt  gsdd  redirection_file.txt  source
kartheek@SAILS-DM87:~$ unlink brand
kartheek@SAILS-DM87:~$ ls
destination  file1.txt  file2.txt  file3.txt  gsdd  redirection_file.txt  source
kartheek@SAILS-DM87:~$
```

### Now we will create Symlink to a directory: We have sample directory in this location "/home/kartheek/source/gsdd/medguides/generic_medguides/brand_medguides/brand_drugs" and we will create Symlink.
```
kartheek@SAILS-DM87:~$ ln -s /home/kartheek/source/gsdd/medguides/generic_medguides/brand_medguides/brand_drugs/ brand
```
```
kartheek@SAILS-DM87:~$ ls -l brand
lrwxrwxrwx 1 kartheek kartheek 83 Oct 12 20:16 brand -> /home/kartheek/source/gsdd/medguides/generic_medguides/brand_medguides/brand_drugs/
```
```
kartheek@SAILS-DM87:~$ cd brand
kartheek@SAILS-DM87:~/brand$ ls
brand_drugs.txt
```

### 12.tar command: A Linux tarball (“tar.gz” or “tar.bz2” file ) is nothing but a system file format that combines and compresses multiple files.

### Here’s what those switches actually mean:
- -c: Create an archive.
- -z: Compress the archive with gzip.
- -v: Display progress in the terminal while creating the archive, also known as “verbose” mode. The v is always optional in these commands, but it’s helpful.
- -f: Allows you to specify the filename of the archive.

### Creating 150 MB random file. 
```
kartheek@SAILS-DM87:~$ head -c 150MB /dev/urandom > sample_tar.txt    
```
### Creating tar file.

```
kartheek@SAILS-DM87:~$ tar -czvf sample.tar.gz  first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleven
th/
first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/
first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/sample.txt
first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/sample_tar.txt
```
### Extract the tar.gz file i.e sample.tar.gz

```
kartheek@SAILS-DM87:~$ ls -human sample.tar.gz
-rw-r--r-- 1 1000 1000 144M Oct 12 21:54 sample.tar.gz
kartheek@SAILS-DM87:~$ tar -zxvf sample.tar.gz
first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/
first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/sample.txt
first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/sample_tar.txt
```

```
kartheek@SAILS-DM87:~$ ls
brand        file1.txt  file3.txt  gsdd  redirection_file.txt  source
destination  file2.txt  first      home  sample.tar.gz         twogb.txt
kartheek@SAILS-DM87:~$  
```

### 13.zip a folder in Ubuntu Linux using the cli:To compress archive files use zip command. 

```
kartheek@SAILS-DM87:~$ sudo apt install zip unzip
Reading package lists... Done
Building dependency tree
Reading state information... Done
zip is already the newest version (3.0-11build1).
The following NEW packages will be installed:
  unzip
0 upgraded, 1 newly installed, 0 to remove and 117 not upgraded.
Need to get 0 B/169 kB of archives.
After this operation, 593 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Selecting previously unselected package unzip.
(Reading database ... 84603 files and directories currently installed.)
Preparing to unpack .../unzip_6.0-25ubuntu1_amd64.deb ...
Unpacking unzip (6.0-25ubuntu1) ...
Setting up unzip (6.0-25ubuntu1) ...
Processing triggers for mime-support (3.64ubuntu1) ...
Processing triggers for man-db (2.9.1-1) ...
kartheek@SAILS-DM87:~$  
```
### To create compressed archive named first.zip of first folder in the current directory.

```
kartheek@SAILS-DM87:~$ zip -r first.zip first/
  adding: first/ (stored 0%)
  adding: first/second/ (stored 0%)
  adding: first/second/third/ (stored 0%)
  adding: first/second/third/fourth/ (stored 0%)
  adding: first/second/third/fourth/fifth/ (stored 0%)
  adding: first/second/third/fourth/fifth/sixth/ (stored 0%)
  adding: first/second/third/fourth/fifth/sixth/seventh/ (stored 0%)
  adding: first/second/third/fourth/fifth/sixth/seventh/eighth/ (stored 0%)
  adding: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/ (stored 0%)
  adding: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/ (stored 0%)
  adding: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/ (stored 0%)
  adding: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/sample.txt (stored 0%)
  adding: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/sample_tar.txt (deflated 0%)
kartheek@SAILS-DM87:~$                                          
```

### Now we will unzip first.zip

```
kartheek@SAILS-DM87:~/source$ unzip first.zip
Archive:  first.zip
   creating: first/
   creating: first/second/
   creating: first/second/third/
   creating: first/second/third/fourth/
   creating: first/second/third/fourth/fifth/
   creating: first/second/third/fourth/fifth/sixth/
   creating: first/second/third/fourth/fifth/sixth/seventh/
   creating: first/second/third/fourth/fifth/sixth/seventh/eighth/
   creating: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/
   creating: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/
   creating: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/
 extracting: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/sample.txt
  inflating: first/second/third/fourth/fifth/sixth/seventh/eighth/nineth/tenth/eleventh/sample_tar.txt
kartheek@SAILS-DM87:~/source$ ls
first  first.zip  gsdd  sampl1.txt  sampl2.txt
kartheek@SAILS-DM87:~/source$     
```

### 14.grep command in Linux: grep stands for globally search for regular expression and print out.The grep filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern.
### Syntax: grep [options] pattern [files] and some of the options description are shown below.
- -c : This prints only a count of the lines that match a pattern
- -n : Display the matched lines and their line numbers.
- -v : This prints out all the lines that do not matches the pattern
- -w : Match whole word

```
kartheek@SAILS-DM87:~$ grep -c "road" road_not_taken.txt
2
```

```
kartheek@SAILS-DM87:~$ grep -o "road" road_not_taken.txt
road
road
```

```
kartheek@SAILS-DM87:~$ grep -n "road" road_not_taken.txt
1:Two roads diverged in a yellow wood,
21:Two roads diverged in a wood, and I—
```

```
kartheek@SAILS-DM87:~$ grep -h "road" road_not_taken.txt
Two roads diverged in a yellow wood,
Two roads diverged in a wood, and I—
kartheek@SAILS-DM87:~$            
```                            


