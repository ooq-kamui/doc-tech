
# python


## koubun


### if


### for




## var

## cp or ref

list ( ary ) は ref



## scope

何も指定しないと local になる

関数内で global を使用する場合に global と指定する

php と同じ


ex

```
a = 0

def tst():
  global a
  a = 1


tst()
print(a)
# => 1
```



