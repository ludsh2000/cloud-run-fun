FROM nginx
RUN  rm /usr/share/nginx/html/index.html
RUN  mkdir /etc/nginx/html
RUN  echo "" >> /var/log/nginx/error.log
RUN  chmod 766 /var/log/nginx/error.log
RUN  mkdir /etc/nginx/html/news
COPY index.html /etc/nginx/html/news
RUN  date >> /etc/nginx/html/news/index.html
RUN rm /etc/nginx/conf.d/default.conf
COPY site.template /etc/nginx/conf.d/site.template
CMD /bin/bash -c "envsubst < /etc/nginx/conf.d/site.template > /etc/nginx/conf.d/site.conf && exec nginx -g 'daemon off;'"

