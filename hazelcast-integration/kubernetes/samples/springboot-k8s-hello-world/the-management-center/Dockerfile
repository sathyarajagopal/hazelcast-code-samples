FROM hazelcast/management-center:5.5.2

LABEL version=$APP_VERSION

RUN curl -o ${MC_HOME}/hazelcast-kubernetes.jar \
     https://repo1.maven.org/maven2/com/hazelcast/hazelcast-kubernetes/2.2.3/hazelcast-kubernetes-2.2.3.jar

ENV JAVA_OPTS='-Dhazelcast.mc.healthCheck.enable=true'
ENV MC_CLASSPATH "${MC_HOME}/hazelcast-kubernetes.jar"

CMD ["bash", "/opt/hazelcast/management-center/bin/hz-mc", "start"]
