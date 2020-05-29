.. include:: /globals.rst

Functionalities
===============

* Enable NextCloud account for a user

Click on Users icon in FusionDirectory

.. image:: images/nextcloud-users.png
   :alt: Picture of Users icon in FusionDirectory

Select a user

.. image:: images/nextcloud-user.png
   :alt: Picture of User line in FusionDirectory

Go to NextCloud tab

.. image:: images/nextcloud-tab.png
   :alt: Picture of NextCloud tab in FusionDirectory

Click on Add NextCloud settings button

.. image:: images/nextcloud-add-settings.png
   :alt: Picture of Add NextCloud settings button in FusionDirectory

Fill-in NextCloud account

.. image:: images/nextcloud-account.png
   :alt: Picture of NextCloud Account in FusionDirectory

Available attributes:
  * File quota: quota allowed for user in NextCloud
  * Home folder: to override default NextCloud home folder

.. tip::

    These attributes (``fdNextCloudQuota`` and ``fdNextCloudHomeFolder``) need then to be configured on NextCloud side, see `NextCloud administration manual`_.

.. _NextCloud administration manual: https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/user_auth_ldap.html#special-attributes

Click on Apply button bottom right to save your settings 

.. image:: images/nextcloud-apply.png
   :alt: Apply settings in FusionDirectory
