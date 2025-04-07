Extractor Task Execution
========================

.. _extractor-task-execution-label:

Once the task is configured, execute it using the **fusiondirectory-orchestrator-client** tool. You have two execution options:

.. code-block:: bash

   fusiondirectory-orchestrator-client --extract

.. note::
   **Recommendation** automate this process within a CRON job.

.. note::
   Add the ``--verbose`` flag to the command for detailed output during execution.

.. note::
   The logs are stored by default at the following location:

   ``/srv/orchestrator/``

.. note::
   You can specify a custom path for the extracted files by adding a directory path to the ``--extract`` option. For example:

   .. code-block:: bash

      fusiondirectory-orchestrator-client --extract /var/log/

   This will save the generated files in the specified directory instead of the default location.

File Naming Format
------------------

The generated files follow a specific naming convention to ensure clarity and avoid duplication:

``NameOfTheTask-date+hour.format``

- **NameOfTheTask**: The name you assigned to the task.
- **date**: The current date in `YYYYMMDD` format (e.g., `20250407` for April 7, 2025).
- **hour**: The hour of execution in `HH` format (e.g., `14` for 2 PM).
- **format**: The output format, such as `csv`.

For example, a task named `UserExport` executed on April 7, 2025, at 2 PM will generate a file named:

``UserExport-20250407-14.csv``