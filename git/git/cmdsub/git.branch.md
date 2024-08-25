
# git branch


## branch list, 現在の branch を表示

```
git branch
```


## remote の branch list を表示

```
git fetch
```

のあと

```
git branch -a
```


## コミットの先端情報も表示する

```
git branch -v
```


## branch を作る

```
git branch branch_name
```


## branch name を変更する

```
git branch -m name_old name_new
```

ex

```
git branch -m master main
```


## branch を切り替える

branch の切り替えは `git branch` ではなく checkout, または switch

```
git checkout branch_name
```


## local branch を削除

```
git branch -d branch_name
```


## remote branch を削除

```
git push origin --delete branch_name
```



