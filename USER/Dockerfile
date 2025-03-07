FROM almalinux:9
RUN dnf install nginx -y
RUN useradd dtuser
# USER dtuser
CMD [ "nginx", "-g", "daemon off;" ]

# Since ports below 1024 require root privileges, you can run Nginx on a non-privileged port like 8080:

# solution1 : docker run -d -p:8080:8080 user:v1 
# For privileged ports (80, 443): Run as root or use port forwarding (-p 80:8080).



