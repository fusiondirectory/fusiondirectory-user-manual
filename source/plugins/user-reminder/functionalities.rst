.. include:: /globals.rst

Functionalities
===============

* How to configure User-Reminder plugin

Click on COnfiguration icon in FusionDirectory

.. image:: images/user-reminder-configuration.png
   :alt: Picture of Configuration icon in FusionDirectory

Go to User reminder tab

.. image:: images/user-reminder-tab.png
   :alt: Picture of User reminder tab in FusionDirectory
   
Click on the edit button at the bottom right   

.. image:: images/user-reminder-edit-button.png
   :alt: Picture of User reminder edit button in FusionDirectory
   
Fill-in user-reminder settings:


.. image:: images/user-reminder-settings.png
   :alt: Picture of User reminder settings page in FusionDirectory 


.. code-block:: bash

   Delay before expiration: days before expiration when we send the email
   Delay before sending again: days before sending a second email
   Extension of the validity: number of days for the postpone
   Sender email address: sender e-mail address
   Allow use of alternate addresses: thick this box if needed
    
Fill-in Ppolicy email settings:


.. image:: images/user-reminder-ppolicy-settings.png
   :alt: Picture of Ppolicy settings page in FusionDirectory 


.. code-block:: bash

   Forward alerts to the manager : thick to send alert to manager
   Subject : subject of the e-mail
   Body (%s are cn and login) : content of the e-mail
    
Fill-in Alert email settings:


.. image:: images/user-reminder-alert-email-settings.png
   :alt: Picture of Alert email settings page in FusionDirectory 


.. code-block:: bash

   Forward alerts to the manager : thick to send alert to manager
   Subject : subject of the e-mail
   Body (%s are cn and login) : content of the e-mail
    
Fill-in Confirmation email settings:


.. image:: images/user-reminder-confirmation-email-settings.png
   :alt: Picture of Confirmation email settings page in FusionDirectory 


.. code-block:: bash

   Forward alerts to the manager : thick to send alert to manager
   Subject : subject of the e-mail
   Body (%s are cn and login) : content of the e-mail
   
Click on "ok" to save your configuration

.. image:: images/user-reminder-ok.png
   :alt: Picture of ok button in FusionDirectory 

/!\ Don't forget to add password expiration date in Unix tab. /!\    
