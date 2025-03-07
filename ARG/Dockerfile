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

# docker build -t arg:v1 . --build-arg version=8

# The version value can be used only in the FROM instruction if an ARG instruction is declared before it.
# ARG instructions declared after the FROM instruction are available only during the image build time and do not persist in the final image.
# Values can be assigned to variables declared in ARG instructions using the --build-arg parameter during the docker build command.