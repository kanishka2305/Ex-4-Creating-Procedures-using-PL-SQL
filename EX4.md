# Ex. No: 4 Creating Procedures using PL/SQL

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```py
SQL> CREATE TABLE empl(
  2       empid NUMBER,
  3       empname VARCHAR(10),
  4       dept VARCHAR(10),
  5       salary NUMBER
  6      );

SQL> CREATE OR REPLACE PROCEDURE emp_data AS
  2      BEGIN
  3      INSERT INTO empl(empid,empname,dept,salary)
  4      values(1,'SHRIRAM','MD',10000000);
  5      INSERT INTO empl(empid,empname,dept,salary)
  6      values(2,'KANISHKAR','HR',500000);
  7      INSERT INTO empl(empid,empname,dept,salary)
  8      values(3,'PRAVEEN','IT',200000);
  9      COMMIT;
 10     FOR emp_rec IN (SELECT * FROM empl)LOOP
 11     DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
 12     ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
 13     END LOOP;
 14     END;
 15    /
```
### Output:
![image](https://github.com/kanishka2305/Ex-4-Creating-Procedures-using-PL-SQL/assets/113497357/7e21c1e0-eb81-432a-b7ff-c69f957fde77)

### Result:
The program has been implemented successfully.
