Notifications
=============

The **Notification** task allows you to defined specific attributes you wish to monitor.
If a modification (not a creation), happens to the selected attribute, a notification via email can be send.

Notifications also allows to monitor supann resource.
The supan resource targeted is configurable and a notification will be sent when the supann resource is **entering that specific**
state.

.. note::
   It must be used with FusionDirectory Orchestrator.

FusionDirectory Configuration
=============================

Task Configuration
------------------

1. **Create a Task**:
   - Open the **Tasks** section and define the schedule and repetition interval for this task.

   .. image:: images/notifications-t1.png
      :alt: Life cycle - Task creation step 1
      :width: 600px

2. **Notifications Configuration**:
   - Navigate to the **Tasks Notifications** tab.
   - Select attributes you want to monitor, the list is configurable via the configuration menu / notifications.
   - Select the members. This can be a simple group or a dynamic group (allowing great flexibility).

   .. image:: images/notifications-t2.png
      :alt: Life cycle - Task creation step 2
      :width: 600px

Task Execution
--------------

For your configured task to be executed, you need to configure your fusiondirectory-orchestrator-client

See :ref:`Notifications Task Execution <notifications-task-execution-label>`. for more information.

.. important::
   Notifications relies on the last executable date.
   When running the task for the first time, no previous executable date exists.
   As a protective measure, you must execute the task manually once to create an
   initial "last execute" timestamp. This timestamp will serve as the basis for
   triggering notifications in subsequent executions.


Summary
-------

This task, configured as per the example, will, on a hourly basis, analyze the monitored attributes or supan states for
selected members and offer a notification mechanism based on above preset.