Audit Task
==========

The **Audit** task helps in managing the backlog of audit logs, freeing up disk space and improving performance by removing logs older than the configured retention period.

.. NOTE::
  It must be used with FusionDirectory Orchestrator

Task Setup
----------

Creating the Task
-----------------

   - Open the **Tasks** section in FusionDirectory
   - Define the task’s schedule and repetition interval.

   .. image:: images/audit_t1.png
      :alt: Audit - Task creation step 1
      :width: 600px

Configuring Audit Task
----------------------

- Go to the Tasks Audit tab.
- Configure the desired time retention settings in days, and then click **Save**.

   .. image:: images/audit_t2.png
      :alt: Audit - Task creation step 2
      :width: 600px


Task Execution
--------------


For your configured task to executed, you need to configure your fusiondirectory-orchestrator-client

See :ref:`Audit Task Execution <audit-task-execution-label>`. for more information.

Summary
-------

The **Audit Task**, when configured as described, will:

 - Automatically remove all audits that have exceeded the yearly retention period.
 - Ensure compliance and efficient data management on an annual basis.