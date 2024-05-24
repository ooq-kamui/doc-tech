
# amplify env


## env の list 表示

```
amplify env list
```


## env の 追加

```
amplify env add dev
```

ここで追加しているのは backend


## env の 切り替え

```
amplify env checkout dev
```


## env の 詳細情報 表示

```
amplify env get
```


## cloud 上にある env を pull

```
amplify env pull
```

local での修正を破棄して, cloud の状態に 戻す

```
amplify env pull --restore
```

or

```
amplify pull
```


## env の import

```
amplify env import
```

あまり使わない ?


## env の 削除

あまり使わないほうが無難

```
amplify env remove
```



