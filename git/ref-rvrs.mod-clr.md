
# 修正を元に戻す


https://www.atlassian.com/ja/git/tutorials/undoing-changes


## 補足説明

- git checkout : ??
- git reset    : ??
- git restore  : add 済 を add 前 に戻す ??

- git revert   : 
- git rebase   : 

の違い

wip ..


ここでは, push 前 の各段階

- work-tree の変更
- index の変更 ( add 後 )
- local repo の変更 ( commit 後 )

のものを, remote commit ltst ( head ) に戻す 方法を記します


## add 前

work-tree の変更を remote commit ltst ( head ) に戻す

### git checkout

#### head ( repo commit ltst ) に戻す

```
wip .. ?

git checkout -- .
```

```
wip .. ?

git checkout .
```


#### file 名を指定して戻す

```
wip .. ?

git checkout file_path1
```




## add 後 ( commit 前 )

index の変更を remote commit ltst ( head ) に戻す

### git reset

#### head ( repo commit ltst ) に戻す

```
wip .. ?

git reset ??
```
wip ..



#### file 名を指定して戻す

```
wip .. ?

git reset ?? file_path1
```
wip ..


### git restore

#### 1つ前の commit に戻す ( delete file も戻す )

```
wip .. ?

git restore . ??
```
wip ..


#### file 名を指定して戻す

```
wip .. ?

git restore ?? file_path1 ( delete file も戻す )
```
wip ..




## commit 後 ( push 前 )

commit までしてしまった場合, さらなる修正で直すほうが無難です
( どうしてもの場合を除けば )


### git revert

### git rebase




## push 後

push までしてしまった場合, さらなる修正で直すほうが無難です
( どうしてもの場合を除けば )

wip ..



