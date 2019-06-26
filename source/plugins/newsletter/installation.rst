Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-newsletter
   yaourt -S fusiondirectory-plugin-newsletter-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-newsletter
   apt-get install fusiondirectory-plugin-newsletter-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-newsletter
   yum install fusiondirectory-plugin-newsletter-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/newsletter-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/newsletter-fd-conf.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/newsletter-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/newsletter-fd-conf.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/newsletter-fd.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/fusiondirectory/newsletter-fd-conf.schema
