# 基于Python + nginx + supervisord 的博客网站

> 参考 [廖雪峰老师的python实战章节](https://www.liaoxuefeng.com/wiki/1016959663602400/1018138095494592) 实现了基于docker搭建的环境

## 网站启动
> docker-compose up -d

1. 建库
使用数据库工具访问mysql localhost:3306 ，用户名为 root 密码为 my-secret-pw。执行 schema.sql  数据库数据库脚本
2. 重启supervisor
> docker-compose restart supervisor 
3. 注册用户
   访问网站： http://localhost:8001
4. 添加管理员
   在数据库awesome库 user表中更改字段admin为1即可
5. 访问：http://localhost:8001/manage  登录管理员，就可以管理评论、文章等信息了