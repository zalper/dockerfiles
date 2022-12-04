FROM alper/minidebjava10:v1

COPY ./assos-jar-with-dependencies.jar /usr/src/myapp/assos-jar-with-dependencies.jar

WORKDIR /usr/src/myapp
RUN mkdir logs
VOLUME logs

CMD ["java", "-XX:MetaspaceSize=29m", "-XX:MaxMetaspaceSize=29m", "-Xms70m", "-Xmx70m", "-XX:+UseG1GC", "-jar", "assos-jar-with-dependencies.jar", "1", "assos"]



