# ORDER BY CLAUSE :

- ORDER BY CLAUSE is used to arrange the records in result table, either in ascending (or) in descending order.
- We use the keyword in asc for ascending desc for descending order.
- By default order by clause will arrange the records in ascending order.
- Order by clause is the only clause which is written at the last and executing last.
- Order by clause will always executes row by row.
- we can pass multiple arguments in order by clause.

## SYNTAX :

```
 SELECT COL-NAME/EXPRESSION
 FROM TABLE-NAME
 [WHERE FILTER_CONDITION]
 [GROUP BY COL-NAME]
 [HAVING GROUP-FILTER CONDITION]
 ORDER BY COL-NAME ASC/DESC
```
## ORDER OF EXECUTION

1. FROM
2. WHERE (ROW BY ROW)
3. GROUP BY (ROW BY ROW)
4. HAVING (GROUP BY GROUP)
5. SELECT (GROUP BY GROUP)
6. ORDER BY (ROW BY ROW)

## EXAMPLE :

1. WAQTD ALL THE DETAILS OF THE EMPLOYEE ARRANGE IN THE DESC ORDER OF THEIR SALARY.

```
 SELECT * FROM EMP
 ORDER BY SAL DESC;
```



# ESCAPE CHARACTER.

- ESCAPE CHARACTER are used to remove the special behavior of wild character (_,%) and treat then as normal character.
- Escape character should be used before the character whose special behavior has to be remove.
- One escape character can remove the special behaviour of only one wild character.


## SYNTAX :

```
 COL-NAME/EXPRESSION LIKE 'FILTER TO MATCH' ESCAPE ESC CHAR;
```

>**Note**
>Must use [#,$,!,@] FOR ESCAPE.

1. WAQTD NAMES OF EMP WHOSE NAME START WITH '_'.

```
 SELECT ENAME FROM EMP WHERE ENAME LIKE '#_%' ESCAPE '#';
```

2. WAQTD DETAILS OF EMO WHOSE NAME A '__'

```
SELECT * FROM EMP WHERE ENAME LIKE '%!_%!_%' ESCAPE '!';
```

3. WAQTD EMP NAME WHOSE NAME STARTS WITH '_' AND END WITH '%'

```
 SELECT ENAME FROM EMP WHERE ENAME LIKE '#_%#%' ESCAPE '#';
```