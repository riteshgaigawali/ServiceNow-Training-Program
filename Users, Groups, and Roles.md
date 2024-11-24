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
