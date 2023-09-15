# Employee Management Application - Spring Boot

## Introduction
This Spring Boot application is designed for managing employees, providing essential features such as viewing, adding, editing, and deleting employees. Below are the core functionalities:

## Functionality and Implementation

### Viewing Employees
- The application displays a list of all created employees on the paths `/` and `/employees` using the `list.html` template.

### Adding Employees
- Users can add new employees by clicking the "Add" button on the `list.html` template.
- Upon clicking "Submit," a new entity is created and stored in the database, and the user is redirected to the `/employees` page.

### Deleting Employees
- Employees can be deleted by clicking the "Delete" button on the `list.html` template.
- The corresponding employee record is removed from the database, and the user is redirected to the `/employees` page.

### Editing Employees
- Users can edit employee information by clicking the "Edit" button on the `list.html` template.
- This action redirects the user to the `form.html` template at the path `/employees/[id]/edit`, where the input fields display the values of the entity being edited.
- After making changes and clicking "Submit," the modified data is updated in the database, and the user is redirected to the `/employees` page.

### Authentication and Authorization
- The application supports user authentication on the `/login` page and user logout on the `/logout` page.
- Only the `/` page is publicly accessible, while all other pages are restricted to users with the `ROLE_ADMIN` role.
- The "Edit," "Delete," and "Add" buttons on `list.html` are only visible to users with the `ROLE_ADMIN` role.
- User authentication is based on email and password properties stored in the employee database. Passwords are securely encrypted.
- User roles are set based on the employee type with a `ROLE_` prefix.

### Employee Filtering
- The application allows users to search for employees based on their skills and minimum work experience (time since hiring).
- The filtering is performed through the form with the `id="filter-form"` in the `list.html` template.
- The filtered results are displayed on the same page, showing only employees that meet the specified criteria.
- Filtering is performed only based on the entered fields; empty fields are ignored.


  
