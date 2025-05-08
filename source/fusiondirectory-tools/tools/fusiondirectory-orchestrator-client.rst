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

Execute a Task of Type "Extractor"
""""""""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --extract [optional path]

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

The `--audit` option allows you to execute tasks of type "Audit". This includes two modes of operation:

1. **Standard Audit Deletion**:

   - Removes audit logs older than the configured retention period.

     .. code-block:: shell

        fusiondirectory-orchestrator-client --audit

2. **Syslog Transformation**:

   - Transforms audit logs into syslog format and appends them to a daily syslog file.

     .. code-block:: shell

        fusiondirectory-orchestrator-client --audit syslog

Execute a Task of Type "Archive"
""""""""""""""""""""""""""""""""

.. code-block:: shell

   fusiondirectory-orchestrator-client --archive

.. note::
   The client can be used with the `--help` option to obtain more details about the available commands.

Conditions
----------

To process any task, the following conditions are evaluated:

- The task's schedule set within FusionDirectory.
- Specialized configuration for the task, either within the task tab itself or through its backend configuration.
