## Running the Test Suite

### Collection name
- Employee_API_Test_Suite.postman_collection.json

### CRUD Flow
- Folder: `CRUD Flow`
- Data File: `employee_data.json` (1 record)
- Purpose: Create, update, and delete a single employee

### Multiple Employee Creation
- Folder: `Multiple Employees - Create`
- Data File: `employee_data_set.json` (3 records)
- Purpose: Demonstrates data-driven POST requests

### Multiple Employee Verification
- Folder: `Multiple Employees - Verify`
- No data file needed
- Purpose: Validates that all 3 employees were created

### Please note (related to negative tests)
- Since crudcrud.com does not enforce validation, these negative test cases are simulated using Postman test scripts that mimic common backend validation logic (e.g., missing fields, invalid formats). These assertions will fail if input data doesn't meet the expected criteria, even if the API responds with 201.
