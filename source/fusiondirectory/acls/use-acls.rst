.. include:: /globals.rst

Use ACLs
========

ACLs Assignment
---------------

Click on ACL assignments on FusionDirectory main page

.. image:: images/acl-assignments-icon.png
   :alt: Picture of ACL Assignments icon in FusionDirectory
   
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


.. image:: images/acl-assignment-properties-options2.png
   :alt: Picture of ACL Assignment properties filled in FusionDirectory
   
Select a user by clicking on Add button under Members field
   
Select the user to whom you wish to assign student role (in this example, leheros toto)      

.. image:: images/acl-leheros-toto.png
   :alt: Picture of leheros toto user line in FusionDirectory

Click on Add button bottom right   

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory 
   
In ACL Assignment tab you can now see toto in Members field     

.. image:: images/acl-members-toto.png
   :alt: Picture of ACL Member filled-in field in FusionDirectory 

Click on Add button bottom right   

.. image:: images/acl-add-button.png
   :alt: Picture of Add button in FusionDirectory
   
You can see that ACL Assignment tab is now correctly filled

.. image:: images/acl-assignements-tab-list.png
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
   
Click on Edit button bottom right   

.. image:: images/acl-edit.png
   :alt: Picture of Edit button in FusionDirectory
   
You will see that the only editable field is Mobile (this user can only modify his mobile number as per the ACL that we set earlier)

.. image:: images/acl-organizational-contact-info.png
   :alt: Picture of Organizational contact info fields in FusionDirectory
