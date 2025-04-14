FROM openjdk:17-slim

LABEL version=$APP_VERSION

# Copy from Maven build output
ARG JAR_FILE
ADD target/${JAR_FILE} application.jar

# Set in 'deployment.yaml', default to empty string
ENV K8S ""

ENTRYPOINT exec java -Dk8s=$K8S -jar application.jar
