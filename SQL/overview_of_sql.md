# 2.1 OVERVIEW OF SQL :

1. DATA DEFINITION LANGUAGE (DDL).
2. DATA MANIPULATION LANGUAGE (DML).
3. TRANSACTION CONTROL LANGUAGE (TCL).
4. DATA CONTROL LANGUAGE (DCL).
5. DATA QUERY LANGUAGE (DQL).

## 2.1.1 DATA QUERY LANGUAGE :

* This language is use to retrieve the data from the database.
* They have four statements under **DQL**.
    1. SELECT.
    2. PROJECTION.
    3. SELECTION.
    4. JOINS.

- **SELECT** : This statement is use to retrieve the data from the table and display the result.
- **PROJECTION** : 
    - The process of retrieving a data by selecting only the columns is known as projection.
    - In projection all the records under the column will be selected by default.
- **SELECTION** : The process of retrieving data by selecting both rows and columns is known as selection.
- **JOINS** :The process of retrieving data from multiple table simultaneously is known as joins.

## 1. PROJECTION :

 - The process of retrieving a data by selecting only the columns is known as projection.
 - In projection all the records under the column will be selected by default.

### SYNTAX :

``` SELECT * /[DISTINT]col-name/EXPRESSION[ALIAS] FROM Table-name; ```

### Order of execution:

* FROM -> statement/keyword/**CLAUSE**
* SELECT -> statement/keyword/**CLAUSE**

**QUERY EXAMPLE :**
- SELECT SNAME FROM STUDENT;
- SELECT SNAME,BRANCH FROM STUDENT;

EXAMPLE :
- Write query to display names of all the students.

``` ANSWER: SELECT SNAME FROM STUDENT; ```

[STUDENT TABLE](https://drive.google.com/file/d/1liH_jM04bJVSxJFPba3gKYTC-rf7MM9a/view?usp=share_link)

- From clause start the execution, it will go to database and search for the table, if the table is present it will put the table under execution.
- To FROM CLAUSE we can pas table name as an argument(input).
- SELECT CLAUSE execute after the execution of from clause.
- The work of select clause is use to retrieve the data from the table and dispaly the result.
- to SELECT CLAUSE we can pass three argument.
    1. '*' (ASTERISK).
    2. COLUMN NAME.
    3. EXPRESSION.
- 
    1. **'*'** it is use to retrieve all the columns from the table.
    2. **';'** it is use to specify the end of the statement (or) end of the query.

> **Note**
> To see the table
> **SELECT * FROM TAB;** to see the column name **DESC TABLE_NAME;** 

**Write a query to display name and for all the students :**

``` ANSWER : SELECT SNAME,BRANCH FROM STUDENT; ```

**Write a query to display Student id, student name, percentage :**

``` ANSWER : SELECT SID,SNAME,PER FROM STUDENT; ```

**write a query to display student name, student id, branch :**

``` ANSWER : SELECT SNAME,SID,BRANCH FROM STUDENT;```

**write a query to display student id, branch, percentage, name for all the student :**

``` ANSWER : SELECT SID,BRANCH,PER,SNAME FROM STUDENT; ```

**Write a query to display all the details of students :**

``` ANSWER : SELECT * FROM STUDENT;```