.. include:: /globals.rst

Functionalities
===============

* Add sieve service


Click on the System button located in the System section of FusionDirectory main page

.. image:: images/sieve-services-button.png
   :alt: Picture of Services button in FusionDirectory
   
   
Click on the server you wish to configure sieve service, in this exemple we assume that the server name is 'demo-fixes'


.. image:: images/sieve-demo-fixes-server.png
   :alt: Picture of demo-fixes server line in FusionDirectory
   
   
Click on 'Services' tab and click on 'action - create - Sieve:    


.. image:: images/sieve-create-sieve.png
   :alt: Picture of sieve in FusionDirectory
   
   
Fill in required fields then click 'Save': 


.. image:: images/sieve-settings.png
   :alt: Picture of sieve settings in FusionDirectory
   
   
Sieve settings

    * Hostname: Hostname of the Sieve server.
    * Port: Port number on which Sieve server should be contacted.
    * Option: (required) Options for contacting Sieve server. Valid values are notls, tls and ssl.
    * Valide certificats: Whether or not to validate server certificate on connexion. Valid values are validate and no-validate.
    * Admin user: (required) sieve server admin user.
    * Password: (required) Admin user password.
    
Click on 'save'



Now, in services column, you can see the sieve icon:     


.. image:: images/sieve-icon.png
   :alt: Picture of sieve icon in FusionDirectory
   
   

    
   

