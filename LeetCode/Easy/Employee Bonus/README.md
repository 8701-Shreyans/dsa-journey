# Employee Bonus

| Field | Value |
|-------|-------|
| **Platform** | LeetCode |
| **Difficulty** | Easy |
| **Language** | mysql |
| **Solved On** | September 9, 2026 |
| **Tags** | Database |
| **Link** | [View Problem](https://leetcode.com/problems/employee-bonus/) |
| **Runtime** | 92 ms |
| **Memory** | 0B |

## Problem Description

<p>Table: <code>Employee</code></p>

<pre>+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| empId       | int     |
| name        | varchar |
| supervisor  | int     |
| salary      | int     |
+-------------+---------+
empId is the column with unique values for this table.
Each row of this table indicates the name and the ID of an employee in addition to their salary and the id of their manager.
</pre>

<p>&nbsp;</p>

<p>Table: <code>Bonus</code></p>

<pre>+-------------+------+
| Column Name | Type |
+-------------+------+
| empId       | int  |
| bonus       | int  |
+-------------+------+
empId is the column of unique values for this table.
empId is a foreign key (reference column) to empId from the Employee table.
Each row of this table contains the id of an employee and their respective bonus.
</pre>

<p>&nbsp;</p>

<p>Write a solution to report the name and bonus amount of each employee who satisfies either of the following:</p>

<ul>
	<li>The employee has a bonus <strong>less than</strong> <code>1000</code>.</li>
	<li>The employee did not get any bonus.</li>
</ul>

<p>Return the result table in <strong>any order</strong>.</p>

<p>The&nbsp;result format is in the following example.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre><strong>Input:</strong> 
Employee table:
+-------+--------+------------+--------+
| empId | name   | supervisor | salary |
+-------+--------+------------+--------+
| 3     | Brad   | null       | 4000   |
| 1     | John   | 3          | 1000   |
| 2     | Dan    | 3          | 2000   |
| 4     | Thomas | 3          | 4000   |
+-------+--------+------------+--------+
Bonus table:
+-------+-------+
| empId | bonus |
+-------+-------+
| 2     | 500   |
| 4     | 2000  |
+-------+-------+
<strong>Output:</strong> 
+------+-------+
| name | bonus |
+------+-------+
| Brad | null  |
| John | null  |
| Dan  | 500   |
+------+-------+
</pre>


##  Top Community Optimal Approach

<details>
<summary>Click to expand</summary>

**Title**: LEFT JOIN Solution.🤹‍♂️
**Author**: [@ravithemore](https://leetcode.com/ravithemore/)
**Upvotes**: 625 👍
**Link**: [View Original Post](https://leetcode.com/problems/employee-bonus/solutions/3788149/)

---

This one is very simple as you have to use `LEFT JOIN` You use Normally just the thing here is that you will have to aslo include the one whose value is null so use `IS NULL`  for bonus.

# Code
```
# Write your MySQL query statement below
SELECT Employee.name,Bonus.bonus FROM Employee 
LEFT JOIN Bonus ON Employee.empID = Bonus.empID
WHERE bonus < 1000 OR Bonus IS NULL ;
```
![images.jpeg](https://assets.leetcode.com/users/images/539bc15d-1677-4947-b269-fe68849adc78_1689777081.6770382.jpeg)



</details>
