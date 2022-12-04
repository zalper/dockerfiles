FROM alper/minidebjava10:v1

COPY ./assos-jar-with-dependencies.jar /usr/src/myapp/assos-jar-with-dependencies.jar

WORKDIR /usr/src/myapp
RUN mkdir logs
VOLUME logs

CMD ["java", "-XX:MetaspaceSize=28m", "-XX:MaxMetaspaceSize=28m", "-Xms52m", "-Xmx52m", "-XX:+UseG1GC", "-jar", "assos-jar-with-dependencies.jar", "0", "assos"]



