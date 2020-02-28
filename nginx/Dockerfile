FROM nginx
RUN  rm /usr/share/nginx/html/index.html
RUN  mkdir /etc/nginx/html
COPY index.html /etc/nginx/html
COPY index.html /usr/share/nginx/html
RUN  date >> /usr/share/nginx/html/index.html
RUN  date >> /etc/nginx/html/index.html
RUN rm /etc/nginx/conf.d/default.conf
COPY site.template /etc/nginx/conf.d/site.template
CMD /bin/bash -c "envsubst < /etc/nginx/conf.d/site.template > /etc/nginx/conf.d/site.conf && exec nginx -g 'daemon off;'"

