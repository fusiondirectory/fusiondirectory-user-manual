.. include:: /globals.rst

Functionalities
===============

Add a web application
^^^^^^^^^^^^^^^^^^^^^

.. image:: images/applications-create-webapp.png
   :alt: Picture of Applications create web application in FusionDirectory
   
A new dialog box will open, fill the forms and save your application :


* Base: where is the application entry in the LDAP
* Name: applications name
* Description: description of the application
* URL: URL of the application
* Display Name: the name that we display (FusionDirectory portal)
* Set your icon for you application (FusionDirectory portal)


.. image:: images/applications-webapp-filled.png
   :alt: Picture of Applications web application filled page in FusionDirectory   
   
Click "ok", and you will see the wordpress line created in the application

.. image:: images/applications-webapp-created.png
   :alt: Picture of Applications webapp created line in FusionDirectory
   

Now, if you click on the menu entry "Groups and roles" on the left, you will find a "role-test" group


.. image:: images/applications-role-test.png
   :alt: Picture of User and roles role-test line in FusionDirectory
   
If you click on the role-test group, you will see the Applications tab   
   
.. image:: images/applications-list.png
   :alt: Picture of Applications tab of role-test in FusionDirectory
   

Click on the entry that you created before and click "add", and you will see your webapplication added


Now go to LDAP tab and click on the entry you see

.. image:: images/applications-ldap-tab.png
   :alt: Picture of Applications LDAP tab in FusionDirectory
   
   
This will give you an overview of attributes **fdApplicationAllowed** that you will be able to use in a filter to restrict who can login



Use FusionDirectory as portal
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


* Activate portal mode


Go in configuration 

.. image:: images/applications-configuration-menu-ok.png
   :alt: Picture of Configuration tab in FusionDirectory
   
   
Click on plugins section and then click edit in the bottom right corner

.. image:: images/applications-plugins-tab.png
   :alt: Picture of Plugins tab in FusionDirectory


.. image:: images/applications-edit-button.png
   :alt: Picture of Edit button in FusionDirectory
   
   
