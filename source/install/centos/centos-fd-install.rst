Installing Dependencies
'''''''''''''''''''''''

FusionDirectory requires both the `EPEL`_ repository and
the Software Collection `SCL`_ for php 5.6 or higher.

-  To install epel

.. code-block:: shell

   yum install epel-release
   
-  To install php 5.6 Software Collection

.. code-block:: shell

   yum install centos-release-scl

   yum install rh-php56

- To enable php 5.6

.. code-block:: shell

   scl enable rh-php56 bash

Install the FusionDirectory Repos
'''''''''''''''''''''''''''''''''

To easily install the latest version, you can install the fusion
directory repos

Chose the repositories that goes with your centos version

:ref:`rpm-repository-centos6-label`

:ref:`rpm-repository-centos7-label`

Create 2 new repo file your favorite text editor.

- One for fusiondirectory
- One for fusiondirectory-extra

Install FusionDirectory
'''''''''''''''''''''''

You can then install FusionDirectory by running: 

.. code-block:: shell

   yum install -y fusiondirectory
   yum install -y fusiondirectory-selinux fusiondirectory-schema schema2ldif

.. warning::   

   If you use SELinux (same in permissive), you must install fusiondirectory-selinux !

FusionDirectory Schema Setup
''''''''''''''''''''''''''''

Now that we have FusionDirectory installed, we need to install the
FusionDirectory schemas into our LDAP database.

We can easily do this by running:

.. code-block:: shell

   fusiondirectory-insert-schema -i /etc/openldap/schema/cosine.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/inetorgperson.schema
   fusiondirectory-insert-schema -i /etc/openldap/schema/nis.schema
   fusiondirectory-insert-schema

Now we just need to restart apache:

.. code-block:: shell

   systemctl restart httpd

You should see the FusionDirectory setup page come up by going to:

http://SERVER-IP/fusiondirectory

.. _EPEL : https://fedoraproject.org/wiki/EPEL
.. _SCL : https://www.softwarecollections.org
.. _rh-php56 : https://www.softwarecollections.org/en/scls/rhscl/rh-php56


