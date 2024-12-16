Reminder Task
=============

The **Reminder Task** manages account expiry notifications by monitoring the end date of a specified Supann resource. It sends an email to the affected users, potentially including a link to extend their account validity.

.. note::
   This task must be used with **FusionDirectory Orchestrator** to function properly.

FusionDirectory Configuration
=============================

Task Setup
----------

Creating the Task
-----------------

- Open the **Tasks** section in FusionDirectory.
- Define the task’s schedule and repetition interval.

   .. image:: images/user-reminder-task-p1.png
      :alt: Reminder Task - Step 1: Task creation
      :width: 600px
      :align: center

Configuring the Life Cycle
--------------------------

- Go to the **Tasks Reminder** tab.
- Select the resource to monitor for expiration. You can also define the desired next Supann resource for cases where prolongation is enabled.

  - **Tip**: You can choose an alternate targeted resource for specific or edge-case scenarios.
- Assign members to the task. This can be:

  - A **simple group**.
  - A **dynamic group**, offering flexibility for user management.

   .. image:: images/user-reminder-task-p2.png
      :alt: Reminder Task - Step 2: Life cycle configuration
      :width: 600px
      :align: center

Task Execution
--------------

Once the task is configured, execute it using the **orchestrator-client** tool. You have two execution options:

Automated Execution via Cron
----------------------------

To automate the task, set up a cron job with the following command:

.. code-block:: bash

   fusiondirectory-orchestrator-client --reminder

Manual Execution
----------------

If needed, you can manually run the task with the same command:

.. code-block:: bash

   fusiondirectory-orchestrator-client --reminder

   .. note::
      Add the ``--verbose`` flag to the command for detailed output during execution.

Audit Logs
----------

By default, all task-related activities are logged at the following location:

``/var/log/orchestrator/orchestrator.log``

.. note::
   Regularly review audit logs to verify that the task is functioning as expected and ensure compliance with your organization’s policies.

Summary
-------

The **Reminder Task**, when configured as described, will:

- Run daily (or according to your configured schedule).
- Analyze the Supann resource for targeted users.
- Send expiry notifications to:

  - The affected users.
  - Any recipients listed in the **forward-to** list.

By ensuring timely reminders, this task helps maintain active user accounts while offering the flexibility to handle specific organizational needs.
