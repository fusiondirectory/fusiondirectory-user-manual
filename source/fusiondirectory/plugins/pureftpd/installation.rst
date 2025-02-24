Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-pureftpd
   apt-get install fusiondirectory-plugin-pureftpd-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-pureftpd
   yum install fusiondirectory-plugin-pureftpd-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/pureftpd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/pureftpd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/pureftpd/description.yaml
