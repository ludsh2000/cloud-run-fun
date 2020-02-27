FROM nginx
RUN  rm /etc/nginx/html/index.html
COPY index.html /etc/nginx/html/
RUN  date >> /etc/nginx/html/index.html
CMD /bin/bash -c "exec nginx -g 'daemon off;'"
