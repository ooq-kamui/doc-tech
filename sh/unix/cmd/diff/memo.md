
# diff


## vimdiff を使う

```
$ vimdiff a.txt b.txt
```

次でも同じ
```
$ vim -d a.txt b.txt
```


操作
dp   左の差分を右へマージ
do   右の差分を左へマージ
]-c  次の差分へジャンプ
[-c  前の差分へジャンプ


## git diff

```
$ git diff a.txt b.txt
```


## option

```
-y  左右に並べて表示

-u  unified 形式
     違いのある箇所を1つにまとめて, - 記号 と + 記号 で変更箇所を示す
```



