
# awscli dynamo db


## ref

https://www.wakuwakubank.com/posts/675-aws-cli-dynamodb/

https://qiita.com/ekzemplaro/items/93c0aef433a2b633ab4a

https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/cli-services-dynamodb.html

iam setting

https://www.hands-lab.com/tech/t4379/


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

ex

```
aws dynamodb put-item --table-name fe-wa.m \
--item '{"prt": { "S": "chara"   }, "id": { "S": "camilla" }, "name": { "S": "カミラ" } }'
```


## item get by key ( select )

ex

```
aws dynamodb get-item --table-name fe-wa.m \
--key '{"prt": {"S": "chara" }, "id": { "S": "camilla" } }'
```


## query ( select )

ex

wip:

```
aws dynamodb query --table-name fe-wa.m \
--key-condition-expression 'prt = :prt and id = :id ' \
--expression-attribute-values '{":prt": {"S": "chara" }, ":id": {"S": "camilla" } }'
```


## scan ( select )

ex

wip:

```
aws dynamodb scan --table-name fe-wa.m \
--filter-expression 'msg = :msg' \
--expression-attribute-values '{ ":msg": { "S": "cc" } }'
```


## 予約語

https://dev.classmethod.jp/articles/dynamodb_handling_reserved_keyword/




