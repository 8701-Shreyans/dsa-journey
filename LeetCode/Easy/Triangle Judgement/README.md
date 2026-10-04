# Triangle Judgement

| Field | Value |
|-------|-------|
| **Platform** | LeetCode |
| **Difficulty** | Easy |
| **Language** | mysql |
| **Solved On** | October 4, 2026 |
| **Tags** | Database |
| **Link** | [View Problem](https://leetcode.com/problems/triangle-judgement/) |
| **Runtime** | 269 ms |
| **Memory** | 0B |

## Problem Description

<p>Table: <code>Triangle</code></p>

<pre>+-------------+------+
| Column Name | Type |
+-------------+------+
| x           | int  |
| y           | int  |
| z           | int  |
+-------------+------+
In SQL, (x, y, z) is the primary key column for this table.
Each row of this table contains the lengths of three line segments.
</pre>

<p>&nbsp;</p>

<p>Report for every three line segments whether they can form a triangle.</p>

<p>Return the result table in <strong>any order</strong>.</p>

<p>The&nbsp;result format is in the following example.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre><strong>Input:</strong> 
Triangle table:
+----+----+----+
| x  | y  | z  |
+----+----+----+
| 13 | 15 | 30 |
| 10 | 20 | 15 |
+----+----+----+
<strong>Output:</strong> 
+----+----+----+----------+
| x  | y  | z  | triangle |
+----+----+----+----------+
| 13 | 15 | 30 | No       |
| 10 | 20 | 15 | Yes      |
+----+----+----+----------+
</pre>


##  Top Community Optimal Approach

<details>
<summary>Click to expand</summary>

**Title**: Attention Coders:  Determine if Three Sides Form a Triangle -  Beats 98.54%
**Author**: [@deepankyadav](https://leetcode.com/deepankyadav/)
**Upvotes**: 314 👍
**Link**: [View Original Post](https://leetcode.com/problems/triangle-judgement/solutions/3570676/)

---

# ***Please Upvote my solution, if you find it helpful ;)***

# Intuition
When we talk about triangles, we know that they are formed by connecting three sides. The intuition behind the Triangle Judgement query is to determine whether a given set of three sides can actually form a valid triangle or not. To do this, we need to check if the sum of any two sides is greater than the third side. If this condition holds true for all three combinations of sides, then we can say that a triangle can be formed. Otherwise, it means the sides cannot form a triangle.

# Approach
To solve the Triangle Judgement problem, we will create an IF statement to check the validity condition for each row in the "Triangle" table. The IF statement will compare the sum of two sides with the third side, for all possible combinations of sides. If all three comparisons are true, we will assign the value "Yes" to a new column called "triangle". If any of the comparisons are false, we will assign the value "No" to the "triangle" column. This approach allows us to easily evaluate the triangle formation condition for each set of sides.

# Complexity
- Time complexity:
The complexity of the Triangle Judgement query is quite simple. It involves only one SQL query with an IF statement. The time complexity is determined by the number of rows in the "Triangle" table since we need to evaluate the condition for each row.

- Space complexity:
The space complexity is low, as we don\'t require any additional data structures or variables.

# Code
```
# Write your MySQL query statement below

SELECT *, IF(x+y>z and y+z>x and z+x>y, "Yes", "No") as triangle FROM Triangle
```
***Please Upvote my solution, if you find it helpful ;)***
![6a87bc25-d70b-424f-9e60-7da6f345b82a_1673875931.8933976.jpeg](https://assets.leetcode.com/users/images/70f61842-bc2f-45aa-87dc-66aab8229f5c_1687456022.9749289.jpeg)



</details>
