.. include:: ../../globals.rst

Functionalities
===============

Create a subnet
^^^^^^^^^^^^^^^

Click on Ipam icon in FusionDirectory 

.. image:: images/ipam-icon-main.png
   :alt: Picture of Ipam icon in FusionDirectory

On Ipam main page, click on Actions --> Create --> Subnet

.. image:: images/ipam-action-create-subnet.png
   :alt: Picture of Action Create subnet menu in FusionDirectory

This will bring you to subnet configuration page     

.. image:: images/ipam-subnet-configuration-page.png
   :alt: Picture of subnet configuration page in FusionDirectory  
   
Fill-in the following fields :

* **Base** : object base
* **Name** : subnet name (required)
* **Description** : description of this subnet
* **Active** : is the subnet active (required)
* **Organization** : organization who asked for the subnet
* **Type** : subnet type (lan, wan, wifi)
* **Applicant** : name of the person who asked for the subnet
* **Allocation date** : start allocation
* **Release date** : end allocation date   
* **VLANs** : VLANs linked to this subnet
* **IP** : subnet IP
* **Netmask** : subnet netmask
* **Gateway** : gateway IP
* **Broadcast** : Broadcast IP


.. note::

   You can attach multiple VLANs to a subnet.
      

Example of Subnet
^^^^^^^^^^^^^^^^^

.. image:: images/ipam-subnet-example.png
   :alt: Picture of Subnet configuration page in FusionDirectory


When you are done, click on Apply button bottom right to save your subnet     

.. image:: images/ipam-apply-button.png
   :alt: Picture of Apply button in FusionDirectory 

Then, click on OK button. This will bring you back to Ipam main page

.. image:: images/ipam-ok-button.png
   :alt: Picture of OK button in FusionDirectory
   
You can now see you just created subnet in the list

.. image:: images/ipam-subnet-line.png
   :alt: Picture of Ipam subnet line in FusionDirectory
   
Create a VLAN
^^^^^^^^^^^^^

On Ipam main page, click on Actions --> Create --> VLAN

.. image:: images/ipam-action-create-vlan.png
   :alt: Picture of Action Create vlan menu in FusionDirectory

This will bring you to VLAN configuration page     

.. image:: images/ipam-vlan-configuration-page.png
   :alt: Picture of vlan configuration page in FusionDirectory
   
Fill-in the following fields :

* **Base** : object base      
* **Name** : subnet name (required)
* **Description** : description of this vlan
* **Active** : is this subnet active (required)
* **Organization** : organization who asked for the subnet
* **Inner ID** : inner VLAN ID (required)
* **QinQ ID** : QinQ ID VLAN ID
* **Applicant** : name of the person who asked for the subnet

Example of VLAN
^^^^^^^^^^^^^^^

.. image:: images/ipam-vlan-example.png
   :alt: Picture of VLAN configuration page in FusionDirectory

When you are done, click on Apply button bottom right to save your vlan

.. image:: images/ipam-apply-button.png
   :alt: Picture of Apply button in FusionDirectory 

Then, click on OK button. This will bring you back to Ipam main page

.. image:: images/ipam-ok-button.png
   :alt: Picture of OK button in FusionDirectory
   
You can now see you just created vlan in the list

.. image:: images/ipam-subnet-line.png
   :alt: Picture of Ipam subnet line in FusionDirectory
   
* VLAN section when creating  `Systems <https://fusiondirectory-user-manual.readthedocs.io/en/1.4/plugins/systems/index.html>`_

Note that when you create a system in "Systems" section, additional IPAM fiends will appear and need to be filled :

.. image:: images/ipam-interfaces-configuration-page.png
   :alt: Picture of Ipam interface configuration menu in FusionDirectory
   
* **VLAN** : if you select a vlan, the network subnet will be restricted to the vlan contained in this subnet
* **Add free IP from subnet** : the ADD IP button allows you to automatically add a free ip in the subnet selected
