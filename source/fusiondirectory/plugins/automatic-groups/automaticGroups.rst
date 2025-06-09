Automatic Groups task
=====================

The **Automatic Groups** task dynamically manages group memberships based on specific criteria.
It monitors users' Supann resource states and automatically adds or removes them from designated groups.

.. note::
   It must be used with FusionDirectory Orchestrator.

Task Setup
----------

Creating the Task
-----------------

   - Open the **Tasks** section of FusionDirectory
   - Define the task's schedule and repetition interval.

   .. image:: images/automaticGroups-p1.png
      :alt: Automatic Groups - Task creation step 1
      :width: 600px

Configuring Automatic Groups Task
---------------------------------

- **Navigate** to the **Tasks Automatic Groups** tab.
- **Select** the target group where users will be added or removed.
- **Choose** the resource, state, and (optionally) sub-state that users must have to be included in the group.
- **Assign** the relevant members or groups whose membership will be managed.

.. note::
   You can select either individual users or groups for processing. When groups are selected, all members will be processed individually.

   The **resource** field can also be set to a regular expression (regex). When a regex is used, any resource name matching the pattern will be taken into consideration. If members possess any of these matching resources with the specified state and sub-state, they will be added to the target group.


.. image:: images/automaticGroups-p2.png
  :alt: Automatic Groups - Task creation step 2
  :width: 600px

.. note::
   
Task Execution
--------------

For your configured task to be executed, you need to configure your fusiondirectory-orchestrator-client

Add the `--automatic-groups` parameter to your orchestrator client execution:

.. code-block:: bash

   fusiondirectory-orchestrator-client --automatic-groups

This can be scheduled via cron for regular execution.

Summary
-------

The **Automatic Groups Task**, when configured as described, will:

- **Process** each user from the selected members list.
- **Check** if they meet the specified Supann resource state criteria.
- **Add** users to the target group if they match the criteria.
- **Remove** users from the target group if they no longer match the criteria.

.. note::
   This ensures group memberships are always in sync with users' current states, automating what would otherwise be a manual administrative task.


