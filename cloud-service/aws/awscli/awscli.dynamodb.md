
# awscli dynamo db


## ref

https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/cli-services-dynamodb.html

https://qiita.com/ekzemplaro/items/93c0aef433a2b633ab4a

https://www.wakuwakubank.com/posts/675-aws-cli-dynamodb/


## describe table

```
aws dynamodb describe-table --table-name table_name
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



