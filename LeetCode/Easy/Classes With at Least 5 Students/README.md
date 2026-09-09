# Classes With at Least 5 Students

| Field | Value |
|-------|-------|
| **Platform** | LeetCode |
| **Difficulty** | Easy |
| **Language** | mysql |
| **Solved On** | September 9, 2026 |
| **Tags** | Database |
| **Link** | [View Problem](https://leetcode.com/problems/classes-with-at-least-5-students/) |
| **Runtime** | 85 ms |
| **Memory** | 0B |

## Problem Description

<p>Table: <code>Courses</code></p>

<pre>+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| student     | varchar |
| class       | varchar |
+-------------+---------+
(student, class) is the primary key (combination of columns with unique values) for this table.
Each row of this table indicates the name of a student and the class in which they are enrolled.
</pre>

<p>&nbsp;</p>

<p>Write a solution to find all the classes that have <strong>at least five students</strong>.</p>

<p>Return the result table in <strong>any order</strong>.</p>

<p>The&nbsp;result format is in the following example.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre><strong>Input:</strong> 
Courses table:
+---------+----------+
| student | class    |
+---------+----------+
| A       | Math     |
| B       | English  |
| C       | Math     |
| D       | Biology  |
| E       | Math     |
| F       | Computer |
| G       | Math     |
| H       | Math     |
| I       | Math     |
+---------+----------+
<strong>Output:</strong> 
+---------+
| class   |
+---------+
| Math    |
+---------+
<strong>Explanation:</strong> 
- Math has 6 students, so we include it.
- English has 1 student, so we do not include it.
- Biology has 1 student, so we do not include it.
- Computer has 1 student, so we do not include it.
</pre>


##  Top Community Optimal Approach

<details>
<summary>Click to expand</summary>

**Title**: SQL ✅ |GROUP BY, HAVING✅✅✅| Easy to understand
**Author**: [@jasurbekaktamov081](https://leetcode.com/jasurbekaktamov081/)
**Upvotes**: 153 👍
**Link**: [View Original Post](https://leetcode.com/problems/classes-with-at-least-5-students/solutions/3811588/)

---

![image.png](https://assets.leetcode.com/users/images/9a9e8d4a-7d77-4bdb-b090-5cea018b7ca6_1690231204.902454.png)

# Code
```
SELECT class
FROM Courses
GROUP BY class
HAVING COUNT(student) >= 5;

```

</details>
