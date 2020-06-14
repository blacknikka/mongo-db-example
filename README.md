## docker-compose
```bash
$ docker-compose up -d
```

```bash
$ docker-compose exec mongo bash
```

## mongoDBメモ
### `mongotop`, `mongostat`の実行
```bash
$ mongotop -u root --authenticationDatabase=admin
$ mongostat -u root --authenticationDatabase=admin
```

### 基本的なコマンド
- login
```bash
$ mongo admin -u root -p
```

- DB一覧
```bash
> show databases
```

- DB切り替え（なければ新規作成するらしい）
```bash
> use mydb
```

- collection表示
```bash
> show collections
```

- insert
```bash
> db.mycollection.insert({name: "namae", address: "addr", countory: "JPN"})
> db.mycollection.insert({name: "namae2", address: "addr", area: "ASIA"})
```

- select(all)
```bash
> db.mycollection.find()
```

- select(one)
```bash
> db.mycollection.findOne()
```

- 一つのカラムを取得
```bash
> db.mycollection.findOne()["name"]
```

- 条件付きで取得
```bash
> db.mycollection.find({name: "namae2"})
{ "_id" : ObjectId("5ee5a89c0204b6dd749ff0a4"), "name" : "namae2", "address" : "addr", "area" : "ASIA" }
```
