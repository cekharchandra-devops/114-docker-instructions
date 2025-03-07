# FROM almalinux:9
# RUN dnf install nginx -y
# RUN useradd dtuser
# # USER dtuser
# CMD [ "nginx", "-g", "daemon off; user dtuser;" ]

# # Since ports below 1024 require root privileges, you can run Nginx on a non-privileged port like 8080:

# # solution1 : docker run -d -p:8080:8080 user:v1

# #solution2: CMD [ "nginx", "-g", "daemon off;", "user dtuser" ]

FROM almalinux:9  

# Install Nginx  
RUN dnf install nginx -y  

# Create a new user  
RUN useradd -m dtuser  

# Replace 'user nginx;' with 'user dtuser;' in the Nginx config  
RUN sed -i 's/^user .*/user dtuser;/' /etc/nginx/nginx.conf  

# Switch to non-root user  
USER dtuser  

# Start Nginx  
CMD ["nginx", "-g", "daemon off;"]
