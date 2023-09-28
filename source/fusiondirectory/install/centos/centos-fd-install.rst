Installing Dependencies
'''''''''''''''''''''''

FusionDirectory requires both the `EPEL`_ repository and
the `REMI`_ repository for PHP 7.3

-  To install epel

.. code-block:: shell

   yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
   
-  To install remi repository

.. code-block:: shell

   yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm

   yum install yum-utils

- To enable Remi repo an PHP 7.3

.. code-block:: shell

   yum-config-manager --enable remi-php73
   yum-config-manager --enable remi
   yum update

Install FusionDirectory
'''''''''''''''''''''''

You can then install FusionDirectory by running: 

.. code-block:: shell

   yum install -y fusiondirectory
   yum install -y fusiondirectory-selinux fusiondirectory-schema

.. warning::   

   If you use SELinux (same in permissive), you must install fusiondirectory-selinux !

FusionDirectory Schema Setup
''''''''''''''''''''''''''''

Now that we have FusionDirectory installed, we need to install the
FusionDirectory schemas into our LDAP database.

We can easily do this by running:

.. code-block:: shell

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/cosine.schema
   
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/inetorgperson.schema
   
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/nis.schema
   
   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/core-fd.schema

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/core-fd-conf.schema

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/ldapns.schema

   fusiondirectory-schema-manager --insert-schema /etc/openldap/schema/template-fd.schema

Now we just need to restart apache:

.. code-block:: shell

   systemctl restart httpd

You should see the FusionDirectory setup page come up by going to:

http://SERVER-IP/fusiondirectory

.. _EPEL : https://fedoraproject.org/wiki/EPEL
.. _REMI : https://rpms.remirepo.net/


