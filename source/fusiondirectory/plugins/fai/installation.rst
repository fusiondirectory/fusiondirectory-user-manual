Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-fai
   apt-get install fusiondirectory-plugin-fai-schema

Install schemas
---------------

.. note:: 

   The fai plugin depends on the systems and argonaut plugins so the schema for those plugins should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/fai-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/fai.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/fai/description.yaml
