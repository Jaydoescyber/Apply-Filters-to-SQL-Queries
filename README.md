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

![image](https://github.com/user-attachments/assets/dc55c796-c23b-4550-83f2-21a2328c82cf)


### Retrieve Login Attempts on Specific Dates
**Ref 2: Querying login attempts from May 8-9, 2022.**
```sql
SELECT * FROM log_in_attempts
WHERE login_date = '2022-05-08' OR Login_date = '2022-05-09';
```

![image](https://github.com/user-attachments/assets/f0ae8d7d-9675-4763-a040-b87c144ebdda)


### Retrieve Login Attempts Outside of Mexico
**Ref 3: Filtering login attempts originating outside Mexico.**
```sql
SELECT * FROM log_in_attempts
WHERE country NOT LIKE 'MEX%';
```

![image](https://github.com/user-attachments/assets/60b7e1f8-a991-4aa0-b885-9361dc2f6e2b)


### Retrieve Employees in Marketing Department
**Ref 4: Identifying employees in Marketing located in the East building.**
```sql
SELECT * FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
```

![image](https://github.com/user-attachments/assets/6196b72e-d7cd-4b87-a5f4-d110a8716e0c)


### Retrieve Employees in Finance or Sales
**Ref 5: Filtering employees in Finance or Sales departments.**
```sql
SELECT * FROM employees
WHERE department IN ('Finance', 'Sales');
```

![image](https://github.com/user-attachments/assets/457c0659-a3fd-4e81-b3c9-b8e4c535be5e)


### Retrieve All Employees Not in IT
**Ref 6: Querying employees outside of the IT department.**
```sql
SELECT * FROM employees
WHERE department != 'IT';
```

![image](https://github.com/user-attachments/assets/8c56e2f4-ecd2-4728-bd16-3301b373ceb4)


## Summary
This project utilized SQL queries to analyze login attempts and employee access, helping to identify potential security risks. Logical operators and wildcard filtering were crucial in refining searches and improving security monitoring strategies.
```
