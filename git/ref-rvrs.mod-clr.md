
# 修正を元に戻す


https://www.atlassian.com/ja/git/tutorials/undoing-changes


## 補足説明

- git checkout : ??
- git reset    : ??
- git restore  : add 済 を add 前 に戻す

の違い

書きかけ(調べ中)です..



## add 前

### git checkout

#### head ( repo commit ltst ) に戻す

```
git checkout -- .
```

```
git checkout .
```


#### file 名を指定して戻す

```
git checkout file_path1
```



## add 後, commit 前

### git reset

#### head ( repo commit ltst ) に戻す

```
git reset ??
```
書きかけ(調べ中)です..



#### file 名を指定して戻す

```
git reset ?? file_path1
```
書きかけ(調べ中)です..



### git restore

#### 1つ前の commit に戻す ( delete file も戻す )

```
git restore . ??
```
書きかけ(調べ中)です..


#### file 名を指定して戻す

```
git restore ?? file_path1 ( delete file も戻す )
```
書きかけ(調べ中)です..



## add 後, commit 後

commit までしてしまった場合, さらなる修正で直すほうが無難です
( どうしてもの場合を除けば )

push までした場合は, なおさらです


### git revert

### git rebase





