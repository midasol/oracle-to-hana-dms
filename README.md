# oracle-to-hana-dms

AWS DMS가 SAP HANA DB를 지원하지 않기 때문에 SAP ASE 나 MySQL, PostgreSQL 를 중계 DB로 두고 SAP HANA로 연결해야할 것 같습니다.
S3를 중계 DB로 말씀드리지 않은 경우에는 CDC 기능을 사용하는 것이 간결하지 않기 때문입니다.

다음은 파트너님께서 구상하고 계시는 아키텍쳐에 필요한 AWS DMS에 대한 설명입니다.

1. AWS DataBase Migration Service 란?
https://docs.aws.amazon.com/ko_kr/dms/latest/userguide/Welcome.html
￼￼
2. 마이그레이션 데이타 사이즈가 수 TB 이상일 경우에는 다음과 같이 AWS Snowball 을 이용하여 전송하는 것이 Network을 이용하는 것 보다 빠를 수 있습니다.
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_LargeDBs.Process.html

3. Source DB가 오라클 DB인 경우
Using an Oracle database as a source for AWS DMS
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html

4. CDC function for Oracle
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.Oracle.html#CHAP_Source.Oracle.CDC

5. DDL statements supported by AWS DMS
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Introduction.html#CHAP_Introduction.SupportedDDL
