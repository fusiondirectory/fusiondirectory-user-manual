.. include:: /globals.rst

Functionalities
===============

All plugins can run external scripts when an action is triggered for creating, modifying or deleting. You can use pre and post events depending when you want to run the script. 


Pre triggers
------------

* **precreate** : Execute the script before creation.
* **premodify** : Execute the script before editing.
* **preremove**: Execute the script before removing.


The trigger works well and does not display information if it returns 0 On error, prevents save and displays error.


Post triggers
-------------

* **postcreate** : Execute the script after creation.
* **postmodify** : Execute the script after editing.
* **postremove** : Execute the script after removing.

The hook works well and does not display information if it returns 0 On error, displays command output.


Check triggers
--------------

* Execute the script in the check step (before saving), if it outputs anything, prevent save and show output as an error.

The trigger is considered to have passed if it returns 0 and does not display any message. 
(If it outputs anything it appears as a check failure, if it returns anything other than 0 it is considered a script error, 
for instance if the script was not able to do the check for some reason). 


LDAP attributes
---------------

You can use ldap attributes as command line options. Use the macro syntax.


LDAP arrays
-----------

If you put a var that is an array in the args of the hook, gosaAlternateMailAddress for instance, only the first value will be returned unless you use a modifier: macro


Special variables
-----------------

* **%callerDN%** gives the DN of the author of the modification
* **%callerCN%** gives the CN of the author of the modification
* **%callerUID%** gives the UID of the author of the modification
* **%callerSN%** gives the SN of the author of the modification
* **%callerGIVENNAME%** gives the GIVENNAME of the author of the modification
* **%dn%** gives the dn of the modified object
* **%location%** gives the name of the location of the LDAP

On users you get these extra variables available: 

* **%userPassword%** to get password hash
* **%passwordMethod%** to get password method (usually ssha)
* **%passwordClear%** to get clear password
* **%userLocked%** to get user lock status (0 or 1)






