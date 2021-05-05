Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-argonaut
   apt-get install fusiondirectory-plugin-argonaut-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-argonaut
   yum install fusiondirectory-plugin-argonaut-schema

Install schemas
---------------

.. note:: 
   
   The argonaut plugin depends on the systems plugins so the systems plugins schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/argonaut-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/ldap/schema/fusiondirectory/argonaut-fd.schema
