Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-public-forms
   apt-get install fusiondirectory-plugin-public-forms-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-public-forms
   yum install fusiondirectory-plugin-public-forms-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/public-forms-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/public-forms-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/public-forms-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/public-forms-fd-conf.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/public/description.yaml
