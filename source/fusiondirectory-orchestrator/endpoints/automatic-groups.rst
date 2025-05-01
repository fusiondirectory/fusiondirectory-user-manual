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

Task Types
----------

The automatic groups task supports two operating modes:

1. **Standard Group Assignment**: Adds or removes users from an existing group based on their Supann resource state criteria
2. **Dynamic Group Creation**: Creates a dynamic group with a memberURL filter matching the specified Supann resource state

How It Works
------------

Standard Group Assignment
^^^^^^^^^^^^^^^^^^^^^^^^^

When the standard automatic groups task executes:

1. The system identifies all users specified in the task configuration (either directly or through group membership)
2. For each user, it checks their Supann resource state against the criteria defined in the task
3. Users who match the criteria are added to the target group
4. Users who no longer match the criteria are removed from the target group

This ensures that group memberships remain synchronized with the current state of users in your directory.

Dynamic Group Creation
^^^^^^^^^^^^^^^^^^^^^^

When the dynamic group creation task executes:

1. The system generates a dynamic group name based on the resource, state, and optional substate
2. It builds an LDAP URL with a filter for the specified Supann resource state criteria
3. It creates a new dynamic group with the generated name and LDAP URL filter
4. If a group with the same name already exists, the task succeeds without modifying the existing group

The resulting dynamic group will automatically include all users whose Supann resource state matches the specified criteria, using LDAP's dynamic membership capabilities.

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

Dynamic Group Structure
-----------------------

Dynamic groups created by this task have the following structure:

- **Name Pattern**: dynamic-{resource}-{state}[-{substate}] (always lowercase)
- **LDAP URL**: ldap:///ou=people,{base_dn}??one?(supannRessourceEtat={resource}{state}[:substate])

For example, a dynamic group for resource "COMPTE" with state "A" would be:
- Name: dynamic-compte-a
- LDAP URL: ldap:///ou=people,dc=example,dc=com??one?(supannRessourceEtat={COMPTE}A)