.. include:: /globals.rst

Most frequent mistakes
======================

Nothing happens, the script seems not to be called

* Check the sudoers entry for the webserver user (www-data, wwwrun, ..) and don't forget to use “NOPASSWD”
* Try to run the script as webserver user, use the complete command used in fusiondirectory configuration(/usr/bin/sudo …).
* Ensure that you have placed the post event correctly in the fusiondirectory configuration.


Example


.. code-block:: bash

   %www-data ALL=(ALL:ALL) NOPASSWD:/usr/local/bin/hook.sh
