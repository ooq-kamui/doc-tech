
# mysql


## 新しくユーザーを作成する
```
CREATE USER 'your_name'@'localhost' IDENTIFIED BY 'your_password';
```


## 作成したユーザーに作成したデータベースの操作権限を付与する
```
GRANT ALL PRIVILEGES ON database_name.* TO 'your_name'@'localhost';
```


## 設定を反映する

```
FLUSH PRIVILEGES;
```


## .mylogin.cnf を使用して mysql に login する
```
mysql --login-path=local fe_fu
```


```
kamui / _____
```



