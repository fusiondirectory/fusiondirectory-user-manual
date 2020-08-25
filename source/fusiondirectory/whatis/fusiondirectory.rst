What is FusionDirectory ?
=========================

`FusionDirectory <https://www.fusiondirectory.org/>`__ provides a
solution to daily management of data stored in an LDAP directory.
Becoming the cornerstone of the information system, the corporate
directory becomes more complex offering more data and managing more
infrastructure services.

This interface is simple and can be used to delegate fully or partly the
data management to non-specialists.

Features
^^^^^^^^

- Users, groups, mail, ssh, personal management.
- Supann norm Management.
- `PARTAGE`_ mail integration
- Systems management : dhcp, dns, sudo, all kind of systems.
- System deployment management : `FAI`_, `OPSI`_
- Complex Roles Management.
- Access to multiple LDAP trees.
- FusionDirectory Triggers

Acls and roles
^^^^^^^^^^^^^^

- ACLs are only used by FusionDirectory and not the underlying ldap server.
- ACLs can be assigned to roles.

  - Global administrator : Can do everything.
  - Local administrator : Can manage users and groups and also a branch.
  - Human resources : Can create users from template to optimize the arrival of new people.
  - User : Will only be able to change his data permitted by an administrator


FusionDirectory Triggers
^^^^^^^^^^^^^^^^^^^^^^^^

FusionDirectory incorporates a series of triggers that can launch a specific action based on a task
FusionDirectory must run.

These triggers are associated with a content type (LDAP user, group, server, password, service
and the triggering action (create, edit, delete, change password … )

For example, when creating a user, a script generation form can be executed automatically
with information from the LDAP server.

This can be useful for generating badges with photo, a form of access to the canteen or sending an email
to warn other services of the actual arrival of the person.

This system is also convenient when we want to deploy the account of that person on an application that
does not support LDAP.

Another example is when a user leaves, you must:

*  archive and delete his mailbox
*  archive and remove its network space
*  delete him from third party applications not connected to LDAP.


All of this can be easily done by shell scripts (at least in UNIX environment) and run automatically after
the suppression of the person by the administrator in FusionDirectory

The interaction with non-LDAP applications
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

FusionDirectory stores information of a service or a server on an LDAP
server. How about when this service does not have the opportunity to
interact with LDAP?

This question can be solved by creating:

-  LDAP schema suitable for application to the LDAP server
-  A plugin for its management in FusionDirectory with the simple plugin
   `API`_
-  An `Argonaut`_ module for the client installed on the server

.. _FAI : https://fai-project.org/
.. _OPSI : https://www.opsi.org/
.. _PARTAGE : https://partage.renater.fr/
.. _Argonaut : https://www.argonaut-project.org/
.. _API : https://fusiondirectory-developer-documentation.readthedocs.io/en/1.4/api/index.html
