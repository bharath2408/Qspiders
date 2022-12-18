# OPERATORS :

1. ARITHEMATIC OPERATORS (+,-,*,/).
2. RELATIONAL OPERATORS (>,<,>=,<=).
3. COMPARISON OPERATORS (=,!=,(<>)).
4. CONCATINATION OPERATOR (||).
5. LOGICAL OPERATOR (AND, OR, NOT).
6. SPECIAL OPERATORS.
    * IN
    * NOT IN
    * BETWEEN
    * NOT BETWEEN
    * IS
    * IS NOT
    * LIKE
    * NOT LIKE
7. SUB-QUERY OPERATORS.
    * ALL
    * ANY
    * EXISTS
    * NOT EXISTS

## CONCATINATION OPERATOR :

- Concatination operator is used to join multiple string (set of characters).

>**Note**
>If i want to use n number of operators, the operator should be (n-1).

### Example :

```
 SELECT 'HI '||'DINGA'
 FROM DUAL;
```

[EXAMPLE 1](https://drive.google.com/file/d/19ObT45ymYrcbyRMTuA8DT1Ezaiqbz2Mg/view?usp=share_link)

>**Note**
>Dual is a dummy table, it has one row and one column.

```
 SELECT 'HI '||ENAME||'YOUR SAL IS RS '||SAL
 FROM EMP;
```
[EXAMPLE 2](https://drive.google.com/file/d/13lEPCuKKAbMZnum6aSJZKVnqkRlYpDSo/view?usp=share_link)

## LOGICAL OPERATOR :

- Logical operators are used to write multiple conditions.
    * AND
    * OR
    * NOT

### AND OPERATOR :

- AND operator works as logical multiplication.
- AND operator returns **TRUE** if both the conditions are satisfied.
- If the first condition fails to satisfy, there is no need of checking the second condition. The output will be always false.
- We use AND operator, whenever we need to satisfy both the condition.

```
   C1   C2     Result
   F    F         F
   F    T         F
   T    F         F
   T    T         T
```

### OR OPERATOR :

- OR operator works as logical addition.
- OR operator becomes True, if any one of the condition.
- If the first condition is satisfied, there is no need for checking the second, the result will be always true.
- we use **'or'** operator whenever, we need to satisfy any one of the condition.

```
  C1  C2     Result
  F    F       F
  F    T       T
  T    F       T
  T    T       T
```

### NOT OPERATOR :

- NOT operator works as inverser (or) negation operator.
- NOT operator return true if the input is false or vice verse.

```
  IN1  o/p

  T    F
  F    T
```

### EXAMPLE :
 
1. WAQTD DETAILS OF THE EMPLOYEE WHO IS WORKING AS MANAGER IN DEPTNO=10

```
 SELECT * FROM EMP
 WHERE JOB='MANAGER' AND DEPTNO=10;
```

## ASSIGNMENT IN OPERATORS :

1. WAQTD DETAILS OF THE EMPLOYEES WORKING AS CLERK AND EARNING LESS THAN 1500.

```
 SELECT * FROM EMP
 WHERE JOB='CLERK' AND SAL<1500;
```
[ASSIGNMENT 1](https://drive.google.com/file/d/1EEsurPSqCIW0ZHJPvQc9rExVdMP5LCX-/view?usp=share_link)

2. WAQTD NAME AND HIREDATE OF THE EMPLOYEES WORKING AS MANAGER IN DEPT 30

```
 SELECT ENAME,HIREDATE FROM EMP
 WHERE JOB='MANAGER' AND DEPTNO=30;
```
[ASSIGNMENT 2](https://drive.google.com/file/d/1Klk5Re2R1a4Fs8jStc1v8MQA1TVnL5GD/view?usp=share_link)

3. WAQTD DETAILS OF THE EMP ALONG WITH ANNUAL SALARY IF THEY ARE WORKING IN DEPT 30 AS SALESMAN AND THEIR ANNUAL SALARY HAS TO BE GREATER THAN 14000.

```
 SELECT EMP.*,SAL*12 FROM EMP
 WHERE DEPTNO=30 AND JOB='SALESMAN' AND SAL*12<14000;
```

[ASSIGNMENT 3](https://drive.google.com/file/d/10B8ndjBCDlwoSBRqDMLX7tJkhOONb2m9/view?usp=share_link)

4. WAQTD ALL THE DETAILS OF THE EMP WORKING IN DEPT 30 OR AS ANALYST.

```
 SELECT * FROM EMP
 WHERE DEPTNO=30 OR JOB='ANALYST';
```
[ASSIGNMENT 4](https://drive.google.com/file/d/19NCU1PpR8fz_n5yHRDjoY2jKDEU6TWNT/view?usp=share_link)

5. WAQTD NAMES OF THE EMPLOYEES WHOS SALARY IS LESS THEN 1100 AND THEIR DESIGNATION IS CLERK.

```
 SELECT ENAME FROM EMP
 WHERE SAL<1100 AND JOB='CLERK';
```
[ASSIGNMENT 5](https://drive.google.com/file/d/1Gg0D9ikFFh_a7vrFjQQw_lTDqU1Hs-wu/view?usp=share_link)

6. WAQTD NAME AND SAL, ANNUAL SAL AND DEPTNO IF DEPTNO IS 20 EARNING MORE THAN 1100 AND ANNUAL SAL IS EXCEEDS 12000

```
 SELECT ENAME,SAL,SAL*12,DEPTNO FROM EMP
 WHERE DEPTNO=20 AND SAL>1100 AND SAL*12>12000;
```
[ASSIGNMENT 6](https://drive.google.com/file/d/1AVUWzlaEJ_fz3mg8Gm-mCJtTekPuCg7Z/view?usp=share_link)

7. WAQTD EMPNO AND NAMES OF THE EMPLOYEES WORKING AS MANAGER IN DEPT 20.

```
 SELECT EMPNO,ENAME FROM EMP
 WHERE JOB='MANAGER' AND DEPTNO=20;
```
[ASSIGNMENT 7](https://drive.google.com/file/d/1c0rQttov8kGw-OGKgsY22ZDaTStihQYD/view?usp=share_link)

8. WAQTD DETAILS OF EMPLOYEES WORKING IN DEPT 20 OR 30.

```
 SELECT * FROM EMP
 WHERE DEPTNO=20 OR DEPTNO=30;
```

[ASSIGNMENT 8](https://drive.google.com/file/d/1TTmTzDoWH9CSwOPY4Bbu6gWupWBa6-Gr/view?usp=share_link)

9. WAQTD DETAILS OF EMPLOYEES WORKING AS ANALYST IN DEPT 10.

```
 SELECT * FROM EMP
 WHERE JOB='ANALYST' AND DEPTNO=10;
```
[ASSIGNMENT 9](https://drive.google.com/file/d/1O0frRr_64hV06OlFSJnJhNJW3pVMiU2r/view?usp=share_link)

10. WAQTD DETAILS OF EMPLOYEE WORKING AS PRESIDENT WITH SALARY OF RUPEES 4000.

```
 SELECT * FROM EMP
 WHERE JOB='PRESIDENT' AND SAL=4000;
```
[ASSIGNMENT 10](https://drive.google.com/file/d/1yNJmAVvhKbnK89nGp0DddxQAg0KQfD6V/view?usp=share_link)

11. WAQTD NAMES AND DEPTNO, JOB OF EMPS WORKING AS CLERK IN DEPT 10 OR 20.

```
 SELECT ENAME,DEPTNO FROM EMP
 WHERE JOB='CLERK' AND DEPTNO=10 OR DEPTNO=20;
```
[ASSIGNMENT 11](https://drive.google.com/file/d/1smZn8V076fJy4jxjcOKmUAsiTEmTvzFF/view?usp=share_link)

12. WAQTD DETAILS OF EMPLOYEES WORKING AS CLERK OR MANAGER IN DEPT 10

```
 SELECT * FROM EMP
 WHERE JOB='CLERK' OR JOB='MANAGER' AND DEPTNO=10;
```
[ASSIGNMENT 12](https://drive.google.com/file/d/1OmemsFyIQCCL4QHv4cBB8bE8xtq-WI-E/view?usp=share_link)

13. WAQTD NAMES OF EMPLOYEES WORKING IN DEPT 10,20,30,40.

```
 SELECT ENAME FROM EMP
 WHERE DEPTNO='10' AND DEPTNO='20' AND DEPTNO='30' AND DEPTNO='40';
```
[ASSIGNMENT 13](https://drive.google.com/file/d/1EZ8CT4bW3pYTFer2dHB3yo_6pgdMcCPC/view?usp=share_link)

14. WAQTD DETAILS OF EMPLOYEES WITH EMPNO 7902,7839.

```
 SELECT * FROM EMP
 WHERE EMPNO=7902 AND EMPNO=7839;
```
[ASSIGNMENT 14](https://drive.google.com/file/d/1DZtC0ABKlruhuMcM4-aOtMzm8c4_0xa0/view?usp=share_link)

15. WAQTD DETAILS OF EMPLOYEES WORKING AS MANAGER OR SALESMAN OR CLERK.

```
 SELECT * FROM EMP
 WHERE JOB='MANAGER' OR JOB='SALESMAN' OR JOB='CLERK';
```
[ASSIGNMENT 15](https://drive.google.com/file/d/1TSdNL8XIDg6rXiDMow1AvzCG34NPGd1O/view?usp=share_link)

16. WAQTD NAMES OF EMPLOYEES HIRED AFTER 81 AND BEFORE 87.

```
 SELECT ENAME FROM EMP
 WHERE HIREDATE>'01-JAN-81' AND HIREDATE<'01-JAN-87';
```
[ASSIGNMENT 16](https://drive.google.com/file/d/1JCHssuzcYQMpleLnGOQFXcBONJpjlxgz/view?usp=share_link)

17. WAQTD DETAILS OF EMPLOYEES EARNING MORE THAN 1250 BUT LESS THAN 3000.

```
 SELECT * FROM EMP
 WHERE SAL>1250 AND SAL<3000;
```
[ASSIGNMENT 17](https://drive.google.com/file/d/1Rd1B_c6Mfbok0zFk-G8zPj8Oyl9JXY9G/view?usp=share_link)

18. WAQTD NAMES OF EMPLOYEES HIRED AFTER 81 INTO DEPT 10 OR 30.

```
 SELECT ENAME FROM EMP
 WHERE HIREDATE>'01-JAN-81' AND DEPTNO=10 OR DEPTNO=30;
```
[ASSIGNMENT 18](https://drive.google.com/file/d/1_ckpnFJ9i6iSttiPKt0s34q7b00Gb67k/view?usp=share_link)

19. WAQTD NAMES OF EMPLOYEES ALONG WITH ANNUAL SALARY FOR THE EMPLOYEES WORKING AS MANAGER OR CLERK INTO DEPT 10 OR 30.

```
 SELECT ENAME,SAL*12 FROM EMP
 WHERE JOB='MANAGER' OR JOB='CLERK' AND DEPTNO=10 OR DEPTNO=30;
```
[ASSIGNMENT 19](https://drive.google.com/file/d/1YIUGrMeIkcySHJJ9xx4ZnFWMDQ6VQ5Th/view?usp=share_link)

20. WAQTD ALL THE DETAILS ALONG WITH ANNUAL SALARY IF SAL IS BETWEEN 1000 AND 4000 ANNUAL SALARY MORE THAN 15000.

```
 SELECT EMP.*,SAL*12 FROM EMP
 WHERE SAL>=1000 AND SAL<=4000 AND SAL*12>15000;
```

[ASSIGNMENT 20](https://drive.google.com/file/d/1XozTZpHqW_kjdXy6MRvrW9xJBbxmQBFo/view?usp=share_link)