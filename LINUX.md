# Intro to Linux

Linux is a unix based operating system, here below you will find the some useful information and the most common
commands used in the linux terminal.
Learn to love it, you wont be disappointed.

## basic information

For windows people - Directory == Folder

terminal (cmd on a windows)

` username@linux:~$ `

here the user is located in root ~ .

` username@linux:~/current_directory$ `

here the user would be in current_directory

-> `/directory/otherdirectory/`

absolute path, starts from root directory

-> `directory/otherdirectory/`

this is a relative path, starts from current directory

## Basic commands

### sudo - "superuser do"
allows users to run programs with the security privileges of another user, by default the superuser. Use this command infront of any command if you get access denied.

`username@linux:~$ sudo <command>`

### ls - list files in directory
lists all files in current or specified directory.

` username@linux:~/Downloads$ ls`

lists all files in Downloads directory

` username@linux:~$ ls Music/classic`

lists all files inside the Music/classic directory


#### cd - change directory

` username@linux:~$ cd <directory_path>`
will move you to desired directory

` username@linux:~$ cd ..`
will move you up one directory


#### rm - remove file/directory

` username@linux:~$ rm awesomePythonProgram.py`

Use this to remove a file

` username@linux:~$ rm -r awesomeDirectory`

Use this to remove a directory

` username@linux:~$ rm -rf awesomeDirectory`

Use this to force a remove
### cp - copy file/directory

` username@linux:~$ cp sourcefile tagetdirectroy `

Use this to copy a file to its destination

` username@linux:~$ cp -r sourcedirectory targetdirectory`

Use this to copy a directory to its destination

### mv - move file/directory

` username@linux:~$ mv source taget `

Use this to move a file/directory to its destination

` username@linux:~$ mv file1.txt file.2.txt file3.txt directory`

move multiple files into a directory

` username@linux:~$ mv *.py directory`

move all files with .py extension into a directory

### mkdir - create directory

` username@linux:~$ mkdir directoryname `

Use this to create a directory to current path

## network commands

### ping - ping a server/website

` username@linux:$ ping www.google.com `

use this to ping a website. usefull if you want to test network connection.

### ssh - remote access computer or server.

` username@linux:$ ssh user@server `

use this to remote access a server, e.g. tuxedo.

` username@linux:$ ssh abo-username@tuxedo.abo.fi `

this will connect to your tuxedo user.
more on: [tuxedo-wiki](TUXEDO.md)

### ifconfig - network interface configuration/info

` username@linux:$ ifconfig `

same as ipconfig on windows..

### iwconfig - like ifconfig but dedicated to wireless


` username@linux:$ iwconfig `

same as above but for wireless connections
## Text editors 
This needs its own section


different text editors:

* vi
* vim 
* nano
* gedit
* emacs
    
    
    
# Summary

COMMAND | DESCRIPTION
------------ | -------------
 | <strong> basic </strong>
sudo | "superuser do". Use this command infront of any command if you get access denied.
ls | lists all files in current or specified directory.
cd | move between directories
rm | remove a file
rm -r |remove a directory
cp | copy a file
cp -r | copy a directory
mv | move a file
mkdir | create new directory
 | <strong> network </strong> 
ping | ping server/website to test network connection.
ssh | remote access computer or server.
ifconfig | network interface configuration and info.
iwconfig | network interface configuration and info for wireless connections only.
