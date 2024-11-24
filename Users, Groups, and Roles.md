18-11-2024

# ServiceNow : Users, Groups, and Roles -

## Table of Content :

    - User Table and Fields
    - Group Table and Fields
    - Role Table and Fields
    - How to create a User
    - How to create a Group
    - How to create a Role
    - Activate or Deactivate a User
    - How to add a User to a Group
    - How to add/remove a Role to a User
    - How to add/remove a Role to a Group
    - Group Parent and Child Relationship
    - Impersonate User
    - Inherited Roles

## User :

    What is Users module ?
    >>
      - Users module is available in ServiceNow instance under the User Administration.
      - This particular module will show you the list of User records in the platform.

    What is User in ServiceNow ?
    >>
       - User is an individual who logs in to ServiceNow instance and has User record stored in User table.
       - Every user has different access as per the Role they have.
       - Any person who want to work in ServiceNow platform has to have record in User table.
       - ServiceNow has a table User which stores user details, and the backend name of this table is sys_user.

    What is there in User record ?
    >>
       - User records includes User name, First name, Last name, Password, Email address, etc.
       - Some details are unique like username, email, etc.
       - There is an User Form where we can put this details, where User Id and Email will be always unique.
       - The Department is a reference field in User Form, where there is a another table called as Department in ServiceNow instance.
       - There is an important field which is Active check-box, which determines if the User is active or inactive.
       - We can set the password for a User using Set Password button present in User Form, where we can also Generate a random password.
       - While creating a password for User we can check the Password needs reset check-box, so that when User logs in he have to first reset the Password.
       - User table also have the different Views such as : Default View, Self Service, Service Portal, etc.
       - This Views help to display the table to Users as per their Roles.

    What are the ways to Create an User ?
    >>
      - There are two ways to create an User in ServiceNow :

    	1. Manual :
    			- We can directly create an User manually in the ServiceNow instance.
    			- Steps :- User Administration --> Users --> Fill in the fields. --> Click on Submit.

    	2. Import from External System :
    			- We can connect external systems which has user data and import the data to the ServiceNow instance.
    			- Steps : We will see it later.

## Groups :

    What is Group in ServiceNow ?
    >>
      - The Group is a set of users who share a common purpose.
      - ServiceNow has a table Group which stores group details, and the backend name of this table is sys_user_group.

    What is there in Group record ?
    >>
      - The Group includes information like Name, Manager, Type, Group Email and its members.
      - There is an Group Form where we can put this details.

## Roles :

    What is Role in ServiceNow ?
    >>
      - Role control access to features and capabilities in applications and modules.
      - The admin role provides access to all features and capabilities.
      - Roles can be added to Users and Groups.
      - ServiceNow has a table Role which stores role details, and the backend name of this table is sys_user_role.

---

### **Users in ServiceNow**

1. **What is a user in ServiceNow?**

   - A user is an individual who has access to ServiceNow. Each user has a unique profile containing attributes like username, email, department, roles, and group memberships.

2. **Where can user records be managed in ServiceNow?**

   - User records can be managed in the **User Administration** module, typically found under **Users and Groups**.

3. **What is the importance of the 'User ID' field in a user record?**

   - The `User ID` is a unique identifier for each user. It is used for authentication and logging into ServiceNow.

4. **How can you deactivate a user in ServiceNow?**

   - Open the user record and uncheck the **Active** checkbox. Deactivating a user prevents them from logging in.

5. **What is a delegate user in ServiceNow?**
   - A delegate user can perform tasks or approvals on behalf of another user. Delegates are configured in the **Delegate** module.

---

### **Groups in ServiceNow**

6. **What is a group in ServiceNow?**

   - A group is a collection of users who share a common responsibility, such as working on incidents, approvals, or changes.

7. **What are the benefits of using groups?**

   - Groups simplify role assignment, task assignment, and notification management by organizing users based on responsibilities.

8. **How can you create a new group in ServiceNow?**

   - Navigate to **Users and Groups > Groups**, click **New**, and provide details like Group Name and Description.

9. **How do you assign users to a group?**

   - Open the group record, navigate to the **Group Members** related list, and add users.

10. **Can a user belong to multiple groups?**
    - Yes, a user can be a member of multiple groups, enabling them to access resources or tasks tied to different teams or functions.

---

### **Roles in ServiceNow**

11. **What is a role in ServiceNow?**

    - A role is a collection of permissions that define what actions a user can perform and what data they can access.

12. **What are some common roles in ServiceNow?**

    - Examples include:
      - **admin**: Full access to all features.
      - **itil**: Access to Incident, Problem, and Change Management.
      - **catalog_admin**: Manages Service Catalog items.

13. **How can roles be assigned to a user?**

    - Roles can be assigned:
      - Directly via the user record.
      - Indirectly through group membership.

14. **What is role inheritance?**

    - When a role is assigned to a group, all users in that group inherit the role. Similarly, roles can inherit permissions from other roles.

15. **How do you create a custom role in ServiceNow?**
    - Navigate to **System Security > Roles**, click **New**, define the role, and assign it permissions.

---

### **Relationship Between Users, Groups, and Roles**

16. **How are users, groups, and roles related in ServiceNow?**

    - Users are assigned roles directly or through group membership. Groups can have roles, and all users in the group inherit those roles.

17. **If a user is part of two groups with conflicting roles, how does ServiceNow handle it?**

    - ServiceNow combines all roles assigned to the user, resolving conflicts by granting the highest level of permissions.

18. **What is the best practice for assigning roles in ServiceNow?**

    - Assign roles to groups instead of individual users. This approach simplifies role management and ensures consistency.

19. **Can a user have a role without being part of a group?**

    - Yes, roles can be assigned directly to users, but it is not a recommended practice for scalability.

20. **What happens if you remove a user from a group?**
    - The user loses all roles and permissions associated with that group.

---

### **Advanced Questions**

21. **What are the different ways to assign roles in ServiceNow?**

    - Roles can be assigned:
      - Directly to a user.
      - To a group, with users inheriting the roles.
      - Through scripts or workflows.

22. **What is an elevated privilege in ServiceNow?**

    - Elevated privileges allow a user to temporarily elevate their access (e.g., admin role) for specific tasks. This is managed via the **Security Admin** role.

23. **How do you audit roles assigned to users or groups?**

    - Use the **Roles** related list in user/group records or generate reports from the **Role Allocation** table.

24. **How can you revoke a user's access to specific records or actions?**

    - Use **Access Control Rules (ACLs)** to restrict access based on roles or conditions.

25. **What is the difference between a group role and a user role in ServiceNow?**
    - **Group Role**: A role assigned to a group, inherited by all members.
    - **User Role**: A role directly assigned to an individual user.

---
