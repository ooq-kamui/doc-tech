
# vim


## .vimrc


## 再読み込み
```
:source ~/.vimrc
```

## file

cmd line から複数ファイルタブで起動
```
vim -p **/sp_*.lua
```


---

## neovim の verup

ver 確認
```
nvim -v
```

brew の update
```
brew update
```

neovim の verup
```
brew upgrade neovim
```

netrw ( filer )
```
:Ex
```

```
:e .
```

open
```
:e [filename]
```

標準入力 を vim で開く
```
cat filename | vim -
```

quit all
```
:qa
```

---

## wrap 行の折り返し

行を折り返す
```
:set wrap
```

行を折り返さない
```
:set nowrap
```

---

## mac の vim で tab を入力する

insert mode にする
```
ctl-v
<tab>
```


## visual line にのみコマンドを実行

V などで選択後
: を入力すると
```
:'<,'>
```
と表示されるので, 続けて コマンドを入力すればよい

```
:'<,'>!pwd
```

結果が 選択していた範囲に insert される  
( もとの行は delete される )


sort
```
:sort
```

sort desc
```
:sort!
```

---

## mark

mark lst を表示
```
:marks
```

mark を つける
```
:mark a
:ma a
:k a   < ?
```

mark を はずす
```
:delmark a
```

mark を はずす all
```
:delmark!
```

mark へ jmp
```
`a 
'a 
```

mark へ jmp 検索
```
[`
]`
['
]'
```

---

## register

レジスタを確認する
```
:registers
```

```
:reg
```

register a に登録する
```
"ayy
```

cmd mode で paste
```
c-r レジスタ番号0〜9 ( 直近は 0 )
```

```
yank した文字列を置換
yank した文字列で置換
yank した文字列で検索 ( カーソル位置の単語で検索は * )
```


## grep

sub dir も対象
```
:grep ptrn **.lua
```

2種類の file type を対象
```
:grep ptrn **.lua **.script
```

すべての sub dir file を対象
```
:grep ptrn **
```

1つ目の file を自動的に開かない
```
:grep! ptrn **.lua
```

編集中の file を対象
```
:grep ptrn %
```

grep 結果を tab で開く
```
autocmd QuickFixCmdPost vimgrep,grep tab cwindow
```

quickfix を filter する
```
:packadd Cfilter
:Cfilter ptrn
```

---

## vimgrep

大文字小文字の区別
```
/\c 大文字小文字を区別しない
/\C 大文字小文字を区別する
```

---

## colorscheme

```
:colorscheme [colorscheme]
```

---

## highlight

highlight color confirm
```
:highlight
```

---

## syntax highlight

group name の確認

調べたい場所に cursor 移動してから
```
:echo synIDattr(synID(line("."), col("."), 1), "name")
```

group name の color の確認
```
:highlight [group name]
```

---

## syntax highlight filetype

syntax file を適用

syntax file を下記に置く
```
~/.vim/syntax/lua.vim
```


---

## file 設置場所

vim の場合
```
~/.vim/syntax/lua.vim
```

---

## color set confirm

```
:so $VIMRUNTIME/syntax/colortest.vim
```

---

## c tags

tags file の確認
```
:echo tagfiles()
```

tags file cre
```
ctags -R --languages=lua -f .tags
```

---

## vim script

script 内で normal コマンドを実行
```
:normal cmd
```

---

## key bind の確認

自分で割り当てたキーマップの確認
```
:map  " mode all
:imap " mode insert
:nmap " mode nomal
:vmap " mode visual
:verbose nmap " 定義元ファイル情報も表示
```

mode ins から esc のタイムラグを消去

tmux で
```
set -s escape-time 0
```



