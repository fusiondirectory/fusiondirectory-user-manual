Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-fai
   apt-get install fusiondirectory-plugin-fai-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-fai
   yum install fusiondirectory-plugin-fai-schema

Install schemas
---------------

.. note:: 

   The fai plugin depends on the systems and argonaut plugins so the schema for those plugins should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fai-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fai.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fai-fd-conf.schema
   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/fai.schema
