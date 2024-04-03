
# git stash


手元 ( working directory ) の変更を commit せずに
pull しようとすると
下記のエラーとなる

```
error: Your local changes to the following files would be overwritten by merge:
        path/to/file
Please, commit your changes or stash them before you can merge.
Aborting
```

この場合
stash ( 変更を一時的に隠す ) してから pull します

手順は下記


1. stash save: 現在の状態を保存し, git 上から変更箇所を隠します
```
git stash save "comment"

Saved working directory and index state On master: <コメント>
HEAD is now at 13770bf hoge
```

"comment" を付けることも出来ます
2 の shash list で見たときに何の shash か分かり易くなります


2. stash list の確認
```
git stash list

stash@{0}: On master: <コメント>
```


3. pull
```
$ git pull origin master
```


4. stash pop: 1で stash した変更箇所を元に戻す
```
git stash pop

Auto-merging path/to/file
  :
(snip)
  :
Dropped refs/stash@{0} (fb418991e1ace34585c49007c0976a19e89f3efd)
```

おわり



