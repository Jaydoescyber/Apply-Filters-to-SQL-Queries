# Apply-Filters-to-SQL-Queries

## Objective
The objective of this project was to enhance system security by analyzing login attempts and employee access data using SQL queries. By filtering and investigating specific patterns in login activity, I aimed to identify potential security threats and unauthorized access attempts.

## Skills Learned
- Advanced SQL filtering techniques for security analysis.
- Investigating failed login attempts and suspicious access patterns.
- Using SQL queries to analyze employee access data.
- Applying logical operators (AND, OR, NOT) to refine search results.
- Enhancing security monitoring through structured data analysis.

## Tools Used
- SQL Database Management System for querying and analyzing data.
- Security logs to investigate login attempts.
- Logical operators and wildcard filtering for precise data extraction.

## Steps

### Retrieve After-Hours Failed Login Attempts
**Ref 1: Filtering failed login attempts after 18:00.**
```sql
SELECT * FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;
```

### Retrieve Login Attempts on Specific Dates
**Ref 2: Querying login attempts from May 8-9, 2022.**
```sql
SELECT * FROM log_in_attempts
WHERE login_date IN ('2022-05-08', '2022-05-09');
```

### Retrieve Login Attempts Outside of Mexico
**Ref 3: Filtering login attempts originating outside Mexico.**
```sql
SELECT * FROM log_in_attempts
WHERE country NOT LIKE 'MEX%';
```

### Retrieve Employees in Marketing Department
**Ref 4: Identifying employees in Marketing located in the East building.**
```sql
SELECT * FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
```

### Retrieve Employees in Finance or Sales
**Ref 5: Filtering employees in Finance or Sales departments.**
```sql
SELECT * FROM employees
WHERE department IN ('Finance', 'Sales');
```

### Retrieve All Employees Not in IT
**Ref 6: Querying employees outside of the IT department.**
```sql
SELECT * FROM employees
WHERE department != 'IT';
```

## Summary
This project utilized SQL queries to analyze login attempts and employee access, helping to identify potential security risks. Logical operators and wildcard filtering were crucial in refining searches and improving security monitoring strategies.
```
