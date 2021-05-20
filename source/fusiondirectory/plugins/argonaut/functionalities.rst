.. include:: /globals.rst

Functionalities
===============

Argonaut Server
---------------

* Create a server configuration that contain IP and MAC address

  .. image:: images/argonaut-systems-list.png
     :alt: Picture of server in FusionDirectory with IP and MAC
   
* Edit the server and go to the service tab by clicking on the button

  .. image:: images/argonaut-systems-service-button.png
     :alt: Picture of service button in a server

* Add the Argonaut Server service

  .. image:: images/argonaut-systems-services.png
     :alt: Picture of all the services

* Fill all the informations

  .. image:: images/argonaut-server-filled.png
     :alt: Informations related to Argonaut Server

  * Delete finished tasks: remove tasks that are finished
  * Get packages informations: let consult packages informations from FusionDirectory
  * Protocol: use http or https to connect to Argonaut Server
  * Port: the port used for Argonaut Server
  * Timeout: connection timeout for Argonaut Server
  * Log directory: directory for Argonaut Server logs

  .. image:: images/argonaut-server-ssl-filled.png
     :alt: SSL informations related to Argonaut Server

  * Key: key used for https connection
  * Certificate: certificate used for https connection
  * CA certificate: ca used for https connections
  * CN of the certificate: custom CN if the hostname doesn't match by the certificate

  .. image:: images/argonaut-server-wol-filled.png
     :alt: WOL informations related to Argonaut Server

  * Interface: on which interface listend for wake on lan
  * IP tool: path of the ip tool used

* After saving you will see the Argonaut Server service icon in the system list

  .. image:: images/argonaut-systems-list-end.png
     :alt: Picture of server in FusionDirectory with Argonaut Server service
