## SAP Fiori Tasklists 📝

### General
- []()

##### Fiori Foundation
| Task List Name                    | Short Description                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------|
| `SAP_GW_FIORI_ERP_ONE_CLNT_SETUP` | Performs initial setup for embedded Fiori deployment in S/4HANA.                      |
| `SAP_FIORI_FOUNDATION_S4`         | Initial setup for Fiori applications in S/4HANA, including foundation configurations. |

##### Activating Fiori Apps
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

#### Background Information
- [Configuring SAP Gateway and SAP Fiori](https://learning.sap.com/courses/technical-implementation-and-operation-i-of-sap-s-4hana-and-sap-business-suite/configuring-sap-gateway-and-sap-fiori-1)

---

#### Activating SAP Fiori Foundation Via Task List SAP_FIORI_FOUNDATION_S4
##### Latest Version of Tasklist
- [2712785 - Fiori Setup: Initial Setup for Fiori Applications S/4](https://me.sap.com/notes/2712785/E)
  
##### Background Information
- [Activating SAP Fiori Foundation Via Task List SAP_FIORI_FOUNDATION_S4](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/22bbe89ef68b4d0e98d05f0d56a7f6c8/f7d17065a8234ae0986f45d2f4f419fd.html?locale=en-US)

---

#### Activating SAP Fiori Apps for Custom Business Roles Via Task List SAP_FIORI_FCM_CONTENT_ACTIVATION 📰
You use this task list to specify one or more customer or SAP-delivered business roles (in the scope definition step), and then, automatically activate OData services and ICF nodes for these roles. The task list automatically assigns the OData services and business roles to a transport request.
##### Latest Version of Task List
- [XXXX](https://me.sap.com/notes/2813396/E)

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
