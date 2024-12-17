Audit Task
==========

The **Audit** task helps in managing the backlog of audit logs, freeing up disk space and improving performance by removing logs older than the configured retention period.

.. NOTE::
  It must be used with FusionDirectory Orchestrator

FusionDirectory Configuration
=============================

Task Configuration
------------------

1. **Create a Task**:
   - Open the **Tasks** section and define the schedule and repetition interval for this task.

   .. image:: images/audit_t1.png
      :alt: Audit - Task creation step 1
      :width: 600px


2. **Set Audit Retention Period**:
   - Navigate to the **Audit** tab, configure the desired time retention settings in days, and then click **Save**.

   .. image:: images/audit_t2.png
      :alt: Audit - Task creation step 2
      :width: 600px


Task Execution
--------------


For your configured task to executed, you need to configure your fusiondirectory-orchestrator-client

Read the FusionDirectory Audit Orchestrator Documentation

See  :ref:`audit-task-execution-label` for more information.


Once the task is configured, it will automatically delete audit logs based on the set retention period. The task can be executed in the following ways:

1. **Automated Execution via Cron Job**:
   - To automate this task, you can set up a cron job with the following command:

     .. code-block:: bash

        fusiondirectory-orchestrator-client --audit

2. **Manual Execution**:
   - Alternatively, you can manually execute the task whenever needed using the same command.

.. note::
    By default, the command does not provide output unless the ``--verbose`` flag is specified.

.. note::
    The audit logs are stored by default at the following location:

    ``/var/log/orchestrator/orchestrator.log``

Summary
-------

This task, based on the example above, will annually remove audit logs older than the configured retention period, ensuring better system performance and available disk space.
