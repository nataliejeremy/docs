---
title: Installing Cygwin on Windows
parent_guide:
  - getting-started
filename: source/_docs/installing-cygwin-on-windows.md
---

[Cygwin](http://cygwin.com/install.html) is a collection of tools which provide a Linux tools and utilities for Windows computers. If you do not have access to a Mac or Linux environment you can use Cygwin to generate the .key and .csr file that are needed to get a SSL certificate from a provider.

###Getting started

Before you begin you should be sure to take a look at the [Getting an SSL Cert](/documentation/howto/adding-a-ssl-certificate-for-secure-https-communication/) documentation. Once you have one through the process of generating the command to get a valid CSR certificate for your domain, you can proceed with the rest of this tutorial.

####Download Cygwin

Get started by downloading the lastest version of [Cygwin](http://cygwin.com/install.html) by going to the installer page. 

####Install Cygwin

Start the Cygwin installer using the setup.exe. If you already have Cygwin installed or you would like to add extra packages after you have the program running on your system you can simply click setup.exe and running through the installer again.



 ![Start Cygwin Installer](https://pantheon-systems.desk.com/customer/portal/attachments/40750)  

####Select the Cygwin Root

For ease we have opted to the root directory directly inside the `C:\` directory. This will make it easier when we are trying to locate the CSR files we are going to generate later in the tutorial.



 ![Cygwin Root install directory](https://pantheon-systems.desk.com/customer/portal/attachments/40751)  

####Select the Package Directory

Once you have chosen the default directory to install Cygwin, you will also need to select a Local Package directory. In this case we are using the same directory as the Cygwin Root directory.



 ![Cygwin Local package directory](https://pantheon-systems.desk.com/customer/portal/attachments/40752)
####Choose your internet connection

To download the neccessary packages the recommended settings for this is the _Direct Connection_



 ![Cygwin Connection Type](https://pantheon-systems.desk.com/customer/portal/attachments/40753)  

####Select a download site

Choose the nearest mirror site, or most stable location. If for some reason the download does not work you can always select another mirror.



 ![Choose Cygwin mirror](https://pantheon-systems.desk.com/customer/portal/attachments/40755)  

####Install the SSL package

Start Cygwin and paste in the command that you got from the Wizard.

 ![Select openSSL package](https://pantheon-systems.desk.com/customer/portal/attachments/40768)  

####Generate the CSR

Once the installation is complete you can run start a Cygwin terminal session. Here you can paste in the command to you generated from the Wizard and get your private key and CSR certificate.



 ![Generate the CSR with Cygwin](https://pantheon-systems.desk.com/customer/portal/attachments/40769)
####Get your CSR certificate

Finally you can navigate to the home directory within Cygwin's root and get a copy of both your private key and CSR certificate.



 ![CSR cert in windows](https://pantheon-systems.desk.com/customer/portal/attachments/40770)  

 

####Get your CSR certificate

From this point you can now navigate to the  [Getting an SSL Cert](/documentation/howto/adding-a-ssl-certificate-for-secure-https-communication/#getting-the-SSL-certificate) documentation where you can complete the rest of the installation process on Pantheon.
