
# git  -  ref rvrs


## push してない commit があるか

```
git log origin/main..main
```


## git merge の vim で, 自分の .vimrc を適用したい

- そもそも, default で立ち上がっているのは vim ではなく, vi

なので,

```
git config --global core.editor vim
```

とする


## git merge で vimdiff を使う

```
git config --global merge.tool vimdiff
```

```
git mergetool
```


## git commit のあと, global の user, email を設定していなかったとき

```
git config --global user.name your_name
```

```
git config --global user.email you@example.com
```

```
git commit --amend --reset-author
```

confirm

```
git log
```



