Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-opsi
   apt-get install fusiondirectory-plugin-opsi-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-opsi
   yum install fusiondirectory-plugin-opsi-schema

Install schemas
---------------

.. note:: 
   
   The opsi plugin depends on the systems, argonaut, dns and samba plugins so the schema for those plugins should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/opsi-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/opsi-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/opsi-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/opsi-fd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/opsi/description.yaml
