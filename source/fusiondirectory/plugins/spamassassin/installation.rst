Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-spamassassin
   apt-get install fusiondirectory-plugin-spamassassin-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-spamassassin
   yum install fusiondirectory-plugin-spamassassin-schema

Install schemas
---------------

.. note:: 
   
   The spamassassin plugin depends on the systems plugins so the systems plugins schema should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/spamassassin-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/spamassassin-fd.schema
