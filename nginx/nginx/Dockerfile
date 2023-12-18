FROM nginx:1.19
COPY . /app
RUN rm -rf /etc/nginx/nginx.conf /etc/nginx/conf.d && \
    mkdir -p /etc/nginx/conf.d && \
    ls -l /app/nginx && \
    cp -f /app/nginx/nginx.conf /etc/nginx/nginx.conf && \
    cp -f /app/nginx/web.conf /etc/nginx/conf.d/web.conf