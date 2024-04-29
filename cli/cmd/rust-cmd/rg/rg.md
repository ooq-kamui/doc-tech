
# rg  ( ripgrep )


## vim から call するための option

```
--vimgrep
```

vim で :grep で ripgrep 実行

```
if executable('rg')
    let &grepprg = 'rg --vimgrep'
    set grepformat=%f:%l:%c:%m
endif
```


## ignore 関連

.gitignore は default で無視

.gitignore を 無視しない

```
--hidden
```


## dir 指定

```
rg key dir
```


## 大文字小文字の区別

```
-S  smart
-s  区別する
-i  区別しない
```


## 単語検索

```
rg -w ptrn
```


## file type を指定

```
rg ptn -g "*.lua" -g "*.md"
```


## file name のみ表示

```
rg -l
```


## 行数表示しない

```
rg -N
```


## file name 一括置換

```
rg 'Apple' -l | xargs sd 'Apple' 'Google'
```


## tag jmp 形式 で出力

file path 表示を 先頭の 1行にまとめない

```
--no-heading
```


## and 検索

option による複数単語指定はできない

```
rg key1.+key2
```

のように 正規表現で指定する


## cnf file name

`.ripgreprc`


## cnf file path

bash

```
export RIPGREP_CONFIG_PATH="$HOME/.ripgreprc"
```

fish

```
set RIPGREP_CONFIG_PATH "$HOME/.ripgreprc"
```


## color setting

.ripgreprc

```
--colors=path:fg:cyan
```



