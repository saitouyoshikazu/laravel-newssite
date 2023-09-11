FROM nginx:1.25.2

COPY ssl/server.crt /etc/nginx/ssl/server.crt
COPY ssl/server.csr /etc/nginx/ssl/server.csr
COPY ssl/server.key /etc/nginx/ssl/server.key
COPY ssl/server.password /etc/nginx/ssl/server.password

ADD ./ssl.conf /etc/nginx/conf.d/ssl.conf