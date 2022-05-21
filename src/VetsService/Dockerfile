FROM amazoncorretto:11
ADD https://github.com/aws-observability/aws-otel-java-instrumentation/releases/download/v1.13.1/aws-opentelemetry-agent.jar /opt/aws-opentelemetry-agent.jar
ENV JAVA_TOOL_OPTIONS=-javaagent:/opt/aws-opentelemetry-agent.jar
ADD target/vets-service-0.0.1-SNAPSHOT.jar /usr/vets-service.jar
EXPOSE 80
ENTRYPOINT ["java", "-jar", "/usr/vets-service.jar"]
