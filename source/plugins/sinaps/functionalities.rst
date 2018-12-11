
Functionalities
===============

Diffusion
---------

Once your FusionDirectory instance is correctly set to be receiving user and structures diffusion events in Sinaps and Sinaps plugin is up and running (see configuration_), creation and modification on Sinaps objects will be applied in FusionDirectory with the following rules.

When a Diffusion event is received, FusionDirectory first looks at the cross references and search for the application identifier set in the configuration. If no reference is found or the reference found is then not found in the LDAP, an object is created. Otherwise the matching object is updated.

Structure
+++++++++

Structures are synchronized as SupAnn_ entities.

==========================  ==============================================  ===========
FusionDirectory field       Sinaps XML field                                Details
==========================  ==============================================  ===========
ou                          libelle20
description                 descriptifLong
supannCodeEntite            codeStructure                                   Must be unique as it’s used in the dn
supannTypeEntite            codeSousType                                      You need to configure Sinaps to transcode this into a valid value
supannRefId                 referenceCroisee                                Formated as {identifiantApplication}identifiantExterne
telephoneNumber             methodesDeContact/methodeDeContact/valeur       If codeTypeMethodeContact is TEL
facsimileTelephoneNumber    methodesDeContact/methodeDeContact/valeur       If codeTypeMethodeContact is FAX
postalAddress               methodesDeContact/methodeDeContact/*            If codeTypeMethodeContact is ADR and temoinAdressePrincipale is true
supannCodeEntiteParent      liensStructure/lienStructure/codeStructureMere  If codeTypeLien is HIE
fdSupannStartDate           dateDebutValidite
fdSupannEndDate             dateFinValidite
==========================  ==============================================  ===========

Personne
++++++++

Persons are synchronized as users.

If *rattachements* is empty, the event is considered as a deletion, in which case:

* The current date is stored in fdContractEndDate
* The account is locked
* The fields telephoneNumber, facsimileTelephoneNumber and mobile are emptied
* The mail tab is removed

Otherwhise the following fields are sychronized:

================================= ======================================================================================================  ===========
FusionDirectory field             Sinaps XML field                                                                                        Details
================================= ======================================================================================================  ===========
supannCivilite                    civilite
sn                                nomUsage
description                       descriptifLong
dateOfBirth                       dateNaissance
gender                            sexe
supannRefId                       referenceCroisee                                                                                        Formated as {identifiantApplication}identifiantExterne
givenName                         prenoms                                                                                                 Cut at first ';'
homePhone                         methodesDeContact/methodeContact/valeur                                                                 If typeMethodeContact is TELPERSO. Can only have one value.
fdPrivateMail                     methodesDeContact/methodeContact/valeur                                                                 If typeMethodeContact is MAILPERSO. Can have multiple values.
postalAddress                     methodesDeContact/methodeContact/*                                                                      If codeTypeMethodeContact is ADR and temoinAdressePrincipale is true, and codeTypeAdresse is not ADRPERSO
homePostalAddress                 methodesDeContact/methodeContact/*                                                                      Same as above but codeTypeAdresse is ADRPERSO
supannEntiteAffectationPrincipale rattachements/rattachement/roles/role/personneRessource/affectations/affectation                        Only if role/typeRole is PR and the cross reference is found in the LDAP
supannEntiteAffectation           rattachements/rattachement/roles/role/personneRessource/affectations/affectation                        Same as above
supannEmpCorps                    rattachements/rattachement/roles/role/personneRessource/elementsDeCarriere/elementCarriere/corps        Only if role/typeRole is PR
supannActivite                    rattachements/rattachement/roles/role/personneRessource/elementsDeCarriere/elementCarriere/bapReferens  Only if role/typeRole is PR
supannRoleGenerique               rattachements/rattachement/fonctionsOccupees/fonctionOccupee/fonctionRh
supannTypeEntiteAffectation       rattachements/rattachement/fonctionsOccupees/fonctionOccupee                                            If the cross reference is found in the LDAP
supannEntiteAffectation           rattachements/rattachement/fonctionsOccupees/fonctionOccupee                                            If the cross reference is found in the LDAP
supannRoleEntite                  rattachements/rattachement/fonctionsOccupees/fonctionOccupee                                            Groups values from the three fields above
================================= ======================================================================================================  ===========

Acquisition
-----------

Once FusionDirectory is properly configured to send Acquisition events to Sinaps, it will do so when a user is modified, with the following rules:

* Fields listed in "Contact methods" in the configuration are sent as the indicated contact methods
* *supannEntiteAffectationPrincipale* is send as a *rattachement* with roles/role/typeRole = EXT and roles/role/externe/typeExterne the value configured in "Acquisition external type" in the configuration
