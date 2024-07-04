
# sed  -  use case


## file path 関連

basename, dirname は標準入力を取れない,

sed でやるほうが やりよい ( while read line よりも )

reg exp は, 一見, 複雑だが, 一回 作ってしまえば, それ以上, 考えなくてよい

fish function を作るなどしておけば なおよい


### file path から 拡張子 ext のみ取得

```
sed 's|^.*\.\([^\.]*\)$|\1|'
```


### file path から dir 部分を取得

```
sed 's|\(.*\)/.*|\1|'
```


## 最短一致

sed に最短一致は用意されていない

先頭文字以外の繰り返し でマッチさせる

ex

a.txt
```
{"aaa": {"ccc_a": "zzz"}, "bbb": {"ccc_b": "zzz"}}
```

に対して, 深く考えないと最長一致でこうなる

```
cat a.txt | sed "s/ccc.*}/}/g"
aaa: {}
```

最短一致

```
cat a.txt | sed "s/ccc[^{]*}/}/g"
aaa: {} bbb: {}
```


## カラム 抽出

sed でないほうが無難かも

awk でやるべし



