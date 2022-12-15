## SELECTIION :

- The process of retrieving data by selecting both rows and columns is known as selection.

### WHERE CLAUSE :

- where clause is used to filter the records.
- Where clause executes **Row by Row**.
- where clause executes after the execution of from clause.
- to the where clause we can pass filter conditions as an arguments.
- If the condition satisfying, it returns true(T) else false(F) , it is known as boolean values.
- we can pass multiple condition to the where clause with the help of logical operators.
- Filter condition are of two formats, they are :
    1. col-name operator col-name.
    2. col-name operator values

>**Note**
>values are known as literals.

### Literals :

- Literals are also known as operands or values.
- there are three types of literals.

    - Number literal
    - Character literal
    - Date literal
- character literal and date literal are case sensitive and it should be written within single quote.

#### SYNTAX :

```
SELECT COL-NAME/EXPRESSION/*
FROM TABLE-NAME
WHERE FILTER-CONDITION;
```

#### Order of execution :

1. From clause.
2. Where clause (Row by Row).
3. Select clause.

#### Example :

```
SELECT ENAME
FROM EMP
WHERE DNO=20;
```


**WRITE A QUERY TO DISPLAY SALARY OF SMITH**

```
 SELECT SAL FROM EMP WHERE ENAME='SMITH';
```

**WRITE A QUERY TO DISPLAY DETAILS OF THE EMPLOYEE WHO IS EARNING MORE THAN 2000.**

```
 SELECT * FROM EMP WHERE SAL>2000;
```

**WRITE A QUERY TO DISPLAY EMPLOYEE NAME,SALARY AND DESIGNATION FOR ALL THE EMPLOYEE WHO ARE WORKING AS SALESMAN**

```
 SELECT ENAME,SAL,JOB
 FROM EMP
 WHERE JOB='SALESMAN'
```

**WRITE A QUERY TO DISPLAY DETAILS OF THE EMPLOYEE HIRE BEFORE**

```
 SELECT *
 FROM EMP
 WHERE HIREDATE='01-JAN-81';
```

## ASSIGNMENT ON WHERE CLAUSE :

**1. WAQTD THE ANNUAL SALARY OF THE EMPLOYEE WHOS NAME IS SMITH**

```
 SELECT SAL*12 "ANNUAL SALARY"
 FROM EMP
 WHERE ENAME='SMITH';
```

**2 .WAQTD NAME OF THE EMPLOYEES WORKING AS CLERK**

```
 SELECT * 
 FROM EMP
 WHERE JOB='CLERK';
```

**3. WAQTD SALARY OF THE EMPLOYEES WHO ARE WORKING AS SALESMAN**

```
    SELECT *
    FROM EMP
    WHERE JOB='SALESMAN';
```

**4. WAQTD DETAILS OF THE EMP WHO EARNS MORE THAN 2000**

```
 SELECT *
 FROM EMP
 WHERE SAL>2000;
```

**5. WAQTD DETAILS OF THE EMP WHOS NAME IS JONES**

```
 SELECT *
 FROM EMP
 WHERE ENAME='JONES';
```

**6. WAQTD DETAILS OF THE EMP WHO WAS HIRED AFTER 01-JAN-81**

```
 SELECT *
 FORM EMP
 WHERE HIREDATE>'01-JAN-81';
```
**7. WAQTD NAME AND SAL ALONG WITH HIS ANNUAL SALARY IF THE ANNUAL SALARY IS MORE THAN 1200**

```
  SELECT ENAME,SAL,SAL*12
  FROM EMP
  WHERE SAL*12>12000;
```
**8. WAQTD EMPNO OF THE EMPLOYEES WHO ARE WORHING IN DEPT 30**

```
 SELECT EMPNO
 FROM EMP
 WHERE DEPTNO=30;
```
**9. WAQTD ENAME AND HIREDATE IF THEY ARE HIRED BEFORE 1981**

```
 SELECT ENAME,HIREDATE 
 FROM EMP
 WHERE HIREDATE<'01-JAN-1981';
```
**10. WAQTD DETAILS OF THE EMPLOYEES WORKING A MANAGER**

```
 SELECT *
 FROM EMP
 WHERE JOB='MANAGER';
```
**11. WAQTD NAME AND SALARY GIVEN TO AN EMPLOYEE IF EMPLOYEE EARNS A COMMISSION OF RUPEES 1400**

```
 SELECT ENAME,SAL
 FROM EMP
 WHERE COMM=1400;
```
**12. WAQTD DETAILS OF EMPLOYEES HAVING COMMISSION MORE THAN SALARY**

```
 SELECT *
 FROM EMP
 WHERE COMM>SAL;
```
**13. WAQTD EMPNO OF EMPLOYEES HIRED BEFORE THE YEAR 87**

```
 SELECT EMPNO
 FROM EMP
 WHERE HIREDATE<'01-JAN-87';
```
**14. WAQTD DETAILS OF EMPLOYEES WORKING AS ANALYST**

```
 SELECT *
 FROM EMP
 WHERE JOB='ANALYST';
```
**15. WAQTD DETAILS OF EMPS EARNING MORE THAN 2000 RUPEES PER MONTH**

```
 SELECT *
 FROM EMP
 WHERE SAL>2000;
```