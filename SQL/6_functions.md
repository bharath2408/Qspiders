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
