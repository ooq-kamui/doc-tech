
# win11 env setup


## ctrl2cap install

app installer


## power toys install

win app store ?


## git bash install

app installer


## scoop install

```
set-executionpolicy remotesigned -scope currentuser

iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

or
```
iwr -useb get.scoop.sh | i
```


## power shell install ( v7, core )

app installer


## fd install

```
scoop install fd
```


## rg install

```
scoop install ripgrep
```


## zoxide install

```
scoop install zoxide
```


## fzf install

```
scoop install fzf
```


## neovim install

```
scoop install neovim
```


## vim-plug install

```
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |``
    ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim-data/site/autoload/plug.vim" -Force
```


## neovim plugin fzf-vim install

```
```


## wsl install

```
wsl --install
```



