.. include:: ../../../globals.rst

Functionalities
===============

* Create an entity

.. image:: images/entity.png
   :alt: Picture of Supann entity in FusionDirectory

* Create an establishement

.. image:: images/establishement.png
   :alt: Picture of Supann establishement in FusionDirectory

* Create an user with supann informations

.. image:: images/user1.png
   :alt: Picture of Supann user in FusionDirectory (first part)

.. image:: images/user2.png
   :alt: Picture of Supann user in FusionDirectory (student part)

.. image:: images/user3.png
   :alt: Picture of Supann user in FusionDirectory (role part)

How use custom lists
^^^^^^^^^^^^^^^^^^^^

For some attributes like diplome you can extend them with a custom file in /etc/fusiondirectory/supann/

This process work for the following attributes:

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
