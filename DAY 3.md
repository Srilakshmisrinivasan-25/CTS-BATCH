&nbsp;                                                        **DAY 3**



&nbsp;use database5;

Database changed

mysql> CREATE TABLE reaction (

&nbsp;   -> id INT AUTO\_INCREMENT PRIMARY KEY,

&nbsp;   -> user\_name VARCHAR(100),

&nbsp;   -> reaction\_type VARCHAR(20),

&nbsp;   -> post\_id INT,

&nbsp;   -> created\_at DATETIME,

&nbsp;   -> location VARCHAR(100),

&nbsp;   -> mood\_level INT,

&nbsp;   -> comment TEXT

&nbsp;   -> );

ERROR 1050 (42S01): Table 'reaction' already exists

mysql> INSERT INTO reaction (user\_name, reaction\_type, post\_id, created\_at, location, mood\_level, comment) VALUES

&nbsp;   -> ('Alice', 'like', 101, '2025-08-07 10:15:00', 'New York', 8, 'Nice post!'),

&nbsp;   -> ('Bob', 'love', 102, '2025-08-06 14:20:00', 'Los Angeles', 9, 'Awesome!'),

&nbsp;   -> ('Charlie', 'angry', 101, '2025-08-05 09:10:00', 'Chicago', 3, NULL),

&nbsp;   -> ('Diana', 'wow', 103, '2025-08-07 08:30:00', 'Miami', 7, 'Interesting point.'),

&nbsp;   -> ('Ethan', 'sad', 104, '2025-08-04 16:45:00', 'Dallas', 2, NULL),

&nbsp;   -> ('Fiona', 'love', 102, '2025-08-07 12:00:00', 'Boston', 6, 'Well said.'),

&nbsp;   -> ('George', 'like', 105, '2025-08-03 11:25:00', 'Seattle', 5, NULL),

&nbsp;   -> ('Hannah', 'like', 106, '2025-08-07 15:50:00', 'Denver', 9, 'Completely agree!'),

&nbsp;   -> ('Ian', 'angry', 107, '2025-08-06 13:15:00', 'Phoenix', 4, 'Not okay with this.'),

&nbsp;   -> ('Jane', 'sad', 108, '2025-08-02 18:40:00', 'Atlanta', 1, NULL),

&nbsp;   -> ('Sam', 'like', 101, '2025-08-07 10:50:00', 'New York', 8, NULL),

&nbsp;   -> ('Anita', 'wow', 109, '2025-08-01 20:10:00', 'Houston', 7, NULL),

&nbsp;   -> ('Brian', 'love', 110, '2025-08-07 09:05:00', 'San Francisco', 10, 'Fantastic work!'),

&nbsp;   -> ('Catherine', 'like', 111, '2025-08-07 08:55:00', 'New York', 6, NULL),

&nbsp;   -> ('Daniel', 'angry', 112, '2025-08-05 17:35:00', 'Chicago', 2, NULL);

Query OK, 15 rows affected (0.01 sec)

Records: 15  Duplicates: 0  Warnings: 0



mysql> select \* from reaction;

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location      | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

|  1 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

|  2 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

|  3 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

|  4 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

|  5 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

|  6 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

|  7 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

|  8 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 10 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 11 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | ?                   |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 13 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 14 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 15 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 16 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

| 17 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 18 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 19 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 20 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

| 21 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 22 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

| 23 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 25 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 26 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | ?                   |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 28 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 29 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 30 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 31 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

| 32 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 33 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 34 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 35 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

| 36 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 37 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

| 38 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 40 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 41 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | NULL                |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 43 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 44 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 45 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

45 rows in set (0.00 sec)



mysql> select \* from reaction where user\_name like 'a%';

+----+-----------+---------------+---------+---------------------+----------+------------+------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location | mood\_level | comment    |

+----+-----------+---------------+---------+---------------------+----------+------------+------------+

|  1 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post! |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL       |

| 16 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post! |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL       |

| 31 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post! |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL       |

+----+-----------+---------------+---------+---------------------+----------+------------+------------+

6 rows in set (0.01 sec)



mysql> select user\_name as Reactor,reaction\_Type as Type from reaction;

+-----------+-------+

| Reactor   | Type  |

+-----------+-------+

| Alice     | like  |

| Bob       | love  |

| Charlie   | angry |

| Diana     | wow   |

| Ethan     | sad   |

| Fiona     | love  |

| George    | like  |

| Hannah    | like  |

| Ian       | angry |

| Jane      | sad   |

| Sam       | like  |

| Anita     | wow   |

| Brian     | love  |

| Catherine | like  |

| Daniel    | angry |

| Alice     | like  |

| Bob       | love  |

| Charlie   | angry |

| Diana     | wow   |

| Ethan     | sad   |

| Fiona     | love  |

| George    | like  |

| Hannah    | like  |

| Ian       | angry |

| Jane      | sad   |

| Sam       | like  |

| Anita     | wow   |

| Brian     | love  |

| Catherine | like  |

| Daniel    | angry |

| Alice     | like  |

| Bob       | love  |

| Charlie   | angry |

| Diana     | wow   |

| Ethan     | sad   |

| Fiona     | love  |

| George    | like  |

| Hannah    | like  |

| Ian       | angry |

| Jane      | sad   |

| Sam       | like  |

| Anita     | wow   |

| Brian     | love  |

| Catherine | like  |

| Daniel    | angry |

+-----------+-------+

45 rows in set (0.00 sec)



mysql> select \* from reaction where mood\_level between 4 and 8;

+----+-----------+---------------+---------+---------------------+----------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+----------+------------+---------------------+

|  1 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post!          |

|  4 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point.  |

|  6 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston   |          6 | Well said.          |

|  7 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle  |          5 | NULL                |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix  |          4 | Not okay with this. |

| 11 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York |          8 | ?                   |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL                |

| 14 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL                |

| 16 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post!          |

| 19 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point.  |

| 21 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston   |          6 | Well said.          |

| 22 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle  |          5 | NULL                |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix  |          4 | Not okay with this. |

| 26 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York |          8 | ?                   |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL                |

| 29 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL                |

| 31 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post!          |

| 34 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point.  |

| 36 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston   |          6 | Well said.          |

| 37 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle  |          5 | NULL                |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix  |          4 | Not okay with this. |

| 41 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York |          8 | NULL                |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL                |

| 44 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL                |

+----+-----------+---------------+---------+---------------------+----------+------------+---------------------+

24 rows in set (0.00 sec)



mysql> select select \* from reaction where mood\_level>7;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'select \* from reaction where mood\_level>7' at line 1

mysql> select \* from reaction where mood\_level between 4 and 8;

+----+-----------+---------------+---------+---------------------+----------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+----------+------------+---------------------+

|  1 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post!          |

|  4 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point.  |

|  6 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston   |          6 | Well said.          |

|  7 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle  |          5 | NULL                |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix  |          4 | Not okay with this. |

| 11 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York |          8 | ?                   |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL                |

| 14 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL                |

| 16 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post!          |

| 19 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point.  |

| 21 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston   |          6 | Well said.          |

| 22 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle  |          5 | NULL                |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix  |          4 | Not okay with this. |

| 26 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York |          8 | ?                   |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL                |

| 29 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL                |

| 31 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York |          8 | Nice post!          |

| 34 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point.  |

| 36 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston   |          6 | Well said.          |

| 37 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle  |          5 | NULL                |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix  |          4 | Not okay with this. |

| 41 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York |          8 | NULL                |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL                |

| 44 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL                |

+----+-----------+---------------+---------+---------------------+----------+------------+---------------------+

24 rows in set (0.00 sec)



mysql>  select \* from reaction where mood\_level like '7%';

+----+-----------+---------------+---------+---------------------+----------+------------+--------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location | mood\_level | comment            |

+----+-----------+---------------+---------+---------------------+----------+------------+--------------------+

|  4 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point. |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL               |

| 19 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point. |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL               |

| 34 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami    |          7 | Interesting point. |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston  |          7 | NULL               |

+----+-----------+---------------+---------+---------------------+----------+------------+--------------------+

6 rows in set (0.00 sec)



mysql> select \* from reaction where mood\_level like >'7%';

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '>'7%'' at line 1

mysql> select \* from reaction where reaction\_type love or angry;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'love or angry' at select \* from reaction where reaction\_type love or angry;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'love or angry' at line 1

mysql> SELECT \* FROM reaction

&nbsp;   -> WHERE reaction\_type = 'love' OR reaction\_type = 'angry';

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location      | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

|  2 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

|  3 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

|  6 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 13 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 15 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 17 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 18 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 21 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 28 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 30 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 32 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 33 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 36 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 43 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 45 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

18 rows in set (0.00 sec)



mysql> SELECT \* FROM reaction

&nbsp;   -> WHERE reaction\_type != 'sad';

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location      | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

|  1 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

|  2 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

|  3 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

|  4 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

|  6 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

|  7 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

|  8 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 11 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | ?                   |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 13 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 14 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 15 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 16 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

| 17 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 18 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 19 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 21 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 22 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

| 23 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 26 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | ?                   |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 28 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 29 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 30 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 31 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

| 32 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 33 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 34 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 36 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 37 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

| 38 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 41 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | NULL                |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 43 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 44 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 45 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

39 rows in set (0.00 sec)



mysql> SELECT \* FROM reaction

&nbsp;   -> WHERE reaction\_type IN ('love', 'angry');

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location      | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

|  2 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

|  3 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

|  6 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 13 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 15 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 17 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 18 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 21 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 28 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 30 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 32 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 33 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 36 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 43 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 45 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

18 rows in set (0.01 sec)



mysql> select \* from reaction where reaction is null;

ERROR 1054 (42S22): Unknown column 'reaction' in 'where clause'

mysql> select \* from reaction where reaction\_type is null;

Empty set (0.00 sec)



mysql> select \* from reaction where reaction\_type is not null;

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location      | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

|  1 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

|  2 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

|  3 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

|  4 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

|  5 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

|  6 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

|  7 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

|  8 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 10 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 11 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | ?                   |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 13 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 14 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 15 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 16 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

| 17 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 18 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 19 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 20 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

| 21 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 22 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

| 23 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 25 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 26 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | ?                   |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 28 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 29 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 30 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 31 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

| 32 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 33 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 34 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 35 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

| 36 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 37 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

| 38 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 40 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 41 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | NULL                |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 43 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 44 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 45 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

45 rows in set (0.00 sec)



mysql> select upper(user\_name) from reaction;

+------------------+

| upper(user\_name) |

+------------------+

| ALICE            |

| BOB              |

| CHARLIE          |

| DIANA            |

| ETHAN            |

| FIONA            |

| GEORGE           |

| HANNAH           |

| IAN              |

| JANE             |

| SAM              |

| ANITA            |

| BRIAN            |

| CATHERINE        |

| DANIEL           |

| ALICE            |

| BOB              |

| CHARLIE          |

| DIANA            |

| ETHAN            |

| FIONA            |

| GEORGE           |

| HANNAH           |

| IAN              |

| JANE             |

| SAM              |

| ANITA            |

| BRIAN            |

| CATHERINE        |

| DANIEL           |

| ALICE            |

| BOB              |

| CHARLIE          |

| DIANA            |

| ETHAN            |

| FIONA            |

| GEORGE           |

| HANNAH           |

| IAN              |

| JANE             |

| SAM              |

| ANITA            |

| BRIAN            |

| CATHERINE        |

| DANIEL           |

+------------------+

45 rows in set (0.01 sec)



mysql> select lower (reaction\_type) from reaction;

+-----------------------+

| lower (reaction\_type) |

+-----------------------+

| like                  |

| love                  |

| angry                 |

| wow                   |

| sad                   |

| love                  |

| like                  |

| like                  |

| angry                 |

| sad                   |

| like                  |

| wow                   |

| love                  |

| like                  |

| angry                 |

| like                  |

| love                  |

| angry                 |

| wow                   |

| sad                   |

| love                  |

| like                  |

| like                  |

| angry                 |

| sad                   |

| like                  |

| wow                   |

| love                  |

| like                  |

| angry                 |

| like                  |

| love                  |

| angry                 |

| wow                   |

| sad                   |

| love                  |

| like                  |

| like                  |

| angry                 |

| sad                   |

| like                  |

| wow                   |

| love                  |

| like                  |

| angry                 |

+-----------------------+

45 rows in set (0.03 sec)



mysql> select \* lower (reaction\_type) from reaction;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'lower (reaction\_type) from reaction' at line 1

mysql> select \* from reaction where user\_name like>'\_\_\_\_\_\_';

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '>'\_\_\_\_\_\_'' at line 1

mysql> SELECT \* FROM reaction

&nbsp;   -> WHERE LENGTH(user\_name) > 6;

+----+-----------+---------------+---------+---------------------+----------+------------+---------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location | mood\_level | comment |

+----+-----------+---------------+---------+---------------------+----------+------------+---------+

|  3 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago  |          3 | NULL    |

| 14 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL    |

| 18 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago  |          3 | NULL    |

| 29 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL    |

| 33 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago  |          3 | NULL    |

| 44 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York |          6 | NULL    |

+----+-----------+---------------+---------+---------------------+----------+------------+---------+

6 rows in set (0.01 sec)



mysql> select (now()) from reaction;

+---------------------+

| (now())             |

+---------------------+

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

| 2025-08-07 11:05:13 |

+---------------------+

45 rows in set (0.01 sec)



mysql>  select (now(created\_at)) from reaction;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'created\_at)) from reaction' at line 1

mysql> select date\_format(order\_date '%d'); from reaction;

ERROR 1582 (42000): Incorrect parameter count in the call to native function 'date\_format'

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'from reaction' at line 1

mysql> select created\_at(order\_date '%d'); from reaction;

ERROR 1584 (42000): Incorrect parameters in the call to stored function `created\_at`

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'from reaction' at line 1

mysql> SELECT DATE(created\_at) AS date\_only

&nbsp;   -> FROM reaction;

+------------+

| date\_only  |

+------------+

| 2025-08-07 |

| 2025-08-06 |

| 2025-08-05 |

| 2025-08-07 |

| 2025-08-04 |

| 2025-08-07 |

| 2025-08-03 |

| 2025-08-07 |

| 2025-08-06 |

| 2025-08-02 |

| 2025-08-07 |

| 2025-08-01 |

| 2025-08-07 |

| 2025-08-07 |

| 2025-08-05 |

| 2025-08-07 |

| 2025-08-06 |

| 2025-08-05 |

| 2025-08-07 |

| 2025-08-04 |

| 2025-08-07 |

| 2025-08-03 |

| 2025-08-07 |

| 2025-08-06 |

| 2025-08-02 |

| 2025-08-07 |

| 2025-08-01 |

| 2025-08-07 |

| 2025-08-07 |

| 2025-08-05 |

| 2025-08-07 |

| 2025-08-06 |

| 2025-08-05 |

| 2025-08-07 |

| 2025-08-04 |

| 2025-08-07 |

| 2025-08-03 |

| 2025-08-07 |

| 2025-08-06 |

| 2025-08-02 |

| 2025-08-07 |

| 2025-08-01 |

| 2025-08-07 |

| 2025-08-07 |

| 2025-08-05 |

+------------+

45 rows in set (0.01 sec)



mysql> select Round (mood\_level,5)from reaction;

+----------------------+

| Round (mood\_level,5) |

+----------------------+

|                    8 |

|                    9 |

|                    3 |

|                    7 |

|                    2 |

|                    6 |

|                    5 |

|                    9 |

|                    4 |

|                    1 |

|                    8 |

|                    7 |

|                   10 |

|                    6 |

|                    2 |

|                    8 |

|                    9 |

|                    3 |

|                    7 |

|                    2 |

|                    6 |

|                    5 |

|                    9 |

|                    4 |

|                    1 |

|                    8 |

|                    7 |

|                   10 |

|                    6 |

|                    2 |

|                    8 |

|                    9 |

|                    3 |

|                    7 |

|                    2 |

|                    6 |

|                    5 |

|                    9 |

|                    4 |

|                    1 |

|                    8 |

|                    7 |

|                   10 |

|                    6 |

|                    2 |

+----------------------+

45 rows in set (0.01 sec)



mysql> SELECT user\_name, mood\_level,

&nbsp;   ->        ROUND(mood\_level / 5.0) \* 5 AS rounded\_mood\_level

&nbsp;   -> FROM reaction;

+-----------+------------+--------------------+

| user\_name | mood\_level | rounded\_mood\_level |

+-----------+------------+--------------------+

| Alice     |          8 |                 10 |

| Bob       |          9 |                 10 |

| Charlie   |          3 |                  5 |

| Diana     |          7 |                  5 |

| Ethan     |          2 |                  0 |

| Fiona     |          6 |                  5 |

| George    |          5 |                  5 |

| Hannah    |          9 |                 10 |

| Ian       |          4 |                  5 |

| Jane      |          1 |                  0 |

| Sam       |          8 |                 10 |

| Anita     |          7 |                  5 |

| Brian     |         10 |                 10 |

| Catherine |          6 |                  5 |

| Daniel    |          2 |                  0 |

| Alice     |          8 |                 10 |

| Bob       |          9 |                 10 |

| Charlie   |          3 |                  5 |

| Diana     |          7 |                  5 |

| Ethan     |          2 |                  0 |

| Fiona     |          6 |                  5 |

| George    |          5 |                  5 |

| Hannah    |          9 |                 10 |

| Ian       |          4 |                  5 |

| Jane      |          1 |                  0 |

| Sam       |          8 |                 10 |

| Anita     |          7 |                  5 |

| Brian     |         10 |                 10 |

| Catherine |          6 |                  5 |

| Daniel    |          2 |                  0 |

| Alice     |          8 |                 10 |

| Bob       |          9 |                 10 |

| Charlie   |          3 |                  5 |

| Diana     |          7 |                  5 |

| Ethan     |          2 |                  0 |

| Fiona     |          6 |                  5 |

| George    |          5 |                  5 |

| Hannah    |          9 |                 10 |

| Ian       |          4 |                  5 |

| Jane      |          1 |                  0 |

| Sam       |          8 |                 10 |

| Anita     |          7 |                  5 |

| Brian     |         10 |                 10 |

| Catherine |          6 |                  5 |

| Daniel    |          2 |                  0 |

+-----------+------------+--------------------+

45 rows in set (0.01 sec)



mysql> select substr(user\_name,1,2)upper(user\_name) from reaction;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '(user\_name) from reaction' at line 1

mysql> select substr,upper(user\_name,1,2)from reaction;

ERROR 1582 (42000): Incorrect parameter count in the call to native function 'upper'

mysql> select \* from reaction where user\_name like '%an%';

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location      | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

|  4 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

|  5 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

|  8 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 10 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 13 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 15 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 19 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 20 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

| 23 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 25 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 28 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 30 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 34 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 35 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

| 38 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 40 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 43 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 45 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

24 rows in set (0.00 sec)



mysql> select substr(user\_name,1,2 upper) from reaction;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'upper) from reaction' at line 1

mysql> select upper(substr(user\_name,1,2)) from reaction;

+------------------------------+

| upper(substr(user\_name,1,2)) |

+------------------------------+

| AL                           |

| BO                           |

| CH                           |

| DI                           |

| ET                           |

| FI                           |

| GE                           |

| HA                           |

| IA                           |

| JA                           |

| SA                           |

| AN                           |

| BR                           |

| CA                           |

| DA                           |

| AL                           |

| BO                           |

| CH                           |

| DI                           |

| ET                           |

| FI                           |

| GE                           |

| HA                           |

| IA                           |

| JA                           |

| SA                           |

| AN                           |

| BR                           |

| CA                           |

| DA                           |

| AL                           |

| BO                           |

| CH                           |

| DI                           |

| ET                           |

| FI                           |

| GE                           |

| HA                           |

| IA                           |

| JA                           |

| SA                           |

| AN                           |

| BR                           |

| CA                           |

| DA                           |

+------------------------------+

45 rows in set (0.01 sec)



mysql> SELECT \* FROM reaction

&nbsp;   -> WHERE post\_id NOT IN (10, 20, 30);

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

| id | user\_name | reaction\_type | post\_id | created\_at          | location      | mood\_level | comment             |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

|  1 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

|  2 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

|  3 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

|  4 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

|  5 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

|  6 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

|  7 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

|  8 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

|  9 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 10 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 11 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | ?                   |

| 12 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 13 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 14 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 15 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 16 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

| 17 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 18 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 19 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 20 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

| 21 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 22 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

| 23 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 24 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 25 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 26 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | ?                   |

| 27 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 28 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 29 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 30 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

| 31 | Alice     | like          |     101 | 2025-08-07 10:15:00 | New York      |          8 | Nice post!          |

| 32 | Bob       | love          |     102 | 2025-08-06 14:20:00 | Los Angeles   |          9 | Awesome!            |

| 33 | Charlie   | angry         |     101 | 2025-08-05 09:10:00 | Chicago       |          3 | NULL                |

| 34 | Diana     | wow           |     103 | 2025-08-07 08:30:00 | Miami         |          7 | Interesting point.  |

| 35 | Ethan     | sad           |     104 | 2025-08-04 16:45:00 | Dallas        |          2 | NULL                |

| 36 | Fiona     | love          |     102 | 2025-08-07 12:00:00 | Boston        |          6 | Well said.          |

| 37 | George    | like          |     105 | 2025-08-03 11:25:00 | Seattle       |          5 | NULL                |

| 38 | Hannah    | like          |     106 | 2025-08-07 15:50:00 | Denver        |          9 | Completely agree!   |

| 39 | Ian       | angry         |     107 | 2025-08-06 13:15:00 | Phoenix       |          4 | Not okay with this. |

| 40 | Jane      | sad           |     108 | 2025-08-02 18:40:00 | Atlanta       |          1 | NULL                |

| 41 | Sam       | like          |     101 | 2025-08-07 10:50:00 | New York      |          8 | NULL                |

| 42 | Anita     | wow           |     109 | 2025-08-01 20:10:00 | Houston       |          7 | NULL                |

| 43 | Brian     | love          |     110 | 2025-08-07 09:05:00 | San Francisco |         10 | Fantastic work!     |

| 44 | Catherine | like          |     111 | 2025-08-07 08:55:00 | New York      |          6 | NULL                |

| 45 | Daniel    | angry         |     112 | 2025-08-05 17:35:00 | Chicago       |          2 | NULL                |

+----+-----------+---------------+---------+---------------------+---------------+------------+---------------------+

45 rows in set (0.00 sec)



2\.



&nbsp;use database6;

Database changed

mysql> CREATE TABLE users (

&nbsp;   -> id INT AUTO\_INCREMENT PRIMARY KEY,

&nbsp;   -> username VARCHAR(50),

&nbsp;   -> email VARCHAR(100),

&nbsp;   -> age INT,

&nbsp;   -> city VARCHAR(50),

&nbsp;   -> joined\_at DATETIME,

&nbsp;   -> status VARCHAR(20),

&nbsp;   -> bio TEXT

&nbsp;   -> );

ERROR 1050 (42S01): Table 'users' already exists

mysql> CREATE TABLE user (

&nbsp;   -> id INT AUTO\_INCREMENT PRIMARY KEY,

&nbsp;   -> username VARCHAR(50),

&nbsp;   -> email VARCHAR(100),

&nbsp;   -> age INT,

&nbsp;   -> city VARCHAR(50),

&nbsp;   -> joined\_at DATETIME,

&nbsp;   -> status VARCHAR(20),

&nbsp;   -> bio TEXT

&nbsp;   -> );

Query OK, 0 rows affected (0.06 sec)



mysql> INSERT INTO user (username, email, age, city, joined\_at, status, bio) VALUES

&nbsp;   -> ('Alice123', 'alice@example.com', 25, 'New York', '2025-08-01 10:00:00', 'active', 'Love hiking and travel.'),

&nbsp;   -> ('Bob99', NULL, 30, 'Los Angeles', '2025-07-25 09:30:00', 'inactive', NULL),

&nbsp;   -> ('CharlieX', 'charlie@example.com', 17, 'Chicago', '2025-08-05 14:45:00', 'active', 'High school student.'),

&nbsp;   -> ('Dana\_88', 'dana@example.com', 45, 'Miami', '2025-07-20 08:15:00', 'pending', NULL),

&nbsp;   -> ('Eli', 'eli@example.com', 60, 'Houston', '2025-08-07 13:20:00', 'active', 'Retired engineer.'),

&nbsp;   -> ('Fay', NULL, 33, 'Boston', '2025-08-02 11:10:00', 'inactive', 'Digital nomad.'),

&nbsp;   -> ('Gina007', 'gina@example.com', 28, 'Seattle', '2025-08-07 16:30:00', 'active', 'Coffee lover.');

Query OK, 7 rows affected (0.01 sec)

Records: 7  Duplicates: 0  Warnings: 0



mysql> select \* from user;

+----+----------+---------------------+------+-------------+---------------------+----------+-------------------------+

| id | username | email               | age  | city        | joined\_at           | status   | bio                     |

+----+----------+---------------------+------+-------------+---------------------+----------+-------------------------+

|  1 | Alice123 | alice@example.com   |   25 | New York    | 2025-08-01 10:00:00 | active   | Love hiking and travel. |

|  2 | Bob99    | NULL                |   30 | Los Angeles | 2025-07-25 09:30:00 | inactive | NULL                    |

|  3 | CharlieX | charlie@example.com |   17 | Chicago     | 2025-08-05 14:45:00 | active   | High school student.    |

|  4 | Dana\_88  | dana@example.com    |   45 | Miami       | 2025-07-20 08:15:00 | pending  | NULL                    |

|  5 | Eli      | eli@example.com     |   60 | Houston     | 2025-08-07 13:20:00 | active   | Retired engineer.       |

|  6 | Fay      | NULL                |   33 | Boston      | 2025-08-02 11:10:00 | inactive | Digital nomad.          |

|  7 | Gina007  | gina@example.com    |   28 | Seattle     | 2025-08-07 16:30:00 | active   | Coffee lover.           |

+----+----------+---------------------+------+-------------+---------------------+----------+-------------------------+                



3\.

&nbsp;use database7;

Database changed

mysql> Create the order table

&nbsp;   -> CREATE TABLE orders (

&nbsp;   -> order\_id INT AUTO\_INCREMENT PRIMARY KEY,

&nbsp;   ->

&nbsp;   -> customer\_name VARCHAR(100),

&nbsp;   -> product\_name VARCHAR(100),

&nbsp;   -> order\_date DATETIME,

&nbsp;   -> quantity INT,

&nbsp;   -> price DECIMAL(10,2),

&nbsp;   -> status VARCHAR(20),

&nbsp;   -> shipping\_address TEXT

&nbsp;   -> );

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'the order table

CREATE TABLE orders (

order\_id INT AUTO\_INCREMENT PRIMARY KEY,



' at line 1

mysql> CREATE TABLE orders (

&nbsp;   ->     order\_id INT AUTO\_INCREMENT PRIMARY KEY,

&nbsp;   ->     customer\_name VARCHAR(100),

&nbsp;   ->     product\_name VARCHAR(100),

&nbsp;   ->     order\_date DATETIME,

&nbsp;   ->     quantity INT,

&nbsp;   ->     price DECIMAL(10,2),

&nbsp;   ->     status VARCHAR(20),

&nbsp;   ->     shipping\_address TEXT

&nbsp;   -> );

Query OK, 0 rows affected (0.04 sec)



mysql> INSERT INTO orders (customer\_name, product\_name, order\_date, quantity, price, status, shipping\_address) VALUES

&nbsp;   -> ('Alice', 'Laptop', '2025-08-07 09:00:00', 1, 1200.00, 'shipped', '123 Main St, New York'),

&nbsp;   -> ('Bob', 'Phone', '2025-08-06 14:10:00', 2, 650.50, 'pending', '456 Elm St, LA'),

&nbsp;   -> ('Charlie', 'Tablet', '2025-08-05 11:25:00', 1, 300.00, 'cancelled', NULL),

&nbsp;   -> ('Diana', 'Monitor', '2025-08-07 15:40:00', 3, 199.99, 'shipped', '789 Pine St, Chicago'),

&nbsp;   -> ('Ethan', 'Keyboard', '2025-08-03 08:20:00', 5, 49.99, 'processing', NULL),

&nbsp;   -> ('Fiona', 'Mouse', '2025-08-04 10:30:00', 4, 25.00, 'shipped', '321 Oak St, Houston');

Query OK, 6 rows affected (0.01 sec)

Records: 6  Duplicates: 0  Warnings: 0



mysql> select \* from orders;

+----------+---------------+--------------+---------------------+----------+---------+------------+-----------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price   | status     | shipping\_address      |

+----------+---------------+--------------+---------------------+----------+---------+------------+-----------------------+

|        1 | Alice         | Laptop       | 2025-08-07 09:00:00 |        1 | 1200.00 | shipped    | 123 Main St, New York |

|        2 | Bob           | Phone        | 2025-08-06 14:10:00 |        2 |  650.50 | pending    | 456 Elm St, LA        |

|        3 | Charlie       | Tablet       | 2025-08-05 11:25:00 |        1 |  300.00 | cancelled  | NULL                  |

|        4 | Diana         | Monitor      | 2025-08-07 15:40:00 |        3 |  199.99 | shipped    | 789 Pine St, Chicago  |

|        5 | Ethan         | Keyboard     | 2025-08-03 08:20:00 |        5 |   49.99 | processing | NULL                  |

|        6 | Fiona         | Mouse        | 2025-08-04 10:30:00 |        4 |   25.00 | shipped    | 321 Oak St, Houston   |

+----------+---------------+--------------+---------------------+----------+---------+------------+-----------------------+

6 rows in set (0.00 sec)



mysql> select \* from orders where customer\_name like'%a';

+----------+---------------+--------------+---------------------+----------+--------+---------+----------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price  | status  | shipping\_address     |

+----------+---------------+--------------+---------------------+----------+--------+---------+----------------------+

|        4 | Diana         | Monitor      | 2025-08-07 15:40:00 |        3 | 199.99 | shipped | 789 Pine St, Chicago |

|        6 | Fiona         | Mouse        | 2025-08-04 10:30:00 |        4 |  25.00 | shipped | 321 Oak St, Houston  |

+----------+---------------+--------------+---------------------+----------+--------+---------+----------------------+

2 rows in set (0.00 sec)



mysql> selec \* from orders where product\_name like 'phone';

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'selec \* from orders where product\_name like 'phone'' at line 1

mysql> elec \* from orders where product\_name like '%phone%';

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'elec \* from orders where product\_name like '%phone%'' at line 1

mysql> select \* from orders where product\_name like '%phone%';

+----------+---------------+--------------+---------------------+----------+--------+---------+------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price  | status  | shipping\_address |

+----------+---------------+--------------+---------------------+----------+--------+---------+------------------+

|        2 | Bob           | Phone        | 2025-08-06 14:10:00 |        2 | 650.50 | pending | 456 Elm St, LA   |

+----------+---------------+--------------+---------------------+----------+--------+---------+------------------+

1 row in set (0.00 sec)



mysql> select \* from orders where product\_name like '\_\_\_\_\_';

+----------+---------------+--------------+---------------------+----------+--------+---------+---------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price  | status  | shipping\_address    |

+----------+---------------+--------------+---------------------+----------+--------+---------+---------------------+

|        2 | Bob           | Phone        | 2025-08-06 14:10:00 |        2 | 650.50 | pending | 456 Elm St, LA      |

|        6 | Fiona         | Mouse        | 2025-08-04 10:30:00 |        4 |  25.00 | shipped | 321 Oak St, Houston |

+----------+---------------+--------------+---------------------+----------+--------+---------+---------------------+

2 rows in set (0.00 sec)



mysql> select customer\_name as Buyer,Price as Unit\_price from orders;

+---------+------------+

| Buyer   | Unit\_price |

+---------+------------+

| Alice   |    1200.00 |

| Bob     |     650.50 |

| Charlie |     300.00 |

| Diana   |     199.99 |

| Ethan   |      49.99 |

| Fiona   |      25.00 |

+---------+------------+

6 rows in set (0.00 sec)



mysql> select concat(order\_id,quantity,price) as Total\_cost from orders;

+------------+

| Total\_cost |

+------------+

| 111200.00  |

| 22650.50   |

| 31300.00   |

| 43199.99   |

| 5549.99    |

| 6425.00    |

+------------+

6 rows in set (0.00 sec)



mysql> select  order\_id concat(order\_id,quantity,price) as Total\_cost from orders;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '(order\_id,quantity,price) as Total\_cost from orders' at line 1

mysql> SELECT \* FROM orders

&nbsp;   -> WHERE customer\_name != 'Bob';

+----------+---------------+--------------+---------------------+----------+---------+------------+-----------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price   | status     | shipping\_address      |

+----------+---------------+--------------+---------------------+----------+---------+------------+-----------------------+

|        1 | Alice         | Laptop       | 2025-08-07 09:00:00 |        1 | 1200.00 | shipped    | 123 Main St, New York |

|        3 | Charlie       | Tablet       | 2025-08-05 11:25:00 |        1 |  300.00 | cancelled  | NULL                  |

|        4 | Diana         | Monitor      | 2025-08-07 15:40:00 |        3 |  199.99 | shipped    | 789 Pine St, Chicago  |

|        5 | Ethan         | Keyboard     | 2025-08-03 08:20:00 |        5 |   49.99 | processing | NULL                  |

|        6 | Fiona         | Mouse        | 2025-08-04 10:30:00 |        4 |   25.00 | shipped    | 321 Oak St, Houston   |

+----------+---------------+--------------+---------------------+----------+---------+------------+-----------------------+

5 rows in set (0.00 sec)



mysql> select \* from orders where status != 'shipped';

+----------+---------------+--------------+---------------------+----------+--------+------------+------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price  | status     | shipping\_address |

+----------+---------------+--------------+---------------------+----------+--------+------------+------------------+

|        2 | Bob           | Phone        | 2025-08-06 14:10:00 |        2 | 650.50 | pending    | 456 Elm St, LA   |

|        3 | Charlie       | Tablet       | 2025-08-05 11:25:00 |        1 | 300.00 | cancelled  | NULL             |

|        5 | Ethan         | Keyboard     | 2025-08-03 08:20:00 |        5 |  49.99 | processing | NULL             |

+----------+---------------+--------------+---------------------+----------+--------+------------+------------------+

3 rows in set (0.00 sec)



mysql> select \* from orders where quantity>2 and <500;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '<500' at line 1

mysql> > select quantity from orders where quantity>2 and <500;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '> select quantity from orders where quantity>2 and <500' at line 1

mysql>  select \* from orders where quantity >'2'and <'500';

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '<'500'' at line 1

mysql> select \* from orders where quantity '>' 2and '<' 500;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ''>' 2and '<' 500' at line 1

mysql> ^C

mysql> select \* from orders where quantity graterthan2 and lessthan500;

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'graterthan2 and lessthan500' at line 1

mysql> SELECT \* FROM orders

&nbsp;   -> WHERE quantity > 2 AND quantity < 500;

+----------+---------------+--------------+---------------------+----------+--------+------------+----------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price  | status     | shipping\_address     |

+----------+---------------+--------------+---------------------+----------+--------+------------+----------------------+

|        4 | Diana         | Monitor      | 2025-08-07 15:40:00 |        3 | 199.99 | shipped    | 789 Pine St, Chicago |

|        5 | Ethan         | Keyboard     | 2025-08-03 08:20:00 |        5 |  49.99 | processing | NULL                 |

|        6 | Fiona         | Mouse        | 2025-08-04 10:30:00 |        4 |  25.00 | shipped    | 321 Oak St, Houston  |

+----------+---------------+--------------+---------------------+----------+--------+------------+----------------------+

3 rows in set (0.00 sec)



mysql> select \* from orders where customer\_name='ALICE'and status='shipped';

+----------+---------------+--------------+---------------------+----------+---------+---------+-----------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price   | status  | shipping\_address      |

+----------+---------------+--------------+---------------------+----------+---------+---------+-----------------------+

|        1 | Alice         | Laptop       | 2025-08-07 09:00:00 |        1 | 1200.00 | shipped | 123 Main St, New York |

+----------+---------------+--------------+---------------------+----------+---------+---------+-----------------------+

1 row in set (0.00 sec)



mysql>  select \* from orders where status 'pending' or'processing';

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ''pending' or'processing'' at line 1

mysql> select \* from orders where status ='pending' or status='processing';

+----------+---------------+--------------+---------------------+----------+--------+------------+------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price  | status     | shipping\_address |

+----------+---------------+--------------+---------------------+----------+--------+------------+------------------+

|        2 | Bob           | Phone        | 2025-08-06 14:10:00 |        2 | 650.50 | pending    | 456 Elm St, LA   |

|        5 | Ethan         | Keyboard     | 2025-08-03 08:20:00 |        5 |  49.99 | processing | NULL             |

+----------+---------------+--------------+---------------------+----------+--------+------------+------------------+

2 rows in set (0.00 sec)

&nbsp;      select \* from orders where customer\_name='alice' or customer\_name='diana';

+----------+---------------+--------------+---------------------+----------+---------+---------+-----------------------+

| order\_id | customer\_name | product\_name | order\_date          | quantity | price   | status  | shipping\_address      |

+----------+---------------+--------------+---------------------+----------+---------+---------+-----------------------+

|        1 | Alice         | Laptop       | 2025-08-07 09:00:00 |        1 | 1200.00 | shipped | 123 Main St, New York |

|        4 | Diana         | Monitor      | 2025-08-07 15:40:00 |        3 |  199.99 | shipped | 789 Pine St, Chicago  |

+----------+---------------+--------------+---------------------+----------+---------+---------+-----------------------+

