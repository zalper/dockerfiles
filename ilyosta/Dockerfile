FROM alper/minidebjava10:v1

COPY ./ReplazFat-jar-with-dependencies.jar /usr/src/myapp/ReplazFat-jar-with-dependencies.jar

WORKDIR /usr/src/myapp
RUN mkdir logs
VOLUME logs

CMD ["java", "-XX:MetaspaceSize=24m", "-XX:MaxMetaspaceSize=24m", "-Xms22m", "-Xmx22m", "-XX:+UseG1GC", "-jar", "ReplazFat-jar-with-dependencies.jar", "APP_TYPE__DBSync", "ilyosta"]



