.. include:: /globals.rst

Attributes
==========

Attributes synchronised by zimbra plugin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Here are the fields which are synchronized for users:

=================================== ========================= ======
Zimbra                              LDAP                      Notes
=================================== ========================= ======
zimbraCOSId                                                   COS id from Zimbra service
zimbraMailQuota                     gosaMailQuota             In bytes for Zimbra, in MiB in the LDAP
zimbraPrefMailLocalDeliveryDisabled gosaMailDeliveryMode      Checkbox "No delivery to own mailbox"
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