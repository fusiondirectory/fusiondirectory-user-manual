Functionalities
===============

Each task we have developed has a specific associated endpoint. Tasks are processed based on their configured schedules.

How It Works
------------

Triggering the appropriate endpoint using the allowed HTTP methods will execute the desired action.

Examples
--------

.. note::
   | An Orchestrator client is now available, allowing you to manage your recurring tasks easily within a simple CRON job.
   | Use the `--verbose` option outside of a CRON job to display the result of your command.

Get All Available Tasks
"""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --tasks

Execute a Task of Type "Mail"
"""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --emails

Execute a Task of Type "Life Cycle"
"""""""""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --lifecycle

Execute a Task of Type "Notifications"
"""""""""""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --notifications

Execute a Task of Type "Reminder"
""""""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --reminder

Activate All Cyclic Tasks
"""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --activate

Remove All Completed Sub-Tasks
""""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --remove

Execute a Task of Type "Audit"
"""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --audit

This command manages audit logs, allowing you to delete historical logs based on the retention period defined in the configuration.


.. note::
   The client can be used with the `--help` option to obtain more details about the available commands.

Conditions
----------

To process any task, the following conditions are evaluated:

- The task's schedule.
- The logic for new members.
- Specialized configuration for the task, either within the task tab itself or through its backend configuration.

.. note::
   These settings can be accessed through the **FusionDirectory Configuration Menu**.
