Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-mailinblack
   apt-get install fusiondirectory-plugin-mailinblack-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-mailinblack
   yum install fusiondirectory-plugin-mailinblack-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/mailinblack-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/mailinblack-fd.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/mailinblack/description.yaml
