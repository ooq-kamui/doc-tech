
# git diff


## 概要のみ表示

### 差分情報のみを表示
```
git diff --stat
```


### ファイル名のみ表示
```
git diff --name-only
```



## 説明

### 同種のものを引数で指定する場合

`old` `new` の順

```
git diff old new
```



## 各種 diff 表示

### work tree と stage の diff

```
git diff
```


### work tree と HEAD ( repo ltst ) の diff

```
git diff HEAD
```


### stage と HEAD ( repo ltst ) の diff

```
git diff --staged
```


### branch1 と branch2 の diff

```
git diff branch1 branch2
```


### index と commit latest の diff

```
git diff --cached
```


### commit prv と commit latest の diff

```
git diff HEAD^..HEAD
```


### commit1 と commit2 の diff

```
git diff SHA1..SHA2
```


### local branch と remote branch の diff

```
git diff main origin/main
```
^ fetch しないとうまくいかない?



