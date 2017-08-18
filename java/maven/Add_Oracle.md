### 执行命令：
mvn install:install-file -Dfile=D:/app/liuxx_oracle/product/12.1.0/dbhome_1/jdbc/lib/ojdbc7.jar -DgroupId=com.oracle -DartifactId=ojdbc7 -Dversion=12.1.0 -Dpackaging=jar

---
### 在POM中添加：
<dependency>
	<groupId>com.oracle</groupId>
	<artifactId>ojdbc7</artifactId>
	<version>12.1.0</version>
</dependency>