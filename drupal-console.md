#Work Faster and Smarter with drupal console. 

# Run this in your terminal to get the latest project version:
    
    curl https://drupalconsole.com/installer -L -o drupal.phar

# Or if you don't have curl:
    
    php -r "readfile('https://drupalconsole.com/installer');" > drupal.phar

# Accessing from anywhere on your system:
    
    mv drupal.phar /usr/local/bin/drupal

# Apply executable permissions on the downloaded file:
    
    chmod +x /usr/local/bin/drupal

# Copy configuration files to user home directory:

    drupal init --override

# Check and validate system requirements

    drupal check

# Download, install and serve Drupal 8:

    drupal chain --file=~/.console/chain/quick-start.yml

# Create a new Drupal 8 project:

    drupal site:new drupal8.dev 

# Lists all available commands:

    drupal list

# Update DrupalConsole to the latest version:
    
    drupal self-update
