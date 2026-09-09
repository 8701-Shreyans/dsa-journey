# Find Customer Referee

| Field | Value |
|-------|-------|
| **Platform** | LeetCode |
| **Difficulty** | Easy |
| **Language** | mysql |
| **Solved On** | September 9, 2026 |
| **Tags** | Database |
| **Link** | [View Problem](https://leetcode.com/problems/find-customer-referee/) |
| **Runtime** | 95 ms |
| **Memory** | 0B |

## Problem Description

<p>Table: <code>Customer</code></p>

<pre>+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| id          | int     |
| name        | varchar |
| referee_id  | int     |
+-------------+---------+
In SQL, id is the primary key column for this table.
Each row of this table indicates the id of a customer, their name, and the id of the customer who referred them.
</pre>

<p>&nbsp;</p>

<p>Find the names of the customer that are either:</p>

<ol>
	<li><strong>referred by</strong>&nbsp;any&nbsp;customer with&nbsp;<code>id != 2</code>.</li>
	<li><strong>not referred by</strong> any customer.</li>
</ol>

<p>Return the result table in <strong>any order</strong>.</p>

<p>The result format is in the following example.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre><strong>Input:</strong> 
Customer table:
+----+------+------------+
| id | name | referee_id |
+----+------+------------+
| 1  | Will | null       |
| 2  | Jane | null       |
| 3  | Alex | 2          |
| 4  | Bill | null       |
| 5  | Zack | 1          |
| 6  | Mark | 2          |
+----+------+------------+
<strong>Output:</strong> 
+------+
| name |
+------+
| Will |
| Jane |
| Bill |
| Zack |
+------+
</pre>


##  Top Community Optimal Approach

<details>
<summary>Click to expand</summary>

**Title**: simple query with easy NULL handling using COALESCE
**Author**: [@utkarshaggarwal74](https://leetcode.com/utkarshaggarwal74/)
**Upvotes**: 632 👍
**Link**: [View Original Post](https://leetcode.com/problems/find-customer-referee/solutions/2398637/)

---

SELECT name
FROM Customer
WHERE COALESCE(referee_id,0) <> 2;

here COALESCE  is used to replace NULL values with zero before checking whether it is equal to 2 or not.

if you understand the solution plz do upvote it.

</details>
