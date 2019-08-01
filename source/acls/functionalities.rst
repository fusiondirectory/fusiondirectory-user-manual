.. include:: /globals.rst

Functionalities
===============


ACL roles
---------

* What can a person do in FusionDirectory?

Click on ACL roles icon on the main page of FusionDirectory

.. image:: images/acl-acl-roles-icon.png
   :alt: Picture of ACL Roles icon in FusionDirectory

The ACL role groups all the rights you want to give to a group or a user 

You will see the list of created roles. 

Each role has two columns :

* **Name** : this is the name of the role
* **Description** : a short description of what can be done by this role

.. image:: images/acl-roles-name-and-description.png
   :alt: Picture of ACL Roles list in FusionDirectory
   
Click on a role, in this example manager; you will be on Role tab

Properties settings

.. image:: images/acl-role-properties.png
   :alt: Picture of Role properties settings in FusionDirectory

   
* **Base** : object base

If you put the cursor on the base field, you will see all the base objects and you will be able to choose the one that you need.

* **Name** : a name for this role (required)
* **Description** : short description of this role 

ACLs settings

This field is very important because it defines the settings of the rights that this role has and the objects that it can manage

.. image:: images/acl-role-acls-settings.png
   :alt: Picture Base object field in FusionDirectory
   
In order to see the list of ACL categories assigned to this role, click on the little pencil on the right

.. image:: images/acl-pencil.png
   :alt: Picture of pencil icon in FusionDirectory
   
This will bring you to the whole list of available ACL categories. Scroll down to see the categories assigned to this role.

In this example, User is assigned to this role and it is marked as "ACL for these objects: posixAccount, user".

.. image:: images/acl-available-acl-category.png
   :alt: Picture of User ACL category in FusionDirectory
   
Click on the little pencil next to User category on the right

.. image:: images/acl-pencil.png
   :alt: Picture of pencil icon in FusionDirectory  
   
This will give you a simplified view of Object User attributes, highlighted in purple

.. image:: images/acl-user-atributes.png
   :alt: Picture of user attributes in FusionDirectory
   
The **beauty** and the **strength** of FusionDirectory is that you can also play on each single attribute of the object. 

To do this, click on "Show/hide advances settings" button on next to the object you are interested in

.. image:: images/acl-show-hide-button.png
   :alt: Picture of Show/hide advances settings button in FusionDirectory
   
This wil open a dialog incliding all the object settings and you can check/uncheck the ones you need

.. image:: images/acl-detailed-object-settings.png
   :alt: Picture of advanced object settings in FusionDirectory
   
Then you have a part for each user tab depending on your installed plugins. 
The **Create** right on a tab allows to activate it while the **Remove** one allows to deactivate.\ 
The **Grant permission** to owner checkbox allows to give rights only on the user’s own node as in the editowninfos role we used earlier. 


Special cases about rights
__________________________

Template
........

The template part is available for objects which support templates and allow to give rights on templates, and control rights on the template_cn field.

To be able to create a user using a template, the connected user needs:

* Read right of user/template:template_cn on the template object (or any parent department)

* Create right of user/user on the base the user is created in (or any parent department)

* Write right of the fields required by the templates on the base the user is created in (or any parent department)

Snapshot
........

There is a Snapshot part for objects which supports snapshots.

* Create right means the user will be able to take new snapshots

* Delete right means he will be able to delete existing snapshots

* Write right on restore_over field means he will be able to restore snapshots of an existing object

* Write right on restore_deleted field means he will be able to restore snapshots of deleted objects  


ACL assignments
---------------

* How to assign ACLs

After the creation of a role, we can say what a person has the right to do.

Click on ACL Assignments icon in FusionDirectory

.. image:: images/acl-assignments-icon.png
   :alt: Picture of ACL Assignments icon in FusionDirectory

You will see the list of ACL Assignments

.. image:: images/acl-assignments-list.png
   :alt: Picture of ACL Assignments list in FusionDirectory
   
Click on an ACL Assignment, in thie example test42 and you will see three columns

.. image:: images/acl-assignement-columns.png
   :alt: Picture of ACL Assignments columns in FusionDirectory
   

* **first column** : on what mode of operation the LDAP will work 
* **second column** : the dn of the role. It defines the rights assigned to the person in column 3 in relation to the ACLs assigned to him 
* **third column** : person to which the ACL is assigned
