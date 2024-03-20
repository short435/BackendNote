

# Nginx

## 1. What's Nginx

* 常被使用作為反向代理(==Reverse Proxy==)、負載平衡(==Load Balancer==)、HTTP快取(==Http Cache==)

## 2. Why Choosing Nginx as the Server

### 2.1 Pros

* 記憶體消耗低
* 處理IO並發與靜態文檔上優於Apache
* 配置簡單


### 2.2 Cons

* 可用模組不如Apache多
* Rewrite
* More suitable to work on Ubuntu than Windows

## 3. How to set up Nginx

### 3.1 Linux

* Installation
```shell=
sudo apt install nginx 
```

* Start Services
```shell=
sudo systemctl start nginx
```

* ReStart Services
```shell=
sudo systemctl restart nginx
```

* Enable Services
    *  開機自動啟用Nginx
```shell=
sudo systemctl enable nginx
```

## 4. Configurations

### 4.1 Proxy

* Http Proxy
```nginx=
    server {
        listen 80;
        server_name ${ip};
    }
```
* Https Proxy
```nginx=
    server {
        listen 443 ssl;
        server_name ${ip or domain name};
        ssl_certificate {path for certificate file};
        ssl_certificate_key {path for private key file};
    }
```

延伸閱讀：[How to verify your ssl certification](https://)

## Reference

- https://www.cloudflare.com/zh-tw/learning/cdn/glossary/reverse-proxy/
- [Nginx vs Apache](https://por.tw/Website_Design/%E7%B6%B2%E9%A0%81-http-%E4%BC%BA%E6%9C%8D%E5%99%A8-apache-%E8%88%87-nginx-%E7%9A%84%E5%84%AA%E7%BC%BA%E9%BB%9E%E6%AF%94%E8%BC%83%EF%BC%88%E7%B6%B2%E7%AB%99%E6%9E%B6%E8%A8%AD%E6%95%99%E5%AD%B8/)
- [Intro for Nginx](https://sharefunyeh.gitbooks.io/webdev/content/articles/understand-nginx-proxy-load-balancing-buffer-and-cache.html)