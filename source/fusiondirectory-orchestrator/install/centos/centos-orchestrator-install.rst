Installing Dependencies
'''''''''''''''''''''''

All The needed dependancies are resolved by the centos packages

.. note::

   The repositories are in https for Centos, same repos as FusionDirectory.

Install FusionDirectory Orchestrator 
''''''''''''''''''''''''''''''''''''

You can then install Orchestrator by running: 

.. code-block:: shell

   yum install fusiondirectory-orchestrator
   yum install fusiondirectory-orchestrator-schema

FusionDirectory Orchestrator Schema installation
''''''''''''''''''''''''''''''''''''''''''''''''

Now that we have Orchestrator installed, we need to install the
Orchestrator schemas into our LDAP database.

We can easily do this by running:

.. code-block:: shell

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/fusiondirectory/fusiondirectory-orchestrator.schema



