
# git restore


## 基本

wip : ...


## option なし

wip : おそらく
worktree の file を head の内容に戻す `--worktree` と同じ

```
git restore file_name
```


## worktree の file を head の内容に戻す

```
git restore --worktree file_name
```


## index の file を head の内容に戻す

```
git restore --staged file_name
```


## worktree の file を 指定した commit の内容に戻す

```
git restore --tree commit1 file_name
```



