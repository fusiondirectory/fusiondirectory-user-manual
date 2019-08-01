.. include:: /globals.rst

Use ACLs with department
========================


delegate department management
------------------------------

  
So, let’s say you want to give manager rights to user **Richard Hollandais** to the branch **ou=test42,dc=demo-fusiondirectory,dc=org** 

Start by clicking on Departments icon on FusionDirectory main page

.. image:: images/acl-departments-icon.png
   :alt: Picture of Departments icon in FusionDirectory

Then click on edit icon (pencil) against test42 department line 

.. image:: images/acl-test42-department-line.png
   :alt: Picture of test42 line in FusionDirectory

Go to ACL Assignment tab.

.. image:: images/acl-delegation-assignment-tab1.png
   :alt: Picture of ACL assignmet tab in FusionDirectory

Click on Add button bottom left

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory
   
Fill-in ACL Assignment tab settings

.. image:: images/acl-delegation-acl-assignment.png
   :alt: Picture of ACL Assiogbnment settings tab in FusionDirectory


* **Mode** : subtree
* **Role** : manager
* **Members** : rhollandais

In order to select members, click on add button against member

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory
   
Select user Richard Hollandais from the users list   

.. image:: images/acl-delegation-user-richard-hollandais.png
   :alt: Picture of user ine in FusionDirectory

Click on Add button bottom right

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory 
   
Click again on Add button bottom right

You can now see the ACL Assignment tab filled with role manager for user Richard Hollandais

.. image:: images/acl-delegation-acl-assignment-rhollandais.png
   :alt: Picture of ACL Assignment filled tab in FusionDirectory
   
Click on Ok button bottom right  

.. image:: images/acl-ok.png
   :alt: Picture of Ok button in FusionDirectory    


Result
------

Now in order to see that Manager Richard Hollandais can manage student Paola Italienne, let's sign in FusionDirectory as rhollandais

.. image:: images/acl-delegation-signin-rhollandais.png
   :alt: Picture of FusionDirectory sign-in page

As manager role, he can see Users icon on his interface

.. image:: images/acl-delegation-rhollandais-main.png
   :alt: Picture of FusionDirectory main page
   
Click on Users icon and you will see the users Richard can manage   

.. image:: images/acl-delegation-rhollandais-users-list.png
   :alt: Picture of users list inFusionDirectory
