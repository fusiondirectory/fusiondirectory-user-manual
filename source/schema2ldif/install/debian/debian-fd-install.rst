Installing Dependencies
'''''''''''''''''''''''

All The needed dependancies are resolved by the debian packages

.. note::

   The repositories are in https for Debian
   so you will need to install **apt-transport-https**

Install the Schema2ldif Repos
'''''''''''''''''''''''''''''

To easily install the latest version, you can install the fusion
directory repos

Chose the repositories that goes with your Debian version

:ref:`sl-debian-repository-stretch-label`

Create one new *.list* file fusiondirectory-extra with your favorite text editor in */etc/apt/source.list.d*

Install Schema2ldif
'''''''''''''''''''

You can then install schema2ldif by running: 

.. code-block:: shell

   apt-get install schema2ldif




