Description
-----------

The fusiondirectory.conf file is a XML style configuration file. It is
parsed by FusionDirectory during log in. The file may contain extra tabs
and newlines for formatting purposes. Tag keywords in the file are
case-insensitive. Comments should be placed outside of XML tags and
should be encapsulated inside of <!-- --> tags.

Configuration layout
--------------------

The configuration has to be specified inside of the <conf> tags. It is
composed by a main configuration - including information about several
locations.

Layout example:

.. code-block:: xml

   <?xml version="1.0"?>

     <conf>

       <!-- Global setup -->

         <main>
           <!-- Location specific setups -->
             <location name="">

             </location>

         </main>

      </conf>

Main section
------------

The main section defines global settings, which might be overridden by
each location definition inside of this global definition.

Example layout:

.. code-block:: xml

   <main default="Example Net" listSummary="false" >

     <location name="Example Net">

        logging="TRUE"
        forceSSL="TRUE"

        <referral uri="ldaps://ldap.example.net:636" base="dc=example,dc=net"
        admin="cn=fusiondirectory-admin,dc=example,dc=net"
        password="secret" />

     </location>

   </main>

Main section options
--------------------

**forceSSL** bool
   The forceSSL statement enables PHP security checks to force encrypted
   access to the web interface. FusionDirectory will try to redirect to
   the same URL just with https://.

**logging** bool
   The logging statement enables event logging on FusionDirectory side.
   Setting it to true, FusionDirectory will log every action a user
   performs via syslog. If you use rsyslog and configure it to mysql
   logging, you can browse all events within FusionDirectory.
   FusionDirectory will not log anything, if the logging value is empty
   or set to false.

**templateCompileDirectory** path
   The templateCompileDirectory statements defines the path, where the
   PHP templating engins smarty should store its compiled
   FusionDirectory templates for improved speed. This path needs to be
   writeable by the user your webserver is running with.

**ignoreAcl** dn
   The ignoreAcl value tells FusionDirectory to ignore complete ACL sets
   for the given DN. Add your DN here and you'll be able to restore
   accidentally dropped ACLs.

**displayerrors** bool
   The displayerrors statement tells FusionDirectory to show PHP errors
   in the upper part of the screen. This should be disabled in
   productive deployments, because there might be some important
   passwords around.

Location section options
------------------------

**name** string
   The name of this location section that will appear in the dropdown on
   FusionDirectory homepage

**config** dn
   The config statement defines the LDAP base, where FusionDirectory
   stores management information, such as site wide locking and user
   notifications.

**debuglevel** integer
   The debuglevel value tells FusionDirectory to display certain
   information on each page load. Value is an OR combination of the
   following byte values : 

   - DEBUG_TRACE = 1
   - DEBUG_LDAP = 2
   - DEBUG_DB = 4
   - DEBUG_SHELL = 8
   - DEBUG_POST = 16
   - DEBUG_SESSION = 32
   - DEBUG_CONFIG = 64
   - DEBUG_ACL = 128
   - DEBUG_ARGONAUT = 256
   - DEBUG_MAIL = 512

LDAP options
------------

**ldapTLS** bool
   The ldapTLS statement enables or disables TLS operating on LDAP
   connections.

**ldapFollowReferrals** bool
   The ldapFollowReferrals statement tells FusionDirectory to follow
   LDAP referrals.

LDAP resource definition
------------------------

For every location you define inside your fusiondirectory.conf, you need
at least one entry of the type referral. These entries define the way
how to connect to some directory service.

Example:

.. code-block:: xml

   <referral uri="ldap://ldap.example.net" base="dc=example,dc=net"
    admin="cn=fusiondirectory-admin,dc=example,dc=net"
    password="secret" />

uri is a valid LDAP uri. base is the base this referral is responsible
for. admin is the DN which has the permission to write LDAP entries. And
password is the corresponding password for this DN. You can define a set
of referrals if you have several server to connect to.

