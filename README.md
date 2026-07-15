# MySQL HR Database Analysis
## 25 MySQL queries covering all major MySQL concepts

---

## Overview
Comprehensive SQL analysis of an HR Database containing
Employees, Departments, Jobs, Job history, Locations tables.
Demonstrated proficiency in all major MySQL concepts used in 
enterprise data analyst roles.

---

## Database Structure
| Table | Description |
|-------|-------------|
| EMPLOYEES | Employee details, salary |
| DEPARTMENTS | Department names and IDs |
| JOBS | Job titles and salary ranges |
| JOB_HISTORY | IDs and start date |
| LOCATIONS | Locations IDs |

---

## Concepts Covered
| Concepts | Description |
|----------|-------------|
| SELECT, WHERE, ORDER BY | Basic data retrieval and filtering |
| GROUP BY, HAVING | Aggregating and filtering grouped data |
| INNER JOIN | Combining matching rows from multiple tables |
| LEFT JOIN | All rows from left table including non-matches |
| Subqueries | Nested queries for filtered results |
| Correlated subquery | Inner query referencing outer query |
| CTE | Named temporary result sets for complex logic |
| Stored Procedures | Reusable SQL programs with IN and OUT parameters |
| Views | Virtual tables from saved SELECT queries |
| Window Functions | RANK, DENSE_RANK, ROW_NUMBER for ranking |
| Aggregations | COUNT, SUM, AVG, MAX, MIN |

**Total : 25 Queries**

---

## Key Queries Highlighted
**Query -- Career Summary Report**  
Combined CTE + 3 Table JOIN + DENSE_RANK Window Function +
Aggregation in a single query to generate complete employee career
overview including salary rank and job change history

**Query -- Second Highest Salary**  
Used DENSE_RANK() instead of RANK() to correctly handle
tied salaries -- ensures no salary rank is skipped when
duplicates exist

**Query -- Most Recent Job Change**  
Used ROW_NUMBER() with PARTITION BY EMPL_ID to identify
each employee's most recent job change from history table

**Query -- Employees Above Department Average**  
Used correlated subquery to compare each employee's salary against 
their specific department average -- not the company average

---

## Concepts Explained 

**Why DENSE_RANK over RANK?**  
RANK() skips numbers after ties -- 1,1,3,4  
DENSE_RANK() never skips -- 1,1,2,3  
For finding nth highest salary DENSE_RANK is always correct  

**Why CTE over Subquery?**  
CTEs are more readable, reusable within the same query
and easier to debug than deeply nested subqueries

**Stored Procedure Parameters**
- IN parameter -- accepts input value
- OUT parameter -- returns a value
- INOUT parameter -- both accepts and returns

---

## Files In This Repository
| File | Description |
|------|-------------|
| HR_SQL_PROJECT.sql | All 25 Queries with comments |
| screenshots/ | Query output screenshots |
| README.md | Project documentation |

---

## Tools Used
-MySQL
-phpMyAdmin
-IBM Skills Network Labs

---

## Key Learnings
- DENSE_RANK vs RANK -- handles ties differently
- CTEs make complex queries more readable
- Stored Procedures with IN/OUT parameters
- Window functions for ranking without collapsing rows
- Correlated subqueries for row-level comparisons
- Views for reusable virtual tables

---

## Other Projects
Visit my GitHub profile for more data analytics projects:
github.com/Nivetha7798

