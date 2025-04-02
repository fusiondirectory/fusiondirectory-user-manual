Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-gpg
   apt-get install fusiondirectory-plugin-gpg-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/gpg-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/pgp*

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/gpg/description.yaml
