
# awscli dynamo db


## table lst

```
aws dynamodb list-tables
```


## table describe

```
aws dynamodb describe-table --table-name tbl_name
{
    "Table": {
        "AttributeDefinitions": [
            {
                "AttributeName": "created_at",
                "AttributeType": "S"
            },
            {
                "AttributeName": "post_id",
                "AttributeType": "N"
        ( 省略 )
```


## item put ( ins )

```
aws dynamodb put-item --table-name fe-wa.m \
--item '{"prt": { "S": "chara"   }, "id": { "S": "camilla" }, "name": { "S": "カミラ" } }'
```


## item get by key ( select )

```
aws dynamodb get-item --table-name fe-wa.m \
--key '{"prt": {"S": "chara" }, "id": { "S": "camilla" } }'
```


## query

```
aws dynamodb query --table-name fe-wa.m \
--key-condition-expression 'prt = :prt and id = :id' \
--expression-attribute-values '{":prt":{"S":"chara"}, ":id":{"S": "camilla"}}'
```


## scan

```
aws dynamodb scan --table-name fe-wa.m \
--filter-expression 'msg = :msg' \
--expression-attribute-values '{ ":msg": { "S": "cc" } }'
```


## select count

```
aws dynamodb query --table-name fe-wa.t \
--key-condition-expression 'prt = :prt ' \
--expression-attribute-values '{ ":prt": { "S": "chara" } }' \
--select COUNT
```


## cnd, ~ で始まる

```

```

## val を 別file

```

```


## text 形式で output

```

```


## 予約語

https://dev.classmethod.jp/articles/dynamodb_handling_reserved_keyword/



## ref

https://www.wakuwakubank.com/posts/675-aws-cli-dynamodb/

https://qiita.com/ekzemplaro/items/93c0aef433a2b633ab4a

https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/cli-services-dynamodb.html

iam setting

https://www.hands-lab.com/tech/t4379/



