Life Cycle
==========

The **Life Cycle** task manages the end of life of your accounts.
It uses the end date of a targeted Supann resource and allows for modification, prolongation, or change of state.

.. note::
   It must be used with FusionDirectory Orchestrator.

FusionDirectory Configuration
=============================

Task Configuration
------------------

1. **Create a Task**:
   - Open the **Tasks** section and define the schedule and repetition interval for this task.

   .. image:: images/lifeCycle-p1.png
      :alt: Life cycle - Task creation step 1
      :width: 600px

2. **Life Cycle Configuration**:
   - Navigate to the **Tasks Life Cycle** tab.
   - Select the resource you wish to monitor for expiration and the desired next Supann resource.
   - Select the members. This can be a simple group or a dynamic group (allowing great flexibility).

   .. image:: images/lifeCycle-p2.png
      :alt: Life cycle - Task creation step 2
      :width: 600px

Task Execution
--------------

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

Summary
-------

This task, configured as per the example, will, on a daily basis, analyze the Supann resource for the targeted user and, if expired, change the Supann resource to the desired configuration.
