
# vim script


変数の代入
```
let foo = "hoge"
```

変数の削除
```
unlet foo
```


変数の scope
```
l: 関数のローカル
a: 関数の引数 ( 関数内のみ )
g: グローバル
b: 現在のバッファ  のローカル
w: 現在のウィンドウのローカル
t: 現在のタブページのローカル
s: vim スクリプトのローカル
v: グローバル, vimの定義
```


for 文
```
for val in range(1, 9)
  echo val
endfor
```

```
for val in [1, 2, 3]
  echo val
endfor
```


文字列 連結
```
let str = 'vim'
echo 'this editor is ' . str . ' !'
```


ar list ( idx )
```
let lst = ['one', 'two', 'three']
```

ar dict ( key-val )
```
let dct = {'one': '1', 'two': '2', 'three': '3'}
" dct['two'] で 参照
```


comment
```
" comment
```


func lib
```
https://vim-jp.org/vimdoc-ja/usr_41.html#function-list
```


script 内で normal コマンドを実行
```
normal cmd
```











