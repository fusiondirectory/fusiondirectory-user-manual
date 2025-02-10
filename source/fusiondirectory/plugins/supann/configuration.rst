Configuration
=============

SupAnn standard (2020) documentation can be found `here <https://services.renater.fr/documentation/supann/supann2020/recommandations2020/index>`_.

Additionally, the SupAnn standard specifies how to fill the `cn` attribute: `SupAnn CN Attribute Documentation <https://services.renater.fr/documentation/supann/supann2018/recommandations2018/attributs/cn>`_.

You can modify how FusionDirectory renders the `CN` attribute by adjusting the **CN Pattern** in the configuration backend.
For more details, refer to :ref:`configuration_people_and_group_storage`.

Default CN Pattern
------------------

The default pattern is:

.. code-block:: text

   %t[fr_FR]|sn% %t[fr_FR]|givenName%

This pattern determines how the `cn` attribute is structured within FusionDirectory.


Configure SupAnn Status
^^^^^^^^^^^^^^^^^^^^^^^

To configure the SupAnn status in FusionDirectory, follow these steps:

1. Click on the **Configuration** icon on the FusionDirectory main page.

   .. image:: images/supann-configuration-icon-main.png
      :alt: Configuration icon in FusionDirectory

2. Navigate to the **SupAnn** tab.

   .. image:: images/supann-tab.png
      :alt: SupAnn tab in FusionDirectory

3. Click the **Edit** button at the bottom right.

   .. image:: images/supann-edit-button.png
      :alt: Edit button in FusionDirectory

4. The SupAnn configuration menu will appear:

   .. image:: images/supann-configuration-menu_1.png
      :alt: SupAnn configuration menu in FusionDirectory

- **SupAnn RDN**: Specifies the branch where SupAnn structures will be stored (required).
- **SupAnn mail for recovery**: Allows password recovery using email addresses from the personal mail field in a SupAnn account.
- **Custom resources**: Defines custom resources and their labels.

   .. image:: images/supann-configuration-menu_2.png
      :alt: SupAnn configuration menu continuation in FusionDirectory

**In order to configure a new resource**
1. Fill in the appropriate fields as shown below.
2. Click **Add**.

   .. image:: images/supann-example-library.png
      :alt: Example of resource label configuration in FusionDirectory

- **Substates**: Specifies the allowed substates for an account. There are three types:
  - Active
  - Inactive
  - Suspended
- **Custom labels**: Defines labels for custom substates.

#### Example: Adding a "Lost" Substate

To add the substate **Perdu** (Lost) under the "Library" resource:

   .. image:: images/supann-example-substatus.png
      :alt: Example of substatus label configuration in FusionDirectory

### Finalizing the Configuration

Once all settings are configured, click **OK** at the bottom right.

   .. image:: images/supann-configuration-menu_3.png
      :alt: SupAnn configuration menu continuation in FusionDirectory

- **SupAnn RDN**: Specifies the branch where SupAnn structures will be stored (required).
- **SupAnn mail for recovery**: Allows password recovery using email addresses from the personal mail field in a SupAnn account.
- **Custom resources**: Defines custom resources and their labels.

   .. image:: images/supann-configuration-menu_4.png
      :alt: SupAnn configuration menu continuation in FusionDirectory

---

Configure Multiservice Card
^^^^^^^^^^^^^^^^^^^^^^^^^^^

The **Multiservice Card** settings allow configuration of various card-related parameters. Below is an overview:

   .. image:: images/supann-multiservice-card-settings_1.png
      :alt: Multiservice Card settings in FusionDirectory

   .. image:: images/supann-multiservice-card-settings_2.png
      :alt: Multiservice Card settings continuation in FusionDirectory

### Configuration Options

- **Card types**: Defines available card types and their labels. Prefix non-standard types with `{ORIGIN}`.
- **Card sources**: Specifies possible sources for multiservice cards, using the format `system@domain`.
- **Card formats**: Lists allowed formats for multiservice cards.
- **Card application domains**: Defines the domains in which card applications are valid.

This concludes the configuration guide for SupAnn and Multiservice Cards in FusionDirectory.

