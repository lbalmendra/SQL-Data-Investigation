# Apply filters to SQL queries [cite: 1]

## Project Description [cite: 2]
The organization is working to make their system more secure[cite: 3]. To ensure system safety, I investigate all potential security issues and update employee computers as needed[cite: 4]. The following steps provide examples of SQL filters used to perform security-related tasks[cite: 5].

---

## Security Investigation Scenarios

### 1. Retrieve After-Hours Failed Login Attempts [cite: 6]
There was a potential security incident that occurred after business hours (18:00)[cite: 7]. I created a SQL query to filter for failed login attempts that occurred after this time[cite: 8].

* **Query Logic**: I selected all data from the `log_in_attempts` table[cite: 10].
* **Filter**: Used a `WHERE` clause with an `AND` operator to output only login attempts that occurred after 18:00 and were unsuccessful[cite: 11].

### 2. Retrieve Login Attempts on Specific Dates [cite: 12]
A suspicious event occurred on 2022-05-09[cite: 13]. Any login activity that happened on this date or on the day before needed to be investigated[cite: 13].

* **Query Logic**: This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08[cite: 15].
* **Filter**: Used a `WHERE` clause with an `OR` operator to filter for either date[cite: 17].

### 3. Retrieve Login Attempts Outside of Mexico [cite: 18]
After investigating the organization’s data, I identified a need to filter for login attempts occurring outside of Mexico[cite: 19].

* **Query Logic**: Used a `WHERE` clause with `NOT` to filter for countries other than Mexico[cite: 22].
* **Pattern Matching**: I used `LIKE` with `'MEX%'` as the pattern because the dataset represents Mexico as both 'MEX' and 'MEXICO'[cite: 23].
* **Wildcards**: The percentage sign (`%`) was used to represent any number of unspecified characters[cite: 24].

---

## Asset Management and Updates

### 4. Retrieve Employees in Marketing [cite: 25]
My team needed to obtain information about employees in the ‘Marketing’ department to update certain machines[cite: 26].

* **Query Logic**: Filtered for employees in the Marketing department who also work in the East building[cite: 29].
* **Filter**: Used `department = 'Marketing'` and `office LIKE 'East%'` joined by the `AND` operator[cite: 30, 31].

### 5. Retrieve Employees in Finance or Sales [cite: 32]
The team needed to perform a different update to the computers of all employees in the Finance or the Sales department[cite: 33].

* **Query Logic**: This query returns all employees in the Finance and Sales departments[cite: 35].
* **Filter**: Used the `OR` operator because I wanted all employees who are in either department[cite: 38].

### 6. Retrieve All Employees Not in IT [cite: 41]
A security update was required for employees who are not in the Information Technology department[cite: 42].

* **Query Logic**: The query returns all employees not in the IT department[cite: 45].
* **Filter**: Used a `WHERE` clause with `NOT` to exclude that specific department[cite: 47].

---

## Summary [cite: 48]
I applied filters to SQL queries to get specific information on login attempts and employee machines[cite: 49]. I used two different tables, `log_in_attempts` and `employees`, and applied `AND`, `OR`, and `NOT` operators to filter for the specific information needed for each task[cite: 50]. I also used `LIKE` and the percentage sign (`%`) wildcard to filter for specific patterns[cite: 51].