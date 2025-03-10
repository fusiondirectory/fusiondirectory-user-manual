Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ssh
   apt-get install fusiondirectory-plugin-ssh-schema

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ssh
   yum install fusiondirectory-plugin-ssh-schema

Install schemas
---------------

Debian
^^^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/openssh-lpk.schema

RHEL
^^^^

.. code-block:: bash

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/openssh-lpk.schema

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/ssh/description.yaml
