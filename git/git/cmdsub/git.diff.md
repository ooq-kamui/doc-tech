
# git diff


## 概要のみ表示 ( file の中身を表示しない )

### 差分情報のみを表示

```
git diff --stat
```


### file_name のみ表示

```
git diff --name-only
```



## 基本

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


### index と commit latest の diff

```
git diff --cached
```

wip : 1つ上のと違いは.. ??


### branch1 と branch2 の diff

```
git diff branch1 branch2
```

`clone` 直後などの場合, `git switch` するなどしたあとでないと,
できないときあり


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

^ fetch しないとうまくいかない ?

file を指定する場合は ?



## diff 結果を vimdiff で見る

```
git difftool ...
```



