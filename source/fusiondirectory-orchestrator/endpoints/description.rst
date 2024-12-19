Description
===========

FusionDirectory Orchestrator provides a primary endpoint, referred to as **tasks**, which accepts multiple arguments for execution.
New task objects can be added as plugins and invoked as arguments to this endpoint.

.. note::
   The **tasks** endpoint is accessible via **https://your_fqdn/api/tasks/**.

Arguments
---------

The **tasks** endpoint supports multiple arguments. Below is a list of the officially supported arguments:

.. note::
   Each official plugin within **tasks** can be passed as an argument to the **tasks** endpoint. Additionally, a client is available within **FusionDirectory-Tools** to simplify interactions.

- **login**
   This endpoint facilitates authentication and provides the access and refresh tokens required for further communication with subsequent endpoints.

- **tasks/mail**
   Invoking this endpoint triggers the execution of mail task objects defined within **FusionDirectory**.
   It processes the results from the mail server and reports the status to the associated tasks.

- **tasks/lifeCycle**
   This endpoint executes lifecycle task objects defined within **FusionDirectory**. Based on task configuration, it evaluates whether a specified Supann resource has reached expiration and performs actions accordingly.

- **tasks/activateCyclicTasks**
   Activates all repetitive tasks based on their defined recurrence schedules.

- **tasks/removeSubTasks**
   Removes all sub-tasks marked as completed.
   All sub-tasks status can be seen within FusionDirectory dashboard.

- **tasks/reminder**
   Executes reminder task objects and sends emails to specified groups or individuals. Based on configuration, it can generate tokens for potential account extensions.

- **tasks/notifications**
   Triggers the execution of notification task objects. Any changes to the supplied attributes result in email notifications being sent to the designated individuals or groups.

- **tasks/audit**
   This endpoint allows for the deletion of historical audit logs based on a retention period specified in the task configuration within **FusionDirectory**.
