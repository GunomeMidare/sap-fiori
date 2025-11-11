## SAP Fiori Tasklists 📝

### General
SAP advices to run certain checklists again after upgrades:
- [2902673 - Rapid Activation for SAP Fiori in SAP S/4HANA - Overview](https://me.sap.com/notes/2902673)
- [2886433 - Fiori Setup: Activation of OData Services in Prod Systems with task lists](https://me.sap.com/notes/2886433/E)
- [3452535 - How to update the package assignment of Fiori apps activated via task list](https://me.sap.com/notes/3452535/E)

Before running any Fiori task list in **STC01**, **implement the latest version of the corresponding SAP Note** (and its prerequisites). 

| Task List | Key Update Note |
|----------|-----------------|
| `SAP_GW_FIORI_ERP_ONE_CLNT_SETUP` | [2510134](https://launchpad.support.sap.com/#/notes/2510134) |
| `SAP_FIORI_FOUNDATION_S4` | [2712785](https://launchpad.support.sap.com/#/notes/2712785) |
| `SAP_FIORI_FCM_CONTENT_ACTIVATION` | [2813396](https://launchpad.support.sap.com/#/notes/2813396) |
| `SAP_FIORI_FCM_CATALOG_ACTIVATION` | [3339909](https://launchpad.support.sap.com/#/notes/3339909) |

---

##### Fiori Foundation
These task lists set up core infrastructure. Run in sequence.
| Task List Name                    | Short Description                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------|
| `SAP_GW_FIORI_ERP_ONE_CLNT_SETUP` | Performs initial setup for embedded Fiori deployment in S/4HANA.                      |
| `SAP_FIORI_FOUNDATION_S4`         | Initial setup for Fiori applications in S/4HANA, including foundation configurations. |


##### Enterprise Search
| Task List Name                     | Short Description                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------|
| `SAP_ESH_INITIAL_SETUP_WRK_CLIENT` | Initializes SAP Enterprise Search (ESH) in the current work client                    |


##### Activating Fiori Apps
These activate apps via roles or catalogs, including OData/ICF and transport requests.
| Task List Name                        | Short Description                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------|
| `SAP_FIORI_CONTENT_ACTIVATION`        | Activates SAP Fiori business roles and associated content (catalogs, groups, tiles).       |
| `SAP_FIORI_FCM_CONTENT_ACTIVATION`    | Activates custom SAP Fiori business roles and associated content (catalogs, groups, tiles).|                                                                              |
| `SAP_FIORI_FCM_CATALOG_ACTIVATION`    | Activates SAP Fiori apps by business catalog, including Gateway services and ICF nodes.    |                                                                                    |


##### Fiori General
| Task List Name                    | Short Description                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------|
| `SAP_FIORI_HEALTH_CHECKS`         | Runs health checks for Fiori setup to identify configuration issues.                  |

## SAP Fiori TaskLists

#### Initial setup for embedded Fiori deployment in S/4HANA via Task List SAP_GW_FIORI_ERP_ONE_CLNT_SETUP . 
SAP_GW_FIORI_ERP_ONE_CLNT_SETUP is a task list designed for setting up the SAP Gateway and SAP Fiori in a single client environment. It includes various tasks such as setting the SAP system alias for the Fiori Launchpad, activating HTTP services, and configuring system aliases. 
#### Latest Version
- [2510134 - Fiori Setup: Updates for task lists for Gateway/Fiori configuration](https://me.sap.com/notes/2510134/E)
- [2639552 - Fiori Setup: Improvements for Activate FLP services used in task lists](https://me.sap.com/notes/2639552)

#### Background Information
- [Configuring SAP Gateway and SAP Fiori](https://learning.sap.com/courses/technical-implementation-and-operation-i-of-sap-s-4hana-and-sap-business-suite/configuring-sap-gateway-and-sap-fiori-1)
- [3596749 - Warning during execution of task list "SAP_GW_FIORI_ERP_ONE_CLNT_SETUP" in S/4HANA](https://me.sap.com/notes/3596749/E)

#### Timing
- **New implementation** - Run task list (transaction STC01): SAP_GW_FIORI_ERP_ONE_CLNT_SETUP
- **SAP S/4HANA Upgrade** - It is recommended to run task list SAP_GW_FIORI_ERP_ONE_CLNT_SETUP again. This ensures that you cover all the new configuration settings.
---

#### Activating SAP Fiori Foundation Via Task List SAP_FIORI_FOUNDATION_S4
##### Latest Version of Tasklist
- [2712785 - Fiori Setup: Initial Setup for Fiori Applications S/4](https://me.sap.com/notes/2712785/E)
- [SAP Fiori for SAP S/4HANA - Simplifying My Home Activation from SAP S/4HANA 2023 FPS02 or higher](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-fiori-for-sap-s-4hana-simplifying-my-home-activation-from-sap-s-4hana/ba-p/14005037)

##### Background Information
- [Activating SAP Fiori Foundation Via Task List SAP_FIORI_FOUNDATION_S4](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/22bbe89ef68b4d0e98d05f0d56a7f6c8/f7d17065a8234ae0986f45d2f4f419fd.html?locale=en-US)

##### Timing
- **SAP S/4HANA Upgrade** - It is recommended to run task list SAP_FIORI_FOUNDATION_S4 again. This ensures that you cover all the new configuration settings.

---

#### - Activate Enterprise Search via task list SAP_ESH_INITIAL_SETUP_WRK_CLIENT
##### Latest Version of Tasklist
- []()
  
##### Background Information
- [2626107 - How to execute task list SAP_ESH_INITIAL_SETUP_WRK_CLIENT](https://me.sap.com/notes/2626107/E)
- [Task Lists for Setting Up Enterprise Search](https://help.sap.com/docs/ABAP_PLATFORM_NEW/5d7d37af2a864fe7942178707914e3ec/07f910bf569c4eeba5d0c5e6ba7bd972.html?locale=en-US)

##### Timing
- **New implementation** - Activate Enterprise Search via task list (transaction STC01): SAP_ESH_INITIAL_SETUP_WRK_CLIENT
- **SAP S/4HANA Upgrade** - To update new or changed Search Models re-run task list SAP_ESH_INITIAL_SETUP_WRK_CLIENT.  

---

#### Activating SAP Fiori Apps for Custom Business Roles Via Task List SAP_FIORI_FCM_CONTENT_ACTIVATION 📰
You use this task list to specify one or more customer or SAP-delivered business roles (in the scope definition step), and then, automatically activate OData services and ICF nodes for these roles. The task list automatically assigns the OData services and business roles to a transport request.
##### Latest Version of Task List
- [2813396 - Fiori Setup: Content Activation for Business Roles](https://me.sap.com/notes/2813396/E)

##### Background Information
- [Activating SAP Fiori Apps for Custom Business Roles Via Task List SAP_FIORI_FCM_CONTENT_ACTIVATION](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/22bbe89ef68b4d0e98d05f0d56a7f6c8/865faf026ea94fd4b4298efdf5c5b358.html?locale=en-US)
---

#### Activating SAP Fiori Apps for Catalogs Via Task List SAP_FIORI_FCM_CATALOG_ACTIVATION 📰
Similar to the task list for activation of SAP business roles and customer business roles, there is a task list for activation of services on business catalog level. You use this task list to specify one or more customer or SAP-delivered business catalogs (in the scope definition step), and then, automatically activate OData services and ICF nodes for these catalogs.
##### Latest Version of Task List
- [3339909 - Fiori Setup: Content Activation for Catalogs](https://me.sap.com/notes/3339909/E)

##### Background Information
- [Activating SAP Fiori Apps for Catalogs Via Task List SAP_FIORI_FCM_CATALOG_ACTIVATION](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/22bbe89ef68b4d0e98d05f0d56a7f6c8/cc61ac42f7644d8d98698e83370b9f27.html?locale=en-US)
- [SAP Fiori for SAP S/4HANA – Activating Apps by Business Catalog](https://community.sap.com/t5/technology-blog-posts-by-sap/sap-fiori-for-sap-s-4hana-activating-apps-by-business-catalog/ba-p/13571554)

---

#### Health Checks Via Task List /UI2/FLP_HEALTH_CHECKS 📰
##### Background Information
- [Health Checks Via Task List /UI2/FLP_HEALTH_CHECKS](https://help.sap.com/docs/ABAP_PLATFORM_NEW/a7b390faab1140c087b8926571e942b7/fdd250731393433eb275fc2511a097a0.html?locale=en-US)
