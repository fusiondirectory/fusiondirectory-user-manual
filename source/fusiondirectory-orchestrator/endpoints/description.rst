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

- **tasks/removeSubTasks**
   Removes all sub-tasks marked as completed.
   All sub-tasks status can be seen within FusionDirectory dashboard.

