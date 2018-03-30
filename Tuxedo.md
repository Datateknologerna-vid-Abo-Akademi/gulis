# This is an introduction to Tuxedo
Tuxedo is a Linux computer used within Åbo Akademi University which you can log in to via SSH.
The SSH-protocol encrypts the connection to the communication is secure over the web.

Everyone with a ÅA-username can get access to the tuxedo but everyone does not have it automatically.
For example, everyone in the IT department gets it automatically when applied.

### What you can do with tuxedo: </h4>

* Use it like an other Linux terminal/computer (see Linux section for more info)
* write and run python code
* store and access files from anywhere anytime

### How to connect
##### Linux/Mac:
To establish a SSH-connection you will need a ssh-client. Every Linux distrubution and Mac X comes preinstalled with OpenSSH.
Open up the terminal (e.g. Konsole, Xterm, Macs terminal) and type the following command.

  `$ ssh tuxedo.abo.fi`
  
or

  `$ ssh [USERNAME]@tuxedo.abo.fi`

##### Windows:
windows does not come preinstalled with an SSH-client. You can use any ssh client you want.
for home users PuTTY works great: [Download here](https://the.earth.li/~sgtatham/putty/)

Run PuTTY and insert the Host Name as in for Linux/Mac.

` tuxedo.abo.fi`

or

` [USERNAME]@tuxedo.abo.fi `

Leave the port as 22 and press Open.

**The password is your regular ÅA-password**
