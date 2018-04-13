##Intro to Linux
Linux is a unix based operating system, here below you will find the some useful information and the most common
commands used in the linux terminal

### basic information

For windows people - Directory == Folder

terminal (cmd on a windows)

` username@linux:~$ `

here the user is located in root ~ .


` username@linux:~/current_directory$ `

here the user would be in current_directory

### Basic commands


#### sudo - "superuser do"
allows users to run programs with the security privileges of another user, by default the superuser.
Use this command infront of any command if you get access denied.

`username@linux:~$ sudo <command>`

#### ls - list files in directory
lists all files in current or specified directory.

` username@linux:~/Downloads$ ls`

lists all files in Downloads directory

` username@linux:~$ ls /Music/classic`

lists all files inside the Music/classic directory


##### cd - change directory

` username@linux:~$ cd <directory_path>`
will move you to desired directory

` username@linux:~$ cd ..`
will move you up one directory

## ------------------------------------------
to still be added

#### Files/Directories navigating

* rm - remove file/directory
* cp - copy file/directory
* mv - move file/directory
* mkdir - create directory

Text editors:
    * vim 
    * nano
    * gedit
    * emacs

Networking:
    * ping - send a ping to an address
    * ssh (also in TUXEDO.md) - remotely connect to a computer
    * ifconfig - network interface configuration/info
    * iwconfig - like ifconfig but dedicated to wireless
