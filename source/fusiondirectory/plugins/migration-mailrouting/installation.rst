Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-migration-mailrouting
   apt-get install fusiondirectory-plugin-migration-mailrouting-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-migration-mailrouting
   yum install fusiondirectory-plugin-migration-mailrouting-schema

Install schemas
---------------

.. note::

   The migration-mailrouting plugin depends on the mail plugin so the mail plugin schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/mail-routing.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/mail-routing.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/migration-mailrouting/description.yaml
