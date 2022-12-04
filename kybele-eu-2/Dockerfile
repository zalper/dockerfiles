FROM alper/minidebjava10:v1

COPY ./kybele-jar-with-dependencies.jar /usr/src/myapp/kybele-jar-with-dependencies.jar

WORKDIR /usr/src/myapp
RUN mkdir logs
VOLUME logs

CMD ["java", "-XX:MetaspaceSize=41m", "-XX:MaxMetaspaceSize=41m", "-Xms18m", "-Xmx18m", "-XX:+UseG1GC", "-jar", "kybele-jar-with-dependencies.jar", "eu-2", "kybele"]



