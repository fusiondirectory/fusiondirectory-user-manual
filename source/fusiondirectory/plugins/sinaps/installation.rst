Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-sinaps
   apt-get install fusiondirectory-plugin-sinaps-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-sinaps
   yum install fusiondirectory-plugin-sinaps-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/sinaps-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/sinaps-fd-conf.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/sinaps/description.yaml
   
