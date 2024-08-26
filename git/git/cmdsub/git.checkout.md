
# git checkout


## 基本

基本は

- ある commit の file を worktree  へ取り出す

なのだが, 実質の用途としては,


- branch を指定した場合
  - branch 切り替え
    - 指定 branch の commit head の 全 file が worktree に取り出される
    - 現在の branch も 指定 branch になる


- commit を指定した場合
  - ある commit の file を worktree  へ取り出す

  - 指定 commit が head の場合
    - worktree の file 変更 を破棄



## branch 切り換え 用途

### branch を指定した場合は branch を切り替える

```
git checkout branch_name
```

自分としては,
branch の切り替え は頻繁にやらないのが無難 ( 慣れるまで )

dir ごとに, この dir は この branch と用途を決め, 動かさない

それよりも, 修正を破棄する用途に使用する


### branch 切り替え 強制

```
git checkout -f branch_name
```



## worktree 破棄 用途

### ファイルの変更を 取り消す

```
git checkout -- file_path
```


### ディレクトリ配下の変更を 取り消す

```
git checkout -- dir_path
```


### すべての変更を取り消す

```
git checkout -- .
```



### file の worktree で修正した内容を破棄して, 現在の commit ( head ) の内容に戻す

```
git checkout HEAD -- file_path
```



## 特定 commit の file 取り出し 用途

### commit01 の file01 を worktree へ取り出す

現在の worktree の file01 は破棄される

```
git checkout commit01 -- file01
```

commit_id は 同 branch history になくても, 同 repository のものであれば可



## option

```
-b  新しい branch を作成
```



