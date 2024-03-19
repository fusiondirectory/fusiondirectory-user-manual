
Functionalities
===============

| Tasks are being processed based on their set schedule.
| Two official tasks exists in CORE : "Mail" and "LifeCycle"

How it works
------------

Asking the proper endpoints with the allowed HTTP methods will trigger the required action.

Examples
--------

.. note::

  | An orchestrator client is now available, you may now manage your repeated tasks within a simple CRON job.
  | Use option -v (--verbose) outside a CRON job to output the result of your command.

Get all tasks available
"""""""""""""""""""""""

.. code-block:: shell

  fusiondirectory-orchestrator-client -t (--tasks)


Execute a task of type "Mail"
"""""""""""""""""""""""""""""

.. code-block:: shell

  fusiondirectory-orchestrator-client -m (--emails)

Execute a task of type "Life Cycle"
"""""""""""""""""""""""""""""""""""

.. code-block:: shell

  fusiondirectory-orchestrator-client -c (--lifeCycle)

Activate all cyclic tasks
"""""""""""""""""""""""""

.. code-block:: shell

  fusiondirectory-orchestrator-client -a (--activateCyclicTasks)

Remove all completed sub-tasks
""""""""""""""""""""""""""""""

.. code-block:: shell

  fusiondirectory-orchestrator-client -r (--remove)

.. note::

  | The client can be used with option -h (--help) in order to have more details on some commands.

Conditions
----------

In order to process any tasks, a few conditions are analysed:

- Schedule for the tasks.
- New members logic.
- Specialized configuration for the task at hand, either in the task tab itself or within its backend configuration.

.. note::
   The settings for above conditions may be found within FusionDirectory configuration menu.
