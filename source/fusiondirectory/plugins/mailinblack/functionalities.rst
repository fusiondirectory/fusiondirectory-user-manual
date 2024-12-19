.. include:: /globals.rst

Functionalities
===============

* Edit a user

In FusionDirectory, click on users icon

.. image:: images/personal-user.png
   :alt: Picture of users icon in FusionDirectory

This will bring you to the users overview

.. image:: images/personal-users-tab.png
   :alt: Picture of users overview in FusionDirectory

Click on a user and go to mailinblack tab

.. image:: images/mailinblack-tab.png
   :alt: Picture of mailinblack tab in FusionDirectory

In this example, I selected peter antoine's profile

.. image:: images/personal-peter-antoine.png
   :alt: Picture of peter antoine user in FusionDirectory

Activate the mailinblack tab

.. image:: images/user-mailinblackuser-main.png
   :alt: Screenshot of section Mailinblack of tab Mailinblack of type User

* Protect: Whether this user is in protect mode in Mailinblack

Click on "Apply" button bottom right

.. image:: images/personal-apply-button.png
   :alt: Picture of Apply button in FusionDirectory


Now, if you go back to user list, you will see a new icon that defines that the mailinblack plugin is activated for your user

.. image:: images/mailinblack-icon.png
   :alt: Picture of Mailinblack icon in FusionDirectory

In FusionDirectory, you get a Mailinblack tab on users, which you should activate on users you want synchronized. Then you can check the checkbox if you want the user to be protected.

LDAP Filters
^^^^^^^^^^^^

In mailinblack use :

* ``(objectClass=fdMailInBlackUser)`` as synchronisation filter
* ``(fdMailInBlackProtect=TRUE)`` as protection filter.



