.. _sl-rpm-repository-label:

RPM Repository
''''''''''''''

To install Schema2ldif on Centos 7 you will need to add 1 yum repository

.. _sl-rpm-repository-centos7-label:

CentOS 7 / RHEL 7
^^^^^^^^^^^^^^^^^

Add a file named **fusiondirectory-schema2ldif-release.repo** in /etc/yum.repos.d/

.. code-block:: shell

   [fusiondirectory-schema2ldif-release]
   name=Fusiondirectory Packages for CentOS 7
   baseurl=https://public.fusiondirectory.org/centos7-schema2ldif-release/RPMS
   enabled=1
   gpgcheck=1
   gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-FUSIONDIRECTORY





