SQL> select *from employee_982;

     EMPNO ENAME      JOB              MGR HIREDATE         SAL       COMM
---------- ---------- --------- ---------- --------- ---------- ----------
    DEPTNO
----------
      7369 smith      clerk           7902 17-DEC-80        800
        20

      7499 allen      salesman        7698 20-FEB-81       1600        300
        30

      7499 ward       salesman        7698 22-FEB-81       1250        500
        30


     EMPNO ENAME      JOB              MGR HIREDATE         SAL       COMM
---------- ---------- --------- ---------- --------- ---------- ----------
    DEPTNO
----------
      7566 jones      manager         7839 02-APR-81       2975
        30


                                


SQL> select count (comm) from employee_982;

COUNT(COMM)
-----------
          2

SQL> select count (*) from employee_982;

  COUNT(*)
----------
         4

SQL> SELECT SUM(empno) FROM employee_982;

SUM(EMPNO)
----------
     29933

SQL> SELECT avg(empno) FROM employee_982;

AVG(EMPNO)
----------
   7483.25

SQL> SELECT max(empno) FROM employee_982;

MAX(EMPNO)
----------
      7566

SQL> SELECT min(empno) FROM employee_982;

MIN(EMPNO)
----------
      7369

SQL> SELECT sysdate FROM employee_982;

SYSDATE
---------
17-FEB-22
17-FEB-22
17-FEB-22
17-FEB-22

SQL> SELECT ADD_MONTHS(hiredate,4) FROM employee_982 WHERE sal='100';

no rows selected

SQL> SELECT ADD_MONTHS(hiredate,4) FROM employee_982 WHERE sal=100;

no rows selected

SQL> SELECT ADD_MONTHS(hiredate,4) FROM employee_982 WHERE ename='smith';

ADD_MONTH
---------
17-APR-81

SQL> SELECT LAST_DAY(SYSDATE) FROM employee_982;1
  2  SELECT LAST_DAY(SYSDATE) FROM employee_982;
SELECT LAST_DAY(SYSDATE) FROM employee_982;1
                                           *
ERROR at line 1:
ORA-00911: invalid character


SQL> SELECT LAST_DAY(SYSDATE) FROM employee_982;

LAST_DAY(
---------
28-FEB-22
28-FEB-22
28-FEB-22
28-FEB-22

SQL> SELECT MONTHS_BETWEEN(SYSDATE,'02-apr-81') FROM employee_982;

MONTHS_BETWEEN(SYSDATE,'02-APR-81')
-----------------------------------
                         490.501894
                         490.501894
                         490.501894
                         490.501894

SQL> SELECT NEXT_DAY(SYSDATE,'TUESDAY') FROM employee_982;

NEXT_DAY(
---------
22-FEB-22
22-FEB-22
22-FEB-22
22-FEB-22

SQL> SELECT EXTRACT(MONTH FROM SYSDATE) FROM employee_982;

EXTRACT(MONTHFROMSYSDATE)
-------------------------
                        2
                        2
                        2
                        2

SQL> SELECT ABS(99) FROM employee_982;

   ABS(99)
----------
        99
        99
        99
        99

SQL> SELECT CEIL(-9.1), CEIL(4.5) FROM employee_982;

CEIL(-9.1)  CEIL(4.5)
---------- ----------
        -9          5
        -9          5
        -9          5
        -9          5

SQL> SELECT FLOOR(-9.1), FLOOR(4.5) FROM employee_982;

FLOOR(-9.1) FLOOR(4.5)
----------- ----------
        -10          4
        -10          4
        -10          4
        -10          4

SQL> select mod(19,4) from emploee_982;
select mod(19,4) from emploee_982
                      *
ERROR at line 1:
ORA-00942: table or view does not exist


SQL> select mod(19,4) from employee_982;

 MOD(19,4)
----------
         3
         3
         3
         3

SQL>  select power(9,3) from employee_982;

POWER(9,3)
----------
       729
       729
       729
       729

SQL> select sqrt(81) from employee_982;

  SQRT(81)
----------
         9
         9
         9
         9

SQL>  select trunc(19.8767,2) from emploee_982;
 select trunc(19.8767,2) from emploee_982
                              *
ERROR at line 1:
ORA-00942: table or view does not exist


SQL>  select trunc(19.8767,2) from employee_982;

TRUNC(19.8767,2)
----------------
           19.87
           19.87
           19.87
           19.87

SQL> select * from STUDENT WHERE empno BETWEEN 7000 AND 7500;
select * from STUDENT WHERE empno BETWEEN 7000 AND 7500
              *
ERROR at line 1:
ORA-00942: table or view does not exist


SQL> select * from employee_982 WHERE empno BETWEEN 7000 AND 7500;

     EMPNO ENAME      JOB              MGR HIREDATE         SAL       COMM
---------- ---------- --------- ---------- --------- ---------- ----------
    DEPTNO
----------
      7369 smith      clerk           7902 17-DEC-80        800
        20

      7499 allen      salesman        7698 20-FEB-81       1600        300
        30

      7499 ward       salesman        7698 22-FEB-81       1250        500
        30



SQL> select * from employee_982 WHERE ename like 'J%';

no rows selected

SQL> select * from employee_982 WHERE ename like 'j%';

     EMPNO ENAME      JOB              MGR HIREDATE         SAL       COMM
---------- ---------- --------- ---------- --------- ---------- ----------
    DEPTNO
----------
      7566 jones      manager         7839 02-APR-81       2975
        30


SQL> select * from employee_982 WHERE ename LIKE 's%';

     EMPNO ENAME      JOB              MGR HIREDATE         SAL       COMM
---------- ---------- --------- ---------- --------- ---------- ----------
    DEPTNO
----------
      7369 smith      clerk           7902 17-DEC-80        800
        20


SQL> select * from employee_982 WHERE ename LIKE 's%' AND ename LIKE 'j%';

no rows selected




SQL> select * from employee_982 WHERE ename LIKE 's__h';

no rows selected



SQL>
SQL> SELECT * FROM employee_982 WHERE job='clerk' OR job='manager';

     EMPNO ENAME      JOB              MGR HIREDATE         SAL       COMM
---------- ---------- --------- ---------- --------- ---------- ----------
    DEPTNO
----------
      7369 smith      clerk           7902 17-DEC-80        800
        20

      7566 jones      manager         7839 02-APR-81       2975
        30


SQL> SELECT * FROM employee_982 WHERE job='clerk' AND job='manager';

no rows selected

SQL>
