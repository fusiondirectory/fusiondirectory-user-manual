Audit Task Execution
====================

.. _audit-task-execution-label:

Once the task is configured, execute it using the **orchestrator-client** tool. You have two execution options:

1. **Standard Audit Deletion**:
   - Removes audit logs older than the configured retention period.
   - Example:

     .. code-block:: bash

        fusiondirectory-orchestrator-client --audit

2. **Syslog Transformation**:
   - Transforms audit logs into syslog format and appends them to a daily syslog file.
   - Example:

     .. code-block:: bash

        fusiondirectory-orchestrator-client --audit syslog

.. note::
   **Recommendation** automate this process within a CRON job.

.. note::
   Add the ``--verbose`` flag to the command for detailed output during execution.

.. note::
   The syslogs are stored at the following location:

   ``/var/log/fusiondirectory/``

