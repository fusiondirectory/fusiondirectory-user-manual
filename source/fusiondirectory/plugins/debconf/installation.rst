Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-debconf
   apt-get install fusiondirectory-plugin-debconf-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-debconf
   yum install fusiondirectory-plugin-debconf-schema

Install schemas
---------------

.. note::

   The debconf plugin depends on the systems and argonaut plugins so the schema for those plugins should be installed correctly

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/debconf-fd.schema
   fusiondirectory-schema-manager --install-schema /etc/ldap/schema/fusiondirectory/debconf.schema


RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/debconf-fd.schema
   fusiondirectory-schema-manager --install-schema /etc/openldap/schema/fusiondirectory/debconf.schema
