
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

launch

```
sudo systemctl start nginx sudo systemctl enable nginx
```


## sakura の場合

sakura の場合, パケットフィルター の web を解放しましょう



## setting 反映

```
sudo nginx -s reload
```


## sub domain

/etc/nginx/conf.d/virtualhost.conf

```
server {
    listen 80;
    server_name sub.domain-name.com;
    root /usr/share/nginx/html/sub;

    location / {
      index index.html;
    }
}
```



