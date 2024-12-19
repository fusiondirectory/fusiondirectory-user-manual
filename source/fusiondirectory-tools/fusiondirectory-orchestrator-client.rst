Fusiondirectory-orchestrator-client
===================================

How It Works
------------

This client has been developed to automate the entire task management process, enabling granular control over task execution and providing optional log status tracking.

Examples
--------

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
""""""""""""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --notifications

Execute a Task of Type "Reminder"
"""""""""""""""""""""""""""""""""

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
""""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --audit

.. note::
   The client can be used with the `--help` option to obtain more details about the available commands.

Conditions
----------

To process any task, the following conditions are evaluated:

- The task's schedule set within FusionDirectory.
- Specialized configuration for the task, either within the task tab itself or through its backend configuration.
