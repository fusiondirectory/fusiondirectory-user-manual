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

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/zimbra-fd.schema
   
RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/zimbra-fd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/zimbra/description.yaml
