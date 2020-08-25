FusionDirectory mail concept
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Mail methods

 FusionDirectory supports different ways to manage your mail accounts, each type of mail account is represented by a so called mail method.

 Every method implements a specific storage of mail accounts. The mail methods can also add functionalities specific for each kin of server we manage.

For now we support :

   * The base method explained in the mail plugin you are reading
   * :ref:`The Cyrus mail method <plugins-cyrus>`
   * :ref:`Dovecot <plugins-dovecot>`
   * :ref:`RENATER Partage <plugins-renater-partage>`

The basic method just store the data that can be used by other service like postfix for example. The other method like cyrus, dovecot, renater-partage need the corresponding server

