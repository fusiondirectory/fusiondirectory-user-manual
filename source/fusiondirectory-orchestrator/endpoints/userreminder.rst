Reminder Task Execution
=======================

.. _reminder-task-execution-label:

Once the task is configured, execute it using the **orchestrator-client** tool. You have two execution options:

.. code-block:: bash

   fusiondirectory-orchestrator-client --reminder

.. note::
   **Recommendation** automate this process within a CRON job.

.. note::
  Add the ``--verbose`` flag to the command for detailed output during execution.


.. note::
    The logs are stored by default at the following location:

    ``/var/log/orchestrator/orchestrator.log``

