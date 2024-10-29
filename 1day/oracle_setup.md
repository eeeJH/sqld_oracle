# SQLD 1 Day

### Oracle install
- 이경오의 SQLD를 참고하여 구버전인 $Oracle 11gR2$ 설치
- Oracle 리스너 설정 및 확인
- 오라클 DBMS 접속하기
- SQL*PlUS 기본 설정하기

---


## Oracle DBMS 리스너 확인
```Oracle
lsnrctl status
```
- CLRExtProc, PLSExtProc, XEXDB, xe 가 모두 존재하면 리스너 설정이 정상적으로 완료
- 아래와 같이 _The command completed successfully_ 라는 명렁어라인이 안나온다면 삭제하고 재설치

```
PS C:\> lsnrctl status

LSNRCTL for 64-bit Windows: Version 11.2.0.2.0 - Production on 29-10월-2024 23:44:07

Copyright (c) 1991, 2014, Oracle.  All rights reserved.

Connecting to (DESCRIPTION=(ADDRESS=(PROTOCOL=IPC)(KEY=EXTPROC1)))
STATUS of the LISTENER
------------------------
Alias                     LISTENER
Version                   TNSLSNR for 64-bit Windows: Version 11.2.0.2.0 - Production
Start Date                29-10월-2024 22:00:35
Uptime                    0 days 1 hr. 43 min. 31 sec
Trace Level               off
Security                  ON: Local OS Authentication
SNMP                      OFF
Default Service           XE
Listener Parameter File   C:\oraclexe\app\oracle\product\11.2.0\server\network\admin\listener.ora
Listener Log File         C:\oraclexe\app\oracle\diag\tnslsnr\ljh\listener\alert\log.xml
Listening Endpoints Summary...
  (DESCRIPTION=(ADDRESS=(PROTOCOL=ipc)(PIPENAME=\\.\pipe\EXTPROC1ipc)))
  (DESCRIPTION=(ADDRESS=(PROTOCOL=tcp)(HOST=ljh)(PORT=1521)))
  (DESCRIPTION=(ADDRESS=(PROTOCOL=tcp)(HOST=ljh)(PORT=8080))(Presentation=HTTP)(Session=RAW))
Services Summary...
Service "CLRExtProc" has 1 instance(s).
  Instance "CLRExtProc", status UNKNOWN, has 1 handler(s) for this service...
Service "PLSExtProc" has 1 instance(s).
  Instance "PLSExtProc", status UNKNOWN, has 1 handler(s) for this service...
Service "XEXDB" has 1 instance(s).
  Instance "xe", status READY, has 1 handler(s) for this service...
Service "xe" has 1 instance(s).
  Instance "xe", status READY, has 1 handler(s) for this service...
The command completed successfully
```

## SQL*PLUS를 이용하여 오라클 DBMS 접속
- Oracle DBMS에 접속하기 위해서는 DBMS 도구가 필요
- SQL*PLUS 가 DBMS 도구
```Oracle
sqlplus "/as sysdba"
```
```
PS C:\> sqlplus "/as sysdba"

SQL*Plus: Release 11.2.0.2.0 Production on 화 10월 29 23:44:04 2024

Copyright (c) 1982, 2014, Oracle.  All rights reserved.


Connected to:
Oracle Database 11g Express Edition Release 11.2.0.2.0 - 64bit Production

SQL> Disconnected from Oracle Database 11g Express Edition Release 11.2.0.2.0 - 64bit Production
```