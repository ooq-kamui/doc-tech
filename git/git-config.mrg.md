
# git


## git config


### 基本

- local
  - `.git/config`
- global
  - `~/.gitconfig`
- system
  - os によって dir は異なる, 通常 system はあまり意識しない

がある



### 表示する

```
git config --list
```


### user.name を設定する

local を設定
```
git config user.name "mona lisa"
```

確認
```
git config user.name
```


### user.email を設定する

local を設定
```
git config user.email "smpl@smpl.com"
```

確認
```
git config user.email
```



#### global
```
git config --global user.name "mona lisa"
```

確認
```
git config --global user.name
```



