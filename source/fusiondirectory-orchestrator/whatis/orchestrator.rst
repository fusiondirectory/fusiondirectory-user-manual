What is FusionDirectory Orchestrator ?
======================================

FusionDirectory Orchestrator is a RESTful web service using JWT authentication, designed to manage and execute tasks efficiently.

It supports multiple endpoints with plugin integration for custom processing or specialized tasks.

Tasks are defined within FusionDirectory, with a client available to query endpoints and manage workflows.

Common tasks include account lifecycle, notifications, reminders, mail automation, audit log management, and more.

Features
^^^^^^^^

- Tasks management.
- Tasks execution.
- Workflow management.
- JWT Authentication methods


Tasks management
^^^^^^^^^^^^^^^^

FusionDirectory Orchestrator REST API provides seamless management and retrieval of tasks created within FusionDirectory.
It offers a clear and concise view of the status of each task, including subtasks, allowing for detailed tracking and reporting.

With its extensible design, the Orchestrator supports specialized tasks such as mail automation, notifications, reminders,
account lifecycle management, and audit log processing, enabling tailored workflows to meet diverse needs

Tasks Execution
^^^^^^^^^^^^^^^^

One of the core functionalities of the **FusionDirectory Orchestrator** is the execution and processing of various tasks as defined within FusionDirectory.

- **Mail Tasks**:
  When triggered, tasks of type "Mail" will automatically send the relevant emails if the scheduled conditions are met, ensuring timely communication.

- **Life Cycle Tasks**:
  These tasks are responsible for updating specialized attributes, such as *supann* attributes, in accordance with defined lifecycle processes.

- **Notification Tasks**:
  When attributes are modified, "Notification" tasks will send automated email alerts to keep users informed of changes.

- **Reminder Tasks**:
  These tasks send reminders to users, potentially including links to extend or prolong their account, ensuring critical actions are not missed.

- **Audit Tasks**:
  Tasks of this type allow for the management of audit logs, including the deletion of logs based on configurable retention policies, ensuring compliance and data management.

The **Orchestrator client** provides a user-friendly interface to activate and manage these tasks, allowing for seamless workflow execution and efficient task orchestration across the system.

JWT authentication
^^^^^^^^^^^^^^^^^^

| It was decided to enhance our authentication mechanism and use the JWT methodology.
| Allowing after proper username/password authentication the reception of an access and refresh token.

The access token is to be used for any operations on FusionDirectory Orchestrator endpoints. 


