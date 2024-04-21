
# git stash


## 基本

変更 ( worktree ) を 退避し, git pull 後, 退避した file を元に戻す
ことができる


基本的には下記の流れで 実行すれば 問題ない

```
git stash list            # 確認

git stash save 'comment'

git stash list            # 確認

git status                # 確認

git pull origin main  --rebase

git stash pop

git stash list            # 確認

git status                # 確認
```



## 保存された file 一覧 を表示する

```
git stash list
```


## 変更 を 保存

```
git stash save 'comment'
```


## 直近に 保存された file を復旧

```
git stash pop
```


## 直近に 保存された file を破棄

```
git stash drop
```


## err sample

手元 ( worktree ) の変更を commit せずに
pull しようとすると
下記のエラーとなる

```
error: Your local changes to the following files would be overwritten by merge:
        path/to/file
Please, commit your changes or stash them before you can merge.
Aborting
```



