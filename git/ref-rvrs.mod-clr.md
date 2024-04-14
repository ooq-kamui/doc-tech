
# 修正を元に戻す


https://www.atlassian.com/ja/git/tutorials/undoing-changes


## 概要

- git checkout : commit から worktree, index に file を戻す
  - wip ..

- git commit   : --amend で 直前の commit を破棄する


- git reset    : 指定した commit の状態へ戻す


- git restore  : add 済 を add 前 に戻す ??
  - wip ..


使用度 低

- git rebase   : commit 履歴を変更する

- git revert   : commit を削除する新しい commit を作成する



ここでは, push 前 の各段階

- worktree の変更
- index の変更 ( add 後 )
- local repo の変更 ( commit 後 )

のものを, remote commit ltst ( head ) に戻す 方法を記します



## add 前

worktree の変更を commit ltst ( head ) に戻す

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

### git commit --amend



### git reset --??





## push 後

push までしてしまった場合, さらなる修正で直すほうが無難です
( どうしてもの場合を除けば )




