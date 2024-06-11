# Class 33 Reading Notes

## Introduction

This reading covers the concepts of Role Based Access Control (RBAC) and the features of the `react-cookie` and `react-cookies` libraries in React applications.

## Notes

### What is Role Based Access Control (RBAC)?

Role Based Access Control (RBAC) is a method of regulating access to resources based on the roles of individual users within an organization. Users are assigned specific roles, and those roles have predefined permissions that determine what actions the users can perform.

### Share an example of RBAC including all possible CRUD operations and correlating roles

Example of RBAC:

- **Roles**: Admin, Editor, Viewer
- **CRUD Operations**:
  - **Create**:
    - Admin: Can create new resources.
    - Editor: Can create new resources.
    - Viewer: Cannot create new resources.
  - **Read**:
    - Admin: Can read all resources.
    - Editor: Can read all resources.
    - Viewer: Can read all resources.
  - **Update**:
    - Admin: Can update all resources.
    - Editor: Can update resources they have access to.
    - Viewer: Cannot update resources.
  - **Delete**:
    - Admin: Can delete all resources.
    - Editor: Can delete resources they have access to.
    - Viewer: Cannot delete resources.

### What are the Benefits of RBAC?

- **Improved Security**: Limits access to sensitive information based on user roles.
- **Simplified Management**: Easier to manage user permissions by assigning roles rather than individual permissions.
- **Compliance**: Helps ensure that only authorized users have access to certain data, aiding in compliance with regulations.
- **Efficiency**: Reduces the risk of unauthorized access and simplifies the onboarding process for new users.

### Compare and Contrast the following two Libraries and the following questions. Yes, they are similarly named

#### react-cookie library

- **Features**:
  - Provides hooks and components for managing cookies in React applications.
  - Supports setting, getting, and removing cookies.
  - Handles cookie parsing and serialization automatically.
  - Allows for configuration of cookie attributes such as expiration, path, and domain.

#### react-cookies component

- **Features**:
  - Provides a higher-order component (HOC) and methods for handling cookies in React components.
  - Allows cookies to be set, read, and removed within component lifecycle methods.
  - Supports server-side rendering (SSR) for handling cookies on the server side.
  - Offers methods to manipulate cookies with additional configuration options.

### Which library would you prefer? Why?

I would prefer the `react-cookie` library because it provides a more modern approach with hooks and components, which aligns better with functional component patterns commonly used in contemporary React development. Additionally, its support for automatic cookie parsing and serialization simplifies cookie management, making the code cleaner and more maintainable.
