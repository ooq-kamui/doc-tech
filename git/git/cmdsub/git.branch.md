
# git branch


## branch list, および 現在の branch を表示

```
git branch
```


## remote の branch list を表示

```
git fetch
git branch -a
```


## コミットの先端情報も表示したい場合

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

branch の切り替えは `git branch` ではないので注意

```
git checkout branch_name
```



