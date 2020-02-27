FROM nginx
RUN  rm /usr/share/nginx/html/index.html
COPY index.html /usr/share/nginx/html
RUN  date >> /usr/share/nginx/html/index.html
CMD /bin/bash -c "exec nginx -g 'daemon off;'"
