#Fixing Drupal common errors

##Problem description: 

The file sites/default/settings.php is not protected from modifications and poses a security risk. You must change the file's permissions to be non-writable.
The file sites/default/services.yml is not protected from modifications and poses a security risk. You must change the file's permissions to be non-writable.

## Solution 

cd into the /web/sites directory of your drupal installation and do as follows. 

    $ chmod -R 0755 default/settings.php
    $ chmod -R 0755 default/services.yml 
    
It should fix the write permissions for your files. 
