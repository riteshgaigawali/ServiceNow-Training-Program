# ServiceNow - Modifying List and Forms :

### **Modifying List Views**

1. **How can you customize a List view in ServiceNow?**

   - You can customize a List view by:
     - Right-clicking the header of a list and selecting **Configure > List Layout**.
     - Adding, removing, or reordering columns in the **Configure List Layout** window.

2. **What are views in the List view, and why are they useful?**

   - A view in the List view determines which fields (columns) are displayed. Views are useful for tailoring the List layout to different user roles or specific business needs.

3. **How can you create a new List view?**

   - Navigate to **System UI > Views**, click **New**, and specify the view name.
   - Use **Configure List Layout** to define fields for the new view.

4. **How do you filter records in the List view?**

   - Use the filter icon (top left) to define conditions, or:
     - Right-click a field value and choose **Show Matching** or **Filter Out**.
     - Use the Search bar with encoded queries (e.g., `active=true^priority=1`).

5. **Can you apply different List views for different roles?**
   - Yes, by creating specific views and setting role-based permissions using **UI Policies** or scripts.

---

### **Modifying Form Views**

6. **How do you customize a Form layout in ServiceNow?**

   - Navigate to the Form and:
     - Right-click the Form header and select **Configure > Form Layout**.
     - Add, remove, or rearrange fields, tabs, and sections.

7. **What is Form Designer, and how does it differ from Form Layout?**

   - **Form Designer** is a drag-and-drop interface for modifying Form layouts, adding fields, and managing sections. It is more intuitive than the traditional **Form Layout** module.

8. **How can you make a field mandatory in a Form?**

   - Use **UI Policies** or **Data Policies**:
     - **UI Policy**: Make the field mandatory dynamically based on conditions.
     - **Data Policy**: Enforce the rule at the database level, applicable even for imports or APIs.

9. **How do you make a field read-only on a Form?**

   - Use a **UI Policy** or **Client Script**:
     - **UI Policy**: Define conditions to make the field read-only dynamically.
     - **Client Script**: Use JavaScript to set the `readonly` property programmatically.

10. **What are the different ways to add a new field to a Form?**
    - Add fields using:
      - **Form Layout**: Add existing fields or create new ones.
      - **Form Designer**: Drag a field from the field list onto the Form.
      - **Dictionary Table**: Define a new field directly in the table schema.

---

### **Advanced Customizations**

11. **How do you configure a Form for a specific view?**

    - Navigate to **Configure > Form Layout** and select the desired view from the dropdown. Add fields and sections specific to that view.

12. **How can you add a related list to a Form?**

    - Navigate to the Form, right-click the header, and select **Configure > Related Lists**. Add the desired related list from the available options.

13. **What are the steps to create a custom UI Action on a Form?**

    - Navigate to **System Definition > UI Actions**, create a new UI Action, and define:
      - **Table**: The table where the action applies.
      - **Action**: Specify the action (e.g., a script or redirection).
      - **Condition**: When the action should be visible or enabled.

14. **How can you set different default Form views for different roles?**

    - Use **Form View Rules** or **UI Policies** to define default views based on the user's role or conditions.

15. **How can you make changes to Forms and Lists visible only to specific users or roles?**
    - Use role-based conditions in **UI Policies**, **ACLs (Access Control Rules)**, or **View Rules**.

---

### **Troubleshooting and Best Practices**

16. **What happens if you delete a field from a Form?**

    - Deleting a field from a Form does not remove it from the database. The field is still present in the table schema and other views unless explicitly deleted from the Dictionary.

17. **How do you debug issues with Forms or Lists?**

    - Use:
      - **System Logs**: Check logs for errors related to UI Policies, Client Scripts, or ACLs.
      - **Script Debugger**: Test and debug scripts running on Forms or Lists.
      - **Developer Tools**: Use browser developer tools for client-side issues.

18. **What is the difference between hiding a field using a UI Policy and ACL?**

    - **UI Policy**: Hides the field dynamically on the Form (client-side).
    - **ACL**: Restricts field access at the database level (server-side), ensuring users cannot access it via APIs or back-end queries.

19. **What are the best practices for modifying Forms and Lists?**

    - Use views to avoid overriding default layouts.
    - Group related fields in logical sections.
    - Avoid hardcoding values; use conditions or data-driven rules.
    - Document customizations for future reference.

20. **How can you restore the default Form or List layout?**
    - Remove customizations by reverting changes in **Form Layout** or **List Layout**. Alternatively, compare the layout to a fresh instance if using a development or backup environment.
