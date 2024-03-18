---
Title: DBS101 Flipped Class4
categories: [DBS101, Flipped_Class4]
tags: [DBS101]
---
### Topic: Advanced Aggregate Dunctions
---
Greeting everyone! Before we dive into todays disscussion let's recollect on The GROUP BY clause. It is used to group the aggregate functions according to the specified column. However the GROUP BY clause doesn't perform aggregate operation on multiple levels of hierachy. For example, you can calculate the total of all employee salaries for each department in a company (one level of hierarchy) but you cannot calculate the total salary of all employees regardless of the department they work in (two levels of hierarchy). So we have advanced aggregate function like rollup and cube for such situation.

1.**Rank**: Ranking is a method used to order a set of data points in a specific order. In SQL, the RANK() function is used to assign a unique rank to each distinct row within a partition of a result set. 

#### Demo
SQL query given below ranks employees based on their scores, with the highest score receiving a rank of 1.

` SELECT name, score, RANK() OVER (ORDER BY score DESC) as rank
FROM scores; `
![alt text](<Screenshot from 2024-03-17 18-28-15.png>)
*If two or more rows have the same values, they will receive the same rank, and the next rank will be skipped. For example, if  Wangchuk and Yonten, both have a score of 96 and are tied for the first place, the next individual, Ranjung, will be ranked third, not second.*

2.**Windowing**: A window function performs a calculation across a set of table rows that are somehow related to the current row. This is comparable to the type of calculation that can be done with an aggregate function. But unlike regular aggregate functions, use of a window function does not cause rows to become grouped into a single output row — the rows retain their separate identities. 

#### Demo
Query given below display's each employee's name, their individual score, and the average score of their department. This is useful for understanding how each employee's score compares to the average score of their department.

`SELECT name, score, AVG(score) OVER (PARTITION BY department) as avg_score
FROM employees;`
![alt text](<Screenshot from 2024-03-17 18-33-58.png>)

3.**Pivoting**: Pivoting is a technique used in SQL to transform data from a row-oriented format into a column-oriented. This is particularly useful when we want to summarize data in a way that's easier to read or analyze.

##### Demo
Let's pivot the employees table example to show the total number of employees in each department. We want to transform the data so that each department becomes a column, and the values in these columns represent the total number of employees in each department.

    `SELECT SUM(CASE WHEN department = 'HR' THEN 1 ELSE 0 END) as HR,
       SUM(CASE WHEN department = 'IT' THEN 1 ELSE 0 END) as IT,
       SUM(CASE WHEN department = 'Finance' THEN 1 ELSE 0 END) as Finance,
       SUM(CASE WHEN department = 'Sales' THEN 1 ELSE 0 END) as Sales,
       SUM(CASE WHEN department = 'Marketing' THEN 1 ELSE 0 END) as Marketing
    FROM employees;`

![alt text](<Screenshot from 2024-03-17 21-49-22.png>)


4.**Rollup and Cube**: Rollup and Cube are the extensions of GROUP BY Clause. ROLLUP operators let us extend the functionality of GROUP BY clauses by calculating subtotals and grand totals for a set of columns. The CUBE operator is similar in functionality to the ROLLUP operator; however, the CUBE operator can calculate subtotals and grand totals for all permutations of the columns specified in it. If your 

You can also use ROLLUP to generate grand totals. If you ROLLUP all GROUP BY columns, you'll have an additional row with the grand total. ROLLUP is hierarchical; the order of the columns in the ROLLUP clause affects the output.
#### Demo for Rollup
Since PostgreSQL does not support WITH ROLLUP directly in the same way as MySQL or SQL Server, I have used GROUP BY and UNION ALL to manually add the grand total rows.In the code snippet given below 
i have calculated the subtotals and grand total separately and then combined them into a single result set.

`SELECT department, manager_id, SUM(salary) as total_salary
FROM employees
GROUP BY department, manager_id
UNION ALL
SELECT department, NULL, SUM(salary)
FROM employees
GROUP BY department
UNION ALL
SELECT NULL, NULL, SUM(salary)
FROM employees;
`
![alt text](<Screenshot from 2024-03-18 01-00-57.png>)


CUBE is much like its cousin ROLLUP, except that it's not hierarchical. It generates all possible group-level aggregations. CUBE-ing Country and Medal counts Country-level, Medal-level, and grand totals.

#### **Demo for Cube**
Query given below calculates the total salary for each combination of department and manager, as well as for each department, each manager, and a grand total for all departments and managers.
`SELECT department, manager_id, SUM(salary) as total_salary
FROM employees
GROUP BY department, manager_id WITH ROLLUP;
`
![alt text](<Screenshot from 2024-03-18 01-00-42.png>)