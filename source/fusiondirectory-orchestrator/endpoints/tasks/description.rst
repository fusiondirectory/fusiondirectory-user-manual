Description
===========

Tasks is an endpoints of Orchestrator.

.. note::
  It is reachable via **https://your_fqdn/api/tasks/**

Arguments
---------

- Mail 

You can :
 - Retrieve all tasks of type mail.
 - Process all tasks of type mail and forward the related e-mails.

- lifeCycle

You can :
 - Retrieve all tasks of type "life cycle".
 - Process all tasks of type "life cycle" and updates the related configured attributes.

- activateCyclicTasks

You can :
 - Activate all repetitive tasks based on their redundancy schedule.

- removeSubTasks

You can :
 - It will simply remove the all sub-tasks which are set to be completed.
