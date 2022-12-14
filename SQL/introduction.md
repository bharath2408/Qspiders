# 1 SQL (Structured Query Language)

## 1.1 what is data :

- **DATA :** It is a collection of information (or) a valid information.
- **ENTITY :** It suits for both living & non living things

## 1.2 Database :

 - Database is a place (or) medium, where we can store data in systamatic and organised manner.  We can perform four operations on the database, they are **Create/Insert, Read/Retrive, Update/Modify, Delete/Drop**. These operations are universally referred as **'CRUD'** operations.

 > -> [1.2 DATABASE](https://drive.google.com/file/d/1wAls8ng17gdrngC8LTIkI6r5tW4qeeOq/view?usp=share_link)

## 1.3 Database Management System : [DBMS]

* DBMS is a software which is used to maintain and manage the database. In DBMS data is stored in the form of files.
* DBMS provides two important features they are security & authorisation.
* Query language is used to interact (or) communicate with DBMS.

> -> [1.3 DBMS](https://drive.google.com/file/d/1XaW-RLhMLcUWa8goBnRbiwjLj_Gx6JQw/view?usp=share_link)
## 1.4 Types of DBMS :

* Network DBMS
* Hirarchial DBMS
* Object oriented DBMS
* Relational DBMS

## 1.4.1 Relational model :

* In the year 1970'<sup>s</sup> a data scientist called **E.F. CODD** (Edgar franklin codd) suggested that data can be stored in the form of tables and invented a model called relational model.
* If any DBMS follows relational model it becomes RDBMS.
* If any DBMS follows the rules of E.F. CODD, it becomes RDBMS

> -> [1.4.1 E.F.CODD](https://drive.google.com/file/d/1wgTpiLqGyYQC7RqNQqMM0EjcRk5jdHwZ/view?usp=share_link)

> -> [1.4.1 RDBMS](https://drive.google.com/file/d/1dDaQC45XTRzRXgM6sMPEEPIs3BKbSyjQ/view?usp=share_link)

* RDBMS is a types of DBMS software. It is used to maintain and manage the database.
* RDBMS provides two important features security and authorisation.
* In RDBMS data is stored in the form of tables and it uses a language called SQL (Structured query language).

## 1.4.2 Rules of E.F. Codd :

**Rule 1 :**

- Data enter into the cell must be single value **(Atomic rule)** [to avoid data lose, we use / enter single value in the cell].

> -> [1.4.2 ADTTENDENCE](https://drive.google.com/file/d/1_rfUKt7Wsea_FxEw-E_PHwxn3rKWCveg/view?usp=share_link)

  - Table is a logical arrangement of rows and columns.

**Rule 2 :** 

- we can store data in multiple tables if required we can establish a connection (or) relation between the tables with the help **Key Attributes**

**Rule 3 :** 

- In RDBMS all the data should be stored in the form of tables including **Meta Data**
  - **Meta Data** Details of the data is known as meta data (or) the meta data is a raw fact which describes the attributes of data.
  - **Meta Data** is stored in a table called **Meta Table**.
  - **Meta tables** are auto-generated.

[META TABLE](https://drive.google.com/file/d/1LOP75L5h0ZNgGXAgELzCgh2DEsTwNz5h/view?usp=share_link)

**Rules 4 :** 

- Data enter into the table must be validated (cross checking).
**Two methods for data validation**
- By assigning Data types 
- By assigning Constraints.
- Data types are mandatory but constraints are optional.

> **Note**
> SQL is case insensitive language

# 1.5 DataTypes

- Data types are used to specify what type of data can be stored in particular memory location.
  * CHAR()
  * VARCHAR()/VARCHAR2()
  * NUMBER()
  * DATE
  * LARGE OBJECT
    1. character large object (CLOB)
    2. Binary large object (BLOB)

## 1. CHAR() :

* CHAR() datatype can accept **'A_Z', 'a-z', special char, '0-9', alpha-numeric**.
* Char() datatype follows **fixed length memory allocation system**.
* In char() datatypes unused memory will become memory wastage.
* In char() datatype, we can store upto 2000 character.

> [1 -> CHAR()](https://drive.google.com/file/d/1LFNTFCJehM2vMvo0RjTVirVx6n0SEj-M/view?usp=share_link)

### SYNTAX :

>  ` CHAR(SIZE)`

### SIZE :

* Size is used to specify the total number of blocks required to store the memory.


## 2. VARCHAR() :

* VARCHAR() Datatype can accept **'A_Z', 'a-z', special char, '0-9', alpha-numeric**.
* VARCHAR() follows **Variable length memory allocation system**.
* In the VARCHAR() unused memory is a free memory.
* In VARCHAR() we can store upto 2000 characters.

> -> [2. VARCHAR()](https://drive.google.com/file/d/1g9XUFmGhRf2Z7D-PCEmTD_YDfRXsjYAV/view?usp=share_link)

### SYNTAX :

> ` VARCHAR(SIZE)`

## 2.1 VARCHAR2() :

* VARCHAR2() is the updated version of varchar(), in which we can store upto 4000 characters. 

## 3. Number() :

* This datatype is used to store the numerical values.

* For number datatypes we can pass two arguments **(INPUTS)** precession, scale.

### precession :

* precession is used to specify the total number of integers that can be stored in a memory.
* precession ranges from **1 to 38**, it does not have any default value.

### scale :

* Scale is used to specify the total number of decimal (or) floating values, that can be stored within the **Precession**.
* Scale ranges form **-84 to 127**, its default value is **0 (ZERO)**.

### SYNTAX :

>  `NUMBER(PRECESSION, [SCALE])`

### EXAMPLE
```
[p] -> PRECESSION [s] -> SCALE

Number (5[p]) -> + 99999 to - 99999            -> p > s   
Number (5[p], 0[s]) -> + 99999 to - 99999      -> p > s
Number (5[p], 2[s]) -> + 999.99 to - 999.99    -> p > s
Number (5[p], 5[s]) -> + .99999 to - .99999    -> p = s
Number (2[p], 5[s]) -> + .00099 to - .00099    -> p < s
Number (1[p], 7[s]) -> + .0000009 to - .0000009 -> p < s
```

> **Note**
> If the number (or) value is within the range but having more number of scale values, by default NUMBER() Datatype will roundoff the number & accept it.

## 4. DATE() :

* This Datatype is used to store the date with syntax.

### SYNTAX :

> `DATE`

* There are two format given by ORACLE, they are **DD-MON-YY (or) DD-MON-YYYY**.

### Example :
> 08-DEC-22 (or) 08-DEC-2022 DATE FORMAT.

## 5. LARGE OBJECT :

  1. **Character large object (clob) :** Clob is used to store the huge amount of characters upto **4 GB**.
  2. **Binary large object (Blob) :** This datatype is used to store the binary values of **images, files, MP3, MP4 upto 4 GB**. 


## Constraints :

* Contraints are the rules given for data validation.
  * There are five constraints :
    * UNIQUE
    * NOT NULL
    * CHECK()
    * PRIMARY KEY
    * FOREIGN KEY

### UNIQUE :

* Unique is a constraints which is used to specify that the column should not accept duplicate or repeated values.

### NOT NULL :

* NOT NULL is a constraints which is used to specify that column should not accept null or empty or which is used to specify the mandatory fields.

  - **NULL**
    * NULL does not means zero.
    * NULL means empty (or) nothing.
    * Any arithmetic operations on the null will always results in **"NULL"**.
    * NULL cannot be equated with anything.

### CHECK() :

* CHECK() constraints is used for additional valiation of data.
* To CHECK() constraints we should pass the condition as the argument, If the condition satisfied it will accept the value else reject.

### PRIMARY KEY :

* primary key is a constraints which is used to identify uniquify from the table.

**Characteristics of primary key**

* We can have only one primary key the table.
* Primary will not accept duplicate (or) repeated value.
* Primary key is a combination of **UNIQUE and NOT NULL** constraints.
* Primary key is not mandatory but highly recommanded.

[PRIMARY KEY](https://drive.google.com/file/d/1X7nLAbsxG9dWWZNWY5H5LQyF53sYjgF4/view?usp=share_link)

### FOREIGN KEY :

* Foreign key is a constraints which is use to establish the connection b/w the tables.

**Characteristics of primay key**

* We can have any number of foregin key in table.
* Foreign key will accept duplicate and repeated values.
* Foreign will accept NULL value.
* Foreign key is not a combination of **UNIQUE and NOT NULL** constraints.
* Foreign key is present in the child table but they actually belongs to parent table.
* If any attributes wants to be a Foreign key its mandatory that it should be primary key in its own table.
* Foreign key is also known a **"REFERENTIAL INTIGRITY CONSTRAINTS"**.

[FOREIGN KEY](https://drive.google.com/file/d/10jtk1F5Dlm6K2MfPAEKkHxeg8KCSsFaM/view?usp=share_link)