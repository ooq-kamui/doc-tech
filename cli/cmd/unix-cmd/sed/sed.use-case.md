
# sed  -  use case


basename, dirname は標準入力を取れない,

sed でやるほうがやりよい ( while read line よりも )

reg exp は, 一見, 複雑だが, 一回 作ってしまえば, それ以上, 考えなくてよい



## file path から 拡張子 のみ取得

```
sed 's|^.*\.\([^\.]*\)$|\1|'
```


## file path から dir 部分を取得

```
sed 's|\(.*\)/.*|\1|'
```



