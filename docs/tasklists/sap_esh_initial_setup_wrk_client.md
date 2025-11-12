# Activate Enterprise Search via task list SAP_ESH_INITIAL_SETUP_WRK_CLIENT

## Goal 🎯

The goal of this file is to document the activation of Enterprise Seatch via tasklist SAP_ESH_INITIAL_SETUP_WRK_CLIENT.

## References 📝
#### SAP Notes
- [2626107 - How to execute task list SAP_ESH_INITIAL_SETUP_WRK_CLIENT](https://me.sap.com/notes/2626107/E)
- [2848050 - Search Software components in SAP S/4HANA On-Premise](https://me.sap.com/notes/2848050/E)

#### Blogs, SAP Help and other Sources
- [Task Lists for Setting Up Enterprise Search](https://help.sap.com/docs/ABAP_PLATFORM_NEW/5d7d37af2a864fe7942178707914e3ec/07f910bf569c4eeba5d0c5e6ba7bd972.html?locale=en-US)
- [SAP Learning: Activating Enterprise Search](https://learning.sap.com/courses/technical-implementation-and-operation-i-of-sap-s-4hana-and-sap-business-suite/activating-enterprise-search-1)

## Prerequisites 📝
- XXXX

### Activate Enterprise Search via task list SAP_ESH_INITIAL_SETUP_WRK_CLIENT 🛠️
1. Call transaction `STC01`.
2. Enter `SAP_ESH_INITIAL_SETUP_WRK_CLIENT` and click `Excecute`.

     <img width="1503" height="748" alt="image" src="https://github.com/user-attachments/assets/8a864bfd-c2e2-4ae1-8cf1-08107e044e32" />

3. Click `Fill Parameters` for step `Set TREX Destination or SAP HANA DB Connection`.

     <img width="1580" height="623" alt="image" src="https://github.com/user-attachments/assets/66e2abf3-1477-44ab-847e-928dbed4a53c" />
   
4. Click `Fill Parameters` for step `Select Models to Create Connectors`.

     <img width="1747" height="473" alt="image" src="https://github.com/user-attachments/assets/19489ce6-225b-4d88-8385-291d0492c9f8" />

5. In the field `Software Component` select `SAPAPPLH`.

> [!NOTE]  
> The only relevant Enterprise Search Software Component in On-Premise releases of SAP S/4HANA is SAPAPPLH. Hence Enterprise search connectors should be created only from Software Component SAPAPPLH.

6. XX

### Execute report ESH_REFRESH_RUNTIME_BUFFER 🛠️ 
The report ESH_REFRESH_RUNTIME_BUFFER refreshes the in-memory runtime cache of the Embedded Search (ESH) framework in an S/4HANA system. This ensures that any changes made in transaction ESH_COCKPIT (e.g., creating, activating, deactivating, or regenerating connectors) are immediately available to end users without restarting the system or ICM.

> [!NOTE]  
> This report requires no parameters and it is quick to run (a few minutes).
   



   
