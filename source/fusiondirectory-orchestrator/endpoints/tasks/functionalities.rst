
Functionalities
===============

| E-mails are being sent based on the schedule of the processed task.

How it works
------------

Asking the proper endpoints with the allowed HTTP methods will trigger the required action.

Examples
--------

.. note::

  | An orchestrator client is being developped in order to automate some of the below examples.
  | It will allow easier management of repeated tasks within a CRON job.


Get access-token
""""""""""""""""

.. code-block:: shell

   # Login and get access-token
   curl -X POST -H "Content-Type: application/json" https://example.org/orchestrator/api/login -d '{"username":"admin","password":"secret"}'

Get all mail tasks
""""""""""""""""""

.. code-block:: shell

   # Get all mail tasks using the access-token
   curl -X GET -H "Content-Type: application/json" -H "Authorization: Bearer {token}"  https://example.org/orchestrator/api/tasks/mail

Send e-mails
""""""""""""

.. code-block:: shell

   # Login and get access-token
   curl -X PATCH -H "Content-Type: application/json" -H "Authorization: Bearer {token}"  https://example.org/orchestrator/api/tasks/mail

Refresh access token
""""""""""""""""""""

.. code-block:: shell

    # Refresh access token with refresh token
    curl -X POST -H "Content-Type: application/json" http://192.168.1.100:8080/orchestrator/api/refresh -d '{"token":"refresh-token"}'

Conditions
----------

In order to process mail tasks, a few conditions are analysed:

- Schedule for the tasks.
- A max-emails threshold to be sent.
- A time interval between mail tasks processing.

.. note::
   The settings for above conditions are found within FusionDirectory configuration menu.
