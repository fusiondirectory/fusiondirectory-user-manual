Configurable lists
------------------

Unlike version 1.3, where you had to see the list as it is, in the latest version of FusionDirectory you can decide what you want to see.

Click on Users icon on FusionDirectory main page

.. image:: images/configurablelist-user.png
   :alt: Picture of Users icon in FusionDirectory

You will be directed to Users page

.. image:: images/configurablelist-users-page.png
   :alt: Picture of Users management page in FusionDirectory

On top left page you will see a little icon representing two lines with a dot 
   
.. image:: images/configurablelist-icon.png
   :alt: Picture of configurable lists icon in FusionDirectory

By clicking on this icon, you can decide which items you want to see in the list

.. image:: images/configurablelist-configuration-page.png
   :alt: Picture of Configurable lists configuration page in FusionDirectory
   
You can play with the little arrows to determine the order of the items in the list.  

.. image:: images/configurablelist-arrows.png
   :alt: Picture of arrows icon in FusionDirectory
   
On configuration page, fill in the following fields :

* **Type** : type of column (required)
* **Attribute** : LDAP attributes to display, separated by commas. The special values "nameAttr" and "mainAttr" also work   
* **Label** : title of the column
* **Persistent** : Should this configuration be saved in LDAP as the default configuration for this page
* **Global default** : Should this configuration be saved in LDAP as the default configuration for this page for all users

Click on save button, bottom right 

.. image:: images/configurablelist-save.png
   :alt: Picture of save button in FusionDirectory

Now, on Users main page you will see columns in the order you choose

.. image:: images/configurablelist-columns-list.png
   :alt: Picture of column list in FusionDirectory
