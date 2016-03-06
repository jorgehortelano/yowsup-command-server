# yowsup-commandserver
yowsup layer that auto execute commands using whatsapp.

## Installation

Install [yowsup](https://github.com/tgalal/yowsup/tree/develop) from the develop branch. (This is created for version 2.4.48)

After installing yowsup. Install this extension running:
```
python setup.py install
```

## Config
Create a configuration file where the whatsapp credentials are, as in other examples of yowsup. Something like:

	cc=39
	phone=39111111111
	password=c5NWTzOrsgCRQr77Yhwafdj+Tgg=
	allowed_users = ['39111222333@s.whatsapp.net']

Note: the new line allowed_users. This arrays define which phone numbers can send commands to the server. 

## Execution

To launch yowsup as a command server, from the folder where the file "yowsup-cli" exists, execute: 

	python yowsup-cli demos --config <file.config> --commandserver
	
Where the file.config is the previous defined configuration file.

## Allowing new commands

When it works, modify the layer.py to add all allowed commands you want. If a command needs sudo rights (as "reboot" in the code) you must execute yowsup with sudo or root user if the commands needs admin rights.






