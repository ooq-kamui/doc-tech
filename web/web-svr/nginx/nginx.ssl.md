
# nginx  -  ssl


## ref

https://cn.teldevice.co.jp/blog/p39750/

https://www.bestssl.net/faq/install-nginx/

https://zenn.dev/sakura_and_kina/articles/97d89dcda40de8


## setting

wip:


## sub domain

wip:

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



