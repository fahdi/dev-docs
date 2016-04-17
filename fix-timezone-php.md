##Fix timezone for PHP

First check where the CLI **php.ini** is located:

In terminal, type:

	php -i | grep "php.ini"

In my case I ended up with : Configuration File (php.ini) Path => /etc

Then use **cd ..** all the way back and cd into /etc, on a mac, just use **cd** to go to root directory. Do **ls**. In my case php.ini didn't show up, only a **php.ini.default**.

If you already have a php.ini, edit that and skip the next stroked step.

~~Copy the php.ini.default file named as php.ini:~~

	sudo cp php.ini.default php.ini

In order to edit, change the permissions of the file:

	sudo chmod ug+w php.ini
	sudo chgrp staff php.ini
	    
Open directory and edit the php.ini file:

    open .

Search for [Date] and make sure the following line is in the correct format:

    date.timezone = "Asia/Dubai"
    
Find your timezone at [this link](http://php.net/manual/en/timezones.php).