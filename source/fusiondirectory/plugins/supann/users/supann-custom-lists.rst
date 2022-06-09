.. include:: ../../../../globals.rst

SupAnn custom lists
===================

* How use custom lists

For some attributes like diplome you can extend them with a custom file in /etc/fusiondirectory/supann/

This process works for the following attributes:

*   supannTypeEntiteAffectation (**entite**)
*   supannEtuDiplome_diplome (**diplome**)
*   supannEtuEtape (**etuetape** is empty by default)
*   supannEtuElementPedagogique (**etuelementpedagogique** is empty by default)
*   supannActivite (**activite**)
*   supannRoleGenerique (**role**)

You need to do the following to make it work.

*   Add a file like |file| diplome_CUSTOM in |folder| /etc/fusiondirectory/supann/

    * diplome can be replaced by any bold words above

    * CUSTOM can be replaced by any name, it will be the value between "{ }" by example "{SISE}"

*   Fill your file with your customs entries

.. code-block:: bash

   #DIPLOME_CUSTOM;TYPE_DIPLOME_SISE;SECTEUR_DISCIPLINAIRE_SISE;LIBELLE_INTITULE_1;LIBELLE_INTITULE_2
   1000013;01;16;ANALYSE DES MILIEUX BIOLOGIQUES;

In FusionDirectory you will need to select your **CUSTOM** part before selecting your entry that are in your file

.. note::

   you will find some examples in /usr/share/doc/fusiondirectory-plugin-supann/examples/
