Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-webservice
   yaourt -S fusiondirectory-plugin-webservice-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-webservice
   apt-get install fusiondirectory-plugin-webservice-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-webservice
   yum install fusiondirectory-plugin-webservice-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/webservice-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash
   
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/webservice-fd-conf.schema

RHEL
^^^^

.. code-block:: bash
   
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/webservice-fd-conf.schema
