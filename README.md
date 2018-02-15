
# How it Works

1. Server creates a table for license email, license, experation date, and ip
2. Server generates a license key (XXXX-XXXX-XXXX)
3. Server encrypts it using your Servers key (Generated on setup) and server gives you it
4. You give client to buyer/user with license.dat file that contains the encrypted license
5. Client connects to license server, sending its license.dat
6. Server trys to decrypt liscense.dat and comapire with any in database
7. If Server finds the key it check to see if the license is expiered and update last IP
8. If not expired client runs, else it will tell them its expiered and closes

NOTE: The client must have an internet connection to the license server!

# Licensing.go
Licensing can be called at anytime in your program, Just import and select to settings for it. Its a simple one line command.

Licensing.CheckLicense("{LICESNESSERVER}", {USESSL}, {SILENT})

* {LICESNESSERVER} = http://127.0.0.1:8080
* {USESSL} = true or false to use SSL (Your server will need this setting too).
* {SILENT} = Show messages or not.

# Server
* Ability to add new licenses to database
* Config Setup Tool
* Ability to remove liceses from database

# Config.toml Format

* https://pastebin.com/7wBaXcu1
