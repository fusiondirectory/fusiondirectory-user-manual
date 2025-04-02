Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-webauthn
   apt-get install fusiondirectory-plugin-webauthn-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/webauthn-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/webauthn-fd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/webauthn/description.yaml
