# Mongodb

docker pull mongo:latest

docker run -itd --name mongo -p 27017:27017 mongo --auth

进入镜像配置：

docker exec -it mongo mongosh admin

db.createUser(
  {
    user: "admin",
    pwd: "admin",
    roles: [ { role: "root", db: "admin" } ]
  }
)

db.auth('admin','admin')

1.数据库用户角色：read、readWrite;

2.数据库管理角色：dbAdmin、dbOwner、userAdmin；

3.集群管理角色：clusterAdmin、clusterManager、clusterMonitor、hostManager；

4.备份恢复角色：backup、restore

5.所有数据库角色：readAnyDatabase、readWriteAnyDatabase、userAdminAnyDatabase、dbAdminAnyDatabase

6.超级用户角色：root

db.createCollection("users")

db.users.insertOne({name:'luuuuo'})

db.users.find()

# 项目新知

- npm
- NRM (npm registry manager)是 npm 的镜像源管理工具，有时候国外资源太慢，使用这个就可以快速地在 npm 源间切换。
- yarn 速度超快: Yarn 缓存了每个下载过的包，所以再次使用时无需重复下载。 同时利用并行下载以最大化资源利用率，因此安装速度更快。
  超级安全: 在执行代码之前，Yarn 会通过算法校验每个安装包的完整性。

项目工程搭建

注册功能

登录功能

登录拦截

退出登录

文章发布

文章列表

分页查询

删除文章

修改文章

文章详情页

文件上传
