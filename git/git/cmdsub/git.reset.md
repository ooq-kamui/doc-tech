
# git reset


## 基本

head の位置を 戻す

戻す位置 ( commit ) は 引数で指定


## option

```
--soft  : head を 指定した commit にする ( 戻す )
          worktree, staged は 変更しない

--hard  : head を 指定した commit にする ( 戻す )
          worktree, staged も 変更
            変更していた場合, 破棄され
            指定した commit の内容 になる

--mixed : head を 指定した commit にする ( 戻す )
          worktree は変更しない  
          staged   は変更
            変更していた場合, 破棄され
            指定した commit の内容 になる

option なし : --mixed

```


## --soft

head を 指定した commit にする ( 戻す )  
worktree, staged は 変更しない

```
git reset --soft commit01
```


### --hard

head を 指定した commit にする ( 戻す )  
worktree, staged も 変更  
  変更していた場合, 破棄され  
  指定した commit の内容 になる

```
git reset --hard commit01
```


### --mixed

head を 指定した commit にする ( 戻す )  
worktree は変更しない  
staged   は変更  
  変更していた場合, 破棄され  
  指定した commit の内容 になる

```
git reset --mixed commit01
```



## 事例

### 直前の commit を 破棄

```
git reset --soft HEAD^
```

補足

```
=  worktree, staged の状態はそのままで, HEAD を 1つ前の commit に戻す

=  --soft で HEAD を 1つ前の commit の head にする ( 戻す )

HEAD^ : 現在の head ( の commit ) の 1つ前の commit
```



### add ( staged ) を 破棄

```
git reset --mixed HEAD
```



### local を remote に強制的に合わせる

branch は main とする

```
git reset --hard origin/main
```



