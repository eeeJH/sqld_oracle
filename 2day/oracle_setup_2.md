# SQLD 2 Day

### Oracle install
- 오라클 DBMS 중지
- 오라클 DBMS 마운트 모드로 시작
- 문자 집합설정
---
## DBMS 중지
```
SQL> shutdown immediate;
Database closed.
Database dismounted.
ORACLE instance shut down.
```
## DBMS 시작
```
SQL> startup
ORACLE instance started.

Total System Global Area 1068937216 bytes
Fixed Size                  2260048 bytes
Variable Size             616563632 bytes
Database Buffers          444596224 bytes
Redo Buffers                5517312 bytes
Database mounted.
Database opened.
```

--- 
## Error
- 오라클 SYSDBA 접속 후, 아래의 쿼리를 입력하였으나 오류발생

```
select * from dual;
```
```
SQL> select * from dual;
select * from dual
*
ERROR at line 1:
ORA-01034: ORACLE not available
Process ID: 0
Session ID: 0 Serial number: 0
```

 - 현재 상태
 ```
 SQL> SHUTDOWN IMMEDIATE;
ORA-24324: service handle not initialized
ORA-01041: internal error. hostdef extension doesn't exist
```
```
SQL> startup
ORACLE instance started.

Total System Global Area 1068937216 bytes
Fixed Size                  2260048 bytes
Variable Size             616563632 bytes
Database Buffers          444596224 bytes
Redo Buffers                5517312 bytes
Database mounted.
ORA-01092: ORACLE instance terminated. Disconnection forced
ORA-12701: CREATE DATABASE character set is not known
Process ID: 8776
Session ID: 167 Serial number: 3


SQL>
SQL> select * from dual;
ERROR:
ORA-03114: not connected to ORACLE
```
- not connected to oracle ?
- 생각해보니 시스템 속성변경하고 그냥 종료한 것이 문제
- 재설치진행
