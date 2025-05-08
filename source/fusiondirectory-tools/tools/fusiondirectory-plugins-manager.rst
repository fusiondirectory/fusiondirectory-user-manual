fusiondirectory-plugins-manager
===============================

Description
-----------

This tool is designed to help install FusionDirectory plugin referenced in the FusionDirectory marketplace or a developpers git

Options
-------

**--register-plugin**

Register a plugin within LDAP without copying the required files of the plugin itself. 

**--unregister-plugin**

Un-register a plugin already registered within your LDAP.

**--install-plugin**

Install the required files for your plugin in correct directories an register the plugin within LDAP.

**--remove-plugin**

Remove the registered plugin and its related files. 

**--list-plugins**

List the registered plugins.

Examples
--------

Register a plugin installed

.. code-block:: shell
   
    fusiondirectory-plugins-manager --register-plugin /etc/fusiondirectory/yaml/alias/description.yaml
    Installing : cn=alias,ou=pluginManager,dc=formation-fusiondirectory,dc=org ..

Unregister a plugin installed 

.. code-block:: shell

    fusiondirectory-plugins-manager --unregister-plugin alias
    alias plugin has been successfully unregistered

List plugins installed into FusionDirectory

.. code-block:: shell

    fusiondirectory-plugins-manager --list-plugins
    Number of plugins installed : 1
    Plugin : alias is installed

.. note::

  Those two commands are for plugin installed from outside source like the marketplace or the git of a developer
    
Install a plugin within FusionDirectory.

.. code-block:: shell
   
   fusiondirectory-plugins-manager --install-plugin notes

Remove a plugin within FusionDirectory.

.. code-block:: shell
   
   fusiondirectory-plugins-manager --remove-plugin notes
   sorbonne plugin has been successfully removed.    
