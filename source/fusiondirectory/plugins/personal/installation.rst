Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-personal
   apt-get install fusiondirectory-plugin-personal-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-personal
   yum install fusiondirectory-plugin-personal-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/personal-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/personal-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/personal-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/personal-fd-conf.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/personal/description.yaml
   
