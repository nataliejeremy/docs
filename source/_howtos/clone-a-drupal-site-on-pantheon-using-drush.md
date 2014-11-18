---
title: Clone a Drupal site on Pantheon using Drush
filename: source/_docs/clone-a-drupal-site-on-pantheon-using-drush.md
---

## Clone a Drupal site on Pantheon using Drush

### **Step 1. Archiving Your Live Code/Files/Database**
 **Prerequisites:**  
 [Current drush aliases](/documentation/advanced-topics/drush-command-line-utility/-using-drush-on-pantheon)
1. From the command line, run [the drush ard](http://www.drushcommands.com/drush-6x/archive/archive-dump) command against the live environment. Be sure to set the destination parameter to include a file name.  


### **Step 2. Creating A New Pantheon Site​, Importing Your Archive**

1. Within your dashboard click link below to "Create A New Site".
2. Name your new site, and then select "Import site" from the "Choose your Start State" options. Next, select “import archive”.
3. Enter the full URL of the Live site you are cloning, plus the path of the archive created in Step 1.  

4. The import process will create and deploy a new site based on the file uploaded. If there are issues, please refer to our [importing](/documentation/advanced-topics/importing-an-existing-drupal-site-to-pantheon/-importing-an-existing-site) document for possible solutions or open a support ticket from your dashboard. Be sure to include any error messages or relevant information.