## SQLBOLT

- https://sqlbolt.com/

### 查询

- [x] [SQL Lesson 1: SELECT queries 101]()
- [x] [SQL Lesson 2: Queries with constraints (Pt. 1)](https://sqlbolt.com/lesson/select_queries_with_constraints)
  - 一些操作符：`BETWEEN ... AND ...`/`NOT BETWEEN ... AND ...`
- [x] [SQL Lesson 3: Queries with constraints (Pt. 2)](https://sqlbolt.com/lesson/select_queries_with_constraints_pt_2)
- [x] [SQL Lesson 4: Filtering and sorting Query results](https://sqlbolt.com/lesson/filtering_sorting_query_results)
  - `DISTINCT`
  - `ORDER BY` 
  - `LIMIT x OFFSET x`
- [x] [SQL Review: Simple SELECT Queries](https://sqlbolt.com/lesson/select_queries_review)
- [x] [SQL Lesson 6: Multi-table queries with JOINs](https://sqlbolt.com/lesson/select_queries_with_joins)
  - `INNER JOIN` 等同于 `JOIN`
  - 结果集包含属于两个表的数据（*the resulting table only contains data that belongs in both of the tables*）
  - `SELECT column FROM my_table INNER JOIN another_table ON mytable.id = another_table.id WHERE condition(s) ORDER BY ... ASC/DESC LIMIT x OFFSET x`
- [x] [SQL Lesson 7: OUTER JOINs](https://sqlbolt.com/lesson/select_queries_with_outer_joins)
  - 两表数据不对称（即，`ON` 条件并不完全匹配）
  - `LEFT JOIN`：无论是否匹配 B 表中的行，均显示 A 表中的数据
  - `RIGHT JOIN`：无论是否匹配 A 表中的行，均显示 B 表中的数据
  - `FULL JOIn`：不管在另一表中是否存在匹配行，显示两表中的数据
  - `LEFT OUTER JOIN` / `RIGHT OUTER JOIN` / `FULL OUTER JOIN` 等价于 `LEFT JOIN` / `RIGHT JOIN` / `FULL JOIN`
- [x] [SQL Lesson 8: A short note on NULLs](https://sqlbolt.com/lesson/select_queries_with_nulls) 关于 `NULL` 的说明
  - 尽量减少数据库中 `NULL` 值的可能性
  - `NULL` 的替代方法：适当使用数据类型的默认值
  - 判断是否为空：`IS NULL` / `IS NOT NULL`
- [x] [SQL Lesson 9: Queries with expressions](https://sqlbolt.com/lesson/select_queries_with_expressions) 表达式的使用
  - `SELECT expression AS column ...`
- [x] [SQL Lesson 10: Queries with aggregates (Pt. 1)](https://sqlbolt.com/lesson/select_queries_with_aggregates) 聚合表达式
  - 聚合表达式列表：
    - `COUNT(*)` / `COUNT(column)`
    - `MIN(column)`
    - `MAX(column)`
    - `AVG(column)`
    - `SUM(column)`
  - 分组聚合：
    - `SELECT AGG_FUNC(column_or_expression) AS description, ... FROM mytable WHERE x GROUY BY column;`
    - `GROUP BY`：对指定列中拥有相同值的行进行分组（比如：计算喜剧电影的票房、动作电影的票房 -> `GROUY BY movie_type`）
- [x] [SQL Lesson 11: Queries with aggregates (Pt. 2)](https://sqlbolt.com/lesson/select_queries_with_aggregates_pt_2)
  - 筛选分组：使用 `HAVING` 子句
- [x] [SQL Lesson 12: Order of execution of a Query](https://sqlbolt.com/lesson/select_queries_order_of_execution)

### 增、改、删

- [x] [SQL Lesson 13: Inserting rows](https://sqlbolt.com/lesson/inserting_rows)
  - `INSERT INTO mytable (column1, column2) VALUES (valu1, value2), (value1, value2);`
- [x] [SQL Lesson 14: Updating rows](https://sqlbolt.com/lesson/updating_rows)
- [x] [SQL Lesson 15: Deleting rows](https://sqlbolt.com/lesson/deleting_rows)
  - `DELETE FROM mytable WHERE condition;`

### 创建表

- [x] [SQL Lesson 16: Creating tables](https://sqlbolt.com/lesson/creating_tables)