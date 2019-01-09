Dashboard
---------

.. image:: images/dashboard.png
   :alt: Dashboard screen

The dashboard screen allows you to consult statistics about the content of your LDAP tree.

The first tab shows the number of objects for each type known to your FusionDirectory installation.
Clicking them will lead you the management page for them, if any.

Users
^^^^^

.. image:: images/dashboard-users.png
   :alt: Dashboard users tab

The second tab shows more detailed statistics about users.
It is especially useful to track expired on soon-to-expire users, when using posix plugin.

Passwords
^^^^^^^^^

.. image:: images/dashboard-passwords.png
   :alt: Dashboard passwords tab

The third one shows statistics about passwords, and is especially useful for tracking old accounts still using an obsolete password method in order to update them.