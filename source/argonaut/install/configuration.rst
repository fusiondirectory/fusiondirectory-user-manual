.. _configuration-argonaut-label:

Configure Argonaut
==================

Argonaut use a global configuration file that is used by all programs : **/etc/argonaut.conf**.
This file is composed of various sections, all sections are filled with correct basic values.

.. note::

  To function correctly Argonaut need a correclty configured **/etc/ldap/ldap.conf** or **/etc/openldap/ldap.conf**

Argonaut configuration files section
------------------------------------

[server]
^^^^^^^^

This section contains all the argonaut server parameters : 

.. code-block:: shell

  server_ip   = 172.16.0.1
  
The ip address the server listen to. This address must match with the 
MAC address of argonaut server provided in FusionDirectory interface.

[client]
^^^^^^^^

This section contains all the argonaut server parameters : 

.. code-block:: shell

  client_ip   = 172.16.0.1
  
The ip address the server listen to. This address must match with the 
MAC address of argonaut server provided in FusionDirectory interface.

[ldap]
^^^^^^

This section contains all the ldap parameters : 

.. code-block:: shell

  config   = /etc/ldap/ldap.conf
  
Where is stored your ldap.conf configuration file. 

.. code-block:: shell

  dn = cn=admin,dc=fusiondirectory,dc=org

What is your bind dn. 

.. code-block:: shell
 
  password = secret 
 
What is the password for the provided bind dn.  

.. code-block:: shell

  tls = off

whether communication should be encrypted or not

