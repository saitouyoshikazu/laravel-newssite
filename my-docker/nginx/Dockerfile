FROM nginx:1.25.2

RUN     apt-get upgrade
RUN     apt-get update
RUN     apt-get install -y --no-install-recommends tzdata && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN     apt-get update
RUN     apt-get install -y locales locales-all && update-locale LANG=$LANG && rm -rf /var/lib/apt/lists/*
RUN     apt-get update

COPY ssl/server.crt /etc/nginx/ssl/server.crt
COPY ssl/server.csr /etc/nginx/ssl/server.csr
COPY ssl/server.key /etc/nginx/ssl/server.key
COPY ssl/server.password /etc/nginx/ssl/server.password

ADD ./ssl.conf /etc/nginx/conf.d/ssl.conf