# SDKs, JDKs and other animals

In your studies, you will primarily develop in Python and Java. On this page we have gathered great and simple tutorials that help you set up different development kits.

## Content

* [Python](#python)
  * [Python](#python)
  * [Python online console](#python-3-online-console)
  * [Virtualenv](#virtualenv)
  * [pipenv](#pipenv)

* [Java](#java)
  * [JDK, JRE and JVM](#jdk-jre-and-jvm)
  * [Install Java JDK](#install-java-jdk)

## Python

The first programming course that you take, is in Python, Python 3 to be precise. Linux and macOS usually come pre-installed with some version of Python, so these guides are mostly for Windows users.

As a bonus, Google has a Python course for those who are interested in some examples: [Google Python Course](https://developers.google.com/edu/python/set-up)


#### Windows

To install Python 3.12 on Windows, start by visiting the [Python 3.12 release page](https://www.python.org/downloads/release/python-3125/) (Latest as of 26.8.2024)

Depending on your system architecture, you must choose the correct installation file.

**64-bit systems**: `Windows x86-64 MSI installer`

**32-bit systems**: `Windows x86 MSI installer`

Follow the instructions of the installer, the default settings should work just fine.

If you have some issues, check the [Python on Windows FAQ](https://docs.python.org/3.12/faq/windows.html)

#### Linux

On most distributions Python, and especially Python 3, come pre-installed. The easiest way to test this is via the terminal:

```bash
$ python --version
Python 3.12.5
```

This should show your installed version of python. In the case that it says something like "command not found", you should use your system's package manager to install python. On debian and ubuntu-based systems you would use the apt package manager. Like so:

```bash
# Python 3.11 is the default for Debian 12 as of August 2024
sudo apt update
sudo apt install python3.11 python3-pip
```

The rest of you using something else, you can probably figure it out by yourselves ;)

#### macOS

Python 3.*. should come pre-installed, but you can check by typing in the terminal:

```bash
$ python --version
Python 3.12.5
```

If it is not installed, get it from the [Python 2.7 release page](https://www.python.org/downloads/release/python-3125/)

From there, select the correct installer file depending on your operating system version. For most, it will be the `macOS 64-bit installer`.

Run the installer and follow the instructions.


### Python 3 Online console

Python provides a web shell (online console) running python 3 on thier front page [Check it out](https://www.python.org/shell/).  
A great small tool if you don't have any other snakes to play around with nearby.

### Virtualenv

> Virtualenv is a tool which allows us to make isolated python environments. How does making isolated python environments help us ? Imagine you have an application that needs version 2 of a LibraryBar, but another application requires version 2. How can you use and develop both these applications? If you install everything into /usr/lib/python3.12/site-packages (or whatever your platform’s standard location is), it’s easy to end up in a situation where you unintentionally upgrade an application that shouldn’t be upgraded.

> In another case just imagine that you have an application which is fully developed and you do not want to make any change to the libraries it is using but at the same time you start developing another application which requires the updated versions of those libraries. What will you do ? It is where virtualenv comes into play. It creates isolated environments for you python application and allows you to install python libraries in that isolated environment instead of installing them globally. (https://pythontips.com/2013/07/30/what-is-virtualenv/)

Here is a very short guide how to install virtualenv to get you started. Type the following command in the shell:

```bash
$ pip install virtualenv
```

Then, create an isolated virtualenv environment inside a folder MyEnv

```bash
$ virutalenv MyEnv
```

Activate your virtual environment with (for within the folder)

```bash
$ source bin/active
```

when activated, install required libraries without any disturbance to the gobal libraries or the libraries of the other environments.

Virtualenv might not be used in your first programming course but it's good to know about.  Many if not all IDEs use virtual environments of some sort.

A more detailed description can be found in the [gulis-chat project](https://github.com/Datateknologerna-vid-Abo-Akademi/gulis-chat/tree/master/part2#21-virtual-environments).

### pipenv

#### A brief history of Python package installation

To understand the problems that Pipenv solves, it's useful to show how Python package management has evolved.

Take yourself back to the first Python iteration. We had Python, but there was no clean way to install packages.

Then came Easy Install, a package that installs other Python packages with relative ease. But it came with a catch: it wasn't easy to uninstall packages that were no longer needed.

Enter pip, which most Python users are familiar with. pip lets us install and uninstall packages. We could specify versions, run pip freeze > requirements.txt to output a list of installed packages to a text file, and use that same text file to install everything an app needed with pip install -r requirements.txt.

But pip didn't include a way to isolate packages from each other. We might work on apps that use different versions of the same libraries, so we needed a way to enable that. Along came virtual environments, which enabled us to create small, isolated environments for each app we worked on. We've seen many tools for managing virtual environments: virtualenv, venv, virtualenvwrapper, pyenv, pyenv-virtualenv, pyenv-virtualenvwrapper, and even more. They all play well with pip and requirements.txt files.  
 [Reference](https://opensource.com/article/18/2/why-python-devs-should-use-pipenv)

#### Pipenv fixes this problem, what a great friend!

Learn more about pipenv [here](https://github.com/pypa/pipenv)

## Java

It is mostly recommended to use the latest version of Java and to keep it up to date to avoid any security issues or other problems.

The version that we would recommend for most is Java 21, it has long term support and many new features over the otherwise favored Java 8 or 17.

### JDK, JRE and JVM

#### JVM - Java Virtual Machine

JVM (Java Virtual Machine) is an abstract machine that enables your computer to run a Java program.

When you run the Java program, Java compiler first compiles your Java code to bytecode. Then, the JVM translates bytecode into native machine code (set of instructions that a computer's CPU executes directly).

Java is a platform-independent language. It's because when you write Java code, it's ultimately written for JVM but not your physical machine (computer). Since, JVM ​executes the Java bytecode which is platform independent, Java is platform-independent.  

#### JRE - Java Runtime Environment

JRE (Java Runtime Environment) is a software package that provides Java class libraries, along with Java Virtual Machine (JVM), and other components to run applications written in Java programming. JRE is the superset of JVM.

JRE contains JVM and other Java class libraries.

If you need to run Java programs, but not develop them, JRE is what you need. Not what we need! keep on reading ;)

#### JDK - Java Development Kit

JDK (Java Development Kit) is a software development kit to develop applications in Java. When you download JDK, JRE is also downloaded, and don't need to download it separately. In addition to JRE, JDK also contains number of development tools (compilers, JavaDoc, Java Debugger etc).

JDK contains JRE and other tools to develop Java applications.

### Install Java JDK

To develop using Java, you need the JDK. This is different from the JRE, Which is only used for running the software, while the JDK contains documentation and compilers and other development related content.

The JDK also contains a JRE, so no need to install both

See below for operating system-specific instructions


### Windows

Navigate to the [temurin download page](https://adoptium.net/temurin/releases/?arch=x64&os=windows&version=21)

Select the correct installer (the link leads to the installer for 64-bit windows systems).

**64-bit systems**: `Operating system: Windows, Architecture: x64`

**32-bit systems**: `Operating systen: Windows, Architecture: x86`

Follow the instructions of the installer.

### Linux

Now, Linux users have two alternatives, using the commercial JDK or using the open source alternative [OpenJDK](http://openjdk.java.net).

#### OpenJDK

To develop with OpenJDK, you must install both JRE and JDK.

Debian, Ubuntu and other distributions using `apt` (only has version 17 as of August 2024):

```bash
$ sudo apt-get install openjdk-17-jre openjdk-17-jdk
```

Otherwise you can also install from the temurin website through https://adoptium.net/temurin/releases/?arch=x64&os=linux&version=21

### macOS


Navigate to the [temurin download page](https://adoptium.net/temurin/releases/?arch=x64&os=mac&version=21)

The link leads to the installer for macOS 64-bit systems, select architecture: x86 if you have a 32-bit system.
