ARG version
FROM almalinux:${version}

ARG name

ARG cicd="jenkins" \
    cloud="aws"
RUN echo "cicd: $cicd, cloud:$cloud, name: ${name}"
ENV cicd=$cicd \
    cloud=$cloud
# CMD [ "echo", "cicd: $cicd, cloud:$cloud, name:${name}"]
CMD [ "sleep", "100"]
