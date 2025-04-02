Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-supann-ext
   apt-get install fusiondirectory-plugin-supann-ext-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/supann-ext-fd.schema

Register the plugin
-------------------

.. code-block:: bash

   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/supann-ext/description.yaml
