
# rg  ( ripgrep )


## install

brew ( mac / c9 / linux )

```
brew install ripgrep
```


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


## ignore, exclude 除外 設定 について

### 基本

default で 隠しファイル ( .xxx ) は search 対象外

よって, `.gitignore` の内容も 対象外


隠しファイル ( .xxx ) も search 対象とする

```
--hidden
```


### ignore, exclude 設定 の記述

```
~/.ignore
```

に search 対象外とする file, dir を記述できる


実行している dir の `.gitignore` `.ignore` が有効かは未調査

wip:


## 実行時の option の確認

```
--files
--debug
--trace
```


## dir 指定

```
rg key dir
```


## 大文字小文字の区別

```
-i  区別しない
-s  区別する
-S  smart
```


## 単語検索

```
rg -w ptn
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


## or 検索

```
rg -e "ptn1" -e "ptn2" 
```


## and 検索

option による複数単語指定はできない

```
rg key1.+key2
```

のように 正規表現で指定する

順番固定となるが 諦める


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



