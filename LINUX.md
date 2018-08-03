# Intro to Linux

Linux is a UNIX-like operating system. On this page you find the some useful information and the most common commands used in the Linux environment.

Learn to love it, you won't be disappointed.

If you want more information about a command, the usual way is to use the `--help` argument or the `man <command>` command.

## Table of Contents

Terminal commands
* [SUDO](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#sudo---superuser-do)  
* [man]( ) TODO: fix link
* [top]( ) TODO: fix link
* [pwd]( ) TODO: fix link
* [ls - List files](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#ls---list-files-in-directory)  
* [cd - Change directory](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#cd---change-directory)  
* [rm - Remove file/directroy](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#rm---remove-filedirectory)  
* [cp - Copy file/directory](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#cp---copy-filedirectory)  
* [mv - Move file/directory](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#mv---move-filedirectory)  
* [mkdir - Create directory](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#mkdir---create-directory)  

Network commands
* [ping](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#ping---ping-a-serverwebsite)  
* [ssh](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#ssh---remote-access-computer-or-server)  
* [telnet](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#telnet----talk-to-hosts-at-the-given-port-number)  
* [ifconfig](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#ifconfig---network-interface-configurationinfo)  
* [iwconfig](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#iwconfig---like-ifconfig-but-for-wireless-interfaces)  
* [whois]( ) TODO: fix link  
* [nslookup](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#nslookup---translate-ip-address-to-name)  
* [traceroute](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#traceroute---tracing-route-of-ip-address)  

[text editors](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#text-editors)  
[Summary](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis/blob/master/LINUX.md#summary)  
## Basic information

For windows people - Directory == Folder

### Terminal (the command line cmd on Windows never was)

Here the user is located in their home directory `~` :

```bash
username@linux:~$
```

And here the user would be in current_directory:

```bash
username@linux:~/current_directory$
```

Absolute path, starts from root directory:

```bash
/directory/otherdirectory/
```

Relative path, starts from current directory:

```bash
directory/otherdirectory/
```

## Basic commands

### sudo - "superuser do"

Allows users to run programs with the security privileges of another user, by default the superuser. Use this command in front of any command if you get access denied, or don't, you may potentially destroy something.

```bash
username@linux:~$ sudo <command>
```

### man - show manual for command

Every linux command comes with a manual how to be used. use ``man`` to get manual.

e.g.
```bash
username@linux:~/$ man ls
```
Shows manual for listing files in directory.  

### top - monitor processes and system resources (task manager)

start process by simply typing 
```bash
username@linux:~/$ top
```
``top`` will show all running processes.
TODO: update list (DONT USE THIS!!!)  
```bash
Mem: 60964K used, 1532K free, 0K shrd, 9044K buff, 36972K cached
CPU:   8% usr  57% sys   0% nice   4% idle  29% io   0% irq   0% softirq
Load average: 1.88 0.88 0.39
  PID  PPID USER     STAT   VSZ %MEM %CPU COMMAND
  200   198 root     S     214m 350%  44% ./tuska_interface
   19     2 root     DW<      0   0%  14% [mmcqd]
  249   233 root     R     3144   5%   0% top
   12     2 root     SW<      0   0%   0% [kswapd0]
  203     1 root     S     3144   5%   0% telnetd -p 23 -b 10.10.10.4
  233   203 root     S     3144   5%   0% -sh
  198     1 root     S     3144   5%   0% /bin/sh /etc/init.d/rcS
    1     0 root     S     3140   5%   0% init
   36     1 root     S <   1592   3%   0% /sbin/udevd --daemon
   17     2 root     SW<      0   0%   0% [ubi_bgt0d]
    9     2 root     SW<      0   0%   0% [kmmcd]
    2     0 root     SW<      0   0%   0% [kthreadd]
    3     2 root     SW<      0   0%   0% [ksoftirqd/0]
    4     2 root     SW<      0   0%   0% [events/0]
    5     2 root     SW<      0   0%   0% [khelper]
    6     2 root     SW<      0   0%   0% [kblockd/0]
    7     2 root     SW<      0   0%   0% [ksuspend_usbd]
    8     2 root     SW<      0   0%   0% [khubd]
   10     2 root     SW       0   0%   0% [pdflush]
   11     2 root     SW       0   0%   0% [pdflush]
   13     2 root     SW<      0   0%   0% [aio/0]
   14     2 root     SW<      0   0%   0% [nfsiod]
   15     2 root     SW<      0   0%   0% [scsi_tgtd/0]
   16     2 root     SW<      0   0%   0% [mtdblockd]
   18     2 root     SW<      0   0%   0% [rpciod/0]
  191     2 root     SW<      0   0%   0% [ubi_bgt1d]
  195     2 root     SW<      0   0%   0% [ubifs_bgt1_0]
```
terminate a process by typing ``kill PID`` 

### pwd - print working directory

Self explanatory, prints where you are in directory hierarchy.

```bash
username@linux:~/$ pwd
```
prints working directory from root to where you are.

### ls - list files in directory

Lists all files in current or specified directory.

List all files in the current directory, here Downloads:

```bash
username@linux:~/Downloads$ ls
```

List all files inside the Music/classic directory:

```bash
username@linux:~$ ls Music/classic
```

#### cd - change directory

Move inside a directory:

```bash
username@linux:~$ cd <directory_path>
```
To move up one directory:

```bash
username@linux:~$ cd ..
```

`.` refers to current directory, while `..` refers to the parent.

#### rm - remove file/directory

Remove `awesomePythonProgram.py`:

```bash
username@linux:~$ rm awesomePythonProgram.py
```

Remove a directory:

```bash
username@linux:~$ rm -r awesomeDirectory
```

The `-f` is used to remove forcefully:

```bash
username@linux:~$ rm -rf awesomeDirectory
```

### cp - copy file/directory

Copy a file to a target. If the target is a directory, the filename will remain unchanged:

```bash
username@linux:~$ cp sourcefile tagetdirectroy
```

This would also rename the new file from `a.txt` to `b.txt`:

```bash
username@linux:~$ cp a.txt tagetdirectroy/b.txt
```

Use `-r` to copy a directory and its contents:

```bash
username@linux:~$ cp -r sourcedirectory targetdirectory
```

### mv - move file/directory

Use this to move a file/directory to its destination:

```bash
username@linux:~$ mv source taget
```

Move multiple files into a directory:

```bash
username@linux:~$ mv file1.txt file.2.txt file3.txt directory
```

Move all files with .py extension into a directory

```bash
username@linux:~$ mv *.py directory
```

Rename `a.txt` to `b.txt` by moving inside same directory:

```bash
username@linux:~$ mv a.txt b.txt
```

`mv` can, like `cp`, also move directories.

### mkdir - create directory

Used to create directories.

```bash
username@linux:~$ mkdir directoryname
```

## Network commands

### ping - ping a server/website

Use this to ping a website. useful if you want to test your network connection or if a server is up.

```bash
username@linux:$ ping www.google.com
```

### ssh - remote access computer or server.

Use this to remote access a server, e.g. tuxedo.

```bash
username@linux:$ ssh user@server
```

To connect using a different port than the default 22, use the `-p` flag:

```bash
username@linux:$ ssh user@server -p 1234
```

The following will connect to tuxedo, to your account:

```bash
username@linux:$ ssh abo-username@tuxedo.abo.fi
```

More about tuxedo: [tuxedo-wiki](TUXEDO.md)

### telnet -  Talk to “hosts” at the given port number.

By default, the telnet port is port 23. Few other famous ports are:  
7 – echo port,  
25 – SMTP, use to send mail  
79 – Finger, provides information on other users of the network  

```bash
username@linux:$ telnet host <port>
```

### ifconfig - network interface configuration/info

Shows your network interfaces and displays information about them. Similar to `ipconfig` on Windows.

Show all network interfaces:

```bash
username@linux:$ ifconfig
```

Show a specific interface:

```bash
username@linux:$ ifconfig eth0
```

This command is being slownly replaced py `ip`. Try to do `man ip` to read more about it if it is available on your system.

### iwconfig - like ifconfig but for wireless interfaces

Almost the same as `ifconfig` but only displays wireless interfaces.

```bash
username@linux:$ iwconfig
```

### whois - Who dis?  
domain lookup

```bash
username@linux:$ whois www.google.com
```
TODO: improve description

### nslookup - translate IP address to name

Makes queries to the DNS server to translate IP to a name, or vice versa. eg. nslookup miniclip.com will gives you the IP of miniclip.com

### traceroute - tracing route of IP address

Useful for tracing the route of IP packets. The packet causes messages to be sent back from all gateways in between the source and destination by increasing the number of hopes by 1 each time.

## Text editors

This needs its own section.

Different text editors:

* vi
* vim
* nano
* gedit
* emacs

## Summary

COMMAND | DESCRIPTION
------------ | -------------
 | <strong> basic </strong>
sudo | "superuser do". Use this command infront of any command if you get access denied.
man | Manual for each command.
top | Rerminal task manager
pwd | Print working directory
ls | Lists all files in current or specified directory.
cd | Move between directories
rm | Remove a file
rm -r |Remove a directory
cp | Copy a file
cp -r | Copy a directory
mv | Move a file
mkdir | Create new directory
 | <strong> Network </strong> 
ping | Ping server/website to test network connection.
ssh | Remote access computer or server.
ifconfig | Network interface configuration and info.
iwconfig | Network interface configuration and info for wireless connections only.
whois | Doman lookup
nslookup | Translate IP address to name
traceroute | Tracing route of IP address
