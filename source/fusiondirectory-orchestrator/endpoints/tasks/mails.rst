Mail Task Execution
===================

.. _mail-task-execution-label:

Once the task is configured, execute it using the **orchestrator-client** tool. You have two execution options:

Automated Execution via Cron
----------------------------

To automate the task, set up a cron job with the following command:

.. code-block:: bash

   fusiondirectory-orchestrator-client --emails

Manual Execution
----------------

If needed, you can manually run the task with the same command:

.. note::
  Add the ``--verbose`` flag to the command for detailed output during execution.


.. note::
    The logs are stored by default at the following location:

    ``/var/log/orchestrator/orchestrator.log``