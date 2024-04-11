
# pwsh


## ln -s

$target のシンボリックリンクを $path に作る

```
New-Item -ItemType SymbolicLink -Path $path -Value $target
```



## color setting

### 設定できる箇所, 現在の setting の確認

```
$PSStyle.FileInfo | Get-Member
```


### 設定できる color の確認

```
$PSStyle.Foreground | Get-Member
```

```
$PSStyle.Background | Get-Member
```


### set

文字色 を設定する

```
$PSStyle.FileInfo.Directory = $PSStyle.Foreground.Cyan
```

文字色 と 背景色 を設定する

```
$PSStyle.FileInfo.Directory = $PSStyle.Foreground.White + $PSStyle.Background.Blue
```


cmdline 入力候補 の設定

```
Set-PSReadLineOption -Colors @{ InlinePrediction = $PSStyle.Foreground.BrightCyan }
```


bell sound off

```
Set-PSReadlineOption -BellStyle None
```



