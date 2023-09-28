Installing Dependencies
'''''''''''''''''''''''

All The needed dependancies are resolved by the debian packages

.. note::

   The repositories are in https for Debian
   so you will need to install **apt-transport-https**

Install FusionDirectory
'''''''''''''''''''''''

You can then install FusionDirectory by running: 

.. code-block:: shell

   apt-get install fusiondirectory
   apt-get install fusiondirectory-schema

FusionDirectory Schema Setup
''''''''''''''''''''''''''''

Now that we have FusionDirectory installed, we need to install the
FusionDirectory schemas into our LDAP database.

We can easily do this by running:

.. code-block:: shell

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/core-fd.schema

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/core-fd-conf.schema

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/ldapns.schema

   fusiondirectory-schema-manager --insert-schema /etc/ldap/schema/template-fd.schema
   
You should see the FusionDirectory setup page come up by going to:

http://SERVER-IP/fusiondirectory



