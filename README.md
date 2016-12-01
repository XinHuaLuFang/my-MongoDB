# my-MongoDB

>安装mongodb并添加至系统变量，我的版本是3.4.0。

命令行下运行 MongoDB 服务器
```
    mongod --dbpath d:\MongoDB\db
```

将 MongoDB 添加到系统服务（ :hibiscus: 以管理员身份打开cmd）
```
    mongod --logpath D:\MongoDB\log\mongodb.log --logappend --dbpath D:\MongoDB\db --serviceName MongoDB --install
```

MongoDB后台管理 Shell
```
    mongo
```

查看当前操作的文档（数据库）
```
    db
    // 或者
    db.getName()
```

显示当前db状态
```
    db.stats()
```

列出所有db名称及占用情况（刚创建未添加数据的db不显示）
```
    show dbs
```

连接到test数据库
```
    use test
```

创建数据库（ :hibiscus: 如果数据库不存在，则创建数据库，否则切换到指定数据库。）
```
    use test
```

删除数据库（ :hibiscus: 删除当前数据库 ）
```
    db.dropDatabase();
```

显示当前db中的集合
```
    show collections
    // 或
    db.getCollectionNames()
```

删除集合（ :hibiscus: collection 简写为 col ）
```
    db.col.drop()
```

集合中插入文档（ :hibiscus: document 简写为 doc ）
```
    db.col.insert(doc)
    // 或
    db.col.save(doc)
```

查看集合中的所有文档（ 查看表中的数据 ）
```
    db.col.find()
```

更新文档
```
    db.col.update(
        <query>,
        <update>,
        {
            upsert: <boolean>,
            multi: <boolean>,
            writeConcern: <boolean>
        }
    );
```