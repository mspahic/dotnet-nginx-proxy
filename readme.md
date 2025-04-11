Proxy host should be created in NGINX Proxy Manager localhost:81

with domain name: localhost, port 5000 and advanced configuration:

location /api1/ {
    proxy_pass http://api1:5000/;
    rewrite ^/api1(/.*)$ $1 break;
}

location /api2/ {
    proxy_pass http://api2:5000/;
    rewrite ^/api2(/.*)$ $1 break;
}




