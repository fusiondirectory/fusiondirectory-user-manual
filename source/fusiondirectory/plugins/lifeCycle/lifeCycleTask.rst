Life Cycle
==========

The **Life Cycle** task manages the end of life of your accounts.
It uses the end date of a targeted Supann resource and allows for modification, prolongation, or change of state.

.. note::
   It must be used with FusionDirectory Orchestrator.

FusionDirectory Configuration
-----------------------------

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

For your configured task to be executed, you need to configure your fusiondirectory-orchestrator-client

See :ref:`Life Cycle Task Execution <lifecycle-task-execution-label>`. for more information.

Summary
-------

This task, configured as per the example, will, on a daily basis, analyze the Supann resource for the targeted user and, if expired, change the Supann resource to the desired configuration.
