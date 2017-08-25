# 常用Docker命令
### 运行一个新容器
创建一个新的OracleXE并且运行。
`docker run -d -p 9090:8080 -p 1521:1521 wnameless/oracle-xe-11g`
### 查看容器
查看正在运行的容器
`docker ps`
查看所有容器
`docker ps -a`
