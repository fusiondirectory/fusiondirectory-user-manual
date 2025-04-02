Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-webservice
   apt-get install fusiondirectory-plugin-webservice-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash
   
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/webservice-fd-conf.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/webservice/description.yaml
