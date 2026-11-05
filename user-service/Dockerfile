FROM eclipse-temurin:25-jre
WORKDIR /app
RUN groupadd --system app && useradd --system --gid app app

COPY target/user-service-*.jar app.jar

USER app
EXPOSE 8081
# Size the heap from the container memory limit instead of the host's RAM
ENV JAVA_OPTS="-XX:MaxRAMPercentage=75"
ENTRYPOINT ["sh", "-c", "exec java $JAVA_OPTS -jar /app/app.jar"]
