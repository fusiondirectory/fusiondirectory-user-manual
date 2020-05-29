.. include:: /globals.rst

Create a user template
======================

Click on tab or icon Users, in the Users and groups section in FusionDirectory

.. image:: images/templates-users.png
   :alt: Picture of Users icon in FusionDirectory

Click Actions –> Create –> Template

.. image:: images/templates-create-template.png
   :alt: Picture of create template menu in FusionDirectory
   
Depending on which other plugins you have installed, you can configure your template like you need. Below, you can find some exemple. 

You can find the documentation on how to create a macro here :ref:`fd-macros-label`.

User
----

The user tab is the base of your template, click on User tab

.. image:: images/templates-tab-user.png
   :alt: Picture of User tab in FusionDirectory   
   
Generic User tab : this is the base tab to create a user template.

.. image:: images/template-fd-user-creation.png
   :alt: Picture of templates settings in FusionDirectory
   
In this example we set the following macros to create a user :

  
* Login : **%alps[1]|givenName%%alp|sn%** meaning that login will be first letter of first name in low character followed by last name in low characters
* Password : **%r[12]|%** meaning that password will contain 12 random characters



Unix
----

When you are creating or editing your template, click on Unix tab Then click on Add Unix settings. A new dialog is opened

.. image:: images/templates-unix-tab.png
   :alt: Picture of Unix tab in FusionDirectory

Then click on Add Unix settings. A new dialog is opened

.. image:: images/templates-add-unix-settings.png
   :alt: Picture of Add Unix settings button in FusionDirectory
      
Fill-in Unix settings

.. image:: images/templates-unix-macro-settings.png
   :alt: Picture of Unix macro settings screen in FusionDirectory
   
* Home directory : the path to the home directory of this user (required). 

You can use macro to automatically build the name of home directory users

For example : **/home/%uid%** 

Mail
----   

When you are creating or editing your template, click on Mail tab

.. image:: images/templates-mail-tab.png
   :alt: Picture of Mail in FusionDirectory

Then click on Add Mail settings. A new dialog is opened

.. image:: images/templates-add-mail-settings.png
   :alt: Picture of Add Mail settings buttonin FusionDirectory
   
Fill-in Mail account settings

.. image:: images/templates-user-mail-account-settings.png
   :alt: Picture of Mail user account settings screen FusionDirectory
   
* Primary address : primary mail address (required)

You can use the macros to automatically build the name of mail user account.
 
In this example we set macro **%uid%@acme.com** meaning that the mail account will be userid@acme.com
   
Click on Ok button bottom right   

.. image:: images/templates-ok.png
   :alt: Picture of Ok button in FusionDirectory
   
Now on the main page, on you template line, you will see the mail icon

.. image:: images/template-mail-icon.png
   :alt: Picture of Mail icon in FusionDirectory
