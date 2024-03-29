---
title: Clone a WordPress site on Pantheon with Duplicator plugin
filename: source/_docs/clone-a-wordpress-site-on-pantheon-with-duplicator-plugin.md
---

## Clone a WordPress site on Pantheon with Duplicator plugin
**Prerequisites** :
### [The Duplicator WordPress Plugin](https://wordpress.org/plugins/duplicator/)  
**Step 1. Archive Your Live Code/Files/Database**

1. Log into the site’s dashboard on Pantheon.
2. Enable [SFTP mode](/documentation/getting-started/developing-on-pantheon-directly-with-sftp-mode/-enabling-sftp-mode) on the dev environment’s code tab.
3. Within your WordPress site, go to the Duplicator plugin page and create a new package. Using the default settings, click “Next” and then “Build.” When complete, click “Archive” to download the resulting file.

### **Step 2. Create A New Pantheon Site​, Importing Your Archive**

1. Within your dashboard click link below to "Create A New Site".
2. Name your new site, and then select "Import site" from the "Choose your Start State" options. Next, select “Import Archive”.
3. Select the “File” option and upload the .zip file created in Step 1.2. Then click the "Import Site" button.
4. The import process will create and deploy a new site based on the file uploaded. If there are issues, please refer to our [importing](/documentation/advanced-topics/importing-an-existing-drupal-site-to-pantheon/-importing-an-existing-site) document for possible solutions or open a support ticket from your dashboard. Be sure to include any error messages or relevant information.
