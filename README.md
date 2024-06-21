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

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/97db165a-677b-4303-852a-bc223cac2adc)

*Ref 2: Text goes here*


### Step Three

Description: Retrieve login attempts outside of Mexico

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/50e83c57-d32e-4f63-9c56-620737722636)

*Ref 3: Text goes here*


### Step Four

Description: Retrieve employees in Marketing

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/7c391555-6998-433c-9193-9a4d5b2b5430)

*Ref 4: Text goes here*


### Step Five

Description: Retrieve employees in Finance or Sales

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/e76f46e3-523a-4e52-9165-f440b11c6826)

*Ref 5: Text goes here*


### Step Six

Description: Retrieve all employees not in IT

![image](https://github.com/aehumphrey/SQL-Filtering-Investigation-Project/assets/33531835/2f71cf9f-ca13-40d4-9d22-373ba0d4a533)

*Ref 6: Text goes here*

## Summary











