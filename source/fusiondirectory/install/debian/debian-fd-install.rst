Installing Dependencies
'''''''''''''''''''''''

All The needed dependancies are resolved by the debian packages

.. note::

   The repositories are in https for Debian
   so you will need to install **apt-transport-https**

Install the FusionDirectory Repos
'''''''''''''''''''''''''''''''''

To easily install the latest version, you can install the fusion
directory repos

Chose the repositories that goes with your Debian version

:ref:`fd-debian-repository-stretch-label`

:ref:`fd-debian-repository-jessie-label`

Create 2 new *.list* file your favorite text editor in */etc/apt/source.list.d*

- One for fusiondirectory
- One for fusiondirectory-extra

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

   fusiondirectory-insert-schema

You should see the FusionDirectory setup page come up by going to:

http://SERVER-IP/fusiondirectory



