# Environment

## LAMP

```ruby
apt-get install apache2
apt-get install mysql-server 
apt-get install mysql-client
apt-get install php-mysql php-curl php-json php-cgi php libapache2-mod-php
```

## LNMP

{% code-tabs %}
{% code-tabs-item title="Installation" %}
```bash
apt-get install php
apt-get install php-mysql
apt-get install php-fpm
apt-get install php-curl php-xml php-mcrypt php-json php-gd php-mbstring
apt-get install nginx
apt-get install mysql-server

vi /etc/php/7.1/fpm/php.ini  /# 将cgi.fix_pathinfo=1这一行去掉注释，将1改为0
vi /etc/php/7.1/fpm/pool.d/www.conf # 配置这个 listen = /var/run/php/php7.1-fpm.sock
service php7.1-fpm restart #  /etc/init.d/php7.1-fpm restart
vi /etc/nginx/sites-available/default # configuration
```
{% endcode-tabs-item %}

{% code-tabs-item title="Configuration" %}
```javascript
listen 80 default_server;
listen [::]:80 default_server;

root /var/www/laravel-ubuntu/public;
index index.php index.html index.htm;

# Make site accessible from http://localhost/
server_name localhost;

location / {
        # First attempt to serve request as file, then
        # as directory, then fall back to displaying a 404.
        try_files $uri $uri/ /index.php?$query_string;
        # Uncomment to enable naxsi on this location
        # include /etc/nginx/naxsi.rules
}
location ~ \.php$ {
        try_files $uri /index.php =404;
        fastcgi_split_path_info ^(.+\.php)(/.+)$;
        fastcgi_pass unix:/var/run/php/php7.1-fpm.sock;
        fastcgi_index index.php;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
        include fastcgi_params;
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

