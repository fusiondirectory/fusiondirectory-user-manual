.. include:: /globals.rst

Create ACLs
===========


* How to create an ACL role

To give rights to users, the first step is to define an ACL role which will list the permissions you want to give.

Now let’s get more into the details of which kind of permission an ACL role can give.

Click on ACL roles icon on FusionDirectory main page

.. image:: images/acl-acl-roles-icon.png
   :alt: Picture of ACL roles icon in FusionDirectory

Click on Actions --> Create --> ACL role

.. image:: images/acl-action-create-acl-role.png
   :alt: Picture of ACL role creation menu in FusionDirectory

Fill name and description as you see fit.\\

.. image:: images/acl-creation-properties.png
   :alt: Picture of ACL role properties in FusionDirectory

Click **Add** button bottom left ACLs

.. image:: images/acl-add-acls.png
   :alt: Picture of Add button in FusionDirectory

You will see a screen listing the ACL categories:

.. image:: images/acls-categories.png
   :alt: ACL categories

Click on pencil icon next to User category

.. image:: images/acl-pencil.png
   :alt: Picture of pencil in FusionDirectory

Then you have a part for each user tab depending on your installed plugins. The **Create** right on a tab allows to activate it while the **Remove** one allows to deactivate.

The **Grant permission to owner** checkbox allows to give rights only on the user’s own node as in the editowninfos role we used earlier.

In this case we want to create a role named student having the rights to read and write his phone number.

.. image:: images/acl-edit-acl-for-user.png
   :alt: Picture of User rights menu in FusionDirectory
   
Check the box against Grant permission to owner

.. image:: images/acl-grant-permission.png
   :alt: Picture of Complete object options in FusionDirectory   
   
Go to object User and click on Show/hide advanced settings button   

.. image:: images/acl-show-hide-button.png
   :alt: Picture of Show/hide advanced settings button in FusionDirectory
   
Check read and write options in Business mobilenumber  

.. image:: images/acl-business-mobile-number.png
   :alt: Picture of Complete object options in FusionDirectory

Click on Apply button

.. image:: images/acl-apply.png
   :alt: Picture of Apply button in FusionDirectory   
   
Now, on the List of available ACL categories you can see that User category changed to ACL for these objects: user   

.. image:: images/acl-user-user.png
   :alt: Picture of User category line in FusionDirectory
     
Click on Apply button

.. image:: images/acl-apply.png
   :alt: Picture of Apply button in FusionDirectory  
   
Now you can see that ACL's settings are filled-in

.. image:: images/acl-settings-filled.png
   :alt: Picture of ACLs settings filled in FusionDirectory

Click on Ok button bottom right   

.. image:: images/acl-ok.png
   :alt: Picture of Ok button in FusionDirectory
