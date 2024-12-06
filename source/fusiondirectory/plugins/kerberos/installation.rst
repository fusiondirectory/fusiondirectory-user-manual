Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-kerberos

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-kerberos

Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/kerberos/description.yaml
