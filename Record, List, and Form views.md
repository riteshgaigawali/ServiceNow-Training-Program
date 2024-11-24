# Record, List, and Form views :-

### **ServiceNow Record View Questions**

1. **What is a record in ServiceNow?**

   - A record in ServiceNow is a single entry in a table that stores information about a specific entity, such as an Incident, Change Request, or User. Each record has a unique identifier called the **Sys ID**.

2. **What is the Sys ID, and why is it important?**

   - The **Sys ID** is a 32-character unique identifier for each record in ServiceNow. It is used for referencing records across modules and for integrations between ServiceNow and other systems.

3. **How can you locate a specific record in ServiceNow?**
   - You can locate a record by:
     - Searching in the **Global Search Bar**.
     - Using a filter in the List view.
     - Accessing the record directly via its URL.

---

### **List View Questions**

4. **What is the List view in ServiceNow?**

   - The List view displays multiple records from a table in a grid format, showing selected fields (columns) for each record. It allows users to browse, search, and edit records in bulk.

5. **How can you filter data in a List view?**

   - You can filter data using:
     - **Condition Builder**: Click on the filter icon and set conditions.
     - **Search Bar**: Enter specific keywords or conditions like `priority=1`.
     - **Encoded Query**: Use advanced queries (e.g., `active=true^state=2`).

6. **What is the difference between a List view and a related list?**

   - The **List view** shows records from a single table, while a **related list** displays records from another table that are linked to the current record via a relationship.

7. **How do you export records from a List view?**

   - Click on the **List Actions Menu (gear icon)** > **Export** > Choose a format (Excel, CSV, or PDF).

8. **What is a view in the List view, and why is it important?**
   - A **view** is a predefined layout that determines which columns are displayed. It helps tailor the List view to specific user or business needs.

---

### **Form View Questions**

9. **What is the Form view in ServiceNow?**

   - The Form view is used to view or modify details of a single record. It displays all fields as a customizable layout.

10. **How can you customize a Form view?**

    - Use **Form Designer** to add, remove, or rearrange fields, create new sections, and manage related lists.

11. **What are mandatory fields in a Form? How are they identified?**

    - Mandatory fields require a value before the record can be saved. They are identified with a red asterisk (\*) next to the field name.

12. **What is the purpose of the Activity Stream in a Form?**

    - The Activity Stream shows a chronological log of all actions, comments, and changes related to the record.

13. **What is the difference between UI Policy and Client Script in a Form?**

    - **UI Policy**: Configures Form behavior (e.g., make fields mandatory or read-only) without coding.
    - **Client Script**: Executes JavaScript on the client side to handle more complex logic.

14. **What is a related list on a Form?**

    - A related list displays records from another table that have a relationship with the current record. For example, an Incident Form might show related Problem or Change records.

15. **How can you switch between different Form views?**

    - Use the **View** dropdown in the Form header to select the desired view.

16. **What is Form Designer, and what is it used for?**
    - Form Designer is a drag-and-drop tool to customize Form layouts, manage fields, and group them into sections for better organization.

---

### **Advanced Questions**

17. **What are Data Policies, and how do they work in Forms?**

    - Data Policies ensure data integrity by enforcing rules when data is entered or modified, even outside the Form (e.g., via imports or APIs).

18. **What is the difference between a field dependency and a reference field?**

    - **Field Dependency**: Makes one field’s values dependent on another field’s selection (e.g., Subcategories depend on Category).
    - **Reference Field**: Links to a record in another table (e.g., Caller field in Incident links to User records).

19. **How does ServiceNow ensure security in Forms and Lists?**

    - By using Access Control Rules (ACLs) that define who can view, create, update, or delete records and fields.

20. **What is the purpose of form annotations?**
    - Form annotations provide additional information or guidance to users by adding custom messages or instructions on the Form.

---

### **Practical Scenario Questions**

21. **You need to pre-fill specific fields in a Form for repetitive tasks. How can you achieve this?**

    - Use **Templates** to predefine values for specific fields. Templates can be applied directly to Forms.

22. **How do you make a field visible only when a specific condition is met?**

    - Use a **UI Policy** with a condition. For example, display the "Reason for Reopening" field only when the state is "Reopened."

23. **How do you track changes to a record?**

    - Enable the **Audit Log** or check the Activity Stream to track changes, including field updates, comments, and state transitions.

24. **What happens when you click "Insert" instead of "Update" in a Form?**

    - Clicking **Insert** creates a duplicate of the record with a new Sys ID, while **Update** saves changes to the existing record.

25. **How can you highlight a field in a List view based on its value?**
    - Use **UI Actions** or **List Decorations** to apply visual indicators (e.g., change row color based on priority).

---
