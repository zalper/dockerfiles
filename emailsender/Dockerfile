FROM alper/minidebjava10:v1

COPY ./emailsender-jar-with-dependencies.jar /usr/src/myapp/emailsender-jar-with-dependencies.jar

WORKDIR /usr/src/myapp
RUN mkdir logs
VOLUME logs


CMD ["java", "-XX:MetaspaceSize=48m", "-XX:MaxMetaspaceSize=48m", "-Xms48m", "-Xmx48m", "-XX:+UseG1GC", "-jar", "emailsender-jar-with-dependencies.jar", "APP_TYPE__EMAILSENDER", "emailsender"]



