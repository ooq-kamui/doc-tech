
# python


## 構文


### if


### for



## var


### cp or ref

list ( ary ) は ref



### var scope

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


### var type

```
a = 1
print(type(a))
```


## list

### 要素数

```
a = [1, 2, 3]

cnt = len(a)
```


### list の末尾に 別の list を連結 ( 結合 )

```
a = [1, 2, 3]
b = [4, 5, 6]

a.extends(b)
```



## string

### 文字列が 数字 かどうか

```
isnumeric()
```



## indent tidy

wip:



