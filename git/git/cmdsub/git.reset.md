
# git reset


## 基本

head を 指定した commit にする ( 戻す )


次の 3つの mode がある


## --soft

worktree, index の状態は 何も変更せず,
head を 指定した commit にする

```
git reset --soft commit1
```


単純に 直前の git commit を 取り消したい場合,

= 
worktree, index の状態はそのままで
HEAD を 1つ前の commit に戻す

=
--soft で HEAD を 1つ前の commit に戻す

```
git reset --soft HEAD^
```

HEAD^ : 現在の head ( commit ) の 1つ前の commit



## --hard

head を 指定した commit にする,
worktree, index も指定した commit の状態になる

worktree, index で変更していた内容は, 破棄される

```
git reset --hard commit1
```



## --mixed

head を 指定した commit にする,  
worktree の状態は 何も変更しない  
index は指定した commit の状態にする


mode を 省略した場合は --mixed 

```
git reset --mixed commit1
```


add の取り消し をしたい場合

```
git reset --mixed HEAD
```

上記で add の取り消しと同等となる



