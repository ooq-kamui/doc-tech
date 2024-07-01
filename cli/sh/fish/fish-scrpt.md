
# fish script


## 真偽値

```
真 : 0
偽 : 1
```


## 演算子 ( test コマンドの オプション )

### 文字列

```
-z STR  STR が 空文字
-n STR  STR が 1文字以上の文字列 ( 空文字でない )

STRING1 =  STRING2  STRING1 と STRING2 が同じ
STRING1 != STRING2  STRING1 と STRING2 が異なる
```

### ファイルとディレクトリ関連

```
-b FILE  ブロックデバイス
-c FILE  キャラクタデバイス
-d FILE  ディレクトリ
-e FILE  存在する
-f FILE  通常のファイル
-g FILE  setgidアクセス権を持つ
-G FILE  存在し、ユーザと同じグループIDである
-L FILE  シンボリックリンク
-O FILE  存在し、ユーザ所有である
-p FILE  名前付きパイプ
-r FILE  読み込み可能
-s FILE  ファイルサイズが0より大きい
         (空ファイルではない)
-S FILE  ソケット
-t FD    端末である
-u FILE  setuidアクセス権を持つ
-w FILE  書き込み可能。
         ただし、ファイルシステムが
         読み込み専用であることまではチェックしない
-x FILE  実行可能
```

### 整数関連

```
NUM1 -eq NUM2  NUM1 と NUM2 が同値
NUM1 -ne NUM2  NUM1 と NUM2 が同値ではない
NUM1 -gt NUM2  NUM1 >  NUM2 
NUM1 -ge NUM2  NUM1 >= NUM2 
NUM1 -lt NUM2  NUM1 <  NUM2 
NUM1 -le NUM2  NUM1 <= NUM2 
```
整数のみサポート


### 式を組み合わせる

```
COND1 -a COND2  COND1 と COND2 の両方が真
COND1 -o COND2  COND1 と COND2 のどちらかが真
! EXPRESSION    EXPRESSION が偽
```


### 括弧で囲むことで 条件式をまとめられる

```
( EXPRESSION ) は EXPRESSION の値を返す
```
コマンド置換 として解釈されるのを防ぐために
\( とエスケープが必要



