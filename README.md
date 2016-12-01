# my-MongoDB

>安装mongodb并添加至系统变量，我的版本是3.4.0。

命令行下运行 MongoDB 服务器
```
    mongod --dbpath d:\MongoDB\db
```

将 MongoDB 添加到系统服务（:hibiscus:以管理员身份打开cmd）
```
    mongod --logpath D:\MongoDB\log\mongodb.log --logappend --dbpath D:\MongoDB\db --serviceName MongoDB --install
```

MongoDB后台管理 Shell
```
    mongo
```

命令
|:---------|:--------------------------|
| db       | 查看当前操作的文档（数据库） |
| show bds | 列出所有db名称及占用情况    |
| use test | 连接到test数据库           |

创建数据库（:hibiscus:）
```
    use test
```
