ARG version=${version:-9}
FROM almalinux:$version

ARG name

ARG cicd="jenkins" \
    cloud="aws"
RUN echo "cicd: $cicd, cloud:$cloud, name: ${name}, version: $version"
ENV cicd=$cicd \
    cloud=$cloud
# CMD [ "echo", "cicd: $cicd, cloud:$cloud, name:${name}"]
CMD [ "sleep", "100"]
