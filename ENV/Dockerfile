FROM almalinux:9
ENV profile="test" \
    environment="dev"
LABEL author="sekhar" \
      compontent="docker instructions"
EXPOSE 80

RUN dnf install nginx -y
CMD [ "nginx", "-g", "daemon off;" ]