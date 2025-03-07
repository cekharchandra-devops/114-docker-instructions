FROM almalinux:9
RUN dnf install nginx -y
RUN useradd dtuser
USER dtuser
CMD [ "nginx", "-g", "daemon off; user dtuser;" ]

# Since ports below 1024 require root privileges, you can run Nginx on a non-privileged port like 8080:

# solution1 : docker run -d -p:8080:8080 user:v1

#solution2: CMD [ "nginx", "-g", "daemon off;", "user dtuser" ]