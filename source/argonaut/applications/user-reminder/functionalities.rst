
Functionalities
===============

The user-reminder application is used to send mail to users warning that the account will expire and provide a way of extending it if needed

You will need the user-reminder plugin installed into FusionDirectory to make it work

How it works
------------

Argonaut-user-reminder look at different source (posix, ppolicy, supann) and can send a mail or make the account expire

The arguments are the following:

*  --help
*  --verbose
*  --posix
*  --ppolicy
*  --supann
*  --all (posix, ppolicy and supann)
*  --supan-update (maintain the supann workflow through webservice it need the REST configuration in argonaut.conf)

Depend on which source you want to use you also need the FusionDirectory plugin that match (posix, ppolicy, supann)

You run argonaut-user-reminder in a cron so that it keep all the informations updated

Examples
--------

.. code-block:: shell

   # Expiration for all
   argonaut-user-reminder --verbose --all
   # Expiration for ppolicy
   argonaut-user-reminder --verbose --ppolicy
   # Expiration for posix
   argonaut-user-reminder --verbose --posix
   # Expiration for supann
   argonaut-user-reminder --verbose --supann
   # Maintain supann workflow through webservce
   argonaut-user-reminder --verbose --supann-update


