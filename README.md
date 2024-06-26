# SQL Filtering and Investigation Project

## Objective

The SQL Filtering and Investigation Project simulated real-world cybersecurity investigation scenarios within a large organization. The primary objective was to analyze and address potential security issues discovered in login attempts and employee records. This project involved using SQL queries and filters effectively to investigate after-hours login attempts, review specific date-related login activities, and identify and mitigate suspicious login incidents originating outside of Mexico. This project emphasizes my development of SQL proficiency alongside my critical thinking skills and problem-solving abilities.

### Skills Learned

- Advanced proficiency in constructing SQL queries to filter and retrieve specific data subsets.
- Skill in filtering data based on precise date and time criteria using SQL functions.
- Expertise in using the LIKE operator with wildcards (%) for pattern matching in SQL queries.
- Ability to apply logical operators (AND, OR, NOT) to create complex filtering conditions in SQL.
- Knowledge of conducting forensic analysis by filtering data to investigate security incidents.
- Competence in documenting SQL queries and findings comprehensively for technical reports.

### Tools Used

- MySQL (MariaDB)

## Steps

### Step One 

Description: Retrieve after hours log-in attempts

A potential security incident occurred after business hours. All unsuccessful after-hours login attempts need to be investigated.

The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours:

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/ccf1669e-a2b7-45bd-98e9-a081ed633e4c)

*Ref 1. Using filters to identify unsuccessful after -hours login attempts*

This query filters for failed login attempts that occurred after-hours (18:00). First, I selected the log_in_attempts table. Next, I used WHERE and AND to filter these results. My first condition is login_time > ‘18:00’, which filters for login attempts that occurred after 18:00 (the close of business). The second condition is success = FALSE, which limits these results to display only failed login attempts. 

### Step Two

Description: Retrieve login attempts on specific dates

The security team has identified a suspicious event, which occurred on 2022-05-09. Login activity that occurred on this date or the date before should be identified and investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/97db165a-677b-4303-852a-bc223cac2adc)

*Ref 2: Using filters to identify login attempts on specific dates*

This query filters for login attempts that occurred on 2022-05-09 or 2022-05-08. First, I selected the log_in_attempts table. Next, I used WHERE and OR to filter these results. The first condition is login_date = ‘2022-05-09’, which filters for login attempts (both successful and unsuccessful) on 2022-05-09. The second condition is login_date = ‘2022-05-08’, which filters for login attempts (both successful and unsuccessful) on 2022-05-08. 

### Step Three

Description: Retrieve login attempts outside of Mexico

After further investigation, the team has determined that the suspicious activity originated outside of Mexico. Therefore, any login attempts outside of Mexico should be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico:

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/50e83c57-d32e-4f63-9c56-620737722636)

*Ref 3: Using filters to identify login attempts outside of Mexico*

This query filters for login attempts that occurred in countries other than Mexico.  First, I selected the log_in_attempts table. Next, I used WHERE and NOT to filter these results. I used LIKE with MEX% because Mexico appears in this dataset as both MEX and MEXICO. The percentage sign (%) acts as a wildcard when used with LIKE.


### Step Four

Description: Retrieve employees in Marketing

The team wants to update the computers for certain employees in the Marketing department. Employees in the Marketing department whose offices are in the East building need new computers. I need to filter the dataset to identify these individuals.

The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building:

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/7c391555-6998-433c-9193-9a4d5b2b5430)

*Ref 4: Filtering for employees who work in Marketing in the East building*

This query filters for all employees in the Marketing department in the East building. First, I selected the employees table. Next, I used WHERE and AND to filter these results. I used LIKE with East% because data in the ‘office’ column represents offices in the East building as ‘East - [office number].’

My first condition is department = ‘Marketing’, which filters for employees in the Marketing department. My second condition is office LIKE ‘East%’, which filters for employees in the East building. Both conditions must be met to appear in the output of this query.


### Step Five

Description: Retrieve employees in Finance or Sales

The machines used by employees working in Finance and Sales need to be updated as well. However, their machines need a different security update than those working in Marketing, so I need to create another query.

The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Finance or Sales departments:

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/e76f46e3-523a-4e52-9165-f440b11c6826)

*Ref 5: Filtering for employees who work in Finance or Sales*

This query filters for employees in Finance and Sales. First, I selected the employees table. Next, I used WHERE and OR to filter these results. I used OR instead of AND because I’m filtering for employees who are in either Finance or Sales, rather than employees who are in Finance and Sales.

My first condition is department = ‘Finance’, which filters for employees working in Finance. My second condition is department = ‘Sales’, which filters for employees working in Sales.

### Step Six

Description: Retrieve all employees not in IT

My organization has requested one last security update, which will be applied to employees who do not work in Information Technology.

The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department.

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/2f71cf9f-ca13-40d4-9d22-373ba0d4a533)

*Ref 6: Filtering for employees who do not work in Information Technology*

This query filters for employees who are not in Information Technology.  First, I selected the employees table. Next, I used WHERE and NOT to filter these results. 

## Summary

This lab demonstrates my ability to apply filters to SQL queries. I used two different tables: log_in_attempts and employees. Within these tables, I used the AND, OR, and NOt operators to filter for specific information. I also used LIKE and the wildcard (%) to filter for patterns.












