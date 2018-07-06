# Intro to Linux

Linux is a UNIX-like operating system. On this page you find the some useful information and the most common commands used in the Linux environment.

Learn to love it, you won't be disappointed.

If you want more information about a command, the usual way is to use the `--help` argument or the `man <command>` command.

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
