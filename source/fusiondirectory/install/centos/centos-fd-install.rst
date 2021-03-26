Installing Dependencies
'''''''''''''''''''''''

FusionDirectory requires both the `EPEL`_ repository and
the `REMI`_ repository for PHP 7.1

-  To install epel

.. code-block:: shell

   yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
   
-  To install remi repository

.. code-block:: shell

   yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm

   yum install yum-utils

- To enable Remi repo an PHP 7.1

.. code-block:: shell

   yum-config-manager --enable remi-php71
   yum-config-manager --enable remi
   yum update

Install the FusionDirectory Repos
'''''''''''''''''''''''''''''''''

To easily install the latest version, you can install the fusion
directory repos

Chose the repositories that goes with your centos version

:ref:`fd-rpm-repository-centos7-label`

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
.. _REMI : https://rpms.remirepo.net/


