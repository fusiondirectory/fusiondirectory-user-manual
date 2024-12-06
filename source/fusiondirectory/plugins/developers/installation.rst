Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-developers
   
RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-developers

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/developers/description.yaml
