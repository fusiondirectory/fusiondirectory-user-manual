Installing Dependencies
'''''''''''''''''''''''

Argonaut requires the `EPEL`_ repository 

-  To install epel

.. code-block:: shell

   yum install epel-release
   
Install the FusionDirectory Repos
'''''''''''''''''''''''''''''''''

To easily install the latest version, you can install the fusion
directory repos

Chose the repositories that goes with your centos version

:ref:`rpm-repository-centos7-label`

Create 2 new repo file your favorite text editor.

- One for argonaut
- One for argonaut-extra

Install Argonaut
''''''''''''''''

You can then install Argonaut by running: 

.. code-block:: shell

   yum install -y argonaut-common

.. _EPEL : https://fedoraproject.org/wiki/EPEL


