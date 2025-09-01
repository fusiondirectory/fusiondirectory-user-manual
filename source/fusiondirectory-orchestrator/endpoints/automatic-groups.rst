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

Examples
--------

Standard Group Assignment
^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

   fusiondirectory-orchestrator-client --automatic-groups

Dynamic Group Creation
^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

   fusiondirectory-orchestrator-client --automatic-groups dynamic-group

With Verbose Output
^^^^^^^^^^^^^^^^^^^

.. code-block:: bash

   fusiondirectory-orchestrator-client --automatic-groups --verbose
   fusiondirectory-orchestrator-client --automatic-groups dynamic-group --verbose