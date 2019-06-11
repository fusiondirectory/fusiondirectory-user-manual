.. include:: /globals.rst

Functionalities
===============

FusionDirectory WebService plugin exposes a JSONRPC webservice you can use if you want to access LDAP content through FusionDirectory system.
This way, you ensure that things like foreign keys are kept consistent, and you have a nicer API than the low-level LDAP one.

It is a standard JSONRPC server served on HTTPS protocol. 

Note that you can allow HTTP in plugin configuration, but please avoid doing so except for testing purposes.

The `webservice methods are detailed here <http://api.fusiondirectory.org/classfdRPCService.html#details>`_.
