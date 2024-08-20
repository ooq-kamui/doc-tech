
# git checkout


## 基本

commit から worktree  へ file を取り出す


## branch を指定した場合は branch を切り替える

```
git checkout branch_name
```

注意

branch 切り替えの用途に使用する

が ( 自分としては ),
branch の切り替え は頻繁にやらないのが無難

dir ごとに, この dir は この branch と初めに用途を決め,
動かさないほうが無難, 

それよりも, 修正を破棄する用途に使用する
( 自分としては )


## branch 切り替え 強制

```
git checkout -f branch_name
```


## commit1 の file1 を worktree へ取り出す

現在の worktree の file1 は破棄される

```
git checkout commit1 -- file1
```


## file1 の worktree で修正した内容を破棄して, 現在の commit ( head ) の内容に戻す

```
git checkout HEAD    -- file1
```



