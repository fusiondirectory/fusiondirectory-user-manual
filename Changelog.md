## %"FusionDirectory 1.3.1" - 2023-06-23

### Added

#### user-manual
- user-manual#1 add the code of conduct
- user-manual#27 Add a faq section
- user-manual#30 add a contribute section
- user-manual#44 Document the acls of FusionDirectory
- user-manual#48 Migration of Audit Plugin
- user-manual#49 Migration of Alias plugin
- user-manual#50 Migration of Applications plugin
- user-manual#51 Migration of Autofs plugin
- user-manual#52 Migration of Certificates plugin
- user-manual#53 Migration of Cyrus plugin
- user-manual#54 Migration of Dovecot plugin
- user-manual#56 Migration of DSA plugin
- user-manual#57 Migration of gpg plugin
- user-manual#58 Migration of Ipmi plugin
- user-manual#59 Migration of LDAP Dump plugin
- user-manual#60 Migration of LDAP Manager plugin
- user-manual#61 Migration of Personal plugin
- user-manual#62 Migration of Renater Partage plugin
- user-manual#63 Migration of user-reminder plugin
- user-manual#64 Migration of Weblink plugin
- user-manual#65 Migration of Webservice plugin
- user-manual#66 Migration of Community plugin
- user-manual#68 Migration of EJBCA plugin
- user-manual#69 Migration of Newsletter plugin
- user-manual#70 Migration of Pureftpd plugin
- user-manual#71 Migration of Sogo plugin
- user-manual#72 Migration of Squid plugin
- user-manual#73 Migration of subcontracting plugin
- user-manual#74 Migration of SSH plugin
- user-manual#75 Migration of developers plugin
- user-manual#76 Migration  of Mail plugin
- user-manual#77 Create release note for 1.3.1
- user-manual#79 Ticket for password recovery migration
- user-manual#80 document the usage of template
- user-manual#83 migrate the hooks explanation into the documentation
- user-manual#84 code of conduct
- user-manual#86 specify that the epoch parameter is mandatory when using data macros on unix tab (posix)
- user-manual#93 add release policy to the user manual
- user-manual#94 add the Distribution and PHP support Policy
- user-manual#97 Document CN pattern for SupAnn
- user-manual#118 write a section inside the fusiondrectory manual for schema2ldif
- user-manual#127 put the documentation from the man page of fusiondirectory-setup into the main user web documentation
- user-manual#130 document which attributes are propaged by the partage renater plugin
- user-manual#136 document the argonaut-clean-audit part in the argonaut manual
- user-manual#150 add the documentation for the subscriptions into the repository and how to configure it in fusiondirectory
- user-manual#156 add a reference to the subscription repository into install fusiondirectory on debian / centos
- user-manual#157 add a section on how to get the gpg public key from the public server
- user-manual#159 we need to document the the description and install part for all plugin
- user-manual#161 document the dns plugin
- user-manual#172 we need to add a mention to the documentation for the ppolicy plugin in openldap documentation
- user-manual#174 A lot of schema path are wrong
- user-manual#199 put the fusiondirectory.conf manpage in the official documentation

### Changed

#### user-manual
- user-manual#78 split configuration explanation in his own directory
- user-manual#82 simplify the user documentation
- user-manual#90 urls for professional suuport are wrong in the user manual
- user-manual#119 rearange manual to be able to merge schema2ldif and argonaut inside the manual
- user-manual#122 put the page form certified-distributions of the official website in place of  Linux Distribution & PHP support
- user-manual#131 merge the argonaut manual into the global manual
- user-manual#151 merge the maximu of differences between 1.3 and 1.4 to ease the cherry pick
- user-manual#152 Change the gpg key into the manual
- user-manual#153 change the repository for install from repos to public
- user-manual#193 clarify the php version supported for FusionDirectory 1.3.x
- user-manual#194 update the certified distribution matrix
- user-manual#202 update the documentation for 1.3.1

### Deprecated

#### user-manual
- user-manual#154 move the non supported version 1.2.x to the non suppoerted version part of the documentation

### Removed

#### user-manual
- user-manual#137 remove all reference to arch linux into the documentation
- user-manual#138 remove centos 8 from the certified distributions
- user-manual#148 remove centos 6 from the documentation
- user-manual#149 remove jessie instructions from the manual

### Fixed

#### user-manual
- user-manual#91 remove all reference to opensides in the user manual
- user-manual#92 correct twitter link in contact us
- user-manual#95 Correct the image include for folder and such in supann plugin
- user-manual#102 Fix build errors for user-manual for 1.3 version
- user-manual#124 there is a spelling error in the applications plugins manual in the schema section
- user-manual#145 url for the old webservice based on jsonrpc is wrong in the manual
- user-manual#178 replace freenode by libera
- user-manual#184 FD upgrade : updating fd-core schema not mentioned in the doc

