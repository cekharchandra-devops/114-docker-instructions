# FROM almalinux:9
# RUN dnf install nginx -y
# RUN useradd dtuser
# # USER dtuser
# CMD [ "nginx", "-g", "daemon off;" ]

# # Since ports below 1024 require root privileges, you can run Nginx on a non-privileged port like 8080:

# # solution1 : docker run -d -p:8080:8080 user:v1 
# # For privileged ports (80, 443): Run as root or use port forwarding (-p 80:8080).



FROM almalinux:9  

# Install Nginx  
RUN dnf install nginx -y  

# Create a non-root user  
RUN useradd -m dtuser  

# Modify the Nginx config file to use 'dtuser' instead of 'nginx'  
RUN sed -i 's/^user .*/user dtuser;/' /etc/nginx/nginx.conf  

# Switch to non-root user  
USER dtuser  

# Start Nginx  
CMD ["nginx", "-g", "daemon off;"]
