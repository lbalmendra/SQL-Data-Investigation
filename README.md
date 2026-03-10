# SQL Filter Applications: Security Investigation and Asset Management

## Project Description
This project was completed as part of the **Google Cybersecurity Professional Certificate**. The primary objective was to investigate potential security issues and manage organizational assets by applying SQL filters to internal databases. Using the MariaDB environment, I performed several security-related tasks to ensure system safety and data integrity.

---

## Security Investigation Scenarios

### 1. Retrieve After-Hours Failed Login Attempts
An investigation was required for a potential security incident occurring after 18:00. I filtered for login attempts that were both unsuccessful and occurred outside of standard business hours.

* **Query Logic**: Selected all columns from the `log_in_attempts` table.
* **Filters**: Applied a `WHERE` clause with the `AND` operator to combine two conditions: `login_time > '18:00'` and `success = 'FALSE'`.

### 2. Retrieve Login Attempts on Specific Dates
A suspicious event was identified on 2022-05-09. To understand the scope, I investigated all login activity from that day and the previous day (2022-05-08).

* **Query Logic**: Targeted the `log_in_attempts` table to find activity within a specific 48-hour window.
* **Filters**: Used the `OR` operator to include records matching either of the two specific dates.

### 3. Retrieve Login Attempts Outside of Mexico
During the investigation, it became necessary to audit login attempts originating from locations other than Mexico.

* **Query Logic**: Used pattern matching to identify geographical data.
* **Filters**: Employed `NOT` and `LIKE` with the pattern `'MEX%'`. 
* **Wildcards**: The `%` wildcard was used to ensure the filter excluded both 'MEX' and 'MEXICO' entries from the results.

---

## Asset Management and Updates

### 4. Retrieve Employees in Marketing
To facilitate a hardware update for the Marketing department in the East building, I extracted a specific list of employee machines.

* **Query Logic**: Joined departmental and location criteria.
* **Filters**: Used `AND` to filter for `department = 'Marketing'` and `office LIKE 'East%'`.

### 5. Retrieve Employees in Finance or Sales
The security team scheduled a specialized update for all computers belonging to the Finance and Sales departments.

* **Query Logic**: Identified all users belonging to either department for a batch update.
* **Filters**: Used the `OR` operator to capture employees if they belonged to either the 'Finance' or 'Sales' teams.

### 6. Retrieve All Employees Not in IT
A general security patch was required for all staff members, excluding the Information Technology department.

* **Query Logic**: Used exclusion logic to generate a list of all non-IT personnel.
* **Filters**: Applied the `NOT` operator on the `department` column to filter out 'Information Technology'.

---

## Technical Summary
This project demonstrates proficiency in SQL data retrieval for cybersecurity purposes. Key skills applied include:
* **Database Interaction**: Querying the `log_in_attempts` and `employees` tables.
* **Logic Operators**: Strategic use of `AND`, `OR`, and `NOT` for precise data segmentation.
* **Advanced Filtering**: Utilizing `LIKE` and `%` wildcards for flexible pattern matching in security logs.