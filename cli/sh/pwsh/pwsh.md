
# pwsh


## cp

https://learn.microsoft.com/ja-jp/powershell/module/microsoft.powershell.management/copy-item?view=powershell-7.4


cp $file1 $dir2/

```
Copy-Item -Path $file1 -Destination $dir2/
```

cp -r $dir1 $dir2/

```
Copy-Item -Recurse -Path $dir1 -Destination $dir2/
```

cp -f

```
Copy-Item -Force -Path $dir1 -Destination $dir2/
```


## ln -s

https://learn.microsoft.com/ja-jp/powershell/module/microsoft.powershell.management/new-item?view=powershell-7.4


$target のシンボリックリンクを $path に作る

```
New-Item -ItemType SymbolicLink -Path $path -Value $target
```



## fzf

PSFzf をinstall する必要がある

```
Install-Module -Name PSFzf -scope currentUser
```

確認

```
Get-InstalledModule | ? Name -eq PSFzf
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



