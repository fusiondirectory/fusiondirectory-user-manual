Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-quota
   apt-get install fusiondirectory-plugin-quota-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-quota
   yum install fusiondirectory-plugin-quota-schema

Install schemas
---------------

.. note:: 
   
   The quota plugin depends on the systems plugins so the systems plugins schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/quota-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/quota.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/quota-fd.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/quota.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/quota/description.yaml
   
