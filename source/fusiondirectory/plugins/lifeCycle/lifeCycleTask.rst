Life Cycle task
===============

The **Life Cycle** task manages the end of life of your accounts.
It uses the end date of a targeted Supann resource and allows for modification, prolongation, or change of state.

.. note::
   It must be used with FusionDirectory Orchestrator.

Task Setup
----------

Creating the Task
-----------------

   - Open the **Tasks** section of FusionDirectory
   - Define the task’s schedule and repetition interval.

   .. image:: images/lifeCycle-p1.png
      :alt: Life cycle - Task creation step 1
      :width: 600px

Configuring Life Cycle Task
---------------------------

There are two methods for configuring which resources to monitor:

**Method 1: Using Specific Resource States**

- **Navigate** to the **Tasks Life Cycle** tab.
- In the **Current resources details** section, select the resource, state, and (optionally) sub-state to monitor for expiration.
- In the **Future resources details** section, choose the resource, state, and (optionally) sub-state to be assigned after the expiration of the monitored resource.
- **Define** the extra days to extend the future resource's **end date**. The calculation begins from the last end date of the future resource.
- **Assign** the relevant members.

.. image:: images/lifeCycle-p2.png
  :alt: Life cycle - Task creation step 2
  :width: 600px

**Method 2: Using Regex to Define Monitored Resources**

This method is used when you want to monitor resources based on a pattern rather than a single static name.

- **Navigate** to the **Tasks Life Cycle** tab.
- In the **Current resources details** section:
    - Select ``REGEX`` for the **Resource** field. This will activate the "Regex Pattern Configuration" section.
    - Define the **State** and optionally the **Sub-state** to monitor for expiration in conjunction with the regex pattern.
- **Navigate** to the **Regex Pattern Configuration** section (which becomes active when "REGEX" is chosen above).
   - **Enter** the **Regex Pattern** to match against the names of the user's Supann resources (e.g., the part within ``{}``).
      For example:
         - Use ``^COM.*`` to match resource names starting with "COMPTE".
         - Use ``^M.*`` to match resource names starting with "MAIL".
- Configure the **Future resources details** section as described in Method 1 (defining the target resource name, its new state/sub-state, and extra days).
- **Assign** the relevant members.

.. image:: images/lifeCycle-p3.png
  :alt: Life cycle - Task configuration with Regex
  :width: 600px

.. note::
   In the above example, if either ``{COMPTE}`` or ``{MAIL}`` has expired, the task will modify either one or both of them as needed. This means that a single Life Cycle task is sufficient to handle updates for both resources, ensuring efficient resource management.

.. note::
   You can select either a **static group** or a **dynamic group** for greater flexibility.

Resource Modification Behavior
------------------------------

The Life Cycle task processes users in two main phases:

1.  **Eligibility Check:**
    For each user assigned to the task, it first checks if *any* of their Supann resources meet the expiration criteria defined in the **Current resources details** (or via the **Regex Pattern** if "Regex Pattern" is selected as the Current Resource type). If no monitored resource is found to be expired, no further action is taken for that user.

2.  **Update Execution:**
    If an expired monitored resource is found (making the user eligible), the task then determines which specific user resource(s) to update. The exact behavior depends on the combination of how the **Current resources details** (Monitored) and **Future resources details** (Target) are configured:

    *   **Scenario A: Monitored Resource = Static Name, Target Resource = Static Name**
      
        *   **Trigger:** The specific static resource defined in "Current resources details" (matching by name, state, and optionally sub-state) is found on the user and is expired.
        *   **Action:** The task looks for a user resource whose name matches the static name specified in "Future resources details".
        *   **Update:** If this target resource is found and has a valid end date:
  
            *   It **keeps its original name**.
            *   Its state and sub-state are updated to what is configured in "Future resources details".
            *   Its original end date becomes its new start date.
            *   A new end date is calculated by adding the "Extra days to add" (from "Future resources details") to this new start date.
            *   If the target resource is not found or lacks a valid end date, an error is logged.

    *   **Scenario B: Monitored Resource = Regex Pattern, Target Resource = Static Name**
    
        *   **Trigger:** *Any* user resource whose name matches the **Regex Pattern** AND whose state/sub-state match those in "Current resources details" is found and is expired.
        *   **Action:** The task looks for a user resource whose name matches the static name specified in "Future resources details".
        *   **Update:** Same as Scenario A.

    *   **Scenario C: Monitored Resource = Static Name, Target Resource = Regex Pattern**
     
        *   **Trigger:** The specific static resource defined in "Current resources details" (matching by name, state, and optionally sub-state) is found on the user and is expired.
        *   **Action:** The task looks for *all* user resources whose names match the **Regex Pattern** (specified in "Regex Pattern Configuration").
        *   **Update:** Each such found resource that has a valid end date is updated:
      
            *   It **keeps its original name**.
            *   Its state and sub-state are updated to what is configured in "Future resources details".
            *   Its original end date becomes its new start date.
            *   A new end date is calculated using "Extra days to add".
            *   Resources matching the regex but lacking a valid end date are skipped.

    *   **Scenario D: Monitored Resource = Regex Pattern, Target Resource = Regex Pattern**
     
        *   **Trigger & Action:** The task iterates through all of the user's Supann resources. If a resource:
            1.  Matches the **Regex Pattern** by name, AND
            2.  Matches the state/sub-state defined in "Current resources details", AND
            3.  Is expired.
    
        *   **Update:** *That same resource* (the one that met all trigger conditions) is updated if it has a valid end date:
    
            *   It **keeps its original name**.
            *   Its state and sub-state are updated to what is configured in "Future resources details".
            *   Its original end date becomes its new start date.
            *   A new end date is calculated using "Extra days to add".

.. tip::
   While the task allows updating resources with different names based on the expiration of another (e.g., {MAIL} expiring triggers an update to {COMPTE}), we generally recommend configuring the task so that the "Current Resource" and "Future Resource" refer to the same underlying resource name (e.g., monitor {COMPTE} to update {COMPTE}, or monitor via Regex for "XYZ" and target via Regex for "XYZ"). This ensures more predictable lifecycle management for a single resource. The flexibility for different names is available for specific advanced use cases.

.. warning::
   - The resource(s) targeted for modification **must already exist** on the user's record and **must have a valid end date** for the update to proceed. This original end date is crucial as it becomes the new start date.
   - The task modifies the state, sub-state, and dates of the targeted resource(s). The **name of the targeted resource itself is preserved**.
   - If a targeted resource is not found (in Scenarios A & B) or if it lacks a valid end date, that specific update will be skipped, and an error may be logged.

.. note::
   **Example (Illustrating Scenario A):**
  
   A user has an expired ``{MAIL}`` resource (e.g., state 'X', sub-state 'Y').
   Your task is configured with:
  
   - **Current resources details:** Resource={MAIL}, State=X, Sub-state=Y
   - **Future resources details:** Resource={COMPTE}, State=A, Sub-state=B, Extra days=30

   The task will:
 
   1. Detect the expired ``{MAIL}`` resource matching state X, sub-state Y.
   2. Find the existing ``{COMPTE}`` resource on the user.
   3. If ``{COMPTE}`` exists and has a valid end date (e.g., 20250101):
      - The ``{COMPTE}`` resource's new state becomes A, sub-state becomes B.
      - Its new start date becomes 20250101.
      - Its new end date becomes 20250101 + 30 days.
      The resource string would change from something like ``{COMPTE}Z:W:startDate:20250101`` to ``{COMPTE}A:B:20250101:newEndDate``.

Task Execution
--------------

For your configured task to be executed, you need to configure your fusiondirectory-orchestrator-client

See :ref:`Life Cycle Task Execution <lifecycle-task-execution-label>`. for more information.

Summary
-------

The **Life Cycle Task**, when configured as described, will:

- **Analyze** the Supann resources for the targeted users on a **daily basis**.
- **Check** if the configured state has expired, either using specific current resource values or regex pattern matching.
- **If expired**, update the specified future resource to the desired configuration.

.. note::
   This ensures automatic resource management and helps maintain up-to-date configurations.


