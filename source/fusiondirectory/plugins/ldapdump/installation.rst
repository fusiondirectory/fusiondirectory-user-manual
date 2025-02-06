Installation
============

Install packages
----------------

Debian
^^^^^^

.. code-block:: bash

   apt-get install fusiondirectory-plugin-ldapdump

RHEL
^^^^

.. code-block:: bash

   yum install fusiondirectory-plugin-ldapdump
 
Register the plugin
-------------------

.. code-block:: bash
 
   fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/ldapdump/description.yaml
