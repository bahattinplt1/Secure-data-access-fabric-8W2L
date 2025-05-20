# Secure Data Access in Microsoft Fabric

This project demonstrates a full walkthrough of implementing multi-level data access security in Microsoft Fabric. The steps follow the Microsoft Learn lab ["Secure data access"](https://microsoftlearning.github.io/mslearn-fabric/Instructions/Labs/19-secure-data-access.html) and were executed and documented step by step.

## ✅ Overview of Steps Completed

1. **Create a Workspace**
   - Initialized a new Fabric workspace with capacity-enabled licensing.

2. **Create a Sample Warehouse**
   - Used the “Sample warehouse” option to generate structured data in a new warehouse.

3. **Create a Lakehouse with Sample Data**
   - Created a Lakehouse and loaded the **Public Holidays** sample dataset into it.

4. **Apply Workspace Access Controls**
   - Used two browser sessions to simulate an admin user and a second (limited) user.
   - Assigned the second user the “Workspace Viewer” role and verified read access.

5. **Apply Item-Level Permissions**
   - Removed workspace-level access from the second user.
   - Granted item-level `ReadData` access directly on the warehouse.
   - Verified that only the warehouse was accessible via OneLake.

6. **Apply OneLake Data Access Roles (Preview Feature)**
   - Created a custom data access role limited to the `publicholidays` folder in the Lakehouse.
   - Assigned the role to the second user.
   - Verified that only data in that specific folder was accessible while others remained hidden.

## 📂 Screenshots

All screenshots documenting each step of the process are included in the `/screenshots` folder of this repository.

## 🔗 References

- Microsoft Learn Lab: [Secure Data Access in Microsoft Fabric](https://microsoftlearning.github.io/mslearn-fabric/Instructions/Labs/19-secure-data-access.html)
- Microsoft Fabric: https://app.fabric.microsoft.com

## ℹ️ Notes

- All actions were completed in Microsoft Fabric with a trial license.
- This exercise highlights the use of **fine-grained access control** using both role-based and object-level security.
