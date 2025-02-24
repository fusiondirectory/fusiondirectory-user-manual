## %"FusionDirectory 1.5" - 2025-02-24

### Added

#### user-manual
- user-manual#175 add the new fonctionnality to desactivate supann tab in supann plugin manual
- user-manual#176 add new configuration for supann consent in the supann tab in the configuration backend
- user-manual#177 add new configuration for supann etiquettes for mail and tel in the supann tab in the configuration backend
- user-manual#219 [user-manual] - updates supann-ext documentation
- user-manual#241 add the new configuration for the fusiondirectory configuration partage backend configuration
- user-manual#248 [Tasks] - Explaination in details with screenshots of the new tabs life cycle and the incoming notifications
- user-manual#258 explain to user how to register the plugin in each plugin installation section
- user-manual#263 Migration note for 1.4 to 1.5
- user-manual#271 The task explanation page should show the full task menu and then explain the different sections
- user-manual#276 add a sectionn for the marketplace from the dev documentation

### Changed

#### user-manual
- user-manual#253 update the logo with the new one
- user-manual#265 Add new Authors to the Manual
- user-manual#268 Update the readme.md
- user-manual#269 remove the part that talk about stable dev and rewrite the fixes part
- user-manual#274 make clear that FusionDirectory only support PHP 7.4 and that FusionDirectory Orchestrator start at PHP 7.4

### Removed

#### user-manual
- user-manual#256 remove the bionic reference form the manual
- user-manual#260 removing the old gpg singature from the manual
- user-manual#261 remove the development gpg key
- user-manual#262 change support link due to the new website
- user-manual#275 remove the mention of iis in the manual

### Fixed

#### user-manual
- user-manual#244 Change the core/main menu into the documentation to reflect the new FusionDirectory menu organisation
- user-manual#249 Wrong command in "Check for deprecated attributes" section of migration guide from 1.3.-1 to 1.4
- user-manual#251 remove the utilities repository from the documentation as tools is already containing everything
- user-manual#254 Wrong url for orchestrator release
- user-manual#259 Wrong commands in latest/fusiondirectory/plugins/ipam/
- user-manual#264 Documentation for migration from 1.31 to 1.4 missing migrating mail-fd-conf.schema
- user-manual#270 there is an error in the task mail explanation


## %"FusionDirectory 1.4" - 2024-02-22

### Added

#### user-manual
- user-manual#36 document the invitation plugin
- user-manual#37 document the public-forms plugin
- user-manual#47 document the supann 2018 cycle de vie in fusiondirectory
- user-manual#67 Document placeholder %i%
- user-manual#85 Documentation for modifier m is missing
- user-manual#87 ACL documentation for new user filter and target filter
- user-manual#100 document the use of %modifiedLdapAttrs%
- user-manual#101 Document the way the triggers works
- user-manual#103 document the new configurable lists
- user-manual#108 explain that the filter on the attribute depend on the attribute visible on the object list
- user-manual#111 document the ipam plugin
- user-manual#112 document the base of the system plugin
- user-manual#117 Document NextCloud plugin
- user-manual#125 document the new dyngroup plugin
- user-manual#126 put the documentation from the man page for fusiondirectory.conf into the official web documentation
- user-manual#128 Document access to interfaces from webservice
- user-manual#129 Document import of systems with interfaces data
- user-manual#135 Document the archive plugin
- user-manual#139 document the new modifier e
- user-manual#142 we need to document the zimbra plugin
- user-manual#143 Document limitation for huge number of values in LDAP fields
- user-manual#144 Document parameter of "a" modifier
- user-manual#146 document the new option for cas verbose
- user-manual#147 Document subscriptions plugin
- user-manual#162 tell user that they need to use the official freeradius schema for the fusiondirectory plugin
- user-manual#169 Document supann France Connect support
- user-manual#170 document the mailinblack plugin
- user-manual#173 we need to document the function of the supann groups in the supann plugin
- user-manual#187 Add an example for d modifier where we only use the year
- user-manual#191 Add a note about inserting dyngroup.schema for dyngroup plugin
- user-manual#192 Update supann list custom documentation
- user-manual#204 [User-Manual] - Adds the new behaviour and updates existings entries related to fusiondirectory-tools
- user-manual#207 Make page to migration 1.3.1 to 1.4
- user-manual#213 we should add an entry of me nu on the left that show the webservice
- user-manual#216 [User-Manual] 1.4 LDAP Numbering needs updates since FranceConnect new schema
- user-manual#217 [User-manual] - FranceConnect - Adds to supann the new schema to be installed
- user-manual#225 There is no mention of askme macro
- user-manual#229 [Orchestrator] - Installation and configuration manual
- user-manual#231 Add the task and mail template fonctionnality to the manual
- user-manual#233 the fusiondirectory-schema-manager documentation doesn't show all possibilities
- user-manual#236 one url is missing from the documentation on repositories
- user-manual#237 add to the upgrade instruction to install all the new repositories

### Changed

#### user-manual
- user-manual#104 hooks have been renamed triggers and have new options
- user-manual#105 redo and update the configuration part of the user manual
- user-manual#106 update audit plugin configuration
- user-manual#107 update the invitations configuration
- user-manual#109 update the supann plugin documentation
- user-manual#110 the prerequisite talk about php 5.6 but its 7.x minimun in 1.4-dev
- user-manual#114 reorganize index plugin
- user-manual#179 we need to clarify how to install the subscription and remove reference to specific subscriptions
- user-manual#182 the minimal version of php for 1.4 has been changed this has to be reflected into the manual
- user-manual#185 Update the documentation for ldapmanager
- user-manual#195 update the prerequisite for fusiondirectory 1.4
- user-manual#205 Rename the docs renater-partage docs
- user-manual#215 change the install method for fusondirectory 1.4
- user-manual#212 FusionDirectory should recommand at least 512MB ram
- user-manual#242 change the wording for the professional support and urls

### Removed

#### user-manual
- user-manual#113 remove squid plugin from 1.4 documentation
- user-manual#211 there is no perl needed anymore
- user-manual#227 Correct contact us in the documentation
- user-manual#228 Remove we recommend to use the most recent php version as we are fixed on certains versions
- user-manual#243 remove the dashboard part as is no longer in FusionDirectory

### Fixed

#### user-manual
- user-manual#123 the name of the schema have changed since supann 2018
- user-manual#189 Documentation for version 1.3 and 1.4 mention Debian Stretch repositories
- user-manual#210 [Webauthn] - Fixes typos in documentation
- user-manual#218 Change --install-schema to --insert-schema
- user-manual#220 [user-manual] - Issue related to the configuration of the zimbra plugin
- user-manual#222 There is a typo in the repository for 1.4 its tell buster when it should tell bullseye
- user-manual#226 [user-manual] missing instructions for inserting core schemas for FusionDirectory

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
