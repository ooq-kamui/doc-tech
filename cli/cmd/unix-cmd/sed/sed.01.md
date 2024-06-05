
# sed


## option

```
-E  拡張正規表現

-r  拡張正規表現
```


実行結果を入力ファイルに上書き保存する

```
sed -i '' -e "s/srch/rpl/g" file_name.txt
```


## sed cmd

別ファイルの内容を差し込む

```
sed "/key/ r file.txt"

# key の行の下の行に差し込まれる
# key の行は消えない
```


元ファイルの表示のみ

```
sed -n "/aa/,/cc/ p"
```

option -n と併用


m 行目を表示

```
sed -n "m p"
```


## 位置指定

最後の行

```
sed "$ s/find/replace/g"
```


m 行目から n 行目

```
sed "m,n s/find/replace/g"
```


m 行のみ

```
sed "m s/srch/rpl/g"
```


key1 のある行から key2 のある行

```
sed "/key1/,/key2/ s/find/replace/g"
```


key のある行

```
sed "/key/ s/find/replace/g"
```


## 削除

key1 のある行から key2 のある行 を削除

```
sed "/key1/ d"
```


key1 のある行から key2 のある行 を削除

```
sed "/key1/,/key2/ d"
```


## etc

置換後に tab

```
t=$'\t'
```

置換後に cr

```
LF=$(printf '\n_');LF=${LF%_}
```



