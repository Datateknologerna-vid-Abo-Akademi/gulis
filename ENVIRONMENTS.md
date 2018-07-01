# SDKs, JDKs and other animals

In your studies, you will primarily develop in Python and Java. On this page we have gathered great and simple tutorials that help you set up different development kits.

## Content

* [Python](#python)
  * [Python 2.7](#python-2.7)
  * [Python 3.7](#python-3.7)

* [Java](#java)

## Python

The first programming course that you take, is in Python, Python 2.7 to be precise. Linux and macOS usually come pre-installed with some version of Python, so these guides are mostly for Windows users.

As a bonus, Google has a Python course for those who are interested in some examples: [Google Python Course](https://developers.google.com/edu/python/set-up)

### Python 2.7

#### Windows

To install Python 2.7 on Windows, start by visiting the [Python 2.7 release page](https://www.python.org/downloads/release/python-2715/)

Depending on your system architecture, you must choose the correct installation file.

**64-bit systems**: `Windows x86-64 MSI installer`

**32-bit systems**: `Windows x86 MSI installer`

Follow the instructions of the installer, the default settings should work just fine.

If you have some issues, check the [Python on Windows FAQ](https://docs.python.org/2.7/faq/windows.html)

#### Linux

On most distributions Python, and especially Python 2.7, come pre-installed. The easiest way to test this is via the terminal:

```bash
$ python --version
Python 2.7.15
```

This should show the installed version of Python. If the command is not found or the version is not 2.7.*, you don't have Python 2.7 installed. To fix this, use for example `apt`, which is the package manager for Ubuntu and other Debian based systems:

```bash
sudo apt update
sudo apt install python2.7 python-pip
```

The rest of you using something else, you can probably figure it out by yourselves ;)

#### macOS

Python 2.7. should come pre-installed, but you can check by typing in the terminal:

```bash
$ python --version
Python 2.7.15
```

If it is not installed, get it from the [Python 2.7 release page](https://www.python.org/downloads/release/python-2715/)

From there, select the correct installer file depending on your operating system version. For most, it will be the `macOS 64-bit installer`.

Run the installer and follow the instructions.

Very // TODO: wtf was I writing here

### Python 3.7

Installing Python 3.7 or any other version, is very similar to the process of installing Python 2.7.

#### Windows

To get the latest version of Python, visit [Python Downloads page](https://www.python.org/downloads/) and click the `Download` button.

The rest should be like the installation of Python 2.7.

#### Linux

Python 3.6 or 3.7 may sometimes come pre-installed and can be tested with.

```bash
$ python3 --version
```
Note the use of the number `3` after `python` without a space.

TODO: Add content

#### macOS

To get the latest version of Python, visit [Python Downloads page](https://www.python.org/downloads/) and click the `Download` button.

The rest is exactly like the installation of Python 2.7

## Java

It is mostly recommended to use the latest version of Java and to keep it up to date to avoid any security issues or other problems.

Oracle recently decided to increase the frequency of Java releases, releasing a new version every 6 months.

However, to get you started, it is probably best if you install Java 8, as it is a LTS (Long Term Support) version, receiving updates at least until March 2022.

To develop using Java, you need the JDK (Java Development Kit). This is different from the JRE (Java Runtime Environment), Which is only used for running the software, while the JDK contains documentation and compilers and other development related content.

The JDK also contains a JRE, so no need to install both

Oh, and we will install Java SE (Standard Edition).

To sum it all up in one phrase, we will install `Java SE Development Kit 8`

All platforms find the Oracle Java SE Development Kit 8 packages at the [downloads page](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html). You must accept the Licence Agreement before you can download.

### Windows

Go to the downloads page and select the correct installer.

**64-bit systems**: `Windows x64`

**32-bit systems**: `Windows x86`

Follow the instructions of the installer.

### Linux

Now, Linux users have two alternatives, using the commercial JDK or using the open source alternative [OpenJDK](http://openjdk.java.net).

#### OpenJDK

To develop with OpenJDK, you must install both JRE and JDK.

Debian, Ubuntu and other distributions using `apt`:

```bash
$ sudo apt-get install openjdk-8-jre openjdk-8-jdk
```

Fedora, Oracle Linux, Red Hat Enterprise Linux, etc.:

```bash
su -c "yum install java-1.8.0-openjdk"
su -c "yum install java-1.8.0-openjdk-devel"
```

#### Oracle JDK

32-bit Linux versions, refer to the page [How do I download and install 32-bit Java for Linux?](https://java.com/en/download/help/linux_install.xml#Java%20for%20Linux%20Platforms).

32-bit Linux versions, refer to the page [Linux 64-bit installation instructions for Java](https://java.com/en/download/help/linux_x64_install.xml).

### macOS

Go to the downloads page and download the `dmg` for `Mac OS X x64` and follow the instructions of the installer.