FROM nginx
COPY ./index.html /usr/share/nginx/html
COPY ./server.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
