
Functionalities
===============

schema2ldif <options> <FILE> > file.ldif

How it works
------------

convert a schema :
^^^^^^^^^^^^^^^^^^

.. code-block:: shell

   schema2ldif cosine.schema > cosine.ldif

the name of the file (without extension) will be used as cn.

options :
^^^^^^^^^

-c

Use CN as cn for the schema (mandatory if no file provided)

-b

Use BRANCH instead of cn=schema,cn=config

.. note::

   If <FILE> is not provided, it will read from standard input. 
   In this case, the -c option is mandatory.
