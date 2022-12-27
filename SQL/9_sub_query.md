# SUB QUERY :

- A query written inside another query known as sub query.


- Let us consider two query

    - Inner query.
    - Outer Query.

    - Inner query starts the execution.
    - Inner query executes first and gives the output.
    - The output of inner query is given as input to the outer query ,by taking this input outer query executes completely and gives result.

    - Therefore we can say that outer query is dependent on inner query.
    - This the working principle of sub query.

## WHEN OR WHY :

### CASE 1 : UNKNOWN PRESENT IN THE QUESTION :

- whenever there is unknown present in the question we use sub query to find out the unknown or whenever the condition is indirect we use sub query.

## EXAMPLE :

1. WAQTD ENAME OF THE EMP EARNING LESS THAN MILLER.

```
 SELECT ENAME FROM EMP WHERE SAL < (SELECT SAL FROM EMP WHERE ENAME='MILLER');
```

2. WAQTD NAME OF THE EMP WHO ARE WORKING IN THE SAME DEPT OF SMITH.

```
 SELECT ENAME FROM EMP WHERE DEPTNO = (SELECT DEPTNO FROM EMP WHERE ENAME='SMITH');
```

3. WAQTD DETAILS OF THE EMP WHO ARE WORKING IN THE SAME DEPT OF EMP WHOSE EMP NO IS 4.

```
 SELECT * FROM EMP WHERE DEPTNO=(SELECT DEPTNO FROM EMP WHERE EMPNO=4);
```

4.WAQTD ENAME DESIGINATION FOR ALL THE EMP WHO ARE WORKING IN THE DESIGINATION AS 'CLARK'.

```
 SELECT ENAME,JOB FROM EMP WHERE JOB = (SELECT JOB FROM EMP WHERE ENAME='CLARK');
```

5. WAQTD ENAME SAL DESIGINATION FOR ALL THE EMP WHO ARE WORKING AS SALESMAN AND EARNING MORE THAN SMITH.

```
 SELECT ENAME,SAL,JOB FROM EMP WHERE JOB='SALESMAN' AND SAL > (SELECT SAL FROM EMP WHERE ENAME='SMITH');
```

6. WAQTD DETAILS OF THE EMP WHO IS EARNING MORE THAN WARD AND LESS THAN ALLEN.

```
 SELECT * FROM EMP WHERE SAL > (SELECT SAL FROM EMP WHERE ENAME='WARD') AND SAL < (SELECT SAL FROM EMP WHERE ENAME='ALLEN');
```

>**Note**
>In the select clause of sub query or inner query we can pass only one argument.

>**Note**
> crossponding col-name need not be same, but there data type should be same.
