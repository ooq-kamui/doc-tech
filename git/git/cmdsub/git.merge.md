
# git merge


## 基本

別の branch ( の commit head ) を 現在の branch へ取り込む

```
git merge branch_other
```


### 補足

`git pull` は `git fetch` + `git merge FETCH_HEAD`



## faq

`git merge` で

```
fatal: refusing to merge unrelated histories
```

が出た場合

```
git merge --allow-unrelated-histories target_branch
```

で いける



## git merge で vim を使う

```
git config --global core.editor vim
```


## merge で vimdiff を使う

https://scior.hatenablog.com/entry/2021/05/05/193113

git mergetoolを使う


```
git mergetool -t vimdiff
```

で, vimdiff を利用した編集となる

config に設定する場合は下記

```
git config --global merge.tool vimdiff
```

```
git mergetool
```


## git mergetool ( vimdiff ) の使いかた

上 : local / base / remote

下 : 作業中のファイル


## `.orig` file とは

git mergetool で編集後にできる backup file

とくに用途がなければ, rm してよい



