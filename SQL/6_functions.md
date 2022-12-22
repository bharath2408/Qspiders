# FUNCTIONS :

- FUNCTIONS are the block of codes (or) set of instructions given to do the given particular task.

## FUNCTION :

- BUILT IN / IN BUILT.
    - SINGLE ROW FUNCTION.
    - MULTI ROW FUNCTION.
- USER DEFINED / USER DERIVED.

## SINGLE ROW FUNCTION :

- SINGLE ROW FUNCTION takes one input at a time, executes and gives one output.
- Single row functions executes row by row.
- If we pass 'n' number of inputs to the single row function it returns 'n' number of outputs.

Length -> it calculates the number of characters.

### EXAMPLE :

```
 SELECT LENGTH(ENAME)
 FROM EMP;
```

### OUTPUT:

```
LENGTH(ENAME)
-------------
    5
    4
    6
```

## MULTI ROW FUNCTION (GROUP FUNCTION/AGGRIGATE FUNCTION) :

- MULTI ROW FUNCTIONS takes all the inputs in single shot, executes and gives only one output.
- MULTI ROW FUNCTIONS executes group by group.
- If we pass 'n' number of inputs to the multi-row function, it returns only one output.


### LIST OF MRF:

1. MAX()
2. MIN()
3. SUM()
4. AVG()
5. COUNT()


### EXAMPLE :

```
 SELECT MAX(SAL)
 FROM EMP;
```

### OUTPUT :

```
    MAX(SAL)
    --------
       300
```

## RULES OF MULTI-ROW FUNCTION :

- MULTI - ROW FUNCTION can accept only one arguments.
- along with multi-row function we cannot pass any other argument in select clause.
- Multi-row functions cannot be used in 'Where' clause.
- Multi-row functions ignore NULL.
- count is the only multi-row function which accept asterisk(*) as an argument.
- Max(),Mix(),Count() Functions can accept any datatype [NUMBER, CHARACTER, DATE].
- SUM() and AVG() functions can accept only number datatype

### EXAMPLE :

1. WAQTD MAXIMUM AND MINIMUM SALARY GIVEN TO THE EMPLOYEES.

```
 SELECT MAX(SAL),MIN(SAL)
 FROM EMP;
```

2. WAQTD MAXIMUM SALARY, MINIMUM SALARY, AVERAGE, SALARY GIVEN TO THE MANAGERS.

```
 SELECT MAX(SAL),MIN(SAL),AVG(SAL)
 FROM EMP
 WHERE JOB='MANAGER';
```

3. WAQTD NUMBER OF EMPLOYEES WORKING IN DEPT 20.

```
 SELECT COUNT(*) FROM EMP
 WHERE DEPTNO=20;
```

4. WAQTD NUMBER OF EMPLOYEES WORKING IN DEPT 20 WHO'S SALARY IS LESS THAN 2500.

```
 SELECT COUNT(*) FROM EMP
 WHERE DEPTNO=20 AND SAL<2500;
```

5. WAQTD NUMBER OF ANALYST IN THE TABLE.

```
 SELECT COUNT(JOB) FROM EMP
 WHERE JOB='ANALYST';
```

6. WAQTD MAXIMUM SALARY, MINIMUM SALARY, SUM OF SALARY, AVERAGE SALARY AND NUMBER OF EMPLOYEES IF EMPLOYEE NAME STARTS WITH A.

```
 SELECT MAX(SAL),MIN(SAL),SUM(SAL),AVG(SAL),COUNT(*)
 FROM EMP
 WHERE ENAME LIKE 'A%';
```