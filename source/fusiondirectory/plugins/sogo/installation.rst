Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-sogo
   apt-get install fusiondirectory-plugin-sogo-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-sogo
   yum install fusiondirectory-plugin-sogo-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/sogo-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/calEntry.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/calRessources.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/sogo-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/calEntry.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/calRessources.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/sogo/description.yaml
