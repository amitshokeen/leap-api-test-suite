# LEAP API Test Suite (Postman)

This repository contains a complete Postman-based automated API test suite that validates CRUD operations on an Employee resource using [crudcrud.com](https://crudcrud.com), a temporary mock REST API.

---

## Included Files

All files are under the `/postman` folder:

| File | Description |
|------|-------------|
| `Employee_API_Test_Suite.postman_collection.json` | Main Postman collection including CRUD, data-driven, verification, and schema tests |
| `crudcrud_environment.postman_environment.json`   | Postman environment with `crudId` placeholder |
| `employee_data.json`                              | Single employee data used in `CRUD Flow` |
| `employee_data_set.json`                          | Multiple employee records used for data-driven tests |
| `Employee_Negative_Tests.postman_collection.json` | Collection focused on negative input validation via Postman test scripts |

---

## Pre-Requisite: Setup crudcrud.com

1. Visit [https://crudcrud.com](https://crudcrud.com)
2. Copy your **unique 24-hour API base URL** (e.g. `https://crudcrud.com/api/abc123xyz`)
3. Extract only the `crudId` part (`abc123xyz`)
4. In Postman, import `crudcrud_environment.postman_environment.json`
5. Set the environment variable `crudId` with your unique value
6. Select `crudcrud_environment` in the top-right of Postman UI

---

## Running the Test Suite

### Collection name
- `Employee_API_Test_Suite.postman_collection.json`

### Folder: `CRUD Flow`
- Data File: `employee_data.json`
- Purpose: Demonstrates full lifecycle (Create → Read → Update → Delete) for one employee

### Folder: `Multiple Employees - Create`
- Data File: `employee_data_set.json`
- Purpose: Runs a data-driven POST test using 3 different employees

### Folder: `Multiple Employees - Verify`
- Data File: *Not required*
- Purpose: Confirms all 3 employees were created successfully via GET

### Folder: `Negative Tests`
- Data File: *Not required*
- Purpose: Validates input format by simulating backend validation inside Postman test scripts

> !! Note: Since crudcrud.com does not enforce validation, these tests rely on self-written scripts that fail on missing or invalid fields (e.g., missing email, invalid mobile).

---

## Import Instructions

1. Open Postman
2. Import the following files (via File > Import):
   - `Employee_API_Test_Suite.postman_collection.json`
   - `crudcrud_environment.postman_environment.json`
3. For data-driven folders, go to Collection Runner:
   - Select the appropriate folder
   - Upload the correct data file (`employee_data.json` or `employee_data_set.json`)
   - Click Run

---

## Notes

- **crudcrud.com** endpoints expire every 24 hours. Ensure you update the `crudId` in your environment before running.
- All tests include clear assertions, schema validations, and simulated backend validations.
- No external dependencies — fully portable with just Postman.

---

## Author

Amit Shokeen  
