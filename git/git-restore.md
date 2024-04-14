
# git restore


## 基本

...



## worktree の file を head の内容に戻す

```
git restore --worktree file1
```


## index の file を head の内容に戻す

```
git restore --staged file1
```


## worktree の file を 指定した commit の内容に戻す

```
git restore --tree commit1 file1
```



