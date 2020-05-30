FusionDirectory mail concept
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Mail methods

 FusionDirectory supports different ways to manage your mail accounts, each type of mail account is represented by a so called mail method. 
 
 Every method implements a specific storage of mail accounts. The mail methods can also add functionalities specific for each kin of server we manage.

For now we support : 

   * The base method explained in the mail plugin you are reading
   * `The Cyrus mail method <https://fusiondirectory-user-manual.readthedocs.io/en/1.3/plugins/cyrus/index.html>`_
   * `Dovecot <https://fusiondirectory-user-manual.readthedocs.io/en/1.3/plugins/dovecot/index.html>`_
   * `RENATER Partage <https://fusiondirectory-user-manual.readthedocs.io/en/1.3/plugins/renaterpartage/index.html>`_
   
The basic method just store the data that can be used by other service like postfix for example. The other method like cyrus, dovecot, renater-partage need the corresponding server   

