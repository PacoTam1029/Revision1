# Revision1

ID:1e4abb9212e5
docker-compose up -d
docker cp dbcreate.sql 1e4abb9212e5:/home/oracle 
docker cp dbdrop.sql 1e4abb9212e5:/home/oracle 
docker cp dbload.sql 1e4abb9212e5:/home/oracle 
docker cp solution11.sql 1e4abb9212e5:/home/oracle 
docker cp solution1_2.sql 1e4abb9212e5:/home/oracle 
docker cp solution2_2.sql 1e4abb9212e5:/home/oracle 
docker cp solution1.sql 1e4abb9212e5:/home/oracle 
docker cp solution2.sql 1e4abb9212e5:/home/oracle 
ls -la ->list the file name docker 
exec -it 1e4abb9212e5 bash 
 sqlplus / as sysdba 
@dbcreate.sql 
@dbload.sql 
@dbdrop.sql 
@solution1_2.sql
 @solution2_2.sql 
 docker cp c6ead132ca6e:/home/oracle/solution1.lst ./ 
 docker cp c6ead132ca6e:/home/oracle/solution2.lst ./

create user paco7 identified by 12345; 
GRANT CONNECT TO paco7;
 GRANT CREATE SESSION TO paco7;
 grant dba to paco7; 
 conn paco7/12345;

debug: 
conn / as sysdba
 grant RESTRICTED SESSION to paco5;