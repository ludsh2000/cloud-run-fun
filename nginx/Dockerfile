FROM nginx
RUN rm /etc/nginx/conf.d/default.conf
COPY site.template /etc/nginx/conf.d/site.template
COPY index.html   /etc/nginx/html/index.html
CMD /bin/bash -c "envsubst < /etc/nginx/conf.d/site.template > /etc/nginx/conf.d/site.conf && exec nginx -g 'daemon off;'"
