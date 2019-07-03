Installation
============

Install packages
----------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   yaourt -S fusiondirectory-plugin-subcontracting
   yaourt -S fusiondirectory-plugin-subcontracting-schema

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-subcontracting
   apt-get install fusiondirectory-plugin-subcontracting-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-subcontracting
   yum install fusiondirectory-plugin-subcontracting-schema

Install schemas
---------------

Archlinux
^^^^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i subcontracting-fd.schema

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i subcontracting-fd.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-insert-schema -i subcontracting-fd.schema
