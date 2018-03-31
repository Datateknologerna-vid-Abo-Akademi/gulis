# An introduction to Tuxedo

Tuxedo is a Linux computer used within Åbo Akademi University, which you can log in to via SSH.
The SSH-protocol encrypts the communication to the server, so the connection over the web is secure.

Everyone with a ÅA-username can get access to the tuxedo, but everyone does not have it automatically.
However, everyone in the IT department gets it when enrolled as a student.

## What you can do with tuxedo

* Use it like an other Linux terminal/computer (see Linux section for more info).
* Write and run python, c and other code.
* Store and access your files from anywhere anytime.
* Use it as an virtual environment.
* Host your users.abo.fi webpage.

## How to connect

Authentication is done with your regular ÅA-username and password.

### Linux/Mac

To establish a SSH-connection you will need a ssh-client. Every Linux distrubution and macOS comes preinstalled with OpenSSH.
Open up the terminal (e.g. Konsole, Xterm, macOS terminal) and type the following command:

```bash
$ ssh tuxedo.abo.fi
```

or

```bash
$ ssh [USERNAME]@tuxedo.abo.fi
```

### Windows

Windows does not come preinstalled with an SSH-client. You can use any SSH-client you want.
For home users PuTTY works great: [Download here](https://the.earth.li/~sgtatham/putty/)

Run PuTTY and insert the Host Name as in for Linux/Mac.

```text
tuxedo.abo.fi
```

or

```text
[USERNAME]@tuxedo.abo.fi
```

Leave the port as 22 and press Open.
