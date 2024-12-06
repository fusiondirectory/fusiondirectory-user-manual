Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-dhcp
   apt-get install fusiondirectory-plugin-dhcp-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-dhcp
   yum install fusiondirectory-plugin-dhcp-schema

Install schemas
---------------

.. note:: 
   
   The dhcp plugin depends on the systems plugins so the systems plugins schema should be installed correctly
   
Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/dhcp-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/dhcp-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/dhcp-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/dhcp-fd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/dhcp/description.yaml
