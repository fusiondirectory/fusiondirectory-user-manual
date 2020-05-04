.. include:: ../../../globals.rst

SupAnn custom lists
===================

* How use custom lists

For some attributes like diplome you can extend them with a custom file in /etc/fusiondirectory/supann/

This process works for the following attributes:

*   supannTypeEntiteAffectation (entite) only from FD 1.3
*   supannEtuDiplome_diplome (diplome)
*   supannEtuEtape (etuetape is default empty)
*   supannEtuElementPedagogique (etuelementpedagogique is default empty)
*   supannActivite (activite)
*   supannRoleGenerique (role)

You need to do the following to make it work.

*   Add a file like |file| diplome_CUSTOM in |folder| /etc/fusiondirectory/supann/
*   Fill your file with your customs entries

In FusionDirectory you will need to select your "CUSTOM" part before selecting your entry that are in your file
