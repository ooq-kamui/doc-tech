
# ssl


## 基本

一般的に site を ssl 化するときに必要なのは, 次

- key
  - 秘密鍵, pem などとも呼ばれる
- csr
  - 公開鍵, 証明書署名要求 などとも呼ばれる
- crt
  - デジタル証明書, サーバー証明書 などとも呼ばれる



## 自己証明書 の作成

上記を openssl で 作成する


### 作業 dir へ移動

```
sudo mkdir /etc/nginx/ssl
```

```
cd /etc/nginx/ssl
```


### key の作成

```
sudo openssl genrsa -out server.key 2048
```

方式によっては pass phrase を入力して設定


### key から csr を作成

次のものを訊かれるので考えておく

- `Country Name (2 letter code) [XX]` : `JP`
- `State or Province Name (full name) []` : `Tokyo`
- `Locality Name (eg, city) [Default City]` : `Komae-shi`
- `Organization Name (eg, company) [Default Company Ltd]` : `ooq-kamui`
- `Organizational Unit Name (eg, section) []` :
- `Common Name (eg, your name or your server's hostname) []` : `ooq.jp`
- `Email Address []` :
- `A challenge password []` : `xxx`
- `An optional company name []` :


sakura で必要なのは次

- 国名(C) : `JP`
- 都道府県名(S/ST) : `Tokyo`
- 市町村名(L) : `Komae-shi`
- 組織名(O) : `ooq-kamui`
- コモンネーム(CN), 実際に接続する URL : `ooq.jp`

https://help.sakura.ad.jp/ssl/2327/?_gl=1*14itm43*_gcl_au*MTE0MDkzODAwOS4xNzI3MDQ0NTgz#heading-1


command

```
sudo openssl req -new -key server.key -out server.csr
```

ex

```
_ sudo openssl req -new -key server.key -out server.csr
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) [XX]:JP
State or Province Name (full name) []:Tokyo
Locality Name (eg, city) [Default City]:
Organization Name (eg, company) [Default Company Ltd]:
Organizational Unit Name (eg, section) []:
Common Name (eg, your name or your server's hostname) []:
Email Address []:

Please enter the following 'extra' attributes
to be sent with your certificate request
A challenge password []:xxx
An optional company name []:
_ 
```

`A challenge password` は 必須入力

`pass phrase` を訊かれる場合は key の `pass phrase` を入力



### key, csr から crt を作成

```
sudo openssl x509 -days 3650 -req -signkey server.key -in server.csr -out server.crt
```

pass phrase を訊かれる場合は key の pass phrase を入力


## ref

https://qiita.com/ll_kuma_ll/items/13c962a6a74874af39c6

https://qiita.com/clown0082/items/551d7c081ff6b41b1717



