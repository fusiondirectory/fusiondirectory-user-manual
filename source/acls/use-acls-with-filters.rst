.. include:: /globals.rst

ACLs Assignment with user filter
================================

ACLs Assignment
---------------

Click on ACL assignments on FusionDirectory main page

.. image:: images/acl-assignments-icon.png
   :alt: Picture of ACL Assignments icon in FusionDirectorys
   
Click on the ACL assignment that you need

.. image:: images/acl-list.png
   :alt: Picture of ACL Assignments icon in FusionDirectory
   
ACL Assignment tab you can see all the assignments

.. image:: images/acl-assignements-tab-list0.png
   :alt: Picture of ACL Assignment tab in FusionDirectory
   
Click on Add button bottom left   

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory
   
Select ACL Assignment properties as follows 

* **Mode** : subtree
* **Role** : student
* **All users** : ticked

.. image:: images/acl-assignment-user-filter-properties-filled.png
   :alt: Picture of ACL Assignment properties filled in FusionDirectory

Add your member filter as follows

* **Member filter**: (uid=toto)

.. image:: images/acl-assignment-user-filter-advanced-user-filter-filled.png
   :alt: Picture of ACL Assignment advanced filled in FusionDirectory

Click on Add button bottom right   

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory
   
You can see that ACL Assignment tab is now correctly filled

.. image:: images/acl-assignements-user-filter-tab-list.png
   :alt: Picture of ACL Assignment tab in FusionDirectory
   
Click on Ok button bottom right to save   

.. image:: images/acl-ok.png
   :alt: Picture of Ok button in FusionDirectory


Result
------
   
* User view

Now let's see how the ACL has been applied to our User

Login as toto

.. image:: images/acl-fd-login-toto.png
   :alt: Picture of FD Login page
   
Click on User icon

.. image:: images/acl-user-icon.png
   :alt: Picture of user icon in FusionDirectory
   
We only have our mobile info because we assign ACL Role student for everyone but it applied only for (uid=toto)

.. image:: images/acl-organizational-user-filter-contact-info.png
   :alt: Picture of Organizational contact info fields in FusionDirectory


ACLs Assignment with target filter
==================================

ACLs Assignment
---------------

Click on ACL assignments on FusionDirectory main page

.. image:: images/acl-assignments-icon.png
   :alt: Picture of ACL Assignments icon in FusionDirectorys
   
Click on the ACL assignment that you need

.. image:: images/acl-list.png
   :alt: Picture of ACL Assignments icon in FusionDirectory
   
ACL Assignment tab you can see all the assignments

.. image:: images/acl-assignements-tab-list0.png
   :alt: Picture of ACL Assignment tab in FusionDirectory
   
Click on Add button bottom left   

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory
   
Select ACL Assignment properties as follows 

* **Mode** : subtree
* **Role** : manager
* **Members** : toto

.. image:: images/acl-assignment-target-filter-properties-filled.png
   :alt: Picture of ACL Assignment properties filled in FusionDirectory

Add your target filter as follows

* **Member filter**: (manager=%dn%)

.. image:: images/acl-assignment-target-filter-advanced-user-filter-filled.png
   :alt: Picture of ACL Assignment advanced filled in FusionDirectory

Click on Add button bottom right   

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory
   
You can see that ACL Assignment tab is now correctly filled

.. image:: images/acl-assignements-target-filter-tab-list.png
   :alt: Picture of ACL Assignment tab in FusionDirectory
   
Click on Ok button bottom right to save   

.. image:: images/acl-ok.png
   :alt: Picture of Ok button in FusionDirectory

Result
------
   
* User view

Now let's see how the ACL has been applied to our User

Login as toto

.. image:: images/acl-fd-login-toto.png
   :alt: Picture of FD Login page
   
Click on User icon to manage them

.. image:: images/acl-user-manager-icon.png
   :alt: Picture of user icon in FusionDirectory
   
We see that we can manage another user because the target filter give the manager right for the objects where (manager=%dn%) match (%dn% mean our own dn)

.. image:: images/acl-list-target-filter.png
   :alt: Picture of list of managable users in FusionDirectory
