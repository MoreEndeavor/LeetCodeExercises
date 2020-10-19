# LeetCodeExercises

this is my sql script for [177. Nth Highest Salary](https://leetcode.com/problems/nth-highest-salary/)

``` CREATE FUNCTION getNthHighestSalary(N INT) RETURNS INT
BEGIN
declare m INT;
set m = N-1;
  RETURN (
      # Write your MySQL query statement below.
      select
      Salary
      from
      (select distinct Salary from Employee order by Salary desc limit m, 1)
      as temp
  );
END ```
