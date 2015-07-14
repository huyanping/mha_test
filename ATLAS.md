atlas介绍
1.读写分离
2.从库负载均衡
4.支持分表
5.DBA可平滑上下线DB
6.自动摘除宕机的DB

分表原理：
当通过Atlas执行（SELECT、DELETE、UPDATE、INSERT、REPLACE）操作时，
Atlas会根据分表结果（id%100=k），定位到相应的子表（stu_k）。
例如，执行select * from stu where id=110;，
Atlas会自动从stu_10这张子表返回查询结果。
但如果执行SQL语句（select * from stu;）时不带上id，
则会提示执行stu 表不存在。

社区不活跃，没有pull request
bug较多
功能限制太多

