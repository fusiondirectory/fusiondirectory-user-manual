Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-subscriptions
   apt-get install fusiondirectory-plugin-subscriptions-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-subscriptions
   yum install fusiondirectory-plugin-subscriptions-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/subscriptions-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/subscriptions-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/subscriptions-fd-conf.schema
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/subscriptions-fd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/subscriptions/description.yaml
