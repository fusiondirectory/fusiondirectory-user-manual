Installing Dependencies
'''''''''''''''''''''''

All The needed dependancies are resolved by the debian packages

.. note::

   The repositories are in https for Debian
   so you will need to install **apt-transport-https**

Install FusionDirectory Orchestrator 
''''''''''''''''''''''''''''''''''''

You can then install Orchestrator by running: 

.. code-block:: shell

   apt-get install fusiondirectory-orchestrator
   apt-get install fusiondirectory-orchestrator-schema

FusionDirectory Orchestrator Schema installation
''''''''''''''''''''''''''''''''''''''''''''''''

Now that we have Orchestrator installed, we need to install the
Orchestrator schemas into our LDAP database.

We can easily do this by running:

.. code-block:: shell

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/fusiondirectory/fusiondirectory-orchestrator.schema



