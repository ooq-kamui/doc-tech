
# git restore


## 基本

wip:

### HEAD とは

その branch の 最新 commit のこと



## option なし の場合

おそらく, 
`--worktree` と同じ, worktree の file を HEAD の内容に戻す
wip : ^ confirm

```
git restore file_name
```


## worktree の file を HEAD の内容に戻す

```
git restore --worktree file_name
```


## staged の file を HEAD の内容に戻す

```
git restore --staged file_name
```


## worktree の file を 指定した commit の内容に戻す

```
git restore --tree commit1 file_name
```


## ref

https://tracpath.com/docs/git-restore/


