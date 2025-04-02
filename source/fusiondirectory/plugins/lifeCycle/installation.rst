Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-lifecycle
   apt-get install fusiondirectory-plugin-lifecycle-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/lifecycle-fd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/lifecycle/description.yaml
