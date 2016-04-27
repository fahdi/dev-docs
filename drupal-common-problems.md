#Fixing Drupal common errors

##Problem description: 

The file sites/default/settings.php is not protected from modifications and poses a security risk. You must change the file's permissions to be non-writable.
The file sites/default/services.yml is not protected from modifications and poses a security risk. You must change the file's permissions to be non-writable.

## Solution 

cd into the /web/sites directory of your drupal installation and do as follows. 

    $ chmod -R 0755 default/settings.php
    $ chmod -R 0755 default/services.yml 
    
It should fix the write permissions for your files. 


##Problem description: 

This warning appears when drupla core is out of date. At the time of writing this, the stable core is at version 8.1.0 as drupal is an super active development phase right now. 

    Drupal core update status	Out of date (version 8.1.0 available)
    There are updates available for your version of Drupal. To ensure the proper functioning of your site, you should update as soon as possible. See the available updates page for more information and to install your missing updates.

You can check more details by opening <http://yourdrupalsite.com/admin/reports/updates/update> but at the moment, you can't update the core automatilcally like wordpress or other similar systems. 

## Solution 

So to solve this problem, update composer.json's dependencies and run 
    
    composer update
    
