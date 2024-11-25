# ServiceNow Context Menu

### **General Questions**

1. **What is a Context Menu in ServiceNow?**

   - A Context Menu in ServiceNow is the menu that appears when you right-click on an item in the interface, such as a record, field, or list. It provides quick access to commonly used actions and options.

2. **Where are Context Menus used in ServiceNow?**
   - Context Menus are available in the following areas:
     - **List view** (for rows and headers)
     - **Form view** (for fields and sections)
     - **Fields** (right-clicking on specific fields in a Form)

---

### **List View Context Menu**

3. **What options are typically available in the List view context menu?**

   - Common options include:
     - **Show Matching**: Filters the list to show all records with the same value in the selected field.
     - **Filter Out**: Filters out records with the selected value in the field.
     - **Export**: Options to export the list as CSV, Excel, or PDF.
     - **Configure**: Allows modification of the list layout (requires appropriate roles).
     - **View in New Tab**: Opens the record in a new tab.
     - **Group By**: Groups the list by a specific field.
     - **Copy URL**: Copies the direct URL to the record or view.

4. **How do you access the List view context menu?**

   - Right-click on a record, column header, or anywhere in the list.

5. **Can the List view context menu be customized?**
   - Yes, administrators can customize context menus using the **UI Context Menu** module. You can add or modify options based on requirements.

---

### **Form View Context Menu**

6. **What options are available in the Form view context menu?**

   - Common options include:
     - **Save**: Saves changes to the record.
     - **Insert**: Creates a duplicate of the record with a new Sys ID.
     - **Insert and Stay**: Duplicates the record and keeps the user on the Form.
     - **View History**: Displays the history of changes made to the record.
     - **Copy URL**: Copies the URL of the current Form.
     - **Configure**: Options to personalize the Form layout (requires roles).

7. **How do you access the Form view context menu?**

   - Right-click on the Form header, a specific field, or a section.

8. **What is the difference between "Insert" and "Update" in the Form context menu?**
   - **Insert**: Creates a new record (clone of the current record) with a new Sys ID.
   - **Update**: Saves changes to the current record.

---

### **Field Context Menu**

9. **What is the purpose of the Field context menu?**

   - The Field context menu allows quick actions on specific fields in a Form, such as:
     - **Show Matching**: Filters to records with the same field value.
     - **Filter Out**: Excludes records with the selected value.
     - **Copy Field Value**: Copies the value of the field to the clipboard.
     - **Personalize Label**: Changes the label for the user session (if allowed).

10. **How do you access the Field context menu?**
    - Right-click on a specific field in the Form.

---

### **Customization and Advanced Questions**

11. **Can you customize the Context Menus in ServiceNow?**

    - Yes, Context Menus can be customized using the **UI Context Menu** table. Administrators can:
      - Add custom actions.
      - Modify existing options.
      - Restrict options based on user roles or conditions.

12. **How do you add a new option to a Context Menu?**

    - Navigate to **System UI > UI Context Menus**, create a new menu item, and define:
      - **Table**: The table where the menu applies.
      - **Action**: The script or function to execute.
      - **Condition**: When the option should appear.

13. **What roles are required to modify Context Menus?**

    - The **admin** role is typically required to customize Context Menus.

14. **How can you restrict a Context Menu option to specific roles?**

    - Add conditions in the UI Context Menu configuration that check the current user’s roles.

15. **How can you debug Context Menu issues in ServiceNow?**
    - Use the **System Logs > UI Actions** to check for script execution logs or errors related to context menu actions.

---
