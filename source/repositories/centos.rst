.. _fd-rpm-repository-label:

RPM Repository
''''''''''''''

First add the FusionDirectory tools and libraries repositories

Add a file named **fusiondirectory-integrator.repo** in /etc/yum.repos.d/

.. code-block:: shell

   [fusiondirectory-integrator]
   name=Fusiondirectory Integrator Packages for CentOS 7
   baseurl=https://public.fusiondirectory.org/centos/fusiondirectory-integrator/RPMS
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

Add a file named **fusiondirectory-tools.repo** in /etc/yum.repos.d/

.. code-block:: shell

   [fusiondirectory-tools]
   name=Fusiondirectory Utilities Packages for CentOS 7
   baseurl=https://public.fusiondirectory.org/centos/fusiondirectory-tools/RPMS
   enabled=1 
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

Add a file named **fusiondirectory-external-libraries.repo** in /etc/yum.repos.d/

.. code-block:: shell

   [fusiondirectory-external-libraries]
   name=Fusiondirectory External Libraries Packages for CentOS 7
   baseurl=https://public.fusiondirectory.org/centos/fusiondirectory-external-libraries/RPMS
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

CentOS 7
^^^^^^^^

Add a file named **fusiondirectory-release.repo** in /etc/yum.repos.d/

.. code-block:: shell

  [fusiondirectory-release]
  name=Fusiondirectory Packages for CentOS 7
  baseurl=https://public.fusiondirectory.org/centos/centos7-fusiondirectory-release/RPMS
  enabled=1
  gpgcheck=1
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

To install FusionDirectory Orchestrator

Add a file named **fusiondirectory-orchestrator-release.repo** in /etc/yum.repos.d/

.. code-block:: shell

  [fusiondirectory-orchestrator-release]
  name=Fusiondirectory Packages for CentOS 7
  baseurl=https://public.fusiondirectory.org/centos/centos7-fusiondirectory-orchestrator-release/RPMS
  enabled=1
  gpgcheck=1
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY
