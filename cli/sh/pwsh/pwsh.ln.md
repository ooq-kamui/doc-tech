
# ln -s

https://learn.microsoft.com/ja-jp/powershell/module/microsoft.powershell.management/new-item?view=powershell-7.4


## $target のシンボリックリンクを $path に作る

```
New-Item -ItemType SymbolicLink -Path $path -Value $target
```



