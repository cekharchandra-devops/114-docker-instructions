FROM almalinux:9
RUN dnf install nginx -y
COPY https://raw.githubusercontent.com/cekharchandra-devops/15-docker-concepts/refs/heads/main/readme.MD /usr/share/nginx/html/index.html
RUN chmod +r /usr/share/nginx/html/index.html
CMD [ "nginx", "-g", "daemon off;" ]