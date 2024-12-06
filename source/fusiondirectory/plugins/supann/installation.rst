Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-supann
   apt-get install fusiondirectory-plugin-supann-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-supann
   yum install fusiondirectory-plugin-supann-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/internet2.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/supann-2019-11-22.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/supann-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/fdFranceConnect.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/internet2.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/supann-2019-11-22.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/supann-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/fdFranceConnect.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/supann/description.yaml
