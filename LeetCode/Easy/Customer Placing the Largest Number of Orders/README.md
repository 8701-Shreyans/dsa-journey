# Customer Placing the Largest Number of Orders

| Field | Value |
|-------|-------|
| **Platform** | LeetCode |
| **Difficulty** | Easy |
| **Language** | mysql |
| **Solved On** | September 9, 2026 |
| **Tags** | Database |
| **Link** | [View Problem](https://leetcode.com/problems/customer-placing-the-largest-number-of-orders/) |
| **Runtime** | 70 ms |
| **Memory** | 0B |

## Problem Description

<p>Table: <code>Orders</code></p>

<pre>+-----------------+----------+
| Column Name     | Type     |
+-----------------+----------+
| order_number    | int      |
| customer_number | int      |
+-----------------+----------+
order_number is the primary key (column with unique values) for this table.
This table contains information about the order ID and the customer ID.
</pre>

<p>&nbsp;</p>

<p>Write a solution to find the <code>customer_number</code> for the customer who has placed <strong>the largest number of orders</strong>.</p>

<p>The test cases are generated so that <strong>exactly one customer</strong> will have placed more orders than any other customer.</p>

<p>The result format is in the following example.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre><strong>Input:</strong> 
Orders table:
+--------------+-----------------+
| order_number | customer_number |
+--------------+-----------------+
| 1            | 1               |
| 2            | 2               |
| 3            | 3               |
| 4            | 3               |
+--------------+-----------------+
<strong>Output:</strong> 
+-----------------+
| customer_number |
+-----------------+
| 3               |
+-----------------+
<strong>Explanation:</strong> 
The customer with number 3 has two orders, which is greater than either customer 1 or 2 because each of them only has one order. 
So the result is customer_number 3.
</pre>

<p>&nbsp;</p>
<p><strong>Follow up:</strong> What if more than one customer has the largest number of orders, can you find all the <code>customer_number</code> in this case?</p>


##  Top Community Optimal Approach

<details>
<summary>Click to expand</summary>

**Title**: MYSQL || Database
**Author**: [@shreya_dhanta](https://leetcode.com/shreya_dhanta/)
**Upvotes**: 154 👍
**Link**: [View Original Post](https://leetcode.com/problems/customer-placing-the-largest-number-of-orders/solutions/1916054/)

---

```
select customer_number from Orders group by customer_number order by count(customer_number) desc limit 1;

Explanation:
// First we need to select customer_number from Orders
// Then we need to group by the same column i.e customer_number 
// After that count the occurences of values in customer_number and then with the help of desc (descending) keyword I have converted it into descending order
// In the end I have used limit 1 so that only the max occurring element is shown in the output table


If this solution was helpful then do not forget to upvote :)

</details>
