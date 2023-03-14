fusiondirectory-plugins-manager
===============================

Description
-----------

This tool is designed to help you configure and perform multiple checks on your
FusionDirectory instance and fix usual misconfiguration.

Options
-------

--register-plugin
	 This option allows you to register a plugin within LDAP without copying the required files 
	 of the plugin itself. 

--unregister-plugin
	 This option allows you to un-register a plugin already registered within your LDAP.

--install-plugin
	 This option allows you to install the required files for your plugin in correct directories and
	 register the plugin within LDAP.

--remove-plugin
	 This option allows you to remove the registered plugin and its related files. 

--list-plugins
	 This option allows you to list the registered plugins.

Examples
--------

Install a plugin within FusionDirectory.

.. code-block:: shell
   
   fusiondirectory-plugins-manager --install-plugin /path/to/plugin

Register a plugin within FusionDirectory's LDAP.

.. code-block:: shell
   
   fusiondirectory-plugins-manager --register-plugin /path/to/plugin
