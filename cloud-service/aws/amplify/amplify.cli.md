
# amplify cli


## 基本的な subcmd

```
amplify configure        o    # user ( iam ) を追加するなど
                          
amplify init                  # init backend
                              #   amplify/ src/ が作成される
                          
amplify add                   # app で使用する機能を追加
                          
amplify update                # app で使用する機能を 更新
                          
amplify status           o    # 状態を確認
                              # aws cloud に push されていない local resource の状態を 表示する
                              # ( git status に似ている ? )
                          
amplify pull             o    # ?? を pull する
                              #   sheet 1 の流れの中で
                              #   pull の紐づき対象はどう 設定されているのか
                          
amplify env list         o    # 環境の 確認
                          
amplify env add dev      o    # 環境の 追加

amplify env checkout dev      # 環境の 切り替え

amplify env get               # 環境の 詳細情報 表示

amplify mock                  # local で test

amplify mock api              # local で test, api

amplify push             o    # local の backend resource を cloud で provisioning
                          
amplify publish          o    # amplify push したものを s3 に deploy する
                              # local の backend resource を cloud で provisioning
                          
amplify api              o    # api resource の操作 
                          
amplify function         o    # function resouce の操作


amplify console

amplify console api

amplify delete                # cloud resource をすべて削除

amplify help                  # help
```


## amplify add xxx で 追加可能な aws resource

```
api           - api gateway ( rest ), app sync ( graphql )

auth          - cognito

storage       - s3, dynamo db

function      - lambda

analytics     - pinpoint

hosting       - s3, cloud front distribution

notifications - pinpoint

interactions  - lex
```

ex

```
amplify add api               # api を作成

amplify add hosting           # deploy method select
```



