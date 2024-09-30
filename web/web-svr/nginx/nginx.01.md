
# nginx


## ref

https://kinsta.com/jp/knowledgebase/install-nginx/

https://qiita.com/riita10069/items/5d36dfeb756e3b6c4978


## install

### centos

```
sudo yum install epel-release
```

```
sudo yum install nginx
```


## launch

```
sudo systemctl start nginx sudo systemctl enable nginx
```


## sakura vps の場合

パケットフィルター の web を解放する


## setting の反映

```
sudo nginx -s reload
```



