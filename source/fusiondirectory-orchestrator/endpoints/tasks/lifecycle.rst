Life Cycle - Task Execution
===========================

 .. _lifecycle-task-execution-label:

Once the task is configured, you can execute the orchestrator-client with the options below.

1. **Automated Execution via Cron Job**:
   - To automate this task, set up a cron job with the following command:

     .. code-block:: bash

        fusiondirectory-orchestrator-client --lifecycle

2. **Manual Execution**:
   - Alternatively, you can manually execute the task whenever needed using the same command.

.. note::
   By default, the command does not provide output unless the ``--verbose`` flag is specified.

.. note::
   The audit logs are stored by default at the following location:

   ``/var/log/orchestrator/orchestrator.log``