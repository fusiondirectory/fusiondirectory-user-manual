Installation
============

Install packages
----------------

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

Debian
^^^^^^

.. code-block:: bash
   
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/webservice-fd-conf.schema

RHEL
^^^^

.. code-block:: bash
   
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/webservice-fd-conf.schema
