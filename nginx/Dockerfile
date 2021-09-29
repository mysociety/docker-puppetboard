FROM debian:bullseye-slim

RUN apt-get -qq update \
      && apt-get install -y nginx --no-install-recommends \
      && rm -r /var/lib/apt/lists/*

RUN ln -sf /dev/stdout /var/log/nginx/access.log \
      && ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
