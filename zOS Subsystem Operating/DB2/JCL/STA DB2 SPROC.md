# Start DB2 Stored procedure

```
//${USERID}D JOB (${JOB_ACCOUNTING_INFO}),'START DB2 SPROC',REGION=2M,
//        MSGCLASS=H,CLASS=${JOB_CLASS}
//START1    EXEC PGM=IKJEFT01,DYNAMNBR=20
//SYSTSPRT  DD SYSOUT=*
//STEPLIB   DD DSN=${DB2_SDSNLOAD},DISP=SHR
//SYSPRINT  DD SYSOUT=*
//SYSUDUMP  DD SYSOUT=*
//SYSOUT    DD SYSOUT=*
//SYSTSIN   DD *
  DSN SYSTEM(${SUBSYSTEM_NAME})
  -START PROCEDURE(@{DB2_SPROC_1}.@{DB2_SPROC_2})
  END
//SYSIN     DD DUMMY
```
