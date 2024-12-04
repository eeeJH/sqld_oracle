# SQLD 3 Day

- 계정 생성
- 계정 권한 부여
---
## 계정생성
```
SQL> CREATE USER EEEJH38 IDENTIFIED BY EEEJH38;

CREATE USER EEEJH38 IDENTIFIED BY EEEJH38

            *

1행에 오류:

ORA-65096: 공통 사용자 또는 롤 이름이 부적합합니다.
```
- C##을 붙인 이름은 만들 수 있지만, 일반 이름은 사용할 수 없다.
- SESSION 설정을 변경하면 제약없이 사용할 수 있다.

```
SQL> ALTER SESSION SET "_ORACLE_SCRIPT"=TRUE;

세션이 변경되었습니다.
```

--- 

```
SQL> CREATE USER EEEJH38 IDENTIFIED BY EEEJH38;

사용자가 생성되었습니다.
```