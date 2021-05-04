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
   
   The fai plugin depends on the systems plugins so the systems plugins schema should be installed correctly
   The fai plugin depends on the argonaut plugins so the argonaut plugins schema should be installed correctly

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
