Installation
============

In order to install zimbra plugin, you need to have installed and configured mail plugin.

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-zimbra
   apt-get install fusiondirectory-plugin-zimbra-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-zimbra
   yum install fusiondirectory-plugin-zimbra-schema

Insert schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/openldap/zimbra-fd.schema
   
RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/openldap/zimbra-fd.schema
