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

See :ref:`Audit Task Execution <audit-task-execution-label>`. for more information.

