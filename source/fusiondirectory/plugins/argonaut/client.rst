.. include:: /globals.rst

Argonaut Client
===============

* Edit the system and click on the Argonaut Client tab

  .. image:: images/argonaut-systems-argonaut-client-tab.png
     :alt: Picture of the Argonaut Client tab

* Activate Argonaut Client

  .. image:: images/argonaut-systems-argonaut-client-activate-button.png
     :alt: Activate Argonaut Client

Configuration
-------------

Argonaut client settings
^^^^^^^^^^^^^^^^^^^^^^^^

  .. image:: images/argonaut-client-filled.png
     :alt: Informations related to Argonaut Client

  * Client port: the port used for Argonaut Client
  * Protocol: use http or https to connect to Argonaut Client
  * WakeOnLan interface: on which interface listend for wake on lan
  * Taskid file: file used for writing the taskid
  * Log directory: directory for Argonaut Server logs

SSL paths
^^^^^^^^^

  .. image:: images/argonaut-client-ssl-filled.png
     :alt: SSL informations related to Argonaut Client

  * Key: key used for https connection
  * Certificate: certificate used for https connection
  * CA certificate: ca used for https connections
  * CN of the certificate: custom CN if the hostname doesn't match by the certificate

Service names
^^^^^^^^^^^^^

  .. image:: images/argonaut-client-services-filled.png
     :alt: Services files in /etc/init.d

  * folder: directory where the start scripts for the services are stored
