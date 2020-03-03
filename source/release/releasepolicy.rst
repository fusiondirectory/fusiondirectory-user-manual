FusionDirectory Version policy
==============================

Versioning
----------

FusionDirectory can have 3 digits at maximum in a version : **X.Y.Z**

**Z** version increments (X.Y.Z1 –> X.Y.Z2, for example 1.2.1 to 1.2.2) are minor bug fix only releases.

**Y** or **X** version increments are major releases (X.Y1.Z -> X.Y2.Z, for exemple 1.1 to 1.2) are major releases.

Major Release
-------------

* Can contain any type of bugfix, new features and code refactor.
* Can remove attributes or objectclasses from the schema only if they were declared OBSOLETE in the previous major release.
* Can put **OBSOLETE** attributes and classes which are no longer used by the code.
* Two 2 major releases are needed before removing OBSOLETE attributes and objectClass.
* Can provide migration scripts in fusiondirectory-setup if needed for those, and/or migration instructions in the documentation.
* Have to provide migration instruction from previous major release.

Minor release
-------------

Minor release are small releases containing only bugfix to the last major release. It should be numbered with 3 digits.

Minor release **cannot** contain :

* Schema changes
* New features
* Code refactor
* Poorly tested code
* Changes which may break existing plugins or themes for previous release (or scripts based on the webservice)

Minor release contain :

* bugfix : should fix a bug observed in a previous release, something which did not work as intended.

Exceptions can be made :

* New feature can be included if it does not require any schema change and does not interfere with existing features
* Code refactor can be included if it leads to a significant performance gain and is thoroughly tested
* New plugin may be added if it does not require schema change (but it can add new schemas as this is non-intrusive)

Minor release must be released as soon as possible when :

* Security breach is found in the last stable release
* Regression (a bug which was not there in previous releases) is found in the last stable release
* Major bug is found in the last stable release
