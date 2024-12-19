Subscription
============

A subscription object stores the information about the subscription of a client.

Information
^^^^^^^^^^^

.. image:: images/subscription-subscription-main.png
   :alt: Screenshot of section Information of tab Subscription of type Subscription

* Base: Object base
* Name: Name to identify this subscription
* Description: Description of this subscription
* Type: Subscription type
* Contract: Contract identifier from Dolibarr

Login
^^^^^

.. image:: images/subscription-subscription-login.png
   :alt: Screenshot of section Login of tab Subscription of type Subscription

* Login: Login for this subscription
* Password: Password

Status
^^^^^^

.. image:: images/subscription-subscription-status.png
   :alt: Screenshot of section Status of tab Subscription of type Subscription

* Active: Whether this subscription is active
* Start date: Start date of this subscription
* End date: End date of this subscription

Repositories
^^^^^^^^^^^^

.. image:: images/subscription-subscription-repositories.png
   :alt: Screenshot of section Repositories of tab Subscription of type Subscription

* Apt repository: Apt repository
* RPM distribution: RPM distribution

Export
^^^^^^

The "Export" section allows generating files for FusionDirectory and package managers to send to the client.

.. image:: images/subscription-subscription-export.png
   :alt: Screenshot of section Export of tab Subscription of type Subscription

* Subscription file: Generate the subscription file to send to the client
* APT auth.conf: Generate the auth.conf file to send to the client if he uses Debian or a derivate
* APT: Generate the fusiondirectory-subscription.list file to send to the client if he uses an Apt based distribution
* RPM: Generate the fusiondirectory-subscription.repo file to send to the client if he uses an RPM based distribution


