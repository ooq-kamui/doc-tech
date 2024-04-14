
# git checkout


## git checkout とは

repo ( commit ) から work-tree, index へ file を取り出すこと


## 注意

branch を指定した場合は branch の切り替えが行われる

つまり, branch 切り替えの用途にも使える,
が, いったん ( 自分としては ),

branch の切り替えは git branch でやるとして,
この用途は忘れる


それよりも, 修正を破棄する用途に使用する ( 自分としては )


## 基本

wip ..

```
git checkout commit1 -- file
```


wip ..

```
git checkout HEAD   -- file
```



