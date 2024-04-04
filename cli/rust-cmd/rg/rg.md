
# rg  -  ripgrep


```
vim で :grep で ripgrep 実行
if executable('rg')
    let &grepprg = 'rg --vimgrep'
    set grepformat=%f:%l:%c:%m
endif
```


vim からコールするためのオプション
```
--vimgrep
```


.gitignore は default で無視

.gitignore を 無視しない
```
--hidden
```


dir 指定
```
rg key dir
```


大文字小文字の区別
```
-S  smart
-s  区別する
-i  区別しない
```


単語検索
```
rg -w ptrn
```


file name のみを検索対象 ( find の代替 )
```
rg --files -g "*filename*"
```


file type を限定 ( wildcard )
```
rg "pattern" -g "*.lua" -g "*.script"
```


file name のみ表示
```
rg -l
```


行数表示しない
```

```


file name 一括置換
```
rg 'Apple' -l | xargs sd 'Apple' 'Google'
```


grep 形式で出力
```
--no-heading
```


# env

conf file
```
.ripgreprc
```


path set
```
export RIPGREP_CONFIG_PATH="$HOME/.ripgreprc"
^ fish だと違うかも
```


and 検索
```
key1.+key2 のように 正規表現で指定する

^ option による複数単語指定はできない
```



