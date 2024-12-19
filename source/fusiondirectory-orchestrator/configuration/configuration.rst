Configuration
-------------

| Orchestrator requires a one file to be configured properly.

Configuration file
""""""""""""""""""
.. note::
	The editable file is located at **/etc/fusiondirectory-orchestrator/orchestrator.conf**

[LDAP settings]
^^^^^^^^^^^^^^^
.. code-block:: shell
	
  LDAP_HOST="localhost"

Required in order to connect to the proper host.
FQDN or IP must be provided.

.. code-block:: shell
	
  LDAP_ADMIN="cn=admin,dc=fusiondirectory,dc=org"

Required by LDAP in order to use the proper privileges.

.. code-block:: shell
	
  LDAP_PWD="ldap_pwd"

Required password to authenticate LDAP

.. code-block:: shell
	
  LDAP_OU_USER="ou=people,dc=fusiondirectory"

Required to ease the research of the branch people by endpoints.

[JWT token settings]
^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell
	
  #SECRET_KEY can be generated via a 256 bit Wep key generator such as 
	#https://allkeysgenerator.com/
	SECRET_KEY="256 bit key"

Required to secure and validate the generation of access and refresh tokens.

[SMTP server settings]
^^^^^^^^^^^^^^^^^^^^^^
.. code-block:: shell
	
  MAIL_USER="mail_user"

The login ID to authenticate to the specified SMTP server.

.. code-block:: shell
	
  MAIL_PASS="mail_pwd"

The password used for above authentication.

.. code-block:: shell
	
  MAIL_HOST="fqdn or IP"

The SMTP server domain name or IP.

.. code-block:: shell
	
  MAIL_SEC="ssl"

The required secure methode. "TLS" can be used for "STARTLS".
Please note the importance of lowercase in 'ssl' or 'tls'.

.. code-block:: shell
	
  MAIL_PORT="SMTP port number"

The TCP/UDP port number of the SMTP server.(Example: SSL 465 / TLS 586).

.. Note::

  | Orchestrator is highly depending on the URL rewriting mechanism of the web server.
  | In case of Apache2 ".htaccess" files are responsible for that logic.

  | Although informative, there should not be any value of modifying the contents of those files.
  | The goal is to redirect any call on URI to the main index file located in API directory. 
