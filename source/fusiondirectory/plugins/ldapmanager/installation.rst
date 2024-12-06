Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ldapmanager
   
RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ldapmanager
   
Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/ldapmanager/description.yaml
