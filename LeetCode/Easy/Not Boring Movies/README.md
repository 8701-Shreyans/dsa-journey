# Not Boring Movies

| Field | Value |
|-------|-------|
| **Platform** | LeetCode |
| **Difficulty** | Easy |
| **Language** | mysql |
| **Solved On** | October 5, 2026 |
| **Tags** | Database |
| **Link** | [View Problem](https://leetcode.com/problems/not-boring-movies/) |
| **Runtime** | 261 ms |
| **Memory** | 0B |

## Problem Description

<p>Table: <code>Cinema</code></p>

<pre>+----------------+----------+
| Column Name    | Type     |
+----------------+----------+
| id             | int      |
| movie          | varchar  |
| description    | varchar  |
| rating         | float    |
+----------------+----------+
id is the primary key (column with unique values) for this table.
Each row contains information about the name of a movie, its genre, and its rating.
rating is a 2 decimal places float in the range [0, 10]
</pre>

<p>&nbsp;</p>

<p>Write a solution to report the movies with an odd-numbered ID and a description that is not <code>"boring"</code>.</p>

<p>Return the result table ordered by <code>rating</code> <strong>in descending order</strong>.</p>

<p>The&nbsp;result format is in the following example.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre><strong>Input:</strong> 
Cinema table:
+----+------------+-------------+--------+
| id | movie      | description | rating |
+----+------------+-------------+--------+
| 1  | War        | great 3D    | 8.9    |
| 2  | Science    | fiction     | 8.5    |
| 3  | irish      | boring      | 6.2    |
| 4  | Ice song   | Fantacy     | 8.6    |
| 5  | House card | Interesting | 9.1    |
+----+------------+-------------+--------+
<strong>Output:</strong> 
+----+------------+-------------+--------+
| id | movie      | description | rating |
+----+------------+-------------+--------+
| 5  | House card | Interesting | 9.1    |
| 1  | War        | great 3D    | 8.9    |
+----+------------+-------------+--------+
<strong>Explanation:</strong> 
We have three movies with odd-numbered IDs: 1, 3, and 5. The movie with ID = 3 is boring so we do not include it in the answer.
</pre>


##  Top Community Optimal Approach

<details>
<summary>Click to expand</summary>

**Title**: ✅ 100% EASY || FAST 🔥|| CLEAN SOLUTION 🌟
**Author**: [@kartik_ksk7](https://leetcode.com/kartik_ksk7/)
**Upvotes**: 129 👍
**Link**: [View Original Post](https://leetcode.com/problems/not-boring-movies/solutions/3839979/)

---

IF THIS WILL BE HELPFUL TO YOU, PLEASE UPVOTE !

# Code
```
/* Write your PL/SQL query statement below */
SELECT * FROM Cinema WHERE MOD( id, 2) = 1 AND 

description <> \'boring\' ORDER BY rating DESC
```
![5kej8w.jpg](https://assets.leetcode.com/users/images/1c3b060c-d239-4c22-bc8b-7ccd74b5cb42_1690744091.6429114.jpeg)


</details>
