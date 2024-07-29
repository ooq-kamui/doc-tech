
# centos stream 9  -  env setup  -  ( sakura vps )


## git

```
sudo dnf -y install git
```


## ruby

```
sudo dnf module -y install ruby:3.3/common
```


## brew

bash にて

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```
(echo; echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"') >> /home/centos/.bashrc
```

```
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
```


## tar

```
sudo dnf install tar
```


## noevim

```
brew install neovim
```


## fish

```
brew install fish
```

install は success したように見える, が

```
fish
```

で, 下記の err

```
fish: error while loading shared libraries: libstdc++.so.6: cannot open shared object file: No such file or directory
```

`libstdc++.so.6` が どの package に入っているかを調べる

```
yum whatprovides */libstdc++.so.6
```

念のためレベルで 32bit and 64bit とも install

```
sudo yum install libstdc++.i686
```

```
sudo yum install libstdc++.x86_64
```

err 解消されない

share lib path を確認

```
sudo ldconfig -p | grep stdc
```

or

```
sudo ldconfig -v
```

問題なさそう

cache clear

```
sudo ldconfig
```

解消されない

```
cat /etc/ld.so.conf
include ld.so.conf.d/*.conf
```

```
ll /etc/ld.so.conf.d/
total 0
```

こちらは 確かに 空である..

では `sudo ldconfig -v` `sudo ldconfig -p` の表示は何なのか..?

try

上記の設定

それでもダメなら

`LD_LIBRARY_PATH` を設定してみる

doing..


ムリなら, いったん, 諦める ( bash を使用 )



