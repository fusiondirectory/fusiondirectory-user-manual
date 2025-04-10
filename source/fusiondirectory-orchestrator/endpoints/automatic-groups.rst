Automatic Groups Task Execution
===============================

.. _automatic-groups-task-execution-label:

Once the automatic groups task is configured in FusionDirectory, execute it using the **fusiondirectory-orchestrator-client** tool:

.. code-block:: bash

   fusiondirectory-orchestrator-client --automatic-groups

.. note::
   **Recommendation**: Automate this process within a CRON job to ensure group memberships are regularly updated.

.. note::
   Add the ``--verbose`` flag to the command for detailed output during execution.

How It Works
------------

When the automatic groups task executes:

1. The system identifies all users specified in the task configuration (either directly or through group membership)
2. For each user, it checks their Supann resource state against the criteria defined in the task
3. Users who match the criteria are added to the target group
4. Users who no longer match the criteria are removed from the target group

This ensures that group memberships remain synchronized with the current state of users in your directory.

Examples
--------

Basic Execution
^^^^^^^^^^^^^^^

.. code-block:: bash

   fusiondirectory-orchestrator-client --automatic-groups

With Verbose Output
^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

   fusiondirectory-orchestrator-client --automatic-groups --verbose