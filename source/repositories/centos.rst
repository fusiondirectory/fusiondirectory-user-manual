.. _fd-rpm-repository-label:

RPM Repository
''''''''''''''

To install FusionDirectory on Centos 7 you will need to add 3 yum repositories

.. _fd-rpm-repository-centos7-label:

CentOS 7 / RHEL 7
^^^^^^^^^^^^^^^^^

Add a file named **fusiondirectory-release.repo** in /etc/yum.repos.d/

.. code-block:: shell

  [fusiondirectory-release]
  name=Fusiondirectory Packages for CentOS 7
  baseurl=https://public.fusiondirectory.org/centos7-fusiondirectory-release/RPMS
  enabled=1
  gpgcheck=1
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

Add a file named **fusiondirectory-schema2ldif-release.repo** in /etc/yum.repos.d/

.. code-block:: shell

   [fusiondirectory-schema2ldif-release]
   name=Fusiondirectory Packages for CentOS 7
   baseurl=https://public.fusiondirectory.org/centos7-schema2ldif-release/RPMS
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

Add a file named **fusiondirectory-extra.repo** in /etc/yum.repos.d/

.. code-block:: shell

   [fusiondirectory-extra]
   name=Fusiondirectory Packages for CentOS 7
   baseurl=https://public.fusiondirectory.org/centos7-fusiondirectory-extra/RPMS
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY




