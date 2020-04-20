Acls Issues
===========

* How can I let a person do administrative tasks under a specific department?

FusionDirectory implements a flexible but complex ACL management, please have a look at the following wiki page: FusionDirectory Acls


* How can I permit users to change some of their own attributes?

FusionDirectory implements a flexible but complex ACL management system, please have a look at the following wiki page: FusionDirectory Acls

Additionally you have to check the option 'Apply this acl only for users own entries'.


* How can I disable ACLs in case of misconfiguration?

  The **ignoreAcl** value tells FusionDirectory to ignore complete ACL sets for the given DN.
  Add your DN and you'll be able to restore accidently dropped ACLs.

  You need to add **ignoreAcl** in the main section of your **fusiondirectory.conf** like in this exemple :

.. code-block:: xml

   <main default="default">
        <!-- ... -->
        ignoreAcl="put_the_desired_dn"
        <!-- ... -->
    </main>
  

