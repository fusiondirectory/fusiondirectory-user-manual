
Functionalities
===============

The clean-audit application is used to purge audit entries after a selected amount of time

You will need the audit plugin installed into FusionDirectory to make it work

How it works
------------

Argonaut-clean-audit look at conservation delay in FusionDirectory configuration, by default its 120 days

When run argonaut-clean-audit it will purge all the entries older than the number of days mentionned in FusionDirectory config 

The arguments are the following:

*  --verbose

You run argonaut-clean-audit in a cron so that it purge older audit entries

Examples
--------

.. code-block:: shell

   # Basic clean audit run
   argonaut-clean-audit
   # Clean audit run in verbose mode
   argonaut-clean audit --verbose


