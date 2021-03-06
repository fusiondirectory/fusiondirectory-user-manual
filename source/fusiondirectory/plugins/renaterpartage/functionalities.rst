.. include:: /globals.rst

Functionalities
===============

Add Renater Partage service
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Go to Systems

.. image:: images/renaterpartage-systems.png
   :alt: Picture of Systems icon in FusionDirectory

Create your server or edit an existing server

.. image:: images/renaterpartage-server-line.png
   :alt: Picture of server line in FusionDirectory

Click on services tab

.. image:: images/renaterpartage-services.png
   :alt: Picture of Services tab in FusionDirectory

Add the Renater Partage service

.. image:: images/renaterpartage-add-service.png
   :alt: Picture of Add Renaterpartage in FusionDirectory

Fill the fields for the Renater plugin and save it

.. image:: images/renaterpartage-settings.png
   :alt: Picture of Renaterpartage settings page in FusionDirectory

* Global settings :

   * URI: url of the webservice
   * User Agent: name of the user agent
   * Mailbox deletion: should i delete the mailbox after removing the account

* Per domains settings :

   * Domain: mail domain ex: acme.com
   * Key: API key received from Renater
   * Class of service: Service class name | cos id (zimbra cos id)

Click on "save" button bottom right to save your server

.. image:: images/renaterpartage-save.png
   :alt: Picture of Renaterpartage save button in FusionDirectory

Add Renater Partage to a user
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Click on "users" button in FusionDirectory main page

.. image:: images/renaterpartage-users.png
   :alt: Picture of Users icon in FusionDirectory

Select a user

.. image:: images/renaterpartage-user.png
   :alt: Picture of User line in FusionDirectory

Go to Mail tab and click on "Add mail settings"

.. image:: images/renaterpartage-add-mail-settings.png
   :alt: Picture of Add mail settings button in FusionDirectory

Fill in all the required information : mail account and other addresses and redirections

.. image:: images/renaterpartage-mail-account-info.png
   :alt: Picture of mail account entries in FusionDirectory

.. image:: images/renaterpartage-other-addresses.png
   :alt: Picture of other addresses entries in FusionDirectory

Click on "Apply" button bottom right to save your settings

.. image:: images/renaterpartage-apply-button.png
   :alt: Picture of other addresses entries in FusionDirectory

Add Renater Partage to a group
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In the same way you can use the mail tab of a user group to synchronize it with PARTAGE.
In this case you can activate and use the PARTAGE tab of the group to fill additional information.

Fields synchronised by renater-partage plugin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here are the fields which are synchronized for users:

=================================== ========================= ======
PARTAGE                             LDAP                      Notes
=================================== ========================= ======
zimbraCOSId                                                   COS id from Renater Partage service
zimbraMailQuota                     gosaMailQuota             Converted to Mio
zimbraPrefMailLocalDeliveryDisabled                           Checkbox "No delivery to own mailbox"
zimbraPrefMailForwardingAddress     gosaMailForwardingAddress Only one value
----------------------------------- ------------------------- ------
description                         description
displayName                         displayName
facsimileTelephoneNumber            facsimileTelephoneNumber
givenName                           givenName
homePhone                           homePhone
l                                   l
mobile                              mobile
ou                                  ou
pager                               pager
sn                                  sn
st                                  st
telephoneNumber                     telephoneNumber
title                               title
----------------------------------- ------------------------- ------
street                              street                    Activate "Separate address fields" configuration to see this field
postalCode                          postalCode                Activate "Separate address fields" configuration to see this field
postOfficeBox                       postOfficeBox             Activate "Separate address fields" configuration to see this field
----------------------------------- ------------------------- ------
company                             o
physicalDeliveryOfficeName          roomNumber
----------------------------------- ------------------------- ------
zimbraAccountStatus                                           Computed from FD lock status
initials                                                      Computed from givenName and sn
----------------------------------- ------------------------- ------
carLicense                          eduPersonPrincipalName    From SupAnn tab
zimbraHideInGal                     supannListeRouge          From SupAnn tab
----------------------------------- ------------------------- ------
co                                  co                        From personal tab
=================================== ========================= ======

Here are the fields which are synchronized for groups:

=================================================== =================================================
PARTAGE                                             LDAP
=================================================== =================================================
description                                         description
displayName                                         displayName
zimbraMailStatus                                    fdRenaterPartageGroupMailStatus
zimbraNotes                                         fdRenaterPartageGroupNotes
zimbraHideInGal                                     fdRenaterPartageGroupHideInGal
zimbraDistributionListSendShareMessageToNewMembers  fdRenaterPartageGroupSendShareMessageToNewMembers
=================================================== =================================================
