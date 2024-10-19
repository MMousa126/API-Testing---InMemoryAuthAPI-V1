# InMemoryAuthAPI V1 - API Testing

## Overview
This document outlines the manual testing process for the **InMemoryAuthAPI**, with a focus on **authentication**, **contacts**, and **invoice** functionalities.

### Key Focus Areas:
- **Authentication**: Testing user registration, login, and token-based authorization.
- **Contacts**: CRUD (Create, Read, Update, Delete) operations on contacts.
- **Invoices**: Retrieving, creating, returning, and paying invoices.

---

## Test Cases and Bug Reporting

Testing involves both functional and non-functional requirements of the API. All test cases are documented and accessible via the following link:

- [**Test Cases**](https://docs.google.com/spreadsheets/d/1di4_oJrd1n3Hkw6CmIrcpZ4swlGvlpB-00YibXNPqZg/edit?gid=28818539#gid=28818539)

### Bug Reporting:
Any bugs found during testing will be reported for tracking and resolution.

---

## API Modules

### 1. Authorization
- **Registration**: Verifies user registration functionality.
- **Login**: Validates login credentials and token generation.
- **Authorization**: Ensures proper access control for various API resources.

### 2. Contacts
- **Get All Contacts**: Retrieves all contacts in the system.
- **Create Contact**: Creates a new contact.
- **Get Specific Contact**: Retrieves a contact by ID.
- **Update Contact**: Updates an existing contact.
- **Delete Contact**: Deletes a contact from the system.

### 3. Invoices
- **Get All Invoices**: Retrieves all invoices.
- **Create Invoice**: Creates a new invoice.
- **Return Invoice**: Processes the return of an invoice.
- **Pay Invoice**: Processes the payment for an invoice.
## Pre-Conditions

1. **Open Swagger API Documentation**  
   - Access the [Swagger API Documentation](https://qa-assignment.sortcrm.com/swagger/index.html) to explore and interact with the API.

2. **Register a New User**  
   - Use a `POST` request to `/api/Auth/register` to register a new user with a valid username.  
   - Click **Execute** to submit the request and store the new user in the database.

3. **Log In with Registered Credentials**  
   - Use a `POST` request to `/api/Auth/login` with the registered account credentials.  
   - Copy the token from the response body after a successful login.

4. **Set Authorization Header**  
   - Navigate to the **Authorization** section in Swagger.  
   - Add `Bearer` followed by a space and your copied token to the authorization header to authenticate your API requests `Bearer "Token"`.


# Bugs

- ** Bug_1 **: Create Contact -> Request Body Doesn't Match the request Body [Bug 1](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_1)
- ** Bug_2 **: Contacts -> ID is not a unique identifier and many contact could have the same id [Bug 2](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_2)
- ** Bug_3 **: Contact -> Corruption of data [Bug 3](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_3)
- ** Bug_4 **: Contacts -> Balance -> The balance doesn't update when entering new value it stays the same [Bug 4](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_4)
- ** Bug_5 **: Contact -> Delete -> When Deleting the Contact, The contact isn't fully deleted from the DB [Bug 5](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_5)
- ** Bug_6 **: Invoice -> ID -> ID is not unique and multiple invoice can have the same ID [Bug 6](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_6)
- ** Bug_7 **: Invoice -> Status -> status could be changed to any numbers not only 1, 2 and 3 [Bug 7](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_7)
- ** Bug_8 **: Invoice -> Data corruption because id is not unique and more than one invoice could have the same id [Bug 8](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_8)
- ** Bug_9 **: Invoice -> unable to change the invoice to return [Bug 9](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_9)
- ** Bug_10 **: Invoice -> Unable to pay the amount of feeds [Bug 10](https://github.com/MMousa126/API-Testing---InMemoryAuthAPI-V1/tree/master/Issues/issue_10)



By thoroughly testing these areas, we aim to ensure that the API meets all functional requirements for the CRM module.


