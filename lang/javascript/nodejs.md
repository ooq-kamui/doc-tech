
# nodejs


nodebrew で install が無難


## nodebrew

### nodebrew の install

brew で nodebrew を install
```
brew install nodebrew
```


### nodebrew で nodejs の install

```
nodebrew install latest
```

上記で, nodejs, npm が install される


### nodebrew で nodejs の ver confirm
```
nodebrew ls
v.16.6.0
```

### nodebrew で nodejs の ver 指定
```
nodebrew use v16.6.10
```

### nodebrew で nodejs を uninstall, ver 指定
```
nodebrew uninstall vxx.x.xx
```



### npm が使えなくなったとき

path が通っていなくなった可能性がある

path の confirm

npm の install dir

通常は下記
```
~/.nodebrew/current/bin/
```

上記はあるが
具体的な current_ver の dir 配下に npm がない
という現象が起きる
このときは, use ver をnpm が存在する ver に指定し直して対応した








