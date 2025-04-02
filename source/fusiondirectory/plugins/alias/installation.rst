Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-alias
   apt-get install fusiondirectory-plugin-alias-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/alias-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/alias-fd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/alias/description.yaml
