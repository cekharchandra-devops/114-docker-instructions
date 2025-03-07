FROM almalinux:9
RUN dnf install nginx -y
RUN useradd dtuser
USER dtuser
CMD [ "nginx", "-g", "daemon off;" ]