
# git


## git diff

引数は `old` `new` の順
```
git diff old new
```

### worktree と index のdiff を表示
```
git diff
```

### 差分の情報のみを表示
```
git diff --stat
```

### branch1 と branch2 のdiff を表示
```
git diff branch1 branch2
```

### index と commit latest のdiff を表示
```
git diff --cached
```

### commit latest と commit 2nd のdiff を表示
```
git diff HEAD^..HEAD
```

### commit と commit のdiff を表示
```
git diff SHA1..SHA2
```

### ファイル名のみを表示
```
git diff --name-only
```



