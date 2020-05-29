Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-public-forms
   yaourt -S fusiondirectory-plugin-public-forms-schema

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

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/public-forms-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/public-forms-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/public-forms-fd.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/public-forms-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/public-forms-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/public-forms-fd-conf.schema
