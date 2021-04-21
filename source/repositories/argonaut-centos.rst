.. _ar-rpm-repository-label:

RPM Repository
''''''''''''''

To install Argonaut on Centos 7 you will need to add 2 yum repositories

.. _ar-rpm-repository-centos7-label:

CentOS 7 / RHEL 7
^^^^^^^^^^^^^^^^^

Add a file named **argonaut-release.repo** in /etc/yum.repos.d/

.. code-block:: shell

  [argonaut-release]
  name=Argonaut Packages for CentOS 7
  baseurl=https://public.fusiondirectory.org/centos7-argonaut-release/RPMS
  enabled=1
  gpgcheck=1
  gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY

Add a file named **argonaut-extra.repo** in /etc/yum.repos.d/

.. code-block:: shell

   [argonaut-extra]
   name=Argonaut Extra Packages for CentOS 7
   baseurl=https://public.fusiondirectory.org/centos7-argonaut-extra/RPMS
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY




