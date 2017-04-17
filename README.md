# Glossary DB setup procedure

---


### Install H2 database

http://www.h2database.com/html/main.html

java -cp h2-1.4.193.jar org.h2.tools.Server -webAllowOthers -tcpAllowOthers -pgAllowOthers


### Console

http://xx.xx.xx.xx:8082/


### Create table

glossary-db-sql\create_glossary.txt

glossary-db-sql\create_glossary_zh.txt

glossary-db-sql\create_glossary_index.txt



### Import 

glossary-db-sql\insert_glossary.txt

glossary-db-sql\insert_glossary_zh.txt

glossary-db-sql\insert_glossary_index.txt



### Export for backup

glossary-db-sql\export_bkup.txt




### For test application as glossary web; tomcat context.xml

`<Resource name="jdbc/bootcamp/datasource" auth="Container" type="javax.sql.DataSource"
    driverClassName="org.h2.Driver"
	url="jdbc:h2:tcp://xx.xx.xx.xx:9092/~/.local/var/h2/glossary-test;MVCC=TRUE;AUTOCOMMIT=FALSE"
	username="sa" password="" defaultAutoCommit="false"
	factory="org.apache.tomcat.jdbc.pool.DataSourceFactory" />`




### Test for user interface API

http://localhost:8080/glossary-web/api/glossary/search



### Just for my knowledge and memorandom..

http://mabu-you-dev.hatenablog.com/entry/2014/11/14/154251

