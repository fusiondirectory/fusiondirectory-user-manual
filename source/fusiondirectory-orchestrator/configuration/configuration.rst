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
	
  LDAP_URI="ldaps://ldap.fusiondirectory.org"

Required in order to connect to the proper host.
FQDN or IP must be provided with ldap(s) to secure the connection.

.. code-block:: shell

  LDAP_BASE="dc=fusiondirectory,dc=org"

Required to operate with ldap libraries.

.. code-block:: shell
	
  LDAP_BIND_DN="cn=admin,dc=fusiondirectory,dc=org"

Required by LDAP in order to use the proper privileges.

.. code-block:: shell
	
  LDAP_PASSWORD="ldap_password"

Required password to authenticate LDAP

[FusionDirectory Webservice]
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. code-block:: shell

  FUSIONDIRECTORY_WEBSERVICE_URL="https://fd.fusiondirectory.org/rest.php/v1"
  FUSIONDIRECTORY_WEBSERVICE_LOGIN="weblogin_username"
  FUSIONDIRECTORY_WEBSERVICE_PASSWORD="weblogin_password"

Information related to the webservice of fusiondirectory. This is required for fusiondirectory-orchestrator
to activate specific actions within FusionDirectory webservice.

.. Note::

  | Orchestrator is highly depending on the URL rewriting mechanism of the web server.
  | In case of Apache2 ".htaccess" files are responsible for that logic.

  | Although informative, there should not be any value of modifying the contents of those files.
  | The goal is to redirect any call on URI to the main index file located in API directory. 

[JWT token settings]
^^^^^^^^^^^^^^^^^^^^

.. code-block:: shell
	
  #SECRET_KEY can be generated via a 256 bit Wep key generator such as 
	#https://allkeysgenerator.com/
	SECRET_KEY="256 bit key"

Required to secure and validate the generation of access and refresh tokens.

.. code-block:: shell

	TOKEN_EXPIRY="300"

Required to limit the availability of an issued token. In seconds.

.. code-block:: shell

	REFRESH_EXPIRY="432000"

Required to limit the availability of an issued refresh token. In seconds.

[SMTP server settings]
^^^^^^^^^^^^^^^^^^^^^^
.. code-block:: shell

  MAIL_AUTH="TRUE/FALSE"

If authentication is required, the following settings will be applied.
Note that some mail servers, such as relay servers, may not require authentication.

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

  MAIL_SEC_VERIFY="TRUE/FALSE"

This setting determines whether to accept all types of certificates,
including self-signed certificates, if necessary.

.. code-block:: shell
	
  MAIL_SEC="TLS/SSL"

The required secure methode. "TLS" can be used for "STARTLS".
Please note the importance of lowercase in 'ssl' or 'tls'.

.. code-block:: shell
	
  MAIL_PORT="SMTP port number"

The TCP/UDP port number of the SMTP server.(Example: SSL 465 / TLS 586).

