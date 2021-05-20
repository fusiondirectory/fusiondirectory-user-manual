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

Argonaut Client
---------------

* Create a server configuration that contain IP and MAC address

  .. image:: images/argonaut-systems-list.png
     :alt: Picture of server in FusionDirectory with IP and MAC
   
* Edit the server and click on the Argonaut Client tab

  .. image:: images/argonaut-systems-argonaut-client-tab.png
     :alt: Picture of the Argonaut Client tab

* Activate Argonaut Client

  .. image:: images/argonaut-systems-argonaut-client-activate-button.png
     :alt: Activate Argonaut Client

* Fill all the required informations and click on ok

  .. image:: images/argonaut-client-filled.png
     :alt: Informations related to Argonaut Client

  * Client port: the port used for Argonaut Client
  * Protocol: use http or https to connect to Argonaut Client
  * WakeOnLan interface: on which interface listend for wake on lan
  * Taskid file: file used for writing the taskid
  * Log directory: directory for Argonaut Server logs

  .. image:: images/argonaut-client-ssl-filled.png
     :alt: SSL informations related to Argonaut Server

  * Key: key used for https connection
  * Certificate: certificate used for https connection
  * CA certificate: ca used for https connections
  * CN of the certificate: custom CN if the hostname doesn't match by the certificate

  .. image:: images/argonaut-client-services-filled.png
     :alt: Services files in /etc/init.d

  * folder: directory where are stored the start scripts for the services
  * You not need to fill all the services names only the one you will use
