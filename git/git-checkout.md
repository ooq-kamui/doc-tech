
# git checkout


## 基本

commit から worktree  へ file を取り出す


## 注意

branch を指定した場合は branch の切り替えが行われる

つまり, branch 切り替えの用途にも使える,
が ( 自分としては ),
branch の切り替え はやらないのが無難

dir ごとに, この dir は この branch と初めに用途を決め,
動かさないほうが無難, 
よって, この用途は忘れる

それよりも, 修正を破棄する用途に使用する ( 自分としては )


## 基本

commit1 の file1 を worktree へ取り出す

現在の worktree の file1 は破棄される

```
git checkout commit1 -- file1
```


file1 の worktree で修正した内容を破棄して,
現在の commit ( head ) の内容に戻す

```
git checkout HEAD    -- file1
```



