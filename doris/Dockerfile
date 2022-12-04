FROM alper/minidebjava10:v1

COPY ./doris-jar-with-dependencies.jar /usr/src/myapp/doris-jar-with-dependencies.jar

WORKDIR /usr/src/myapp
RUN mkdir logs
VOLUME logs

CMD ["java", "-XX:MetaspaceSize=30m", "-XX:MaxMetaspaceSize=30m", "-Xms20m", "-Xmx20m", "-XX:+UseG1GC", "-jar", "doris-jar-with-dependencies.jar", "APP_TYPE__PRESEARCH", "doris"]



