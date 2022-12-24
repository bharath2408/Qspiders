# 1. GROUP BY CLAUSE :

- GROUP BY CLAUSE is used to group the records.
- Group by clause executes row by row.
- To the group by clause we can pass col-name as an argument.
- Any clause which executes after group by clause, there must execute group by group.
- Col-name which is used in the group by clause is known as group by expression, this group by expression can be used along with multi row function in select clause.
- Group by clause can be used without where clause.

## SYNTAX :

```
 SELECT COL-NAME/EXPRESSION
 FROM TABLE-NAME
 [WHERE FILTER-CONDITION]
 GROUP BY COL-NAME; 
```

## ODER OF EXECUTION :

1. FROM.
2. WHERE (ROW BY ROW).
3. GROUP BY (ROW BY ROW)
4. SELECT (GROUP BY GROUP)

>**Note**
>To the group by clause we can pass multiple argument it will group the record if the combination of the arguments are same.

### EXAMPLE :

1. WAQTD NO OF EMPLOYEES WORKING IN EACH DEPT.

```
 SELECT COUNT(*),DEPTNO FROM EMP
 GROUP BY DEPTNO;
```

2. WAQTD MAX SAL AND MIN SAL GIVEN TO EACH DEPT.

```
 SELECT MAX(SAL),MIN(SAL),DEPTNO FROM EMP
 GROUP BY DEPTNO;
```

3. WAQTD NO OF EMP AND TOTAL SAL GIVEN TO EACH DEPT EXCEPT PRESIDENT.

```
 SELECT COUNT(*),SUM(SAL),DEPTNO
 FROM EMP WHERE JOB != 'PRESIDENT'
 GROUP BY DEPTNO;
```

4. WAQTD NO OF EMP, MAX SAL,MIN SAL,GIVEN TO EACH JOB.

```
 SELECT COUNT(*),MAX(SAL),MIN(SAL), JOB FROM EMP
 GROUP BY JOB;
```


# 2. HAVING CLAUSE

- HAVING CLAUSE is used to **filter the groups**.
- Having clause execute **Group-by-Group**.
- To the having clause we can pass group filter condition as an arguments.
- To use having clause group by clause mandatory.
- We can pass multiple condition in the having clause with the help of logical operator (or) special operator.
- We can pass multi row function in the having clause.

## SYNTAX :

```
 SELECT COL-NAME/EXPRESSION
 FROM TABLE-NAME
 [WHERE FILTER-CONDITION]
 GROUP BY COL-NAME
 HAVING GROUP FILTER CONDITION;
```

## ODER OF EXECUTION :

1. FROM
2. WHERE (ROW BY ROW)
3. GROUP BY (ROW BY ROW)
4. HAVING (GROUP BY GROUP)
5. SELECT (GROUP BY GROUP)

### EXAMPLE :

1. WAQTD NO OF EMP WORKING IN EACH DEPT IF THERE ARE ATLEAST 3 EMP WORKING IN THE DEPARTMENT.

```
 SELECT COUNT(*),DEPTNO FROM EMP
 GROUP BY DEPTNO HAVING COUNT(*) >=3;
```



1. WAQTD NO OF EMP , TOTAL SAL NEEDED TO PAY EACH DEPT IF THE MAX SAL GIVEN TO THE DEPT EXEED 3000.

```
 SELECT COUNT(*),SUM(SAL),DEPTNO FROM EMP
 GROUP BY DEPTNO
 HAVING MAX(SAL) > 3000;
```

2. WAQTD MAX SAL, MIN SAL GIVEN IN EACH DEPT EXCEPT PRESIDENT, IF THERE ARE ATMOST 5 EMP IN THE DEPT.

```
 SELECT MAX(SAL),MIN(SAL),DEPTNO FROM EMP
 WHERE JOB != 'PRESIDENT'
 GROUP BY DEPTNO HAVING COUNT(*) <= 5;
```

